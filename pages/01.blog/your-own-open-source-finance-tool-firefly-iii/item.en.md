---
title: 'Your own open source finance tool - Firefly III'
author: Dan
published: true
date: '06-01-2023 23:04'
taxonomy:
    category:
        - news
    tag:
        - tutorials
        - firefly3
        - opensource
        - finance
aura:
    author: dan
media_order: firefly-iii-logo.png
---

# Your own open source finance tool - Firefly III

New year - new opportunities!  
Maybe firefly can help you to reach your goal(s) faster with an easier overview of your finances and your bad and good habits. 

It's open source as usual and covers the privacy part as well.  
You shouldn't use a [cloud](../media/there_is_no_cloud.jpg) at all if it's not your own, and especially when it comes to your finances. So it has privacy in mind as well.... a quote from the developer:

> It is completely self-hosted and isolated, and will never contact external servers until you explicitly tell it to.

There are many others, but this one is a simple system for all your financial management. Gnucash, for example, is another very helpful tool for your accounting - business and personal. But having everything together, private (your bank account, your partner's bank account, savings accounts, credit, visa debit,...), company 1, company 2.... So you have the ultimate overview of all your finances in just one software. 

> - You can create and edit transactions, accounts, and give them budgets, categories and tags.
> - You can automate part of this with recurring transactions and auto-budgets.
> - You can keep track of liabilities.
> - You can import data into Firefly III from almost any bank.

# Features

Just check the link https://docs.firefly-iii.org/firefly-iii/about-firefly-iii/introduction/?mtm_campaign=docu-internal&mtm_kwd=introduction. It is not necessary to list them here as well. But one thing is good to mention:

> Supports any currency you want, including crypto currencies such as ₿itcoin and Ξthereum

So if you're a crypto guy and/or have money in other countries, that's possible too.


# Installation

We will use a quick and dirty [Docker installation](https://docs.firefly-iii.org/firefly-iii/installation/docker/) here. Just to show what Firefly III can do. Check the other options if you prefer another way and please take responsibility for your own security.  
We've also an installation process on Arch in [our wiki](https://wiki.techsaviours.org/en/extras/firefly3), if you prefer not to use docker.


## Docker & docker compose

```
pacman -Sy docker docker-compose --noconfirm
systemctl enable --now docker.service
```


## docker-compose.yml
```
mkdir /opt/firefly3
cd /opt/firefly3
wget https://raw.githubusercontent.com/firefly-iii/docker/main/docker-compose.yml
```

> **NOTE**:  
> Change `docker-compose.yml` to your needs - `ports`, `password`


## .env
```
wget https://raw.githubusercontent.com/firefly-iii/firefly-iii/main/.env.example -O .env
```

Change at least:
```
TRUSTED_PROXIES=**
APP_URL=http://SERVER_IP:PORT
```


### Example docker-compose file
```
version: '3.3'

services:
  app:
    image: fireflyiii/core:latest
    restart: always
    volumes:
      - firefly_iii_upload:/var/www/html/storage/upload
    env_file: .env
    ports:
      - 80:8080
    depends_on:
      - db
  db:
    image: mariadb    
    hostname: fireflyiiidb
    restart: always
    environment:
      - MYSQL_RANDOM_ROOT_PASSWORD=yes
      - MYSQL_USER=firefly
      - MYSQL_PASSWORD=secret_firefly_password
      - MYSQL_DATABASE=firefly
    volumes:
      - firefly_iii_db:/var/lib/mysql
volumes:
  firefly_iii_upload:
  firefly_iii_db:
```


## Download & start
```
docker compose up -d
```


# Firefly III

Go to `http://SERVER_IP:PORT`.

> **HINT**:  
> `Unable to connect`, just wait a bit longer.

https://firefly-iii.org  
https://docs.firefly-iii.org/


## Register a new account

Straight forward...  
![Registration.png](d7abb9575c78ee282f42cde304965184.png)


## Getting started

![Getting_started.png](767c0c2d5cc0bf0ee003e9b475979bed.png)

1. First of all, read the page ;) 
2. Start with your private bank (Bankname - Your name)
	- If you are just by your own, you can use just the bankname. If you add your partners bank and ggf company etc. its easier to have a proper overview with your name behind as well. Especially, if it's the same bank. You can change it later as well of course.
3. `Submit` when you're ready and read the intro.


## Navigation
![Navigation.png](3c416b33c37e1c1e5f7a16e232d3ffd5.png)


### Dashboard
![Dashboard.png](0a8d160ff60ee0b10ff46c13f6356fe7.png)


### Budgets

![Budget.png](f6e4db7283f5ed5fc148ff2aedf80afa.png)

Probably one of the most use budget is for *Groceries*. Give yourself a limit for your weekly/monthly groceries budget. 

![Budget - auto-budget.png](d2588f30e8522a5fb76e4ed05641896b.png)

The common question will be here which one do you want to choose in `Auto-budget`.

1. `Set a fixed amount every period`
	 
	 It's actually straight forward. Every week you'll get the same amount. "Starting new" every week.

2. `Add an amount every period`

	This gives you the opportunity to buy more the next week if you saved the week before. The unspent money from last week is simply added to the next week's limit. It can show how much money you can increase (save). At the same time, you will probably end up spending more money than the set amount. It depends a bit on what your personal discipline is. Are you more of a person like:
	
        - Wow! I saved so much money last week, let's see how much money I can save this week. LET IT GROW! 
        - Wow! I saved so much money last week! This week I'm going to go crazy and spend it all!

Using fixed amounts is probably the best way to save money if that is your goal.

https://docs.firefly-iii.org/firefly-iii/concepts/budgets/  


### Bills

![bills](../media/bills.png)

Just add here all fixed costs like mortgage, rent, .....

The *minimum and maximum* amount depends on what you need it for. For example, power varies between this and that. If your rent is always the same, just add the same amount for both.

It is important that you specify the correct date for the next invoice. If you pay rent fortnightly, you must *Skip* 1 week.

> If you enter a number in the "skip" field, the bill will be automatically skipped every X times; a bill that arrives every 3 months can be entered by filling in "2".

Also add a *Group* which will give you a [better overview](link here) later. The rest is basically self explained.

> *NOTE:*  
> Don't be surprised if you are redirected to *Automation* - *Rules*. Go to [Automation - Rules](#rules) (here in the tutorial) if you want to continue with your setup. I will continue with the structure of the navigation/Firefly3.

https://docs.firefly-iii.org/firefly-iii/advanced-concepts/bills/


### Piggy banks

![piggy_bank](../media/piggy_bank.png)

Actually, everything is pretty much self explained, the only "problem" you will come across is how you are going to achieve your goal. If you have a big goal, you may need to add two or even four bank accounts to one goal ("Group"). Having multiple accounts in a "Group" can be a little confusing because you don't know which bank account is which when you "Name" it as your actual goal. I like to use the name of my bank account when I need to add multiple accounts to a "Group". Take a look at the image below.

![piggy_bank2](../media/piggy_bank2-1.png)

So there are 35 euros left (under "Account status") in my main account that I would like to add to the roof repair, but is it the main account?

https://docs.firefly-iii.org/firefly-iii/advanced-concepts/piggies/


### Transactions

This does not need to be explained. You will find all your transactions there (expenses, revenue/income, transfers).


### Automation

#### Rules

Now it gets a bit more complicated because there are many things happening at once here. We will more or less only cover the basics here.

![creating_a_rule](../media/creating_a_rule.png)

You can create a `Rule group `directly under `Rules`. You can open it in another tab to create it. A rule group could be your main accounts (`Personal`, `Company1`, `Company2`).

The `Description contains` option in `Trigger` is one of the most important options here. Download a `csv` file from your bank and check the names of your transactions. We will import the `csv` file later using Firefly's data importer. The rest in `Trigger` is pretty much self explained. There are also a lot of other things that might suit you better.

The part `Action` contains more important things, which also has to be created before like `Rule group`, but you have to start somewhere and I will just continue.  
The `Set category to..` function gives you a good overview of all your categories in your bank account during the specified period. And here you need to think about how you want it.  
A good example of this is `Insurances`. Are you satisfied with a category with only insurances or do you want to see all your insurances in the chart? Then you need to add a category for each insurance.  
Another example would be suppliers, a category for all suppliers or do you want to know which suppliers get the most money from you?

`Add tag` feature can be very helpful if you set a category as a supplier, but want to see how much you paid for a particular supplier. Or if you have all insurances in each category separately. And a tag that covers all `Insurances`.  
Can be seen as a subcategory without the benefit of a chart in your bank account.


`Set destination account to..` ...  
Depends on how many `Expense accounts` you want to add, e.g. `Personal`, `Company1`, `Company2`, ...  
I suggest to keep it simple. If you set up many expense accounts, you will lose track. The same goes for too many categories and too many tags. Let's say you have 4 personal accounts: 2 for you (main account and savings account) and the same for your partner. All transactions on all your personal accounts are actually just a `Personal` expense.

As I mentioned earlier, the main reason for creating rules is to automatically assign the transaction to the correct bank account, category and tags when importing the csv file. Otherwise, you will lose track very quickly if you add everything manually and you get confused with the tags because you simply forget what the tag name was, likewise, with too many categories. These steps are really important. Think carefully about how you want your structure to look. Otherwise, you won't use it for long because it will cost you too much time and it won't be fun.

Check also [categories](https://docs.firefly-iii.org/firefly-iii/concepts/categories/) and [tags](https://docs.firefly-iii.org/firefly-iii/concepts/tags/).


#### Recurring transactions 

I personally don't use this because I prefer to import all my transactions. And I'm not a fan of automating payments. The same goes for setting them up in your real bank account. These payments are too quickly forgotten.

https://docs.firefly-iii.org/firefly-iii/advanced-concepts/recurring/


### Accounts


#### Asset accounts

You should have also at least 3 accounts:
1. BankName - YourName
2. BankName - YourName savings account
3. Cash wallet

Here you can change and add more accounts.

![asset_accounts](../media/asset_accounts.png)

https://docs.firefly-iii.org/firefly-iii/concepts/accounts/#default-asset-accounts

#### Expense accounts

![expenses](../media/expenses.png)

I prefer to keep it simple here. I work more with categories and tags. It is up to you if you want to add all expenses already here or under categories. For example, I only use private and have "grocery shops" as a category and if I want to know how much I spend on a particular store, I have the shop name as a tag. But you can also do it like this:

![expenses2](../media/expenses2.png)

Maybe you need a "Expense" already as "Grocery shops" and the specific store as a category and different tags for everything you bought in that store. This way you could track how much milk you bought last year.


https://docs.firefly-iii.org/firefly-iii/concepts/accounts/#expense-accounts


#### Revenue accounts 

![revenue](../media/revenue.png)

Actually similar like expenses. You can also use private or if you get a refund from an online store. 


####  Liabilities

![liabilities](../media/liabilities.png)

Another good feature if you have given someone money or if you have loans, debts or mortgages to pay. Here you have the possibility to manage them as well.

https://docs.firefly-iii.org/firefly-iii/concepts/accounts/#liabilities


### Classification (Categories, Tags & Groups)

As already explained more under [Rules](#Rules), I won't go into more detail here.


https://docs.firefly-iii.org/firefly-iii/concepts/categories/  
https://docs.firefly-iii.org/firefly-iii/concepts/tags/  
https://docs.firefly-iii.org/firefly-iii/concepts/groups/


### Reports

![reports](../media/reports.png)

An overview of what your accounts have done. You can select all accounts or only specific accounts. The same goes for categories and tags.
You can see some charts and other information about your accounts.

https://docs.firefly-iii.org/firefly-iii/advanced-concepts/reports/


### Export data

![export_data](../media/export_data.png)

I have never used it. So no comment here. Just look at the link below.

https://docs.firefly-iii.org/firefly-iii/exporting-data/


### Options

Nothing to mention here, really. I will just leave some screenshots below. 


#### Profile

![profile](../media/profile.png)    


#### Preferences

![preferences](../media/preferences.png)  
![preferences2](../media/preferences2.png)  
![preferences3](../media/preferences3.png)  


#### Currencies

![currencies](../media/currencies.png)  


#### Administration

![administration](../media/administration.png)  
![administration2](../media/administration2.png)  
![administration3](../media/administration3.png)  
![administration4](../media/administration4.png)  
![administration5](../media/administration5.png)  


# Data importer

An easy way to import all your transactions via csv files.

https://docs.firefly-iii.org/data-importer/


## docker-compose.yml

Add the following to the [docker-compose.yml](#example-docker-compose-file) file:
```
  fidi:
    image: fireflyiii/data-importer:latest
    restart: always
    env_file: .fidi.env
    ports:
      - 8081:8080
    depends_on:
      - app
```

Just before:
```
volumes  :
  firefly_iii_upload:
  firefly_iii_db:
```


## Create access token

Go to your http://SERVER_IP:PORT(firefly3)/profile and create a new  access token and name it `Importer` or whatever suits you.

![token](../media/token.png)  


## .fidi.env
```
wget https://raw.githubusercontent.com/firefly-iii/data-importer/main/.env.example -O .fidi.env
```

The link to the Firefly main page will be important. So whatever you set in  [.env](#.env) (`APP_URL=`) must also be set here:

```
FIREFLY_III_URL=http://app:8080
VANITY_URL=http://SERVER_IP:PORT(firefly3)
FIREFLY_III_ACCESS_TOKEN=YourTOKEN
TRUSTED_PROXIES=**
APP_URL=http://SERVER_IP:PORT(data-importer)
```


## Download & start
```
docker compose up -d
```

Go to http://SERVER_IP:PORT(data-importer). 

![data_importer](../media/data_importer.png)


## Import file

Go to your bank and export your transactions to a csv file. 

![data_importer2](../media/data_importer2.png)

You can create a configuration file later so that you do not have to keep changing the following information.

![data_importer3](../media/data_importer3.png)

I mainly use the default settings. Only "Import tag" and "Date format" are different. But the settings really depend on how your bank exports your transactions. You have to test that a bit yourself. Every bank is different so it makes no sense to put here a reasonable config for all. See the link https://docs.firefly-iii.org/data-importer/usage/configure/#file-options for that while you're setting it up for yourself.

After the import you will see all transactions under the selected bank account - http://SERVER_IP:PORT(firefly3). Start creating your [rules](#rules) if you think they will appear frequently.


# That's it! 

I hope it helps you a little to save/earn more money this year while prices are blowing up.  
And if you like it, leave the developer your personal transaction in his instance as well - https://www.patreon.com/jc5 and/or https://github.com/sponsors/JC5. 

Have a good year  
Dan
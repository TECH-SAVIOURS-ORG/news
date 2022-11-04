---
title: 'What''s been going on lately? New Server, Matrix, ...'
author: Dan
published: true
date: '04-11-2022 03:24'
taxonomy:
    category:
        - news
    tag:
        - 'TECH SAVIOURS'
        - server
        - matrix
aura:
    author: dan
---

# New Server Info
A bit more info on what's been going on lately. Especially around the Matrix server.

We have decided to give the server a little more resources during the latest issues with matrix. The cost will increase by another 3 EUR. The exact amount is now 10,08 EUR monthly, paid by us. This is all free to use. We just want to give something back and spread more privacy options. Just another option for you to use. There are other servers too if you prefer another one.

The new server is hosted by netcup in Nuremberg (Germany). As usual with netcup, you can't just upgrade the server. We have set up the server from scratch and moved the services over one by one. You could also do a snapshot and restore it to the new server but a fresh start is always good to ged rid off anything unused stuff or whatever as well. 

The [VPS 2000 G10](https://www.netcup.de/vserver/vps.php#v-server-details) should give us enough performance and storage for now.

# Matrix
The Matrix database had a range of sizes from 90 GB to 115 GB. The few users here don't actually spend every second of their lives just using this service, so it really shouldn't be that big. It's a pity that we enabled retention a few months ago to reduce the history, media files, etc. since the history can't really be controlled by the user themselves, we decided on a 90-day retention in a poll.

Instead of decreasing, it increased! Very fast! In just arround 15 days or so by 50GB.

The top 3 rooms:
```
              room_id            | num_rows  
----------------------------------------------------------
 Matrix HQ:matrix.org		 |   400673076
 BlackArch:matrix.org		 |     7139888
 Arch Linux:archlinux.org	 |     4855957
```

Currently there is a bug with this retention option that we were able to find a solution for as part of some GitHub issues.
To be honest, matrix and the retention option, deleting/purging a room, it's just a mess. We hope that this will be solved soon and most importantly that the user can decide for himself if he wants to delete the history or to keep it.  
**But** we can't do any better, and we know that one day the Matrix people will solve the problem and new features will come and new problems will arise. That's just the way it is.

At the moment we were even able to reduce the database to 13 GB. The goal was under 40 and we are pretty sure that we will reach this number again.  

We have also blocked the main #matrix:matirx.org room because it grows the database too fast.  
We may block more rooms in the future, depending on how the database grows. Maybe the first 5 biggest rooms from that list https://view.matrix.org/.

Retention is disabled for now and registrations are enabled again. We will probably start a new poll as soon as the retention is bug free.

The whole process had a positive side effect in the end, we now have a faster server in place ;)

# General information
We do this mainly in our free time, and there's not much of that at the moment. Work dominates our lives. And when there is free time, there is also family, friends and simply breaks, which we all need.
Free and open source is the way to go, be patient with any project out there, including this one. 

# What is next?
Matrix will run smoothly and the wiki will be top priority again and Pinephone and co. will follow suit. And if you want, you are more then welcome to add your favorite device, OS, services... https://wiki.techsaviours.org/en/wiki  
Our plan is still to add nextcloud, wireguard, etc. pp. to achieve at least some kind of "foundation" for your privacy.

And another "Your own extras" is planned for January. That one will focus mainly on your finances. This might be very interesting for one or the other.

So, have a nice weekend and sorry for the ups and downs of the Matrix instance lately
Dan
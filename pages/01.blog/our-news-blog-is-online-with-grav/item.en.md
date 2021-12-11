---
title: 'Our News/Blog is online with GRAV'
taxonomy:
    category:
        - news
    tag:
        - 'TECH SAVIOURS'
        - grav
media_order: 'ts&grav.png'
aura:
    author: dan
date: '04-12-2021 12:40'
published: true
---

We are very excited to launch our new News section!

# WordPress, Drupal, Grav ... which one?!
After comparing a few options out there like WordPress, Drupal & co. we've decided to go with GRAV. Which is a great CMS (Content Management System) written in php. GRAV is just like the other two mentioned, but GRAV doesn't need a database. It stores data in a flat-file CMS that are organised in folders rather than in a database. Which makes it really quick and very lightweight.  
GRAV's first release was in July 30, 2014, so it's relatively new compared to WordPress (2003) and Drupal (2001) for example, but it has become a well-known CMS alternative. GRAV is used by less than 0.1% of all CMS systems - [w3techs.com](https://w3techs.com/technologies/details/cm-grav). It's not much when compared to the big one - WordPress has the market under control with a respectable [65.1%](https://w3techs.com/technologies/details/cm-wordpress) and Drupal's market share is [2.1%](https://w3techs.com/technologies/details/cm-drupal).  
Take a look at the usage statistics of the most popular [Content Management Systems](https://w3techs.com/technologies/overview/content_management).

# Drupal or GRAV
Our main comparison at the end were Drupal and GRAV. Both have excellent security practices. 
Checking the latest vulnerability statistics on CVE-Details for [Drupal](https://www.cvedetails.com/product/2387/Drupal-Drupal.html?vendor_id=1367) and [GRAV](https://www.cvedetails.com/product/59205/Getgrav-Grav-Cms.html?vendor_id=20511), we moved more into the direction of GRAV.  
And in the end, our news feeds are just a few letters and pictures. The others would be way too heavy for our little goal.  
GRAV uses [Markdown syntax](https://learn.getgrav.org/17/content/markdown), which we prefer, and the configuration files/pages are in [YAML syntax](https://learn.getgrav.org/17/advanced/yaml), which you will find in many tools like Ansible, Kubernetes, Prometheus, Matrix ... just to name a few.   
So GRAV not only fits our needs, it also matches our infrastructure.  

# Pinpress theme
After the decision was made, we started looking for a theme. And there are quite a few of them. Simple and easy to read was now the next goal. And a similar look to our main website, which is made via [Bootstrap](https://getbootstrap.com/).  
The [PinPress theme](https://demo.getgrav.org/pinpress-skeleton/) seems to be a good choice and so far we don't really have anything to complain about. It was a bit difficult to adapt it to our design because the default theme settings didn't work as good as we thought but a little code sorted that out.

## Theme inheritance aka child theme
We started first with an [_Inheriting theme_](https://learn.getgrav.org/16/themes/customization#inheriting-manually) (child theme), with that we can make our changes and keep the ability to update the theme without overwriting our changes.  
Once we had everything ready, our first step was a "clean up". We've removed all third-party connections to get even more performance out of GRAV to achieve a better usability when reading our news and especially  clicking through the content, but also for us while we work on it.  
In order to host everything directly from the server, we also decided to download [Fork Awesome's](https://forkaweso.me/Fork-Awesome/) icon pack. Yeah, they are really ... awesome!  
Finally, we gave the theme our personal touch like favicon, logo, footer etc. and changed the [twig files](https://en.wikipedia.org/wiki/Twig_(template_engine)) to our needs.  

# MIT license
GRAV is licensed under the [MIT License](https://github.com/getgrav/grav/blob/develop/LICENSE.txt). This is a very straightforward license.

>The MIT License (MIT)
>
>Copyright (c) 2021 Grav
>
>Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:
>
>The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
>
>THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Rights
You have the right to use, copy, modify, merge, distribute, publish, sublicense, and sell copies of the software. 

## Conditions
MIT License text & copyright notice must still be included with any unmodified MIT-licensed code. Your new work can be another license.

# Conclusion
The outcome is now visible and we are very happy with it.  
But not everything is perfect. There is one big problem GRAV has, especially for news and blog writers. Posting news automatically to various media channels will still be a hassle in 2021. Probably even in 2022. You need to post your messages manually or find other solutions like [IFTTT](https://ifttt.com/explore/new_to_ifttt).  
Our plan is to publish news every two weeks or monthly. It's fine for us to manually post this on social media until we find another solution that suits us.  
So we will see what the future will bring and how GRAV works in the long run.  

If you want to read more about GRAV check the link - [What is Grav?](https://learn.getgrav.org/17/basics/what-is-grav)

# What next?

We are in the process of setting up a few more social media accounts to allow you to follow our news as you like. You can find the links in the gray box at the top right or below the news, depending on your device/resolution settings.
  
@reddit followers
Not every article will be published in our subreddit. Reddit rules are not meant to promote yourself, so we will only post information about privacy and other things without promoting our news/blog. This means that any changes to TECH SAVIOURS will only appear on the other channels.   

If you have any suggestions or feedback, let us know.

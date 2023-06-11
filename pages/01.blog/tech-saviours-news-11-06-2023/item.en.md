---
title: 'TECH SAVIOURS News - 11.06.2023'
author: Dan
published: true
date: '11-06-2023 07:13'
taxonomy:
    category:
        - news
    tag:
        - 'TECH SAVIOURS'
        - matrix
        - wiki
        - searx/ng
aura:
    author: dan
---

# Personal
It has become a bit quiet around the services, wiki etc pp.  
Mainly due to workload, health and a move to another house, which prevented me from doing anything for .ORG.
But slowly I'm starting to work on it again.

# Updates & searx/ng
Updates were still done regularly.  
Due to the updates to python 3.11 the searx instance has changed a bit. Instead of searx it now runs searxng.  
The differences between the two are listed here - https://github.com/searxng/searxng#differences-to-searx.

The domain stays the same - https://searx.techsaviours.org.  
Basically everything is left on default settings. Except that it generally runs on dark theme and a bit of branding was added.

# Wiki
The wiki is almost finished. Wireguard will be added soon to complete the wiki. So that also your server/s at home will be reachable from everywhere.  
The wiki can be seen as a kind of basic. But there is so much more you can do for your privacy but it depends on your own use.  
I personally use a few cameras in my house. This brings up a few questions:
- what kind of devices are needed for that
- what software
- blocking the propriety devices via firewall & AdGuardHome
- ...

Sooner or later there will be various open source software that can extend your privacy. In this case, Home Assistant, Frigate, ... would be a good extension for the Wiki.  

Also a Linux section for "Phone" should come. The well known PinePhone (Pro) was used by me last year for about 10 months as a daily driver. It is great and I wish the battery lasts at least one day. For me the available apps are enough but the phone and especially the battery was not worth to use it further.  

The keyboard gave me another 6000mah of battery. It was just enough for one day ... very annoying having the brick in a pocket ... The quality of calls is also not that great. Often people asked what I had said at all.  
Nevertheless, I see great potential in Linux for mobile devices. Also the new pinetab2, looks very promising.  
Long talk... this will also be added to the wiki.

# Matrix
There will be some downtime in the near future. Since the retention has been on hold since the end of last year (https://techsaviours.org/news/en/whats-been-going-on-lately-new-server-matrix#matrix), manual intervention will take place. So at least the top 15 rooms will be a bit purged:
```
        canonical_alias         |              room_id               | num_rows 
--------------------------------+------------------------------------+----------
 #space:midov.pl                | !bFbQyriMFLThCXRMyE:midov.pl       | 35317776
 #fedora:fedoraproject.org      | !zAeWUNBoXONgkVtgqn:mozilla.org    | 10049292
 #grapheneos:grapheneos.org     | !UVEsOAdphEMYhxzTah:grapheneos.org |  6392182
 #raspberrypi:matrix.org        | !wOlkWNmgkAZFxbTaqj:matrix.org     |  5684690
 #blackarch:matrix.org          | !cNwjdQwVpRMsIMkUpx:matrix.org     |  4123174
 #archlinux:archlinux.org       | !GtIfdsfQtQIgbQSxwJ:archlinux.org  |  3130399
 #offtopic:grapheneos.org       | !tgbPIxPlvGiwpsGJuu:matrix.org     |  2953462
 #grapheneos-old:grapheneos.org | !SayHlEYXdrpSerhLMC:matrix.org     |  2918382
 #community:grapheneos.org      | !lAoVmVifHHtoeOAmHO:grapheneos.org |  2777457
 #ipfs-chatter:ipfs.io          | !gWiVYCURkxIapWZaGy:ipfs.io        |  2272075
 #fdroid:f-droid.org            | !hbPGQxyHEvFEncGQxE:f-droid.org    |  1471245
 #CalyxOS:matrix.org            | !aPqEsAdWuysydZNCic:matrix.org     |  1217819
 #users:ansible.com             | !czpAhMQgXXiRMvhOef:libera.chat    |  1212796
 #Nextcloud:matrix.org          | !TEwfEWdDwdaFazXmwD:matrix.org     |   915336
 #ubuntu:matrix.org             | !uGTCmJuKfnAYNPNsZz:matrix.org     |   814721
```
The database size (70GB) is still moderate but better too early than too late.

Also, all users who have not logged in for more than a year will be deleted. So if you haven't logged in for more than a year and you want to keep your account or username, just log in.

That should be it for now. For all of you who are hanging around here, you know what's going on.  
Have a good rest of the weekend!  
Dan
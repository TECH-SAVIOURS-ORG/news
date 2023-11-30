---
title: 'OPNsense 23.7.9 released'
author: Dan
published: true
date: '30-11-2023 07:39'
taxonomy:
    category:
        - news
    tag:
        - opnsense
        - release
aura:
    author: dan
---

A good day to you all,

As the end of the year inches closer the changes published today are naturally
smaller additions and cleanups, notably changes for IPsec VTI connection for
IPv6 and dual-stack operation, a possible OpenVPN CSO mismatch bug and optional
support for SHA-512 password hashing.

Note that the HTTPS bump for the firmware mirrors updates the published URLs
in the firmware selection, but if you already use LeaseWeb or NYC BUG you need
to reselect them in order to move from HTTP to HTTPS connectivity.

Of further note is that the Squid web proxy will be moved to a plugin in
version 24.1 but for everyone using it the upgrade procedure will make sure
to install it automatically when enabled.  A meta package was added to the
plugins already in order for this to work just in case there are questions
about what it is supposed to be doing... apart from providing dependencies
it does not do anything at the moment.  ;)

Last but not least, we have been successfully testing and ironing out OpenSSL
3 ports builds in the past week and inclusion in 24.1 seems very likely at this
point.  The effort continues and we will also be looking into backport material
from FreeBSD 13 stable branches for further preparation.

Here are the full patch notes:

More at https://forum.opnsense.org/index.php?topic=37173.msg181957#msg181957
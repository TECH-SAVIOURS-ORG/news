---
title: 'OPNsense 23.7.8 released'
author: Dan
published: true
date: '11-11-2023 23:46'
taxonomy:
    category:
        - news
    tag:
        - wireguard
        - opnsense
        - release
        - GUI
        - changes
aura:
    author: dan
media_order: opnsense.png
---

The configuration restore GUI has been improved in a number of ways due to
recent demand and Squid was updated to the new major release version 6.

A number of reliability improvements were also added to the WireGuard
kernel plugin which from our perspective is now ready for core inclusion.
The documentation is being updated accordingly, but will take a bit more
time to ensure consistency following up on the GUI changes it received.

This update also includes FreeBSD security advisories and assorted fixes.
We are aware of OpenSSL 1.1.1 CVE-2023-5678 and we are already testing
builds based on OpenSSL 3 which can be available in 24.1 when it does not
negatively impact overall operation.  We also expect fixes for version
1 to be available sooner, but without OpenSSL providing such fixes directly
the roundtrip time is likely going to increase for them.

More at https://forum.opnsense.org/index.php?topic=36891.msg180396#msg180396
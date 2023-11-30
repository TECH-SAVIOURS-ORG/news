---
title: 'KeePassXC Audit Report'
author: Dan
published: true
date: '30-11-2023 07:58'
taxonomy:
    category:
        - news
    tag:
        - keepassxc
        - audit
aura:
    author: dan
---

An audit of KeePassXC has been on the wish list since we started this project over six years ago. Today we are happy to announce the release of an audit conducted by Zaur Molotnikov, an independent security consultant, that was completed on January 19, 2023 against KeePassXC 2.7.4. This audit was conducted free of charge to the KeePassXC Team and the findings and writeup were reviewed for correctness.

Overall, Zaur provides a detailed review of the KeePassXC application and its underlying code base. He also provides several recommendations for users to follow to improve their own security while using KeePassXC.

Here are excerpts from the report:

KeePassXC provides sufficient cryptographic protection (confidentiality, integrity and authenticity) to the confidential information the user is storing in the database, given that the user selects a strong authentication method, e.g. a strong passphrase and a confidential random key file, and that the user will use KeePassXC with its latest secure file format.

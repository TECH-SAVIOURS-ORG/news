---
title: 'Log4shell - Five Eyes published a scanner for everyone'
published: true
taxonomy:
    category:
        - news
    tag:
        - vulnerabilities
media_order: l4j.png
date: '26-12-2021 10:42'
aura:
    author: dan
---

# Log4shell
As you may have heard, since December 9 there is a severe vulnerability called [Log4shell](https://nvd.nist.gov/vuln/detail/CVE-2021-44228) (and other Log4j-related vulnerabilities) that affects a wide range of Java applications. The "Apache Log4j2 2.0-beta9 through 2.12.1 and 2.13.0 through 2.15.0 JNDI" library. 

# Scanners

## Five Eyes
[The Five Eyes](https://en.m.wikipedia.org/wiki/Five_Eyes) have published a scanner that is basically just a combination of other software and slightly changes:

> As many in industry, we did not feel the need to "re-invent the wheel". This recommended scanning solution is derived from the great work of others (with slight modifications). We've included two additional projects to avoid using third-parties.

Everything is open sourced at https://github.com/cisagov/log4j-scanner
Check your services if you can. 

## Anchore
There are also [syft](https://github.com/anchore/syft) and [grype](https://github.com/anchore/grype) provided by [anchore](https://anchore.com/).


# Grafana's Loki
We use [Loki](https://github.com/grafana/loki) from Grafana, which can be a very fast solution for identifying services with Log4j.
Just use the regular expression `jndi` and `(?i)log4j`.
See [Grafanas statement](https://grafana.com/blog/2021/12/14/grafana-labs-core-products-not-impacted-by-log4j-cve-2021-44228-and-related-vulnerabilities/).

# Update your devices
If you have to wait for updates from hosters etc., check the news about them to see if they have already patched the vulnerability or if they are affected at all or not. Our services are not affected.
Also update your devices (phones, laptop/desktop, servers, IoT...) as soon as possible, better now, which should be generally on a regular basis and now more than ever.
There is a list that shows which software is affected or has a patch already available.
[Check it out](https://github.com/cisagov/log4j-affected-db/blob/develop/SOFTWARE-LIST.md).

# How to 
If you need help to check your software, we have a quick guide for the [community](https://wiki.techsaviours.org/en/vulnerability_scans/log4shell). Otherwise contact us via email etc..

Stay safe - in real and virtual life
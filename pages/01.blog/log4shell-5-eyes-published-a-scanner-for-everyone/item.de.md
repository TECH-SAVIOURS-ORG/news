---
title: 'Log4shell - Five Eyes veröffentlicht einen Scanner für alle'
date: '26-12-2021 11:43'
taxonomy:
    category:
        - news
    tag:
        - vulnerabilities
aura:
    author: dan
---

# Log4shell
Wie du vielleicht schon gehört hast, gibt es seit dem 9. Dezember eine schwerwiegende Sicherheitslücke namens [Log4shell](https://nvd.nist.gov/vuln/detail/CVE-2021-44228) (und andere Log4j-bezogene Sicherheitslücken), die eine Vielzahl von Java-Anwendungen betrifft. Die "Apache Log4j2 2.0-beta9 bis 2.12.1 und 2.13.0 bis 2.15.0 JNDI"-Bibliothek. 

# Scanners

## Five Eyes
[Die Five Eyes](https://de.m.wikipedia.org/wiki/UKUSA-Vereinbarung) haben einen Scanner veröffentlicht, der im Grunde nur eine Kombination aus anderer Software ist und leicht verändert wurde:

> As many in industry, we did not feel the need to "re-invent the wheel". This recommended scanning solution is derived from the great work of others (with slight modifications). We've included two additional projects to avoid using third-parties.  

> Übersetzt:
> Wie viele in der Industrie hatten auch wir nicht das Bedürfnis, "das Rad neu zu erfinden". Diese empfohlene Scan-Lösung ist von der großartigen Arbeit anderer abgeleitet (mit leichten Änderungen). Wir haben zwei zusätzliche Projekte aufgenommen, um die Verwendung von Drittanbietern zu vermeiden.

Alles ist Open Source unter https://github.com/cisagov/log4j-scanner
Überprüfe deine Dienste, wenn es dir moeglich ist. 

## Anchore
Es gibt auch [syft](https://github.com/anchore/syft) und [grype](https://github.com/anchore/grype), die von [anchore](https://anchore.com/) bereitgestellt werden.

# Grafana's Loki
Wir verwenden [Loki](https://github.com/grafana/loki) von Grafana, das eine sehr schnelle Lösung für die Identifizierung von Diensten mit Log4j sein kann.
Verwende einfach die regular expression `jndi` und `(?i)log4j`.
Siehe [Grafanas statement](https://grafana.com/blog/2021/12/14/grafana-labs-core-products-not-impacted-by-log4j-cve-2021-44228-and-related-vulnerabilities/).

# Aktualisiere deine Geräte
Wenn du auf Updates von Hostern usw. warten musst, solltest du die Nachrichten von denen folgen, ob sie die Schwachstelle bereits gepatcht haben oder ob sie überhaupt betroffen sind oder nicht. Unsere Dienste sind nicht betroffen.
Aktualisiere auch deine Geräte (Smartphones, Laptops/Desktops, Server, IoT...) so bald wie möglich, am besten jetzt, was im Allgemeinen regelmäßig und jetzt mehr denn je der Fall sein sollte.
Es gibt eine Liste, die zeigt, welche Software betroffen ist oder für die bereits ein Patch verfügbar ist.
[Check it out](https://github.com/cisagov/log4j-affected-db/blob/develop/SOFTWARE-LIST.md).

# How to
Wenn du Hilfe bei der Überprüfung deiner Software benötigst, haben wir eine Kurzanleitung für die [Community](https://wiki.techsaviours.org/de/vulnerability_scans/log4shell) bereitgestell. Ansonsten kontaktiere uns einfach per E-Mail etc.

Bleib geschützt - im realen und virtuellen Leben
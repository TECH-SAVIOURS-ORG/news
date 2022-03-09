---
title: 'Microsoft und die Seltsamkeiten bei der Abfertigung von E-Mails'
taxonomy:
    category:
        - news
    tag:
        - server
        - microsoft
        - email
        - blacklist
published: true
date: '15-01-2022 20:47'
---

# Microsoft und die Seltsamkeiten bei der Abfertigung von E-Mails

Microsoft hat in diesem Jahr einige Probleme mit seinen Exchange-Diensten gehabt - https://blog.mxtoolbox.com/2022/01/. Vielleicht hat es nichts mit dem Problem eines unserer Kunden zu tun, aber Microsoft hat sehr seltsame Methoden, wenn es um die Annahme von E-Mails geht. 

In diesem speziellen Fehler erwähnt mxtoolbox, dass einige E-Mails möglicherweise nicht einmal das Ziel erreichen. Wundere dich also nicht, wenn die Fotos an deine Familie und Freunde oder eine Rechnung an deine Kunden schicken und keine Antwort zurückbekommen. Es könnte genau der Grund dafür sein, dass sie deine E-Mail nicht erhalten haben.


## Microsoft blockiert willkürlich IPs

In unserem Fall wurde unser Kunde einfach ohne jeden Grund gesperrt. Der Server läuft seit Jahren, und nach einigen Tests ist weder vorher noch nachher ein seltsames Verhalten aufgetreten.  
Microsoft ist dafür bekannt, IPs willkürlich zu sperren oder generell seltsame Techniken anzuwenden, wenn es um E-Mails geht. Hetzner, Digitalocean, Linode, mailbox.org, protonmail.com ... sie alle haben ständig Probleme mit Microsoft. Und niemand kann wirklich sagen, warum Microsoft ständig IPs blockiert.

Nicht einmal Microsoft selbst weiß es:

> Hallo,
>
> Mein Name ist "DER NAME" und ich arbeite für das Outlook.com Sender Support Team.
>
> Ich sehe auf Anhieb nichts bei IP: (UNSERE KUNDEN-IP), was verhindern würde, dass Ihre E-Mail unsere Kunden erreicht. 


Eine weitere E-Mail:

> Wir konnten auf unserer Seite nichts finden, was verhindern würde, dass Ihre E-Mail Outlook.com-Kunden erreicht.
>
> Wenn Sie immer noch Probleme mit der Zustellbarkeit haben, antworten Sie bitte auf diese E-Mail mit einer detaillierten Beschreibung des Problems, einschließlich spezifischer Fehlermeldungen, und ein Mitarbeiter wird Sie kontaktieren.

Wir haben also direkt geantwortet, und es ist ziemlich offensichtlich, dass das Problem auf Microsofts Seite liegt:

> Host
    css-one-microsoft-com.mail.protection.outlook.com[40.93.207.0] sagte: 550
    5.7.511 Zugriff verweigert, gesperrter Absender[IP]. Um die Entfernung
    aus dieser Liste zu beantragen, leiten Sie diese Nachricht bitte an
    delist@messaging.microsoft.com. Für weitere Informationen besuchen Sie bitte
    http://go.microsoft.com/fwlink/?LinkId=526653. AS(1410)
    [CB1PEPF0000205E.namprd00.prod.outlook.com] (als Antwort auf den Befehl RCPT TO)

Aber es scheint, dass hauptsächlich 365/Outlook-Business-Nutzer betroffen sind. Privatanwender mit Outlook- oder Hotmail-Konten scheinen problemlos zu funktionieren. Zumindest haben wir unsere privaten Testkonten (Outlook & Hotmail) ausprobiert und es gibt keine Probleme.  


# Microsoft hat seine eigene RBL (Realtime Blackhole List)

Es wäre für alle schön, wenn Microsoft auch die seit 25 Jahren frei verfügbaren RBL-Listen verwenden würde. Aber leider ist das nicht der Fall. Microsoft verwendet seine eigene Liste.  
Checks für uns und andere E-Mail-Anbieter lassen uns im Dunkeln tappen. 


# Streichung aus der Microsoft Liste

Es gibt mehrere Möglichkeiten, die du ausprobieren kannst:

- https://sender.office.com/
- https://support.microsoft.com/en-us/supportrequestform/8ad563e3-288e-2a61-8122-3ba03d6b8d75

In unserem speziellen Fall können wir nichts tun. Wir können sie nur ärgern und ihnen weitere E-Mails schicken, damit sie die gesperrte IP endlich löschen. Als Notlösung haben wir eine sehr ähnliche Domain mit einem anderen E-Mail-Server verwendet.   
Wenn du andere Ideen hast, lassen es uns bei [fosstodon](https://fosstodon.org/web/@techsaviours/107625303213896654) wissen.
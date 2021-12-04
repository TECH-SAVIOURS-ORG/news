---
title: 'Unser News/Blog ist online mit GRAV'
taxonomy:
    category:
        - news
    tag:
        - 'TECH SAVIOURS'
media_order: 'ts&grav.png'
aura:
    author: dan
date: '04-12-2021 12:40'
published: true
---

Wir freuen uns sehr, unseren neuen News-Bereich zu veröffentlichen!

# WordPress, Drupal, Grav ... welches?!
Nachdem wir einige Optionen wie WordPress, Drupal & Co. verglichen haben, haben wir uns für GRAV entschieden. Das ist ein großartiges CMS (Content Management System), das in php geschrieben ist. Eigentlich genau wie die anderen beiden genannten, aber GRAV braucht keine Datenbank. Es speichert Daten in einer Flat-File CMS, die in Ordnern organisiert sind, anstatt in einer Datenbank. Das macht es wirklich schnell und sehr leicht.  
Die erste Version von GRAV wurde am 30. Juli 2014 veröffentlicht, es ist also relativ neu im Vergleich zu WordPress (2003) und Drupal (2001), aber es hat sich zu einer bekannten CMS-Alternative entwickelt. GRAV wird von weniger als 0,1% aller CMS-Systeme verwendet - [w3techs.com](https://w3techs.com/technologies/details/cm-grav). Das ist nicht viel im Vergleich zu den Großen - WordPress hat den Markt mit respektablen [65,1%](https://w3techs.com/technologies/details/cm-wordpress) im Griff und Drupals Marktanteil beträgt [2,1%](https://w3techs.com/technologies/details/cm-drupal).  
Wirf einen Blick auf die Nutzungsstatistiken der beliebtesten [Content Management Systeme](https://w3techs.com/technologies/overview/content_management).

# Drupal oder GRAV
Unser Hauptvergleich am Ende waren Drupal und GRAV. Beide haben ausgezeichnete Sicherheitspraktiken. 
Bei der Überprüfung der neuesten Schwachstellenstatistiken auf CVE-Details für [Drupal](https://www.cvedetails.com/product/2387/Drupal-Drupal.html?vendor_id=1367) und [GRAV](https://www.cvedetails.com/product/59205/Getgrav-Grav-Cms.html?vendor_id=20511) haben wir uns mehr in Richtung GRAV bewegt.  
Und am Ende sind unsere Newsfeeds nur ein paar Buchstaben und Bilder. Die anderen wären viel zu umfangreich für unser kleines Ziel.  
GRAV verwendet [Markdown-Syntax](https://learn.getgrav.org/17/content/markdown), die wir bevorzugen, und die Konfigurationsdateien/Seiten sind in [YAML-Syntax](https://learn.getgrav.org/17/advanced/yaml), die man in vielen Tools wie Ansible, Kubernetes, Prometheus, Matrix ... findet, um nur einige zu nennen.   
GRAV passt also nicht nur zu unseren Bedürfnissen, sondern auch zu unserer Infrastruktur.  

# Pinpress theme
Nachdem die Entscheidung gefallen war, begannen wir mit der Suche nach einem Theme. Und davon gibt es eine ganze Menge. Einfach und leicht zu lesen war nun das nächste Ziel. Und ein ähnliches Aussehen wie unsere Haupt-Website, die mit [Bootstrap](https://getbootstrap.com/) erstellt wurde.  
Das [PinPress-Theme](https://demo.getgrav.org/pinpress-skeleton/) scheint eine gute Wahl zu sein, und bisher haben wir nicht wirklich etwas zu beanstanden. Es war ein bisschen schwierig, es an unser Design anzupassen, weil die Standardeinstellungen des Themes nicht so gut funktionierten, wie wir dachten.

## Theme inheritance aka child theme
Wir begannen zunächst mit einem [_Inheriting theme_](https://learn.getgrav.org/16/themes/customization#inheriting-manually) (Child-Theme), mit dem wir unsere Änderungen vornehmen können und die Möglichkeit behalten, das Theme zu aktualisieren, ohne unsere Änderungen zu überschreiben.  
Sobald wir alles fertig hatten, war unser erster Schritt "Aufräumen". Wir haben alle Verbindungen zu Drittanbietern entfernt, um noch mehr Leistung aus GRAV herauszuholen und eine bessere Benutzerfreundlichkeit beim Lesen unserer Nachrichten und vor allem beim Durchklicken des Inhalts zu erreichen, aber auch für uns, während wir daran arbeiten.  
Um alles direkt vom Server aus zu hosten, haben wir uns außerdem entschlossen, das Icon Pack von [Fork Awesome](https://forkaweso.me/Fork-Awesome/) herunterzuladen. Ja, sie sind wirklich ... awesome!  
Schließlich haben wir dem Theme unsere persönliche Note gegeben, wie Favicon, Logo, Footer etc. und die [twig-Dateien](https://en.wikipedia.org/wiki/Twig_(template_engine)) an unsere Bedürfnisse angepasst.  

# MIT license
GRAV ist lizenziert unter der [MIT-Lizenz](https://github.com/getgrav/grav/blob/develop/LICENSE.txt). Dies ist eine sehr unkomplizierte Lizenz.

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

## Rechte
Du hast das Recht, Kopien der Software zu verwenden, zu vervielfältigen, zu modifizieren, zusammenzuführen, zu verbreiten, zu veröffentlichen, Unterlizenzen zu vergeben und zu verkaufen. 

## Bedingungen
Der MIT-Lizenztext und der Copyright-Hinweis müssen weiterhin in jedem unveränderten MIT-lizenzierten Code enthalten sein. Dein neuer Code kann unter einer anderen Lizenz stehen.

# Fazit
Das Ergebnis ist nun sichtbar und wir sind sehr zufrieden damit.  
Aber nicht alles ist perfekt. Es gibt ein großes Problem, das GRAV hat, insbesondere für Nachrichten- und Blog-Autoren. Das automatische Posten von Nachrichten auf verschiedenen Medienkanälen ist auch 2021 noch mühsam. Wahrscheinlich sogar im Jahr 2022, das nicht mehr weit entfernt ist. Du musst deine Nachrichten manuell posten oder andere Lösungen wie [IFTTT](https://ifttt.com/explore/new_to_ifttt) finden.  
Unser Plan ist es, Nachrichten alle zwei Wochen oder wöchentlich zu veröffentlichen. Für uns ist es in Ordnung, diese manuell in den sozialen Medien zu posten, bis wir eine andere Lösung finden, die zu uns passt.  
Wir werden also sehen, was die Zukunft bringt und wie GRAV auf lange Sicht funktioniert.  

Wenn du mehr über GRAV lesen möchtest, schau dir den Link an - [Was ist Grav?](https://learn.getgrav.org/17/basics/what-is-grav)

# Und was jetzt?

Wie wir im [Fazit](#fazit) erwähnt haben, ist unser Plan, alle zwei Wochen oder wöchentlich News zu veröffentlichen.   
Damit du unsere News nach Belieben verfolgen kannst, haben wir einige Accounts in den sozialen Medien eingerichtet. Du findest die Links in der grauen Box, oben rechts oder unter den News, je nachdem, wie dein Gerät/deine Auflösung eingestellt ist.  
  
@reddit followers
Nicht jeder Artikel wird in unserem Subreddit veröffentlicht. Da die Regeln nicht dazu gedacht sind, für sich selbst zu werben, werden wir nur Informationen über den Datenschutz und andere Dinge posten, ohne unsere Nachrichten/Blogs zu erwaehnen. Das bedeutet, dass alle Änderungen an TECH SAVIOURS nur auf den anderen Kanälen erscheinen werden.   

Wenn du irgendwelche Vorschläge oder Feedback hast, lass es uns wissen.

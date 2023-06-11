---
title: 'TECH SAVIOURS News - 11.06.2023 (German)'
published: true
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
Es ist ein bisschen ruhig um die Dienste, Wiki etc. pp. geworden.  
Hauptsächlich liegt es an der Arbeitsbelastung, Gesundheit und eines Umzuges in ein anderes Haus, der mich daran hinderte etwas für .ORG zu tun.  
So langsam kommt aber wieder ruhe rein und es wird wieder dran gearbeitet.

# Updates & searx/ng
Updates wurden aber logischerweise dennoch regelmaessig durchgefuehrt.  
Durch die updates auf python 3.11 hat sich ein bissel an der searx instance was getan. Statt searx laeuft jetzt searxng.  
Die Unterschiede zwischen den beiden sind hier aufgelistet - https://github.com/searxng/searxng#differences-to-searx.

Die Domain bleibt dennoch die gleiche - https://searx.techsaviours.org.  
Im grunde genommen ist alles auf Default-Einstellungen belassen. Abgesehen, das es generell auf Dark-Theme laeuft und ein bissel Branding eingesetzt wurde.

# Wiki
Die Wiki ist eigentlich fast fertig. Demnaechst wird Wireguard als abrundung dazu stossen. Damit auch deine Server zu Hause auch von ausserhalb erreichbar sein werden.  
Die Wiki kann man dann so zu sagen als Basic verstehen. Es gibt aber so viel mehr was man tun kann fuer die eigene Privatsphaere aber das kommt auch immer auf sein eigenen "Gebrauch" an.  
Ich persoenlich zB benutze ein paar Kameras im Haus. Da kommen ein paar fragen auf: 
- was fuer Geraete sind dafuer notwendig
- welche Software
- blocken der Propriety Geraete via Firewall & AdGuardHome
- ...

Sprich, es werden wohl frueher oder spaeter diverse Open Source Software dazu stossen, die deine Privatsphaere erweitern koennen. In diesem Fall, waere wohl Home Assistant, Frigate, ... ein gute erweiterung fuer die Wiki.

Ebenso soll auch ein Linux Bereich fuer "Phones" kommen. Das bekannte PinePhone (Pro) wurde von mir letzten Jahres fuer ca 10 Monate als Daily Driver benutzt. Es ist super und ich wuenschte die Batterie haelt mindestens einen Tag. Fuer mich reichen die vorhandenen Apps aber das Telefonieren und vor allem die Batterie war es nicht wert, es weiterhin zu benutzen.  
Das Keyboard hat einem weitere 6000mah an Batterie verschaft. Es reichte gerade so fuer einen Tag ... sehr nervig ... Die Gespraechsqualitaet ist auch nicht so prickelnd. Oft wurde nachgefragt, was ich denn ueberhaupt gesagt haette.  
Dennoch sehe ich grosses Potenzial in Linux fuer Mobile Geraete. Auch das neue pinetab2, sieht sehr vielversprechend aus.  
Lange rede... dies wird auch noch in die Wiki aufgenommen werden. 

# Matrix
Demnaechste werden ein paar ausfallzeiten kommen. Da die Retention seit ende letzten Jahres ausgestellt wurde (https://techsaviours.org/news/en/whats-been-going-on-lately-new-server-matrix#matrix), wird manuell eingegriffen. So werden mindestens die Top 15 rooms ein bissel entschlackt:
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
Die Database groesse (70GB) haelt sich noch in grenzen aber lieber zu frueh als zu spaet.

Ebenso werden alle User, die sich laenger als seit einem Jahr nicht mehr angemeldet haben, geloescht. Wenn du also dich vor ueber einem Jahr nicht mehr hast blicken lassen und du dein Account bzw Usernamen behalten moechtest, melde dich kurz an.

Das solls erst einmal gewesen sein. Fuer alle die, die sich hier rumtummeln, wissen auf jeden Fall erstmal Bescheid.  
Ein schoenes rest Wochenende!
Dan
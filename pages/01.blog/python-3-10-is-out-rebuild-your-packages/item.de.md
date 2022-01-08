---
title: 'python 3.10 ist erschienen - erstelle deine Pakete neu'
taxonomy:
    category:
        - news
    tag:
        - python
        - arch
aura:
    author: dan
media_order: python-software-logo.jpg
date: '15-12-2021 18:58'
---

Alle neuen Python-Funktionen finden Sie [hier](https://docs.python.org/3/whatsnew/3.10.html).  
Wenn du Probleme mit Arch hast, nachdem du dein System aktualisiert hast, führe einfach die folgenden Befehle aus:
```
pacman -Qoq /usr/lib/python3.9
pikaur -S $(pacman -Qoq /usr/lib/python3.9) --rebuild
```
mit deinem aur-helper.
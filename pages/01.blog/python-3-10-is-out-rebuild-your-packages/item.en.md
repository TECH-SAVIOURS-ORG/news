---
title: 'python 3.10 is out - rebuild your packages'
media_order: python-software-logo.jpg
taxonomy:
    category:
        - news
    tag:
        - python
        - arch
aura:
    author: dan
date: '15-12-2021 18:58'
---

All new Python features can be found [here](https://docs.python.org/3/whatsnew/3.10.html).  
If you have problems with Arch after upgrading your system, just run the command/s:
```
pacman -Qoq /usr/lib/python3.9
pikaur -S $(pacman -Qoq /usr/lib/python3.9) --rebuild
```
with your aur-helper.
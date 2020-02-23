---
author: IW3AMQ
comments: false
date: 2018-08-20 07:04:46+00:00
layout: page
link: https://drc.bz/rittnerhorn-ir3uhf-reflector-xlx321-hat-nun-ambe-transcoder-xc-3006/
slug: rittnerhorn-ir3uhf-reflector-xlx321-hat-nun-ambe-transcoder-xc-3006
title: Rittnerhorn IR3UHF - Reflector XLX321 hat nun AMBE Transcoder XC-3006
wordpress_id: 17049
tags:
- C4FM
- D-STAR
- DMR
- Umsetzer Rittner Horn
---

![](https://drc.bz/wp-content/uploads/2018/08/XC-3006Top.jpeg)

Mit dem D-Star hat vor einigen Jahren alles angefangen, heute gibt's im digitalen Funkamateurbereich vorwiegend 3 verschiedene Betriebsarten: D-Star, DMR und C4FM. Alle 3 Betriebsarten verwenden für die Komprimierung der Sprache einen eigenen Chip von [Digital Voice Systems Corporation](http://www.dvsinc.com/), der sogenannte "[AMBE](https://de.wikipedia.org/wiki/Advanced_Multi-Band_Excitation)" Kodierung (Advanced Multi-Band Excitation) enthält.

Diese Kodierung ist proprietär und durch Patente geschützt. Leider hat Icom damals bei der Ersteinführung von D-Star auf diese Kodierung gesetzt, da es damals auch nichts besseres gab. Später erst entwickelten sich im Funkamateurbereich andere freie Kodierungen zur Komprimierung von Sprache, wie [Free DV](https://freedv.org/) mit nur 1,25 kHz Bandbreite (DStar 6,25 kHz, DMR und C4FM 12,5 kHz, FM-N 12,5 kHz, FM-W 25,0 kHz). Einen interessanten [Artikel dazu hat Kurt, OE1KBC](https://www.oe1-oevsv.at/downloads/ibt_2016-03-10_oe1kbc_betriebsarten_digitale_sprache.pdf) geschrieben.

D-Star verwendet noch eine ältere Komprimierung (AMBE), DMR und C4FM bereits die neuere (AMBE++). Damit nun jemand mit einem D-Star Funkgerät mit einem anderen Teilnehmer mit einem DMR oder C4FM Funkgerät sprechen kann, hat [NW-Digital Radio](http://nwdigitalradio.com/product/xc-3006/) eine Platine entwickelt, die 2 Stück AMBE-3000F enthält und gleichzeitig 6 Audiokanäle von AMBE zu AMBE++ und umgekehrt "transkodieren" kann.

![](https://drc.bz/wp-content/uploads/2018/08/IMG_20180817_161515_607-1024x768.jpg) ![](https://drc.bz/wp-content/uploads/2018/08/XC-3006-e1534748412115.jpg)

Diese Platine, verbunden mit einem Raspberry hängt nun im Hamnet im Serverschrank am Rittnerhorn und erledigt die sprachliche Transkodierung zwischen D-Star und DMR/C4FM. Somit gibt es eine exzellente Sprachqualität und jeder "digitalisierte" Funkamateur kann nun mit jedem anderen digitalisierten Funkamateur sprechen.

Die Hardware wurde von Thomas IW3AMQ vorbereitet (Raspberry, SD-Karte, Spannungsversorung), die Installation erledigte Simon IN3FQQ vor Ort.

Infos über den Südtiroler Reflektor XLX321 findet man in der [Übersicht](https://drc.bz/betriebsarten/digitalfunk/uebersicht/) und im [Dashboard](http://xlx321.net.drc.bz/index.php).

Viel Spaß und 73!

Thomas IW3AMQ & Simon IN3FQQ

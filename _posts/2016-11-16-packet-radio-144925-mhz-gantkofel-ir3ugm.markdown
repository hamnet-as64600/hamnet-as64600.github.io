---
author: IW3AMQ
comments: false
date: 2016-11-16 20:32:10+00:00
layout: page
link: https://drc.bz/packet-radio-144925-mhz-gantkofel-ir3ugm/
slug: packet-radio-144925-mhz-gantkofel-ir3ugm
title: Packet Radio 144,925 MHz - Gantkofel IR3UGM
wordpress_id: 13277
categories:
- HamNet
- Umsetzer Gantkofel
---

Packet Radio? Steinalte Betriebsart, aber ...

... aber es gibt (meistens) einen guten Grund, warum gerade diese Betriebsart am [Gantkofel](https://drc.bz/relaisstandorte/test-mini-link-sudtirol-2/) wieder QRV ist! Pater Peter [OE7MCJ](http://www.mauler.info/adl701/peter.htm) ist Missionar in Mondombe in Kongo und bleibt mit seiner Kurzwellenstation in der Betriebsart Pactor mit seiner Heimat in Kontakt. Peter IN3GHZ stellt dazu sein Kurzwellen Gateway Pactor-Packet Radio zur Verfügung und der DRC den dazu nötigen Packet Radio Einstieg am Gantkofel IR3UGM auf **144,925 MHz**, 1.200 Baud. Dieser Packet Radio Einstieg ist mit dem [Hamnet](https://drc.bz/relaisstandorte/karte-der-relaisstandorte/) verbunden, der die vom Peter IN3GHZ empfangenen Daten zur Gefrorenen Wand OE7XGR schickt, mit 54 MBit auf 5 GHz.

Für den Packet Radio Digipeater wurden ein altes 2 m Zivilfunkgerät von Ducati, ein altes TNC2 mod4 von IN3BQX und das DLC7 von IW3BRC wiederverwendet. Das Eeprom vom Ducati musste neu programmiert, die Anschlüsse für die NF vorbereitet, das Eeprom des TNC2 programmiert, eine Gold-Cap eingesetzt, die Parameter des DLC7 angepasst und schließlich musste alles noch verbunden werden. Und es sollte ja auch getestet werden ... aber da war kein Modem so schnell zur Verfügung.

Ein alter DOS Laptop (CPU 40 MHz!!!) wurde zusammen mit einem altes Baycom Modem für die RS232 Schnittstelle ausgegraben, zusammen mit einem alten Duoband-Handfunkgerät von Standard C558. Der Test auf der Prüfbank lief nach den erforderlichen Programmierungen hervorragend.

Um Packet-Radio aber doch noch mit einem neuen Laptop ohne RS232, aber USB Schnittstelle zu probieren, habe ich eine USB-Soundkarte verwendet, diese mit einem VOX-Ptt versehen und schon konnte auch mit diesem und der Software von [UZ7HO](http://uz7.ho.ua/packetradio.htm) Betrieb gemacht werden. Das PTT - Kriterium wurde durch das Audiosignal in der VOX - Schaltung generiert. So ist Packetradio mit einer USB-Soundkarte ohne eigenen PTT-Anschluß am PC möglich (siehe Schaltplan)! Das Modem würde sich sogar für die schnellere Betriebsart mit 9.600 Baud nach G3RUH eignen, die NF-Anschlüsse können aber dann nicht mehr über die Buchsen des Handfunkgerätes erfolgen, sondern müssen direkt auf den FM-Diskriminator bzw. Modulator zugreifen.

[![20161116_205732](https://drc.bz/wp-content/uploads/2016/11/20161116_205732-300x169.jpg) ](https://drc.bz/wp-content/uploads/2016/11/20161116_205732.jpg)[![usb-soundcard-packetradio](https://drc.bz/wp-content/uploads/2016/11/USB-Soundcard-Packetradio-300x216.jpg)](https://drc.bz/wp-content/uploads/2016/11/USB-Soundcard-Packetradio.jpg)

Die Gerätschaft wurde dann am Freitag, 11.11.2016 mit 5 cm Schnee am Gantkofel installiert. Dafür brauchte es noch einen Duplexer 2m/70cm, ein Switching-Netzteil zu 12 V / 6 A, mehrere HF-Adapter und ein Notchfilter auf 100 MHz für bessere Empfindlichkeit des RX.

[![20161111_141747](https://drc.bz/wp-content/uploads/2016/11/20161111_141747-300x169.jpg)](https://drc.bz/wp-content/uploads/2016/11/20161111_141747.jpg) [![20161112_131645](https://drc.bz/wp-content/uploads/2016/11/20161112_131645-300x169.jpg)](https://drc.bz/wp-content/uploads/2016/11/20161112_131645.jpg)

Involviert waren für dieses kurzfristig beschlossene Projekt: Markus OE7FMI (DLC7), Peter IN3GHZ (Pactor Gateway), Simon IN3FQQ (Hamnet), Thomas IW3AMQ (TNC2, DLC7, Ducati und Installation am Gantkofel), Tobias IW3BRC (DLC7).

An alle ein herzliches DANKE!

73! Thomas, IW3AMQ

---
author: admin
comments: false
date: 2011-08-26 17:56:20+00:00
layout: post
link: https://drc.bz/ir3ugm-erster-pr-digi-im-hamnet/
slug: ir3ugm-erster-pr-digi-im-hamnet
title: 'IR3UGM: Erster PR-Digi im HAMNET !'
wordpress_id: 3584
categories:
- HamNet
- Packet Radio
---

Hallo Hamnettler und Packet Radio Freaks,

endlich haben wir heute den ERSTEN Packet-Radio-Digi in Südtirol der einerseits die klassische Betriebsart beherrscht (also Packet Radio 1k2 auf 144.925 MHz) und andererseits bereits im HAMNET eingebunden ist!

**HAMNET Digipeater Gantkofel - Monte Maccaion JN56ol / 1866m**

**[![](https://drc.bz/wp-content/uploads/2011/08/paxon_ir3ugm.png)](https://drc.bz/wp-content/uploads/2011/08/paxon_ir3ugm.png)
**

IR3UGM ist auf dem Gantkofel positioniert, wo auch zugleich einer von zwei bereits aktiven Hamnet-Zugängen geschalten wurde. Somit ist der DIGI keineswegs mehr irgend ein Relikt aus alten Zeiten, sondern der einfache beweis, dass sich "Altes" mit "Neuem" wunderbar kombinieren lässt. Hier die erreichbaren Ziele via IR3UGM:

[![](https://drc.bz/wp-content/uploads/2011/08/destinations.png)](https://drc.bz/wp-content/uploads/2011/08/destinations.png)

Natürlich ist der Digi nun auch im Hamnet via **Webbrowser (http://44.134.190.18/)** erreichbar.

[![](https://drc.bz/wp-content/uploads/2011/08/browser_ir3ugm.png)](https://drc.bz/wp-content/uploads/2011/08/browser_ir3ugm.png)

Hier noch ein paar Worte zur Technik:

**(PR-)Zugang via HAMNET**

Packet Radio kann nicht nur ueber die herkoemmlichen 1200 bzw. 9600 Baud Zugaenge gemacht werden. Auch im HAMNET - Highspeed Amateur Multimedia Network kann man sich Zugang zum Packet Radio Netzwerk verschaffen. Etwa am Marlinger Berg (IR3UHE) bei Meran besteht fuer Benutzer die Moeglichkeit sich via 2,4GHz zum Accesspoint zu verbinden, und mit herkoemmlicher Software wie Flexnet und Paxon PR-Betrieb zu machen.

Bitte Fragen an den lokalen Sysop (iw3brc@drc.bz).

Ueber die schnelleren Einstiege koennen im Gegensatz zu den 1k2 und 9k6 Zugaengen nicht nur klassische textbasierte Packet Radio-Systeme gearbeitet werden, sondern dort stehen auch weiteren Anwendungen im sog. HAMNET zur Verfuegung. Einige davon sind auch mit PR querverknuepft. (z.B.: Winlink, Mailserver Packet Radio Mailboxen, DX-Cluster etc ...), andere (ATV, Wetterstationen, Webserver, APRS, Fonie) sind eigenstaendig.

**Technische Infos: PR-Strecken via HAMNET (Transport von AX25 im HAMNET)**

Unter Anwendung des OSI-Modells koennen AX.25 Datenpakete mittels AXUDP oder AX-over IP Paketen 'per Rucksack' im HAMNET transportiert bzw. eingebettet werden. Die Geschwindigkeit uebertrifft dabei ein vielfaches der bestehenden 23cm 9k6 oder 19k2-FSK-Technik.

Die AX.25 Pakete koennen ueber Schnittstellen zu RMNC-Digipeater (zb.: KISS-Karte) oder direkt an neuere Knotenrechner (z.B: DLC7 mit XNET) in das HAMNET eingespeist und auf den Protokollschichten 'huckepack' genommen werden.

So koennen Packet-Linkstrecken zwischen Digipeatern auch ueber HAMNET-HF-Strecken zusammengeschaltet werden. Es ist auch moeglich, als Funkamateur ueber einen HAMNET-HF-Userzugang in das Packet-Radio-Netz einzuloggen.

Eine bisher gebraeuchliche Art des Huckepackverkehrs war der umgekehrte Fall, das sogenannte 'IP over AX25' oder oft auch 'TCP/IP over AX' genannt. Hierbei koennen ueber PR-Usereinstiege auch Webseiten oder andere IP-Dienste in z.T. langsamer Geschwindigkeit genutzt werden. Da AMPR einen TCPIP Stack ueber das AX25 Packetradio Netz benoetigt, muss eine entsprechende Software wie Flexnet, AGW, WAMPES oder ax25-Linux vorhanden sein. Dabei ist der TCPIP-Stack fuer die jeweilige Anwendung transparent und es koennen diverse gewohnte Anwendungen verwendet werden.



* * *



In beiden Faellen ('IP over AX' und 'AX over IP') werden IP-Adressen benoetigt.
** **

**Die IP-Hamnet-Koordination fuer die Zone Bozen/Trient uebernimmt IW3BRC (Tobias) - iw3brc@drc.bz - 73!**

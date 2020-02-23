---
author: IN3DOV
comments: false
date: 2016-04-02 11:20:41+00:00
layout: page
link: https://drc.bz/hamnet-anbindung-clublokal-bruneck-richtung-kronplatz-verbessert/
slug: hamnet-anbindung-clublokal-bruneck-richtung-kronplatz-verbessert
title: HAMNET- Anbindung Clublokal Bruneck Richtung Kronplatz verbessert.
wordpress_id: 11867
tags:
- Clublokal
- HamNet
---

[![IMG_5662](https://drc.bz/wp-content/uploads/2016/04/IMG_5662-225x300.jpg)](https://drc.bz/wp-content/uploads/2016/04/IMG_5662.jpg)Am gestrigen Freitag waren Benjamin IN3GKJ, Thomas IW3AMQ und ich im Clublokal Bruneck, um die HAMNET-Anbindung zu verbessern.

Die Signalwerte von ca. -90 dBm haben auch schon bei der Audio/Video-Übertragung beim letzten OV-Abend für Probleme gesorgt.

Folgendes war geplant:

Austausch der 2,4 GHz Panelantenne im Clublokal durch eine Grid-Parabel mit mehr Gewinn.

In einem zweiten Moment: Austausch der 120° Sektorantenne am Kronplatz durch genau diese Panelantenne, die im CL installiert war.



Die Ausgangslage am Freitag Nachmittag mit der Panelantenne war die folgende:



	
  * TX/RX Signal:** -90 dBm, -76 dBm**

	
  * SNR:** 11 dB**


Nachdem Benjamin und Thomas ganz fleißig ihre Arbeiten auf dem Dach erledigt hatten und die neue (deutlich größere) Antenne installiert war, waren die Werte leider immer noch gleich schlecht. Einige dB besser war es zwar, aber immer noch nicht besonders gut.

Nachdem auch Herbert IW3BRH im Clublokal eingetroffen war, lieferte er uns den entscheidenden Hinweis: Zwischen dem Routerboard, welches im Dachboden installiert war, und der Antenne lag ein zu langer Koaxialkabel RG5!! Wie Thomas feststellen konnte, war dieses auch nicht gerade ideal zur Übertragung von 2,4 GHz Signalen.

Thomas war jedoch wie immer super vorbereitet und hatte einen Mikrotik Groove52 im Gepäck. Wir haben uns kurzerhand entschlossen das alte Routerboard samt Koax komplett abzubauen und den Groove direkt an der Antenne zu montieren.

Nachdem wir ein neues LAN-Kabel vom Rack-Schrank im Clublokal aufs Dach verlegt und alles nötige verkabelt hatten, sahen die Werte schon bedeutend besser aus! Signale bewegten sich um -48 bis -60 dBm, mit einem SNR von gut 30 dB!

Da die Signalwerte nun so gut ausfielen, habe ich auch gleich die Internet Anbindung vom CL umgestellt. Diese läuft nun ebenfalls über den Kronplatz. Ich habe dafür auf dem Router am Kronplatz (IR3DV1, 44.134.190.97), welcher für die Useranbindung verantwortlich ist, eine NAT-Regel eingefügt, welche explizit und ausschließlich dem Clublokal den Internetzugang ermöglicht.
Damit das ganze halbwegs flüssig läuft, haben wir die Bandbreite des Userzugangs auf 10 MHz umgestellt.

Die technischen Daten sind nun folgende:

	
  * Protokoll: im Moment** 802.11b/g**

	
  * Tx/Rx Signal:** ca -60/-50 dBm**

	
  * SNR: ca. **30 dB**


Das Clublokal hat somit jetzt sowohl Internet als auch Hamnet-Zugang. Das Routing passiert automatisch, d.h. auf den Rechnern im Clublokal müssen keine besonderen Einstellungen vorgenommen werden um Seiten im Hamnet aufrufen zu können.

Grüße Simon IN3FQQ
[![IMG_5657](https://drc.bz/wp-content/uploads/2016/04/IMG_5657-300x225.jpg)](https://drc.bz/wp-content/uploads/2016/04/IMG_5657.jpg) [![IMG_5658](https://drc.bz/wp-content/uploads/2016/04/IMG_5658-300x225.jpg)](https://drc.bz/wp-content/uploads/2016/04/IMG_5658.jpg) [![IMG_5659](https://drc.bz/wp-content/uploads/2016/04/IMG_5659-300x225.jpg)](https://drc.bz/wp-content/uploads/2016/04/IMG_5659.jpg) [![IMG_5660](https://drc.bz/wp-content/uploads/2016/04/IMG_5660-300x225.jpg)](https://drc.bz/wp-content/uploads/2016/04/IMG_5660.jpg) [![IMG_5661](https://drc.bz/wp-content/uploads/2016/04/IMG_5661-300x225.jpg)](https://drc.bz/wp-content/uploads/2016/04/IMG_5661.jpg)

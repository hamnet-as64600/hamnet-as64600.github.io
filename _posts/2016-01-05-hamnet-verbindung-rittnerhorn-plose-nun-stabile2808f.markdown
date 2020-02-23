---
author: IW3AMQ
comments: false
date: 2016-01-05 14:50:17+00:00
layout: page
link: https://drc.bz/hamnet-verbindung-rittnerhorn-plose-nun-stabil%e2%80%8f/
slug: hamnet-verbindung-rittnerhorn-plose-nun-stabil%e2%80%8f
title: HAMNET-Verbindung Rittnerhorn-Plose nun stabil‏
wordpress_id: 11391
tags:
- HamNet
- Umsetzer Plose
- Umsetzer Rittner Horn
---

[5.1.2016] Hallo zusammen,




die HAMNET-Verbindung vom Rittnerhorn auf die Plose war über lange Zeit ziemlich instabil. Man hat das vor allem bei Link-Südtirol-QSOs gemerkt, weil oftmals vom Knoten Plose von einem Moment zum Nächsten kein Ton mehr ausgesendet wurde oder die Übertragung unterbrochen war.




Nun habe ich gestern beim Durchforsten der Logfiles das Problem lokalisieren und wie es aussieht, beheben können.
[![Hamnet südtirol](https://drc.bz/wp-content/uploads/2016/01/Hamnet-südtirol.jpg)](https://drc.bz/wp-content/uploads/2016/01/Hamnet-südtirol.jpg)
Zuerst wurde ein zu geringes SNR oder allgemein schlechte Übertragungsbedingungen auf dem 2,3GHz-Band vermutet. Es stellte sich jedoch heraus, dass die Signalwerte sowie das SNR und die Kanalqualität sehr gut ausfielen.




Das Problem lag am verwendeten Mikrotik NSTREME Protokoll, welches den Datendurchsatz in Punkt-zu-Punkt Anwendungen gegenüber klassischem 802.11 verbessern soll.
Dieses Protokoll sieht ein "Polling" zwischen den beiden Endpunkten vor. Wenn für eine bestimmte Zeit keine solchen "Polls" mehr durchkommen, dann wird die Verbindung abgebrochen.




Das war dann schlussendlich auch das Problem. Fast im Minutentakt führte es zu Verbindungsabbrüchen. Ich habe gestern Abend dann gegen 20:20 Uhr das Polling auf der Linkstrecke deaktiviert. Von dem Moment an blieb die Strecke aktiv. Jetzt läuft sie ohne Unterbrechungen seit 19 Stunden.




Ich werde in den nächsten Tagen noch ein Auge darauf haben, aber wie es aussieht scheint das Problem behoben zu sein.




Grüße
Simon IN3FQQ

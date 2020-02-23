---
author: IN3FQQ
comments: false
date: 2018-06-24 18:39:25+00:00
layout: page
link: https://drc.bz/erneuerung-der-sender-am-kronplatz/
slug: erneuerung-der-sender-am-kronplatz
title: Erneuerung der Sender am Kronplatz
wordpress_id: 16734
categories:
- Allgemein
- D-STAR
- DMR
- Umsetzer Kronplatz
---

Am gestrigen Samstag, 23. Juni 2018 haben sich Simon IW3BWH, Thomas IW3AMQ und Simon IN3FQQ auf den Weg zum Kronplatz gemacht, um dort die anstehenden Arbeiten zu erledigen. Auf dem Programm standen die folgenden Tätigkeiten:



 	
  * Bessere Positionierung der Digitalfunk-Antenne am Mast

 	
  * Austausch vom DStar-Relais durch das neue Multimode-Digitalrelais

 	
  * Austausch vom LinkSüdtirol Relais

 	
  * Verlegen eines zusätzlichen Ethernet-Kabels vom Turm ins Rack

 	
  * Installation vom neuen Router RB3011, neuem Switch und neuem Sender für den HAMNET-Userzugang


Um 8.00 Uhr ging es von Bozen los auf den Kronplatz. Nach einem kurzen Frühstücks-Zwischenstopp in Kiens ging es dann direkt los mit den Arbeiten: Simon IW3BWH und ich begannen sofort das nötig gewordene zusätzliche Ethernet-Kabel von unserem Antennenplatz am Turm bis ins Rack zu verlegen. Währenddessen hat Thomas IW3AMQ die Antennen von R2 und Link Südtirol neu angeordnet, um Platz für den Dipol für das Digitalrelais zu schaffen. Dieser Dipol war leider bisher an einem recht ungünstigen Punkt montiert und hat vermutlich deshalb nie recht gute Abdeckung erzielt.

Nach den Arbeiten sieht die Antennenanordnung nun so aus:

[![](https://drc.bz/wp-content/uploads/2018/06/IMG_20180623_170034_326-300x225.jpg)](https://drc.bz/wp-content/uploads/2018/06/IMG_20180623_170034_326.jpg)

Von oben nach unten: 2 Element für den R2, Dipol 70cm für das Digitalrelais, Dipol 70cm für Link Südtirol und darunter die Foto-Webcam.

Nach den Außenarbeiten haben wir dann wohlverdient zu Mittag gegessen, um dann mit neuer Kraft im Geräteraum die weiteren Arbeiten durchzuführen. Zuerst wurden die neuen Netzwerkgeräte (Router und Switch) installiert, konfiguriert und dann erste Tests durchgeführt.

[![](https://drc.bz/wp-content/uploads/2018/06/IMG_20180623_175259_501-300x225.jpg)](https://drc.bz/wp-content/uploads/2018/06/IMG_20180623_175259_501.jpg)

Nachdem die HAMNET-Konnektivität wieder vorhanden war haben wir dann das alte, kombinierte Rack mit Link Südtirol und D-STAR Umsetzer abgebaut und durch die zwei neuen, nur 1HE hohen (nur 4,4 cm!) Umsetzer ausgetauscht. Dies war nötig, da der Platz im Rack langsam knapp wurde.

Außerdem haben wir festgestellt, dass der D-STAR Empfänger, ein Motorola GM900, den Geist aufgegeben hatte. Das erklärt, warum das D-STAR Relais in letzter Zeit zwar fleißig alle 10 Minuten die Kennung ausgesendet, aber ansonsten überhaupt nicht mehr reagiert hat.

Im Bild die neuen Umsetzer im 1HE hohen Gehäuse, oben der Link Südtirol (2x Motorola GM900 mit Orange Pi und Svxlink) und unten der neue Multimode-DV Umsetzer (2x Motorola GM340 mit Raspberry Pi und MMDVM)

[![](https://drc.bz/wp-content/uploads/2018/06/IMG_20180623_175438_949-300x225.jpg)](https://drc.bz/wp-content/uploads/2018/06/IMG_20180623_175438_949.jpg) [![](https://drc.bz/wp-content/uploads/2018/06/IMG_20180623_175428_848-300x225.jpg)](https://drc.bz/wp-content/uploads/2018/06/IMG_20180623_175428_848.jpg)

Während Thomas den neuen Link Südtirol Umsetzer getestet hat, ist ihm dann ein interessantes Phänomen aufgefallen: Einigen OMs ist bestimmt schon aufgefallen, dass bei QSO-Durchgängen die vom Kronplatz kommen, die Sprache immer von einem unangenehmen Brummton begleitet wird. Wir haben immer vermutet, dass es an einer falschen Einstellung oder einem Problem auf dem Empfänger liegt.

Thomas hat aber bemerkt, dass das Problem nur bei Subaudio 136.5Hz auftritt. Bei dem eingestellten Subaudio 136.5Hz erzeugen die in der Software programmierten Filter beim Empfangssignal zufälligerweise einen Ton zwischen 600 und 700Hz, welcher dann mitgesendet wird und lokal am Kronplatz sowie auf den anderen Link Südtirol Relais gehört wird.

Aufgrunddessen werden wir den Subaudioton demnächst von 136.5Hz auf 110.9Hz ändern. Damit sollte der Brummton verschwinden.

![](https://drc.bz/wp-content/uploads/2018/06/20180610_235839-1-300x169.jpg) ![](https://drc.bz/wp-content/uploads/2018/06/20180610_235756-1-300x169.jpg)

In den beiden Bildern sieht man das neue Link Südtirol Relais mit den beiden GM900 RTX, links das 10 A Schaltnetzteil und rechts oben der [Orange Pi Zero (Svxlink)](https://drc.bz/technik/analog-digitaltechnik/svxlink-mit-orange-pi-zero/) mit Lochrasteraufsteckplatine für Ptt-Transistor und regelbaren Widerständen für die Rx und Tx Nf-Pegel.

![](https://drc.bz/wp-content/uploads/2018/06/20180612_231711-300x169.jpg) ![](https://drc.bz/wp-content/uploads/2018/06/20180612_231627-300x169.jpg)

Das MMDVM Multimode Digitalrelais habe ich dann ebenfalls in DSTAR und DMR getestet. Beide Betriebsarten liefen perfekt.

Im den beiden Bildern sieht man die beiden RTX GM340, links das 10 A Schaltnetzteil und rechts oben den Rasbperry Pi mit der MMDVM Aufsteckplatine mit dem ST Prozessor.

Da es im Pustertal einige OMs mit Digitalen Yaesu Geräten gibt, ist eine Erweiterung um die Betriebsart C4FM / System Fusion geplant. Dies ist mit dem verbauten MMDVM ebenfalls möglich. **Wir suchen dafür noch dringend Yaesu-Funker, die hier mithelfen wollen.**

Zur Benutzung des Digitalrelais werden wir beim nächsten OV-Abend einige Worte sagen. Ich würde mich über zahlreiche Tests und Reports eurerseits freuen!

Zu guter Letzt sind wir dann noch im Clublokal Bruneck eingekehrt, wo wir dann bei einem gemütlichen Bier die Qualität der neuen HAMNET-Anbindung und die Remotestation getestet haben. Resultat: die Remotestation hat nach Änderung der HAMNET-QRG perfekt und ohne Aussetzer funktioniert, selbst wenn gleichzeitig im Internet gesurft wird.

Alles in Allem ging somit ein sehr erfolgreicher Tag zu ende.

Viel Spaß mit den neuen Relais!

73! Simon, IN3FQQ

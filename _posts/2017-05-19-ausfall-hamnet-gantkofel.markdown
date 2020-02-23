---
author: IW3AMQ
comments: false
date: 2017-05-19 21:45:23+00:00
layout: post
link: https://drc.bz/ausfall-hamnet-gantkofel/
slug: ausfall-hamnet-gantkofel
title: Aufrüstung Hamnet und D-STAR am Gantkofel
wordpress_id: 14245
categories:
- D-STAR
- HamNet
- Link Suedtirol
- Umsetzer Gantkofel
---

Seit Donnerstag, 11. Mai 2017 bestand auf dem Gantkofel ein Problem mit der Richtfunkverbindung Richtung Seceda. Für das Link Südtirol und das Link Zugspitze eine vitale Verbindung.

Der etwas ins Alter gekommene Linkstreckensender, ein RB333 mit einem 802.11b/g Radiomodul von Mikrotik schien den Geist aufgegeben zu haben.

Simon IN3FQQ bemerkte am Montag morgen den Ausfall und konnte noch Montags das Hamnet zwischen Gantkofel und Seceda provisorisch via Fernwartung und mit Hilfe der vor kurzem gedrehten 2. Antenne aktivieren.

Am heutigen Freitag nachmittag, 19. Mai 2017 packten Simon IN3FQQ und ich die Gelegenheit beim Schopf und fuhren trotz Regenvorhersage, auf den Gantkofel.. und wir hatten Glück! Oder besser, alles genau berechnet - der Regen kam erst gegen 16:30, genau wie von der [Niederschlagsvorhersage](http://www.provinz.bz.it/wetter/niederschlagsvorhersage.asp) prognostiziert!

Die alten Radiomodule wurden durch moderne Metal5-Linkstreckensender erstzt, welche neben der erheblich höheren Sendeleistung auch mindestens 10dB mehr Empfangsempfindlichkeit bringen. Außerdem werden höherstufige Modulationsverfahren unterstützt, was wiederum mehr Bandbreite bringt.

Als dann wie vorhergesagt gegen 16:30 der Regen einsetzte, waren wir gerade mit den Arbeiten am Mast fertig. Während dem mittlerweile starken Regenfall nutzten wir dann die Zeit um alle Arbeiten im Container durchzuführen. Im Container wurde ein neuer Router installiert (RB750 Mikrotik vom ex. Rittnerhorn), welcher von nun an die beiden alten Routerboards RB433 und RB333 ersetzt. Der neue Router versorgt alle Richtfunkstrecken via PoE mit Strom und vereinfacht die Netzinfrastruktur am Standort erheblich.

Am Masten haben wir die externe Aluschachtel mit den alten Routerboards RB433 und RB33 von Mikrotik inklusive der Koaxialkabel, die zu den 5GHz und 2,3GHz Antennen führten, entfernt.

Da es beim D-Star Gantkofel schon seit seiner Installation vor knapp 2 Jahren durchwegs Probleme mit der Empfangsempfindlichkeit gegeben hat, wurde bei der Gelegenheit dann auch endlich das D-Star Relais durch ein neueres mit 2 RTX von Motorola GM140 und einem UP4DAR ausgetauscht (spendiert von Christian DL1MCG).  **Wir bitten um Empfangsrapporte!**

Um 17:00 Uhr war dann alles wieder [Online](https://drc.bz/relaisstandorte/test-mini-link-sudtirol-2/)! Hamnet (2,397 GHz für User), Link Südtirol (431,4000 MHz), Link Zugspitze (431,2875 MHz), D-Star (431,5000 MHz), DMR (430,9875 MHz), Packet Radio (144,9250 MHz) und Foto-webcam.

73! Thomas, IW3AMQ

[caption id="attachment_14246" align="aligncenter" width="576"]![](https://drc.bz/wp-content/uploads/2017/05/20170519_190630-e1495230084580-576x1024.jpg) Beschreibung von oben nach unten: Vertikalantenne Dualband 2 m und 70 cm für D-Star und Fernsteuerung, Dipol 70 cm Link Südtirol, Dipol 70 cm Link Zugspitze, Gitterantenne 5 GHz Marlinger Berg, Vertikalantenne Dualband Packet Radio, Userantenne Hamnet 2,397 GHz mit Notchfilter wegen Radiorichtfunk (im Plastikgehäuse) und Metal, Panelantenne 5 GHz Rittnerhorn, Parabolspiegel 5 GHz Seceda (1,20 m Durchmesser)[/caption]

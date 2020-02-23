---
author: IW3AMQ
comments: false
date: 2015-11-20 19:18:59+00:00
layout: page
link: https://drc.bz/r4-rittnerhorn-ir3uhf-neuer-umsetzer-installiert-svx-link/
slug: r4-rittnerhorn-ir3uhf-neuer-umsetzer-installiert-svx-link
title: R4 - Rittnerhorn, IR3UHF. Neuer Umsetzer installiert (SVX-Link)
wordpress_id: 11141
tags:
- Echolink
- Umsetzer Rittner Horn
---

## **WICHTIG: bitte Subaudioton (CTCSS) von 123,0 Hz am eigenen TX aktivieren!!!**


Heute nachmittag (20.11.2015) wurde am Rittnerhorn ein neuer (alter, revisionierter) Umsetzer für den [IR3UHF](https://drc.bz/relaisstandorte/rittner-horn-ir3w/) installiert. Vielen ist es vielleicht schon aufgefallen, da das Audiosignal am Repeater doch eine Verzögerung, so wie bereits am Link Südtirol oder am R2 Kronplatz gewohnt, erfährt.

[![ic-rp1520](https://drc.bz/wp-content/uploads/2015/11/ic-rp1520.jpg)](https://drc.bz/wp-content/uploads/2015/11/ic-rp1520.jpg)

In den letzten Wochen wurde ein ICOM Repeater, Modell RP-1520, spendiert von Ulrich DJ2LR und Maggie DL4TTB durch Intervention von Christian DL1MCG, so umgebaut, dass alles aus der Ferne eingestellt werden kann. Simon IN3FQQ hat dazu eine Intel D2500 ITX Computerplatine mit Soundkarte, Speichermedium Compact-Flash zu 8 GB und Spannungsversorgung eingebaut und die Softwareinstallation vorgenommen: Linux und [SVX-Link](http://svxlink.de/). Die Software verwaltet den gesamten Repeater über die USB-Soundkarte: Squelchauswertung, CTCSS Auswertung, Nachhang, CTCSS Aussendung, Echolinkverbindung und vieles mehr!

[caption id="attachment_11146" align="aligncenter" width="640"][![???????????????????????????????](https://drc.bz/wp-content/uploads/2015/11/IMG_20151117_213848.jpg)](https://drc.bz/wp-content/uploads/2015/11/IMG_20151117_213848.jpg) Links oben die Compact Flash zu 8 GB, in der Mitte die Computerplatine von Intel D2500 mit Dualcore 1,8 GHz und passivem Kühlblech, link unten die Platine mit den Schiebeschaltern für die QRG-Einstellung von RX und TX, rechts daneben der Spannungswandler von 12 V auf alle für den Computer nötigen Spannungen (+5V, -5V, +12V, -12V, 3,3V), ganz rechts unten die alte nicht mehr benötigte Steuerplatine. Unter dem roten Lankabel ist die USB-Soundkarte zu erkennen.[/caption]



Da Anfang dieser Woche die Installation der Hardware abgeschlossen war, wurde das Gerät von Thomas IW3AMQ getestet und justiert. Bei den Tests mit dem Radiotestset ist aufgefallen, dass der Empfänger leider um ganze 15 db weniger Empfindlichkeit aufzeigte als normal (statt den üblichen -120 dbm bis -123 dbm öffnete der Squelch bei -105 dbm. Eindeutig taub! Nach genauerem Begutachten der RX-Platine ist aufgefallen, dass bereits aktive Bauteile getauscht wurden:



	
  * der Empfangsverstärker, Q1 3SK121, wurde mit einem BF988 getauscht.

	
  * der monolithische Treiber des Lokaloszillators, IC5 uPC1651G, der das Signal zum Mischer führt, wurde mit einem nicht bekannten Typ getauscht.


[![Schaltplan RX RP-1520](https://drc.bz/wp-content/uploads/2015/11/Schaltplan-RX-RP-1520-1024x528.jpg)](https://drc.bz/wp-content/uploads/2015/11/Schaltplan-RX-RP-1520.jpg)

Leider haben die hier ausgetauschten Teile nicht dieselben technischen Eigenschaften jener der Originalteile. Also entschied ich mich, diese Teile mit moderneren auszuwechseln.

Als Q1 wurde ein [PGA-103](https://www.minicircuits.com/pdfs/PGA-103+.pdf) eingesetzt, nachdem auch das gesamte Anpassungsnetzwerk rundherum angepasst wurde. Der PGA-103 ist unter Kennern bestens bekannt, hat er doch exzellente Rausch- (0,5 db), Intermodulations- (37 dbm !) und Verstärkereigenschaften (25 db), um Welten besser als der BF988.

[caption id="attachment_11144" align="aligncenter" width="438"][![???????????????????????????????](https://drc.bz/wp-content/uploads/2015/11/IMG_20151117_204104.jpg)](https://drc.bz/wp-content/uploads/2015/11/IMG_20151117_204104.jpg) Die Unterseite der RX-Platine: links der Q1 (PGA-103) in rechteckiger Form als Vorverstärkerersatz, rechts oben Q5 (MSA-0866) in runder Form mit der Aufschrift A08 als Treiberersatz.[/caption]

Für den Q5, der als Originalteil ca. 19 db Gewinn aufweist (der als Ersatz eingesetzte Verstärker :-(  hatte nur 9 db), wurde ein monolytischer Verstärker MGA-0866 gewählt, der 31,5 db Gewinn aufweist und eine Ein- und Ausgangsimpedanz von 50 ohm aufweist.

Für beide Bauteile mußte natürlich der BIAS-Widerstand berechnet werden, um den Strom bzw. den Spannungswert auf die vorgegebenen zu begrenzen.

[caption id="attachment_11145" align="aligncenter" width="436"][![???????????????????????????????](https://drc.bz/wp-content/uploads/2015/11/IMG_20151117_212424.jpg)](https://drc.bz/wp-content/uploads/2015/11/IMG_20151117_212424.jpg) Die Oberseite der RX-Platine: für den MSA-0866 musste ein eigener Spannungsregler in SMD Form her ... (der gelbe Draht hängt dran)[/caption]

Die Ergebnisse lassen sich sehen: Öffnung Rauschsperre -126 dbm, Empfindlichkeit bei -20 db SINAD -122 dbm. Ich bin gespannt auf Empfangsrapporte.

Der Sender des RP-1520 hat auch eine höhere Leistung als der vorher eingesetzte Motorola MC Compact. Er gibt 25 W, wovon nach dem Duplexer noch 17 übrig bleiben. Durch den relativ langen Koaxialkabel verliert sich noch an Leistung, an der Antennenbuchse sind dann noch die genormten 10 W vorhanden, die voll in die Antenne fließen können.

In den nächsten Tagen wird auch die [Echolink](http://www.echolink.org)-Funktion von Simon programmiert werden. Das System ist identisch mit jenem des [R2 vom Kronplatz](https://drc.bz/relaisstandorte/kronplatz/) (IR3DV).

[![IMG_20151122_160123](https://drc.bz/wp-content/uploads/2015/11/IMG_20151122_160123-1024x614.jpg)](https://drc.bz/wp-content/uploads/2015/11/IMG_20151122_160123.jpg)

Besonders gefreut habe ich mich auf die wirklich in letzter Sekunde organisierte Begleitung: Benjamin IN3???, Kursbesucher beim Funkamateurkurs in Meran und bereits aktiv beim DRC (3 Zinnenlauf) tätig, hat mich kurzerhand heute nachmittag auf das Rittnerhorn begleitet!

Danke an Simon IN3FQQ für die Konfigurierung des PC-Systems! Computer Intel D2500, Spannungswandler, Soundkarte, Compact Flash mit CF Karte 8GB, HF-Bauteile und sonstige Kleinteile wurden von Thomas IW3AMQ spendiert.

Viel Spaß mit dem neuen R4 wünscht Euch allen,

Thomas, IW3AMQ

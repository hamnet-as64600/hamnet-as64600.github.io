---
author: IN3DOV
comments: false
date: 2013-07-29 07:06:23+00:00
layout: page
link: https://drc.bz/link-sudtirol-by-iw3amq-thomas/
slug: link-sudtirol-by-iw3amq-thomas
title: '"Link Südtirol" by IW3AMQ Thomas'
wordpress_id: 6735
tags:
- Link Suedtirol
---






**Geschichte:**

Meine Leidenschaft war immer schon die Zusammenschaltung von Umsetzern. Im Kopf schwirrte die Idee schon seit über 20 Jahren. Damals noch zeichnete ich Schaltpläne mit den ersten Digitalbausteinen der TTL und CMOS Reihe. Die ersten Erfahrungen konnte ich dann im [Cisar Südtiro](http://www.cisarbz.org/)l mit dem “[Link Nazionale](http://www.cisar.it/index.php?option=com_content&view=category&id=57&Itemid=251)” sammeln, ein Italienweites Umsetzersystem, dem ca. 30 Umsetzer im 70 cm Bereich angehören und die ständig miteinander verbunden sind. Nach mehreren provisorischen Lösungen, die vorletzte mit dem “Minilink Südtirol”, bei dem der Gantkofel mit dem Gitschberg dauerhaft über eine 23 cm Strecke über das Rittnerhorn verbunden waren, nun eine endgültige Lösung. Diese reifte im Jahr 2012 langsam heran und nun im Juli 2013 führte sie zum Neubeginn des  “Link Südtirol”. Die 70 cm Umsetzer am Chavalatsch, Jaufen, Gantkofel und Kronplatz sind nun dauerhaft zusammengeschlossen. Die Schlüssel für das System sind “[Allstarlink](http://www.allstarlink.org/)” und “[HamNet Südtirol](http://hamnet.cisarbz.org/doku.php)“.

**Technische Daten (alle QRG’s => Ablage + 1,6 MHz):**



	
  1. 


Plose:   431,3750 MHz, Subaudio 123,0 Hz - aktiv ab Sommer 2014


	
  2. 


Gantkofel:   431,4000 MHz, Subaudio 123,0 Hz – **AKTIV **


	
  3. 


Jaufen:   431,3625 MHz, Subaudio 123,0 Hz -  **AKTIV **


	
  4. 


Flatsch: 431,3875 MHz, Subaudio 123,0 Hz – aktiv ab Sommer 2014


	
  5. 


Kronplatz:   431,4000 MHz, Subaudio _**136,5 Hz **_– **AKTIV**


	
  6. 


Chavalatsch:   431,3875 MHz, Subaudio 123,0 Hz - **AKTIV**



**Tonsignale der Umsetzer des Link Südtirol Netzes:**



	
  * Doppelton (hoch – tief) am Ende des Nachhanges: eigener Umsetzers hat ein Signal empfangen

	
  * Tiefer Ton am Ende des Nachhanges: ein im Netz hängenden Umsetzer hat ein Signal empfangen

	
  * Kein Ton am Ende des Nachhanges: Linkverbindung zwischen den Umsetzern (HamNet) ist unterbrochen


Es ist möglich, einen Zwischenruf abzusetzen, der von allen gehört wird. Voraussetzung ist allerdings, daß man auf einen anderen Umsetzer hört, als auf dem, der gerade vom sprechenden Funkamateur verwendet wird. Beispiel: IN3ABC spricht gerade auf dem Umsetzer Gantkofel, IN3XYZ kann auf dem Umsetzer Chavalatsch oder Jaufen oder Kronplatz dazwischenrufen und wird von allen gehört (außer natürlich von IN3ABC, der ja gerade spricht, hi!). Ein Zwischenruf auf dem Umsetzer Gantkofel ist nicht möglich (dort sendet ja gerade IN3ABC).**Technische Hintergründe:**



	
  * _Allstarlink:_
[![Bild8](https://drc.bz/wp-content/uploads/2013/07/Bild8-300x60.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild8.jpg)
Eine Software, die unter Linux (CentOS) läuft und alle Funktionen eines Umsetzers bzw. Telefoniefunktionen durch eine USB-Soundkarte, verbunden mit dem RTX, steuert. Notwendige Signalleitungen sind: PTT, NF Rx, NF Tx und GND. Squelch Pegel Auswertung, Subaudiotöne im RX und TX, DTMF Fernsteuerung, De- und Enphasis werden von der Software erledigt. Jeder PC mit [Allstarlink](http://www.allstarlink.org/) kann in einem Internet bzw. Intranet oder in unserem Fall im HamNet miteinander komunizieren. Allstarlink ist ein Modul der professionellen Voip-Telefoniesoftware “Asterisk”.
.

	
  * _Soundkarte:_
Es musste also eine eigene Soundkarte her. Nach vielem Suchen im Internet war jedoch keine geeignete mit dem Chip CM108 oder CM119 in TFQP-Gehäuse zu finden. Und mit geeignet meine ich auch finanziell … Die [originale URI](http://www.dmkeng.com/URI_Order_Page.htm) kostet fast 70 €, bei ca. 15 Karten wäre das eine Stange Geld! Weiters war nämlich ein Zugriff auf verschiedene Pins des IC notwendig, um verschiedene I/O Pins zu verwenden. Bei den meisten Soundkarten zu 5 € war der Chip einfach als “Klecks” auf die Platine gegossen, die nicht verwendeten Pins sind NICHT herausgeführt. Also hab’ ich selbst eine Platine entwickelt, gestützt auf den Schaltplan des URI => siehe Foto. Alle Pins sind verwendbar und steuerbar für z.B. Leistung HI/LO, QRG Wechsel usw.
.
[![Bild1](https://drc.bz/wp-content/uploads/2013/07/Bild1-300x225.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild1.jpg)  [![Bild2](https://drc.bz/wp-content/uploads/2013/07/Bild2.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild2.jpg)
.

	
  * _Hochfrequenzlösungen:_
Eine besondere technische Herausforderung für mich war sicherlich die Realisierung von 2 Umsetzern im 70 cm Bereich (wie z.B. derzeit am Gantkofel und Chavalatsch), die mit nur einem einzigen Antennenfilter (Kostenpunkt ca. 1.500 €) und einer einzigen Antenne arbeiten konnten. Dies ist mir nun auch gelungen. Es gibt grundsätzlich 2 verschiedene Systeme, die jeweils ihre eigenen Vor- und Nachteile aufweisen.
.
1) Im TX Bereich werden die Signale von der jeweiligen Endstufe über einen Zirkulator in einen 3db Combiner geführt (siehe Ausführung von [DC4KU](http://www.mydarc.de/dc4ku/)). In meinem Falle habe ich einen 4 Port Leistungscombiner verwendet, an zwei Ports werden die beiden TX angeschlossen, an einem Port die Antenne bzw. Filter und am vierten Port ein Lastwiderstand 50 ohm der halben Gesamtleistung. In diesem Falle werden die Hälfte der Sendeleistung eines jeden TX im Lastwiderstand “verbraten” – leider! Vorteil: Es wird nur Strom gebraucht, wenn ein TX wirklich sendet.
.
[![Bild10](https://drc.bz/wp-content/uploads/2013/07/Bild10.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild10.jpg)[![Bild3](https://drc.bz/wp-content/uploads/2013/07/Bild3.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild3.jpg)

.
2) Die TX-Signale mit schwacher Leistung (z.B. 50 mW) werden mit Hybridkopplern bew. Combinern gemischt und danach zu einer gemeinsamen linearen Endstufe geführt. Der Nachteil in diesem Falle: die Endstufe MUSS im Linearbetrieb arbeiten, d.h. die Basis der Leistungstransistoren werden immer durchgesteuert, sie nehmen so dauerhaft den Gesamtstrom auf, der bei der Verstärkung gebraucht wird, unabhängig ob der HF-Träger vorhanden ist oder nicht. Vorteil: man verbratet nur die paar mW der vorverstärkten Signale, die leicht wieder angehoben werden können.
.
3) Im RX-Bereich verfährt man genauso, die Combiner fallen kleiner aus und der Verlust der 3 db bei einem 2-fach Teiler kann durch einen Vorverstärker ausgeglichen werden. Der Vorverstärker bekommt dann meist auch noch einen Bandpassfilter vorgeschalten, um wenigstens ein wenig Vorselektion zu garantieren. Der Vorverstärker besteht aus einem MGA 62563, ein Baustein mit fantastischen Werten von 0,7 db Rauschzahl und einer Großsignalfestigkeit IP3 von + 32 dbm. Er wurde bereits am Rittnerhorn (R4 und Link Nazionale), am Gantkofel (Link Nazionale und Link Südtirol) erfolgreich eingesetzt.
.
[![Bild4](https://drc.bz/wp-content/uploads/2013/07/Bild4.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild4.jpg)  [![Bild5](https://drc.bz/wp-content/uploads/2013/07/Bild5.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild5.jpg)  [![Bild6](https://drc.bz/wp-content/uploads/2013/07/Bild6.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild6.jpg) [![Bild7](https://drc.bz/wp-content/uploads/2013/07/Bild7.jpg)](https://drc.bz/wp-content/uploads/2013/07/Bild7.jpg)




Das Bandpassfilter noch ohne Vorverstärker (zwecks Anpassungsmessung), die Messung des Durchlaufes und die Anpassung des Filters, zuallerletzt der fertige Aufbau mit Vorverstärker.





# ****










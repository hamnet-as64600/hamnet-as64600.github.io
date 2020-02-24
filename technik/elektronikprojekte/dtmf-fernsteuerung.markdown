---
author: IW3AMQ
comments: false
date: 2014-10-13 13:00:25+00:00
layout: page
link: https://drc.bz/technik/analog-digitaltechnik/dtmf-fernsteuerung-20-outputs-mit-atmel-90s8525/
slug: dtmf-fernsteuerung-20-outputs-mit-atmel-90s8525
title: DTMF Fernsteuerung 20 Kanäle
wordpress_id: 9380
---

Diese Fernsteuerung wird an ein Funkgerät oder an einen Umsetzer angeschlossen. Sie hat 20 Ausgänge, die über DTMF eingeschalten und ausgeschalten werden können. Dazu bedarf es eines Passwortes, das mit einem Quittungston bestätigt wird. Es können auch alle Status der Ausgänge abgefragt werden, eine hohe Quittungstonfolge bedeutet “Ein”, eine tiefe Quittungstonfolge bedeutet “Aus”. Damit der Ton eindeutig identifizierbar ist, wird der “Ein” Ton so generiert: tief, hoch, hoch; der “Aus” ton: hoch, tief, tief. Es ist auch eine Änderung des Passwortes über DTMF möglich. Weiters können mit einer einzigen DTMF Folge ganze Gruppen von Ausgängen ein- oder ausgeschalten werden. Nach jeder DTMF Toneingabe erfolgt ein Quittungston. Ein Timeout nach ca. 2 min. verhindert ein Fremdeingreifen.






  * [Schaltplan](https://drc.bz/wp-content/uploads/2014/10/dtmf-fernsteuerung-schaltplan.jpg) der DTMF Fernsteuerplatine


  * [Platine](https://drc.bz/wp-content/uploads/2014/10/dtmf-fernsteuerung-platine.jpg) mit traditionellen Bauteilen (Achtung: Lötbrücke nicht vergessen!)


  * [Schaltplan](https://drc.bz/wp-content/uploads/2014/10/dtmf-fernsteuerung.sch_.zip) im Eagle SCH-Format


  * [Platine](https://drc.bz/wp-content/uploads/2014/10/dtmf-fernsteuerung.brd_.zip) im Eagle BRD-Format, einseitig


  * [Bascom Programm](https://drc.bz/wp-content/uploads/2014/10/fernsteuerung-dtmf-v11.bas_.zip) für AT90S8525 (Der Basic Compiler BASCOM kann von [www.mcselec.com](http://www.mcselec.com) auch als Demo Version heruntergeladen werden)


  * [Anleitung](https://drc.bz/wp-content/uploads/2014/10/sample-electronics-cable-programmer.pdf) für Programmieradapter für AT90S8525




#### Kurze Bedienungsanleitung für die DTMF Fernsteuerung in Verbindung mit Funkgerät oder Umsetzer:




DTMF Fernsteuerung mit 8 + 8 + 4 Ausgängen zum Anschluss an ein Funkgerät; mit Kontrolle, ob RTX ein- oder ausgeschalten ist.




Password = 123456*1 , wobei z.B. für *1 die Fernsteuerung auf dem Gantkofel, für *2 für Plose, *3 für einen anderen beliebigen Standort gedacht ist. Nach Bestätigung der korrekten Passworteingabe (Doppelton tief dann hoch) kann der Status abgefragt oder geändert werden.




Abfrage: Pinnummer + Abfragesymbol (*) => A1* für Pin A1, A2* für Pin A2 bis A8*, von B1* bis B8*, von C1* bis C4*




Ändern: Pinnummer + Änderungssymbol (#) => A1# für Pin A1, usw. wie oben bei jeder Abfrage oder Änderung wird der effektive Status sofort zurückgesendet: Ton hoch, Ton tief, Ton tief => Status low (0); Ton tief, Ton hoch, Ton hoch => Status high (1), mit 111 werden alle Ausgänge auf high (1) geschalten, mit *** wird die Fernsteuerung abgeschlossen.




Die Fernsteuerung hat auch ein Timeout von ca. 60 Sekunden (einstellbar unter “Definition der Konstanten”, nach denen sie selbst abschließt. Falls ein falscher DTMF-Ton getippt wurde, einfach 5 Sekunden warten, es ertönt ein Fehlerstatus, danach neu tippen.




**Zusammenfassung:**




Password: xxxxxxxx (8 Zeichen, wobei x = 0 bis 9, *, #, A bis D) – BEI NEUINSTALLATION IST DAS PASSWORD: 12345678 und alle Ausgänge auf low!




Abfrage: A1* … A8*; B1* … B8*; C1* … C4* Ändern: A1# … A8#; B1# … B8#; C1# … C4# Alle Ausgänge high: 111 Password ändern: DD# Verlassen: ***




Folgende Möglichkeiten wurden, auch aus Platzmangel, noch nicht programmiert: Alle Ausgänge auf low: 000 (Problem: macht allein Reset !?) Alle Ausgänge Port A (8 Pins) auf high: AA1 Alle Ausgänge Port A (8 Pins) auf low: AA0 Alle Ausgänge Port B (8 Pins) auf high: BB1 Alle Ausgänge Port B (8 Pins) auf low: BB0 Alle Ausgänge Port C (4 Pins) auf high: CC1 Alle Ausgänge Port C (4 Pins) auf low: CC0




![](https://drc.bz/wp-content/uploads/2014/10/dtmf-fernsteuerung-schaltplan.jpg)


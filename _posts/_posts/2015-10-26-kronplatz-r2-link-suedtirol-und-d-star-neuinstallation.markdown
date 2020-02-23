---
author: IN3DOV
comments: false
date: 2015-10-26 08:41:59+00:00
layout: post
link: https://drc.bz/kronplatz-r2-link-suedtirol-und-d-star-neuinstallation/
slug: kronplatz-r2-link-suedtirol-und-d-star-neuinstallation
title: Kronplatz R2, Link Südtirol und D-Star - Neuinstallation
wordpress_id: 10990
categories:
- D-STAR
- Link Suedtirol
- Umsetzer Kronplatz
---

**Kurzinfo:**






	
  * **R2 **(145.650 kHz, ECHOLINK Nodenummer 55885, **Achtung: 123 Hz Subaudioton** ist notwendig!)

	
  * **Link Südtirol** (431.400 kHz, +1,6 MHz Shift, Subaudioton 136,5 Hz)

	
  * **D-Star** (IR3DV 431.525 kHz + 1,6 MHz Shift)


**Bericht:**

Seit dem gestrigen Samstag, 24. Oktober, sind auf dem Kronplatz die neuen Gerätschaften für Link Südtirol und D-Star mit Motorola GM900 installiert und in Betrieb.

[caption id="attachment_11040" align="aligncenter" width="640"][![FS-LS-DStar](https://drc.bz/wp-content/uploads/2015/10/FS-LS-DStar-1024x614.jpg)](https://drc.bz/wp-content/uploads/2015/10/FS-LS-DStar.jpg) Motorola GM900 für D-Star und Link Südtirol, DVRPTR-V.2 Interface und ITX-Intel PC[/caption]



Das Link Südtirol wurde wieder aktiviert, der R2 Umsetzer erneut kalibriert und der YAESU-Ersatzumsetzer abgebaut und ins Tal gebracht.



	
  * **R2:** Wie vielleicht einige OMs bemerkt haben, war in den letzten Wochen der R2 Ersatzumsetzer in Betrieb – der wohlgemerkt über keine EchoLink Anbindung verfügt. Ein defektes Reed-Relais zur Koax-Umschaltung verhinderte den sauberen Empfang des Motorola-Umsetzers – dieser Zustand hat Kurt IN3DOV dann schlussendlich gezwungen, auf das Ersatzgerät umzuschalten.
.
Nun wurde im Zuge des Einsatzes das Ersatzgerät abgebaut und dadurch die Koax-Umschaltung überflüssig gemacht. Der Motorola-Umsetzer mit EchoLink hängt nun direkt an der Antenne. Außerdem wurde er erneut kalibriert, um die Sensibilität zu steigern.
.
Bei den Messungen mit dem Radio Test Set kamen wir zum Schluss, dass das Relais mit einem Subaudio-Ton viel sensibler und zuverlässiger anliegende Signale erkennen kann. Versehentliches Öffnen des Relais durch Störungen wird auf diese Art auch weitgehend vermieden.
.
Aufgrund dessen wird **zum Öffnen des R2 nun ein 123.0Hz CTCSS Ton** benötigt. Das Relais sendet den 123.0Hz Ton ebenfalls aus, und zwar dann wenn **Sprache vom lokalen Empfänger oder über EchoLink empfangen wird**. Bei Sprachansagen und Baken-Aussendungen wird kein Ton mitgesendet. Oms, die sich durch die EchoLink Informationen gestört fühlen, können einfach den Subaudio Squelch Dekoder am Funkgerät aktivieren und hören dann nur noch QSOs.
.
[![LS-ASL](https://drc.bz/wp-content/uploads/2015/10/LS-ASL-1024x614.jpg)](https://drc.bz/wp-content/uploads/2015/10/LS-ASL.jpg).

	
  * **Link Südtirol:** wurde wie geplant wieder auf **431.400MHz +1,6 mit 136.5Hz Subaudio** Ton aktiviert. Die neue Steuerplatine verwendet nun eine erst wenige Wochen alte Version der AllstarLink Software, und steuert gleichzeitig auch den D-STAR Digitalumsetzer.
.

	
  * **D-Star:** Der Digitalumsetzer läuft auf **431.525 MHz +1,6** und reagiert auf das Rufzeichen IR3DV  B
**Vorsicht: D-STAR Relais-Rufzeichen sind immer 8 Zeichen lang! Zwischen IR3DV und B müssen zwei Leerzeichen stehen, sonst reagiert das Relais nicht!
.
**Das Relais ist permanent mit dem Südtirol-Reflektor DCS008F verbunden, kann aber vom Benutzer auch auf andere Reflektoren umgeschaltet werden. Nach 5 Minuten Inaktivität schaltet sich das Relais automatisch wieder zum Südtirol Reflektor zurück.
.
Um über den D-STAR Umsetzer sowohl lokal als auch über Reflektor arbeiten zu können, müssen die Rufzeichen wie folgt programmiert werden:
.
**RPT1: IR3DV  B (Achtung: zwei Leerzeichen!!)
****RPT2: IR3DV  G (Auch hier, zwei Leerzeichen)
.
**Über das YOURCALL Feld können neben CQCQCQ oder Zielrufzeichen auch Befehle abgesetzt werden. Bei neueren Funkgeräten sind diese auch schon aus der Konfiguration bzw. aus dem Menü heraus wählbar.
.
_______I: Informationen zum Verlinkungs-Status werden ausgesendet
_______U: Verbindung zum Reflektor wird getrennt
_______E: Echo-Test Modus, Relais nimmt Durchgang auf und sendet danach das Selbe wieder zurück
.
Über das YOURCALL Feld kann auch zwischen den verschiedenen Reflektoren gewechselt werden. Dazu wird einfach der Name des Reflektors, gefolgt von dem Buchstaben **L **für** Link **eingetragen, z.B. DCS009TL für den OE7-Tirol Reflektor.


**Filtereinheiten:** Da nun zwei 70 cm Repeater am Kronplatz sind, mußten auch 2 Serien von Filtern her! Vor einigen Jahren kaufte der Club bereits 6 Notch-Filter und 2 Bandbass-Filter für 70 cm von Label. Um Kosten zu sparen, aber nicht an den technischen Eigenschaften der Filter, wurde folgende Lösung in Angriff genommen:



	
  1. Für D-Star wurden nur mehr 4 Notchfilter (2 x RX, 2 x TX) in Kombination mit einem Zirkulator eingesetzt, die gesamte Durchgangsdämpfung beträgt ca. 2,5 db, der Notch ca. - 65 db und die Trennung zwischen RX und TX über 95 db.

	
  2. Für Link Südtirol wurden die restlichen beiden Notchfilter für den TX-Kreis verwendet, die beiden Bandpässe wurden zu Notchfiltern für RX umgebaut. In Kombination mit einem weiteren Zirkulator wurden fast die selben Werte erreicht, außer den beiden umgebauten Notchfiltern, die im RX-Kreis eine Dämpfung des TX-Signales von über 70 db bringen.


[caption id="attachment_11042" align="aligncenter" width="640"][![Die beiden von Bandpass auf Notch umgebauten Filter](https://drc.bz/wp-content/uploads/2015/10/Filter-1024x614.jpg)](https://drc.bz/wp-content/uploads/2015/10/Filter.jpg) Die beiden von Bandpass auf Notch umgebauten Filter[/caption]

**Fernsteuerung:** Zu allerletzt wurde auch das 70 cm Funkgerät für die DTMF-Fernsteuerung mit einem 2 m Gerät getauscht, das von Georg, IW3ABA zur Verfügung gestellt wurde. Weiters wurde die Software der [AVR Net I/O Fernsteuerung](https://drc.bz/interessante-links/bastelecke-umbau-und-eigenbau/analog-digitaltechnik/dtmf-und-lanhamnet-fernsteuerung/) durch die letzte Version, erstellt von Simon, IW3BWH, ersetzt. Sie erlaubt auch eine Impulsschaltung, besonders interessant zum Neustarten des Hamnet, da bei einfachen Ausschalten ja kein Zugang vom Hamnet mehr möglich ist.

**Antennen:** Vor einigen Wochen schon wurde der Grundstein für die jetzige Installation gelegt. Gabi IN3EMJ, Kurt IN3DOV und Herbert IW3BRH hatten einen zweiten 70 cm Dipol installiert, der nun das D-Star Signal abstrahlt. Da am Kronplatz leider nur 2 Koaxialkabel zur Verfügung stehen, wurde auch ein 2m/70cm Duplexer installiert, der die Signale der 2 m Kathrein Antenne (R2) und des neu installierten 70 cm Dipols (D-Star) mischen. Im Geräteraum werden diese beiden Bänder wieder durch einen Duplexer (siehe Bild) getrennt und zu den jeweiligen RX/TX Weichen geführt.

**Spenden und Arbeiten:**

Die vier Motorola Funkgeräte GM900 wurden von Herbert, IW3BRH spendiert.

Die gesamte Software wurde von Simon, IW3FQQ installiert. Den Zusammenbau im Rack hat auch Simon IN3FQQ (mit einer Flex !!! :-)) erledigt!

Die Filter wurden von Thomas IW3AMQ abgeändert und neu abgeglichen. Die beiden Zirkulatoren, der PC und die [Eigenbau-Soundkarte](https://drc.bz/link-sudtirol-by-iw3amq-thomas/) wurde von Thomas spendiert.

Georg IW3ABA hat das 70 cm Mobilfunkgerät von Yaesu für die Fernsteuerung spendiert.

Dank an allen noch, die zur Realisierung dieses Vorhabens beigetragen haben.

73! Thomas, IW3AMQ und Simon, IN3FQQ


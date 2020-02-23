---
author: IN3DOV
comments: false
date: 2018-01-10 07:50:03+00:00
layout: post
link: https://drc.bz/ein-tipp-fuer-selberbauer-kurzwellenfunkgeraete-%c2%b5bitx/
slug: ein-tipp-fuer-selberbauer-kurzwellenfunkgeraete-%c2%b5bitx
title: 'Ein Tipp für Selberbauer: Kurzwellenfunkgeräte µBITX'
wordpress_id: 15201
categories:
- Bastelecke
---

[![](https://drc.bz/wp-content/uploads/2018/01/bitx.jpg)](https://drc.bz/wp-content/uploads/2018/01/bitx.jpg)Liebe Selberbauer,

schon einmal den Wunsch verspürt, einen QRP Kurzwellen TRX selber zu bauen?.. Es gibt sicherlich gute Gründe, solch ein Projekt zu scheuen, sei es der Aufwand eine Schaltung zu entwickeln, die Platinen zu ätzen, fehlende Zeit und Messmöglichkeiten etc...
In Indien baut OM Ashhar Farhan VU2ESE die PCB fix und fertig zusammen. Nach dem BITX40, welchen ich schon erfolgreich aufgebaut habe, bietet er nun auch die TRX Platine für den µBITX fertig abgeglichen für 109 $ inkl. Versand an.

Was noch fehlt ist das Gehäuse, Lautsprecher und ein paar leicht zu beschaffende Kleinteile.

**Hier die technische Beschreibung:**

Der μBITX ist ein HF-SSB / CW-Transceiver-Kit mit allen Funktionen, die Sie für Bedienkomfort, Benutzerfreundlichkeit und Vielseitigkeit benötigen. Er arbeitet von 3 MHz bis 30 MHz, mit bis zu 10 Watt bei SSB und CW mit einem sehr empfindlichen Empfänger. Er bietet digitales Tuning, Dual VFOs, RIT, CW Keyer und mehr.

Es ist eine Freude damit zu arbeiten. Drücken Sie den Abstimmknopf, um auf alle Funktionen zuzugreifen. Dual VFO, RIT, CW-Geschwindigkeit, Seitenbandauswahl. usw. sind alle über ein einziges Menü erreichbar. Der Transceiver wählt automatisch das richtige Seitenband für Sie aus (Sie können es auch überschreiben).
Die Komplexität ist auf ein Minimum beschränkt, so dass Sie jederzeit Reparaturen und Änderungen vornehmen können.
Der μBITX hat eine durchdachte Bedienoberfläche. Der Abstimmknopf bietet viele Menüoptionen. Von RIT über Dual-VFO bis zum Keyer und viele andere Funktionen sind zugänglich, indem Sie einfach darauf drücken. Es gibt überall intelligente Voreinstellungen (diese können leicht überschrieben werden). 

Beispiel: Unter 10 MHz wählt es automatisch LSB und umgekehrt. Um CW zu bedienen, drücken Sie einfach die Morse-Taste.
Der μBITX verwendet eine Aufwärtsmischung zur ersten ZF von 45 MHz. Dies eliminiert die Notwendigkeit einer großen Anzahl von Bandpassfiltern, wodurch das Design einfach bleibt. Das Roofingfilter bei 45 MHz ist 15 KHz breit. Das Signal wird dann auf 12 MHz heruntergemischt, wobei ein SSB-Filter mit geringer Welligkeit mit 8 Quarzen verwendet wird, um ein sauberes Audiosignal zu liefern.
Der Sender verfügt über Push-Pull-PA mit zwei IRF510 für ein saubere Signal. Die kostengünstigen IRF510 sind einfach und kostengünstig zu ersetzen, sollten sie jemals benötigt werden.

**_Empfänger:_**
Empfindlichkeit:     Ein 0,2-V-Signal ist deutlich hörbar
Selektivität:    2,4 KHz, SSB-Filter mit geringer Welligkeit mit 8 Quarzen
RIT (Empfänger Incremental Tuning)
Kontinuierliche Abdeckung von 500 kHz bis 30 MHz
Seitenbandauswahl
Tune mit größeren Schrittgeschwindigkeiten, wenn schnell abgestimmt werden soll.

_**Sender:**_
Mehr als 10 Watt bis 10 MHz, 7 Watt bis 21 MHz, 2 Watt bei 28 MHz
CW-Übertragung mit dem eingebauten Keyer
Verwendet IRF510s als PA- und 2N3904 -Treiber im Push-Pull-Modus für eine Übertragung mit geringer Verzerrung.

**Raduino-Funktionen:**

Das Raduino ist ein kleines Board mit einem Si5351 Taktgenerator, einem Arduino Nano und einem 16 × 2 LCD Display. Es wird an die Haupt-Funkplatine angeschlossen. Die Software, die den Tranceiver steuert, ist in Arduino C Sprache geschrieben.
Der Funktionsumfang des μBITX wird von der Open-Source-Software von Raduino gesteuert. Open Source ermöglicht es Ihnen, die Software weiter zu verbessern, wenn Sie dies wünschen. Die Menüs sind durch Drücken der Taste am Tuning-Encoder zugänglich. Sie können weitere Funktionen hinzufügen, indem Sie den unter [https://github.com/afarhan/ubitx](https://github.com/afarhan/ubitx) verfügbaren Open Source-Code ändern.
Dual VFOs
RIT
Manuelle Umschaltung der LSB / USB-Auswahl
CW Keyer Geschwindigkeit und Tonauswahl

Der Zusammenbau ist auf der Webseite [http://www.hfsignals.com/index.php/ubitx-wire-up/](http://www.hfsignals.com/index.php/ubitx-wire-up/) ausführlich beschrieben.

73 de Christian, DL1MCG

---
author: IW3AMQ
comments: false
date: 2015-12-14 22:12:00+00:00
layout: post
link: https://drc.bz/zwei-sdr-empfaenger-fuer-kurzwellevhfuhf-und-vhf-uhf-shf-am-jaufen-installiert/
slug: zwei-sdr-empfaenger-fuer-kurzwellevhfuhf-und-vhf-uhf-shf-am-jaufen-installiert
title: Zwei SDR-Empfänger für Kurzwelle/VHF/UHF und VHF-UHF-SHF am Jaufen installiert
wordpress_id: 11295
categories:
- SDR
- Umsetzer Jaufen
---

[![Jaufen](https://drc.bz/wp-content/uploads/2015/12/Jaufen-576x1024.jpg)](https://drc.bz/wp-content/uploads/2015/12/Jaufen.jpg)14.12.2015

Schon vor ca. einem Jahr wurden auf dem Jaufen, DRC Umsetzerstandort für das Link Südtirol und für APRS, probeweise zwei SDR-Sticks mit PC installiert.

Einer ist der Funcube, der andere ein RTL-USB Empfänger. Ihr könnt nun nach der Anmeldung versuchen, diese via Internet zu bedienen.

Die Anmeldung erfolgt mit e-mail an: **iw3amq@dnet.it**  Bitte unbedingt Namen und Rufzeichen angeben. Die Zugangsdaten werden innerhalb 2 Tagen per e-mail zugesandt. Vorerst ist der Zugang nur DRC und CISAR Mitgliedern vorbehalten.

Für den Anfang wird ein Zeitlimit von 30 Minuten für jeden gesetzt. Je nach Anzahl der Anmelder bzw. Dauer der Nutzung kann diese Zeit vom Sysop erhöht oder gekürzt werden. Es können maximal 2 Benutzer gleichzeitig zugreifen, einer auf den Funcube, der andere auf den DVBT-Usbstick. Man erkennt das daran, daß bei der Auswahl des SDR-Empfängers der gerade besetzte mit einem X versehen ist.

![FuncubeDonglePro](https://drc.bz/wp-content/uploads/2015/12/FuncubeDonglePro.jpg)

[![RTL-Sdr](https://drc.bz/wp-content/uploads/2015/12/RTL-Sdr.jpg)](https://drc.bz/wp-content/uploads/2015/12/RTL-Sdr.jpg)

Am Funcube hängt ein vertikal gespannter Kupferdraht längs dem 15 m hohen Masten für die HF (Kurzwelle), am RTL SDR hängt die mitgelieferte kurze Magnetantenne, die nur für die hohen Bänder VHF, UHF und SHF geeignet ist.

Nachfolgend die Bedienungsanleitung:



	
  1. SDR-Radio v.2.3 Beta (build 2274) [hier](https://www.dropbox.com/s/3jkfox2gk4pzlfg/SDR-RADIO-Pro_v2.3b2274.exe?dl=0) herunterladen

	
  2. Das Programm zur Installation starten

	
  3. Es werden 2 Verknüpfungen auf dem Desktop geschaffen, die Verknüpfung "SDRConsole (V2)" anklicken

	
  4. Beim Start öffnet sich das Fenster "Select Radio", mit Click auf "Cancel" das Fenster schließen

	
  5. Ganz oben links in der Menüleiste "Remote Connection" anklicken

	
  6. Unter "Adress:" folgende IP-Adresse eingeben: node.wifi44.net

	
  7. Unter "Port:" folgenden Port eingeben: 6999

	
  8. Unter "Username:" das eigene Rufzeichen in Großbuchstaben eingeben

	
  9. Unter "Password:" das zugewiesene Password eingeben

	
  10. "Connect" anklicken

	
  11. Bei erfolgter Verbindung erscheint erneut das Fenster "Select Radio", nun den gewünschten USB-SDR Radio auswählen. Die verfügbaren Geräte sind mit einem grünen Häckchen versehen, falls der eine oder andere von jemand anderen benutzt wird, erscheint ein rotes X und ist nicht auswählbar, bis der Benutzer dieses Gerät disconnected

	
  12. Bei der Auswahl von "FUNcube 2.0" unter "Soundcard:" die richtige Soundkarte auswählen: "Line (FUNcube Dongle V2.0)

	
  13. Unter "Sample rate:" folgende Werte einstellen: falls "FUNcube 2.0" ausgewählt => 384 kHz, falls "DVB-T/DAB/FM dongle" ausgewählt => 2 MHz

	
  14. Die Felder "Invert spectrum" und "Converter" leer lassen

	
  15. Auf "Start" klicken

	
  16. Am wichtigsten ist die Einstellung der Antennenverstärkung (Menüleiste links von "Radio Configuration") und "Radio Configuration (dort korrigiert man die Frequenzabweichung vom Ist-Wert).

	
  17. Beim Verlassen nicht vergessen, ""Disconnect" in der Menüleiste oben links zu drücken!


Viel Spaß!

73! Thomas, IW3AMQ

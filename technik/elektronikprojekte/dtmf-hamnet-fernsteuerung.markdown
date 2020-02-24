---
author: IW3AMQ
comments: false
date: 2014-10-14 08:48:32+00:00
layout: page-fullwidth
link: https://drc.bz/technik/analog-digitaltechnik/dtmf-und-lanhamnet-fernsteuerung/
slug: dtmf-und-lanhamnet-fernsteuerung
title: DTMF - LAN Fernsteuerung
wordpress_id: 9507
---

## Projekt ‘AVR-Net-IO’ 2014 - Fernsteuerung via DTMF und Ethernet oder Hamnet


_1. AVR-Net-IO von Pollin:_


Ethernet-Platine mit ATMega32 und Netzwerkcontroller ENC28J60. Die Platine verfügt über 8 digitale Ausgänge, 4 digitale und 4 ADC-Eingänge, welche alle über einen Netzwerkanschluss (TCP/IP) abgerufen bzw. geschaltet werden können.




Die Platine verfügt zudem über alle benötigten Komponenten, wie Netzwerkbuchse, Netzwerkcontroller und ISP-Schnittstelle um auch eigene Projekte kostengünstig, schnell und einfach entwickeln und verwirklichen zu können.




Auf der Internetseite von Pollin [http://www.pollin.de](http://www.pollin.de/) findet man das Fertigmodul bzw. den Bausatz. In der Suchleiste einfach nach "avr net io" suchen.




[![AVR_NetIO](https://drc.bz/wp-content/uploads/2014/10/AVR_NetIO.jpg)](https://drc.bz/wp-content/uploads/2014/10/AVR_NetIO.jpg)


_2. Microcontroller ATMEL ATmega644 (mit doppeltem Speicher, um noch zusätzliche Erweiterungen zu ermöglichen)_


 In der Suchleiste von [http://www.pollin.de](http://www.pollin.de/shop/dt/MzAwOTk4OTk-/Bauelemente_Bauteile/Aktive_Bauelemente/Microcontroller/Microcontroller_ATMEL_ATmega644_20PU.html) nach "atmega 644" suchen.




.


_3. Doku/Schaltplan & Software GPL, die als Vorlage zur DTMF-Erweiterung diente (ohne Passwordschutz!):_


[http://www.schorsch.at/de/technik/funk/30-erweiterungsmodul-fvr-net-io.html](http://www.schorsch.at/de/technik/funk/30-erweiterungsmodul-fvr-net-io.html) und [http://www.schorsch.at/de/technik/funk/39-avr-net-io.html](http://www.schorsch.at/de/technik/funk/39-avr-net-io.html)


.

_4. Passwordschutz für LAN / HamNet und DTMF Zugang_


Simon IW3BWH hat nun den Passwortschutz sowohl auf das Netzwerk als auch auf die DTMF-Steuerung integriert. Weiters hat die Fernsteuerung nun 12 digitale Ausgänge und 4 ADC Eingänge, 2 für Spannungen und 2 für Temperaturen. Die Software kann natürlich nach Belieben angepasst werden:




**[netio_webserver 2014](https://drc.bz/wp-content/uploads/2014/10/netio_webserver.zip)**




.


_5) Programmieren des AVR Net IO von Pollin:_


**Programmieradapter:** Zuallererst sollte man sich einen Progammieradapter besorgen. Ich habe mir den "MySmartUSB light" von [http://shop.myavr.de](http://shop.myavr.de) zugelegt. Er ist kostengünstig. Auf dieser Seite wird auch der Treiber zur Verfügung gestellt und genau beschrieben, wie die Installation unter "Atmel Studio 6", der Programmiersoftware, zu erfolgen hat. Da der Net AVR IO einen 10 poligen Wannenstecker zur Programmierung verwendet, der Programmieradapter jedoch mit einem 6 poligen geliefert wird, kann man entweder selbst einen 10 poligen Wannenstecker an das 6 polige Flatkabel anbringen (Schaltplan bzw. Pinbelegung beachten!) oder den Adapter "ISP Connect Kit 10 / 6polig" gleich dazubestellen.




**Programmiersoftware:** Um den AVR Net IO zu programmieren, bedarf es auch der Software "Atmel Studio 6" oder einer anderne gleichwertigne Software. Atmel Studio 6 kann direkt von der Homepage von Atmel [http://www.atmel.com](http://www.atmel.com) kostenlos heruntergeladen werden. Um das Programm "netio_webserver2014" zu bearbeiten, muss es vorher in das Atmel Studio 6 geladen werden. Dazu unter dem Menüpunkt "File" => "Open Project" die entpackte Projekt-Datei (netio_webserver.cproj) im vorher gespeicherten Ordner (netio_webserver) anklicken. Im Fenster rechts dann die folgenden Dateien für die nötige Personalisierung vornehmen:




- config.h (Änderungen IP-, Netmask- und Gatewayadressierung, MAC-Adresse, DTMF- und Webseitenpassword)
- dtmfin.c (Änderungen bei Relèansteuerung mit negativer Logik)
- httpd.c (Änderungen bei Relèansteuerung mit negativer Logik, Änderungen Spannungs- und Temperaturanzeige)
- webpage.h (Änderungen Webseite)




Die Änderungen abspeichern. Vor dem Programmieren muss die Software noch kompiliert werden. Dazu unter "Build" => "Build netio_wbserver" die Datei kompilieren. Unter "Tools" den Programmieradapter zuweisen (vorher Treiber für den Programmieradapter installieren!) und dann zur Programmierung übergehen. Genaue Details dazu der Beschreibung vom Programmieradapter entnehmen.




.


_6) Beschreibung zur neuen Software 2014 “netio_webserver.zip”:_


Im Konfigurationsfile “config.h” stehen die Daten, um sich über LAN mit dem Modul zu verbinden. Die Webseite kann in “webpage.h” angepasst werden. Bevor alles zusammen kompiliert wird, muss unbedingt darauf geachtet werden, dass die korrekte MAC-Adresse mit angegeben wurde!




Eine Terminalverbindung kann klassischerweise mittels Standardeinstellungen vorgenommen werden: 9600 baud, 8 bit, 1 stopbit, no parity. Darüber kann dann auch das DTMF-Password gesetzt/geändert werden. Mittels ? oder help erhält man alle nötigen Infos.




Unsere DTMF-Steuerung selbst hat 12 digitale Ausgänge und 4 analoge Eingänge mit einer Auflösung von 10 bit (0 – 5 V).




Auf der Webseite sind momentan die digitalen Werte integriert (von 0 a 1023). Sobald die Fernsteuerung auf eine DTMF-Anfrage antwortet, wird nach dem Träger 500 ms zugewartet, bis die Antwort gegeben wird: tief/hoch für 1 und hoch/tief für 0. Bei Eingabe eines falschen DTMF-Passwortes wird keine Antwort gegeben!




Die DTMF-Sequenz arbeitet nach folgendem Schema: * ab01 # 09 0




* = erstes Zeichen obligatorisch ab01 = DTMF-Passwort, das im Quellcode oder via RS232 gesetzt wurde # = weiteres, obligatorisches Zeichen 01 bis 12 = Kanalnummer, die abgefragt/geändert wird (im Beispiel Kanal 09) 0 = Kanal deaktivieren; 1 = Kanal aktivieren; A = Kanalstatus abfragen (im Beispiel wird Kanal 09 deaktiviert)




Die Belegung der DB25-Schnittstelle ist dabei wie folgt:




1 NC 2 Out 01 3 Out 02 4 Out 03 5 Out 04 6 Out 05 7 Out 06 8 Out 07 9 Out 08 10 Out 09 11 Out 10 12 Out 11 13 Out 12 14 NC 15 + 5 V output 16 – 17 NC 18 – 25 GND




Die analogen Eingänge befinden sich an der Schraubklemme, die entsprechend beschriftet ist (Achtung: max. +5V !!): ADC1 In 1 ADC2 In 2 ADC3 In 3 ADC4 In 4. Für ADC1 und 2 sind lineare Temperatursonden MCP9700 vorgesehen, für ADC3 und 4 zwei Gleichspannungseingänge bis 50 V über einen Widerstandsteiler (10 kohm in Serie, 1 kohm gegen GND).




Die Verbindungen an einen externen den DTMF-IC befinden sich an einem 2 x 5 poligen Anschluss (“EXT”): 1 (PD2) not connected 2 (PD3) StD pin (NetIO Input) 3 (PD4) Q1 pin (NetIO Input) 4 (PD5) Q2 pin (NetIO Input) 5 (PD6) Q3 pin (NetIO Input) 6 (PD7) Q4 pin (NetIO Input) 7 (PB0) PTT verso la resistenza che và alla base del transistor NPN (NetIO Output) 8 (PB3) Beep (NetIO Output) 9 GND 10 +5V (NetIO +5V)




**AvrNetIo-DTMF Interface by Thomas IW3AMQ und Simon IW3BHW ([Datei im pdf-Format](https://drc.bz/wp-content/uploads/2014/10/AvrNetIo-DTMF-Interface.pdf))**




[![avrnetio_dtmf](https://drc.bz/wp-content/uploads/2014/10/avrnetio_dtmf-300x208.jpg)](https://drc.bz/wp-content/uploads/2014/10/avrnetio_dtmf.jpg)




Auf Aliexpress gibt es kostengünstig Relaisgruppen zu 4 oder 8 Relais (suche nach "relay module") und bereits auf einer Platine bestückter DTMF-Dekoder (suche nach "MT8870 decoder"). Einzig der NPN-Transistor mit dem Basiswiderstand wird noch für die PTT-Schaltung verwendet und eventuell ein regelbarer Widerstand für den NF-Pegel zum TX!




Bei Fragen kann Thomas, IW3AMQ unter der e-mail [iw3amq@gmail.com](mailto:iw3amq@gmail.com) kontaktiert werden.

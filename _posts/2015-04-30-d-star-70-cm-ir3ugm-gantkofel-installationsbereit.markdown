---
author: IW3AMQ
comments: false
date: 2015-04-30 13:54:28+00:00
layout: post
link: https://drc.bz/d-star-70-cm-ir3ugm-gantkofel-installationsbereit/
slug: d-star-70-cm-ir3ugm-gantkofel-installationsbereit
title: D-Star 70 cm IR3UGM Gantkofel installationsbereit!
wordpress_id: 10383
categories:
- D-STAR
- Umsetzer Gantkofel
---

Letzte Woche am Donnerstag, den 23. April 2015 kam das langersehnte Postpaket mit dem neuen D-Star Interface UP4DAR an. Über das Wochenende wurde das Interface in den 70 cm Motorola MC Compact eingebaut, konfiguriert und eingeschaltet: Nichts! Lcd-Bildschirm leuchtet zwar, aber sonst keine Reaktion :-(

[![UP4DAR_Einbau im McCompact Motorola](https://drc.bz/wp-content/uploads/2015/04/UP4DAR_Einbau-im-McCompact-Motorola-300x225.jpeg)](https://drc.bz/wp-content/uploads/2015/04/UP4DAR_Einbau-im-McCompact-Motorola.jpeg)

Klar, als "Newcomer" in dem Bereich konnte es auch nicht anders sein. Also gings an die Fehlersuche. PTT-Tastung war ok, aber keine Dekodierung beim Handfunkgerät. Digitale Signale wurden hörbar ausgesendet, auch konnte keine Verzerrung der NF festgestellt werden. Umgekehrt war beim RX auch keine Dekodierung auf dem LCD Bildschirm des UP4DAR zu sehen.

Also kontaktierte ich erst mal per e-mail Denis Bederov DL3OCK, einem aktiven Mitentwickler und auch [Shopbetreiber der UP4DAR](http://www.up4dar.de/). Es war Mitternacht und auch gleich kam eine Rückmeldung für eine Skypesitzung am nächsten Abend. Soll aber jetzt nicht heißen, jeder soll jetzt um Mitternacht den Denis kontaktieren, ok?

Am Dienstag dann hörten wir uns per Skype. Als erstes wurde der RX NF-Eingangspegel zum UP4DAR bei Empfang des D-Star Signales, ausgesendet mit einem Handfunkgerät IC-91E, gemessen: 20 mVpp. Denis setzte sich sofort mit dem Entwicklerteam in Kontakt und ganze 15 Minuten später kam der nächste Anruf: 20 mVpp sind zu wenig! **Das UP4DAR benötigt mindestens 60 mVpp an RX-Nf.** Leider ist dieser Wert nicht im Handbuch angegeben, sehr wohl aber der maximale NF Eingangspegel von 2.200 mVpp. Also mußte die NF verstärkt werden. Einen externen Transistor bzw. Operationsverstärker wollte ich nicht bauen, also entschied ich mich, nach Durchsicht des Schaltplanes, den Rückkopplungswiderstand R79 bei IC13A von 15 kohm auf 100 kohm zu erhöhen (ich hatte gerade diesen Wert und in der Größe in der Bastelkiste). Somit wurde das NF-Signal um den Faktor 10 (R75 = 10 kohm) erhöht und der UP4DAR bekommt 200 mVpp, genug für eine saubere Dekodierung des D-Star Signales. Im Foto sieht man klar den getauschten Widerstand mit der Aufschrift 104.

[![UP4DAR_Widerstand](https://drc.bz/wp-content/uploads/2015/04/UP4DAR_Widerstand-300x225.jpg)](https://drc.bz/wp-content/uploads/2015/04/UP4DAR_Widerstand.jpg)

Dann: Strom anschließen, PTT vom Handfunkgerät drücken und ... der Schriftzug IW3AMQ wurde auf dem LCD Bildschirm sichtbar!!!

[![UP4DAR_IR3UGM in Betrieb](https://drc.bz/wp-content/uploads/2015/04/UP4DAR_IR3UGM-in-Betrieb-300x225.jpeg)](https://drc.bz/wp-content/uploads/2015/04/UP4DAR_IR3UGM-in-Betrieb.jpeg)

Nun war nur noch das Problem der TX-Aussendung zu lösen. Mit viel Geduld erklärte mir Denis, daß der "TxGain" des UP4DAR von -127 bis +127 eingestellt werden kann. So steht es auch im Handbuch. Ich hatte ihn auf + 57, was beim meinem Sender des 70 cm Umsetzers einen Hub von genau 1.200 Hz verursachte. Perfekt würde man meinen, wäre da nicht die nötige Phasenverschiebung von 180° bei einigen TX, bei denen die NF eben einen invertierenden Verstärker durchläuft. Aber wie korrigiert man das? Für den RX-Teil im UP4DAR gibt es einen eigenen Flag bei "RxInv" zu setzen, aber für den TX-Teil? Ganz einfach, meinte Denis: **die Einstellung von -127 bis -1 beim "TxGain" bedeutet eine um 180° invertierte TX-Nf** am Ausgang der DIN-Buchse (diese Spezifizierung fehlt leider im Handbuch). Also wurde der Wert auf - 57 eingestellt und ... auf meinem Icom IC-91E wurde sofort der Schriftzug IR3UGM sichtbar!

Der Repeater samt Bandsperrenfilter ist nun installationsbereit für den Gantkofel, höchstwarscheinlich an einem dieser nächsten Wochenenden ist Bozen, Meran und Umgebung in D-Star QRV!

Vielen Dank nochmal an Denis DL3OCK, der mir via Skype so hilfreich zur Seite stand und wesentlich zum schnellen Erfolg beigetragen hat!

73! Thomas, IW3AMQ

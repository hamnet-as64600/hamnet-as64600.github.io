---
author: IW3AMQ
comments: false
date: 2014-10-13 13:17:21+00:00
layout: page
link: https://drc.bz/technik/analog-digitaltechnik/einfache-steuerschaltung-fuer-power-n-mosfet-30-v-70-a/
slug: einfache-steuerschaltung-fuer-power-n-mosfet-30-v-70-a
title: Steuerschaltung Power N-MosFet
wordpress_id: 9399
---

24.8.2013 – Da uns gleich nach der Installation des 70 cm Umsetzers auf dem Chavaltasch der relativ hohe Verbrauch aufgefallen ist, wurde daran gedacht, die beiden getrennt mit einer Zeitsteuerung zu versehen. So könnte besonders bei Nacht, wo kein Betrieb herrscht, der Strom total abgeschalten werden. Realisiert wurde das unter Verwendung der Soundkarten, die ja sowieso über die Software “AllStarLink” die Umsetzer steuert. Später werden in den Parametern die Timerfunktion integriert. Die Soundkarten haben jeweils 8 I/O’s (CM119 Chip), wobei nun die Belegung in der Konfigurationsdatei “usbradio.conf” vom AllStarLink folgendermaßen aussieht:

gpio1=out0 ;out0 = 10 W – out1 = 1 W gpio2=out1 ;out0 = 431,3875 MHz – out1 = 431,4000 MHz gpio4=out1 ;out0 = 12 V LS AUS – out1 = 12 V LS EIN

“gpio3″ wird exclusiv für das PTT verwendet, deshalb fehlt es in der oberen Tabelle. “gpio5″ – “gpio8″ sind noch für zukünftige Anwendungen frei belegbar.

Es wurde also schnell ein Schaltplan gezeichnet (siehe Foto) und gebastelt. Zur Verwendung kamen Bauteile aus der Bastelkiste, MosFet’s fand ich mit dem Namen PHB96NQ03LT. Das sind N-Mosfet, der Nachteil ist, dass der Gate-Pin eine höhere Spannung zur Schaltung braucht, als die Versorgungsspannung. Nicht so bei P-Mosfet, aber die sind teuer und unauffindbar! Also habe ich einen Spannungsverdoppler mit einem NE555 realisiert, der Verbrauch lag bei 15 mA. Dieser wurde also mit einem NE7555 ersetzt, der nur mehr 1,5 mA zog. Der Verbrauch der gesamten Ein/Ausschaltung mit NE7555, den vier Transistoren und zwei Power MosFet (25 V – 60 A!), die aus einem alten Motherboard “ausgeföhnt” [500°C] wurden, beträgt inclusive Spannungsverdoppler NE7555 auf 24 V ganze 2,2 mA. Dieser Verbrauch gilt für 1 oder mehrere Power MosFet’s, immer nur 2,2 mA! 2 Relès würden 100 mA und mehr verbrauchen! Hinweis: die Power MosFets werden Spannungsgesteuert, es fließt so gut wie kein Strom über das Gate.

Der Verbrauch der beiden 70 cm Umsetzer:



	
  * Link Südtirol (431,4000 MHz) RX: 0,5 A (**0,3 A** mit zusätzlicher uP Steuerung des TX) TX (16 W): 10,1 A (die Endstufe bringt 32 W, durch 3db Koppler wird 1/2 Leistung auf Widerstand verbraten) OFF: 0,0 A (über Allstarlink Soundkarte geschalten)



	
  * Zweiter Repeater (431,2875 MHz) RX: 0,6 A (**0,35 A** mit zusätzlicher uP Steuerung des TX) TX (6W): 4,5 A Off: 0,0 A (über Allstarlink Soundkarte geschalten)


27.8.2013 – Und da nun diese 500 mA des Link Südtirol und die 600 mA des zweiten Umsetzers mir noch zu viel waren, wurde mit einer zusätzlichen Schaltung der Verbrauch auf jeweils 300 mA und 350 mA reduziert. Möglich wurde dies durch die totale Abschaltung der TX, erst bei PTT über die Soundkarte wird der TX immer über 2 weitere Power MosFet eingeschalten und mit ca. 100 ms Verzögerung der PTT weitergeleitet. Diese Steuerung übernimmt diesmal ein Microprozessor von Atmel, ein AT Tiny45 mit 6 I/O, zwei werden für die Steuerung der Power MosFet verwendet, 2 für den PTT Eingang und die letzten 2 für den PTT für die TX. Schaltplan folgt …

[![Power-N-MosFet-Schalter1](https://drc.bz/wp-content/uploads/2014/10/Power-N-MosFet-Schalter1-300x269.jpg)](https://drc.bz/wp-content/uploads/2014/10/Power-N-MosFet-Schalter1.jpg)   [![PHB95L03LT](https://drc.bz/wp-content/uploads/2014/10/PHB95L03LT-300x218.jpg)](https://drc.bz/wp-content/uploads/2014/10/PHB95L03LT.jpg)   [![k-20130825_140705](https://drc.bz/wp-content/uploads/2014/10/k-20130825_140705-300x225.jpg)](https://drc.bz/wp-content/uploads/2014/10/k-20130825_140705.jpg)   [![k-20130824_220112](https://drc.bz/wp-content/uploads/2014/10/k-20130824_220112-300x225.jpg)](https://drc.bz/wp-content/uploads/2014/10/k-20130824_220112.jpg)   [![k-20130824_215857](https://drc.bz/wp-content/uploads/2014/10/k-20130824_215857-300x225.jpg)](https://drc.bz/wp-content/uploads/2014/10/k-20130824_215857.jpg)

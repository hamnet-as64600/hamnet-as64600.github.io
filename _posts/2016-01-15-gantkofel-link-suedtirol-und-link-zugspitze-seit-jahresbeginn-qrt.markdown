---
author: IW3AMQ
comments: false
date: 2016-01-15 13:09:05+00:00
layout: page
link: https://drc.bz/gantkofel-link-suedtirol-und-link-zugspitze-seit-jahresbeginn-qrt/
slug: gantkofel-link-suedtirol-und-link-zugspitze-seit-jahresbeginn-qrt
title: Gantkofel Link Südtirol und Link Zugspitze seit Jahresbeginn QRT
wordpress_id: 11425
categories:
- Bastelecke
- Link Suedtirol
- Umsetzer Gantkofel
---

Sicher habt ihr's schon bemerkt! Seit Jahresanfang ist das Link Südtirol und das Link zur Zugspitze am Gantkofel QRT. Da auch alle anderen Umsetzer des Link Südtirol am Chavalatsch, Jaufen, Plose und Kronplatz nicht mehr untereinander verbunden waren, lag es naheliegend, daß der PC den Geist aufgeben hatte.

[![Itx D2500HN Intel](https://drc.bz/wp-content/uploads/2016/01/Itx-D2500HN-Intel-300x157.jpg)](https://drc.bz/wp-content/uploads/2016/01/Itx-D2500HN-Intel.jpg)Also sind Herbert IW3BRH, Simon IN3FQQ und Thomas IW3AMQ am Freitag nachmittag, den 8. Jänner 2016 auf den Gantkofel gefahren. Zum Glück hatten wir einen äußerst milden Winter, die Auffahrt verlief ohne Kettenmontage, die 4 Ketten konnten also im Kofferraum bleiben!

Ausgerüstet mit einem Ersatz PC von Intel, Format ITX (17 cm x 17 cm), Modell D2500HN, einer Ersatzstromversorgung von 12 V für den PC, einer neuen Compact Flash Karte mit neuem Linux-Betriebssystem und neuer Version von Allstarlink und vielen anderem Kleinkram, haben wir also zuallererst den PC getauscht. Es fiel noch auf, daß der alte PC auch Probleme mit der Netzwerkverbindung aufwies.

[![AvrNetIo](https://drc.bz/wp-content/uploads/2016/01/AvrNetIo.jpg)](https://drc.bz/wp-content/uploads/2016/01/AvrNetIo.jpg)Da auch die Fernsteuerung [AVR Net I/O von Pollin](http://www.pollin.de/shop/dt/MTQ5OTgxOTk-/Bausaetze_Module/Bausaetze/Bausatz_AVR_NET_IO.html) nicht mehr ansprach, hat Simon IW3BWH uns auch eine [Softwareänderung](https://drc.bz/interessante-links/bastelecke-umbau-und-eigenbau/analog-digitaltechnik/dtmf-und-lanhamnet-fernsteuerung/) ganz kurzfristig geschrieben, mit der wir einen Hardware Reset via DTMF ausführen können. Es kam nämlich immer öfter vor, daß die Fernsteuerung über das Hamnet nicht mehr erreichbar war, jedoch über DTMF. Diese Tatsache und Recherchen im Internet haben ergeben, daß die 3,3 V Stromversorgung des ENC28J60, Interface IC zwischen LAN und dem Mikroprozessor, ohne Filterkondensatoren versehen war! Also wurden bei dieser Gelegenheit auch ein 10 uF und ein 10 nF Kondensator auf die 3,3 V Versorgung gelötet!

Die aktuelle Software und Schalpläne der Watchdogschaltung und der DTMF - Schaltung findet man [hier](https://drc.bz/interessante-links/bastelecke-umbau-und-eigenbau/analog-digitaltechnik/dtmf-und-lanhamnet-fernsteuerung/).

Zuallerletzt wurde dann alles wieder getestet und im wundervollen Abendrot konnten wir die Heimfahrt antreten!

73! Thomas, IW3AMQ

[8.1.2016]

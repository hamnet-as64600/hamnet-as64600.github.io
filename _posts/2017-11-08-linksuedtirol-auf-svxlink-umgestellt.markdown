---
author: IN3FQQ
comments: false
date: 2017-11-08 21:03:30+00:00
layout: page
link: https://drc.bz/linksuedtirol-auf-svxlink-umgestellt/
slug: linksuedtirol-auf-svxlink-umgestellt
title: LinkSüdtirol auf SVXLink umgestellt
wordpress_id: 14938
categories:
- Allgemein
- Echolink
- Link Suedtirol
---

![](https://drc.bz/wp-content/uploads/2017/11/SVXLink.jpg)

Nach langer Vorbereitungszeit, vielen Tests und Simulationen haben wir den Schritt nun endlich gewagt: **das Link Südtirol wurde vollständig von der bislang eingesetzten Software Allstar Link auf die neue Steuerungs-Software SVXlink umgestellt.**

Da dieser Schritt eine Neukonfiguration und neue Kalibrierung/Justierung der Pegel bei allen Relais bedeutet hat, haben wir uns lange und gut darauf vorbereiten müssen. Insbesondere mussten alle Relais auf einen Schlag auf das neue System umgestellt werden, weil natürlich die beiden verschiedenen Systeme AllstarLink und SVXlink nicht untereinander kommunizieren können.

Nachdem schon vor einem guten halben Jahr begonnen wurde, bei diversen Wartungseinsätzen vorsorglich alle Relais für SVXlink vorzubereiten, zu justieren und die Kalibrierparameter abzuspeichern, war es möglich, am Wochenende von Freitag, 03. November bis Sonntag 05. November 2017 dann alle Relais in einem Rutsch per Remote umzustellen.

Das Link Südtirol verhält sich auch mit der neuen Steuerung weiterhin gleich wie vorher: zwei unterschiedliche Rogerbeeps geben an, ob das Signal vom lokalen Relais oder von einem im Netz hängenden Relais empfangen wurde. Bei Doppelbeep wurde das Signal lokal empfangen, beim einfachen, tiefen Beep kommt das Signal aus dem Netz.

Auch der Echolink-Zugang zum Link Südtirol über den Knoten Gantkofel IR3UGM ist nun wieder möglich! Diverse Test-QSOs mit Stationen, welche sich via Smartphone, via PC oder via Relais verbunden haben liefen allesamt perfekt und mit deutlich besserer Audioqualität als vorher. Dies ist vor allem bei Echolink-Verbindungen zu anderen SVXlink-Basierten Relais deutlich zu merken, weil in dieser Konstellation automatisch zwischen den Relais ein besserer Sprachcodec (Speex) ausgehandelt wird, wohingegen im _Standard-Echolink_, also beim offiziellen Echolink-Client und der offiziellen Echolink-Relaissoftware, nur der GSM-Codec unterstützt wird.

Das LinkSüdtirol selbst arbeitet intern natürlich weiterhin vollständig via HAMNET. Einer der DRC-Server am Rittnerhorn übernimmt die Koordinierung der Audiostreams und verbindet die Relais miteinander. Als Audiocodec wird OPUS verwendet, ein sehr moderner, quelloffener (Open Source) Audiocodec, welcher besonders durch geringe Latenz bei der Codierung/Decodierung sowie durch ausgesprochen gute Sprachqualität bei geringer Datenmenge überzeugen kann.

Als weiterer Pluspunkt können nun alle unsere 2m Relais nativ via HAMNET an das LinkSüdtirol angekoppelt werden, natürlich ebenfalls ohne Qualitätsverlust. Von dieser Eigenschaft können wir vor allem bei der Funkübung und bei Notfällen profitieren.

![](https://drc.bz/wp-content/uploads/2017/11/LS-Dashboard.jpg)

Zu guter Letzt habe ich nun auch ein Dashboard für das LinkSüdtirol eingerichtet, auf welchem man nachschauen kann, auf welchem Relais der Gesprächspartner gerade eingibt, wie lange die Relais schon im Netz hängen, welche Relais vom Netz getrennt sind (Online: Grün, Offline: Grau) und wann das Relais zum letzen mal empfangen hat. Das Dashboard ist im Menü "Link Südtirol" -> "Dashboard" zu finden.

Viel Spaß mit dem neuen Link Südtirol!

73 de IW3AMQ und IN3FQQ



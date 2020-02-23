---
author: IW3AMQ
comments: false
date: 2015-12-01 07:20:46+00:00
layout: page
link: https://drc.bz/r4-ir3uhf-rittnerhorn-echolink-wieder-aktiv/
slug: r4-ir3uhf-rittnerhorn-echolink-wieder-aktiv
title: 'R4 - IR3UHF, Rittnerhorn: Echolink wieder aktiv'
wordpress_id: 11203
tags:
- Echolink
- Umsetzer Rittner Horn
---

[![echolink](https://drc.bz/wp-content/uploads/2015/07/echolink.jpg)](https://drc.bz/wp-content/uploads/2015/07/echolink.jpg)Nachdem am Freitag, 20. November 2015 der von Thomas IW3AMQ und Simon IN3FQQ modifizierte ICOM RP-1520 ([siehe Artikel](https://drc.bz/r4-rittnerhorn-ir3uhf-neuer-umsetzer-installiert-svx-link/)) mit eingebauter Computersteuerung auf dem Rittnerhorn installiert wurde, und dadurch das Fundament für die Echolink-Funktion gelegt wurde, wurde am Samstag, 28. November die Anbindung erneut aktiviert.

Der Umsetzer verfügt nun über eine direkte Anbindung an das Echolink-Netz, ohne 2 m HF-Strecke ins Tal. Die SVXlink Software speist das empfangene Signal über das Hamnet direkt in das Echolink-Netz ein. Erreichbar ist der Umsetzer Rittnerhorn wie gehabt anhand der [Knotennummer 12500](http://echolink.org/logins.jsp) und via Echolink-App oder am PC anhand des Rufzeichens IR3UHF-R .

[![ic-rp1520](https://drc.bz/wp-content/uploads/2015/11/ic-rp1520.jpg)](https://drc.bz/wp-content/uploads/2015/11/ic-rp1520.jpg)

Aufgrund der direkten Echolink-Anbindung wurde für den R4 eine eigene, direkte Internetverbindung nötig. Nachdem Herbert IW3BRH bereits vorgeschlagen hatte, dass sein Internetzugang für den R4 mitbenutzt werden könnte, habe ich zusammen mit ihm am Samstag Nachmittag die nötigen Netzwerkkonfigurationen vorgenommen.

An dieser Stelle nochmals vielen herzlichen Dank an Herbert IW3BRH für das Bereitstellen des Internetzugangs!

Die Bedienung des Relais über DTMF-Töne ist identisch zur Bedienung vom R2 Kronplatz.

Es gibt eine Reihe von **Unterkommandos**, die innerhalb des Echolink-Modules genutzt werden können. Dabei muss der **DTMF Ton ausgesendet und gleich anschließend die PTT (Mikrofontaste) losgelassen** werden.
<table >
<tbody >
<tr class="alt" >

<td width="111" >1
</td>

<td width="541" >Gibt alle verbundenen Stationen der Reihe nach aus
</td>
</tr>
<tr class="" >

<td width="111" >2
</td>

<td width="541" >Ausgabe der lokalen Echolink Node Nummer (IR3UHF-R = 12500)
</td>
</tr>
<tr class="alt" >

<td width="111" >31
</td>

<td width="541" >Verbindung mit einem zufällig gewählten Link oder Repeater
</td>
</tr>
<tr class="" >

<td width="111" >32
</td>

<td width="541" >Verbindung mit einer zufälligen Konferenz
</td>
</tr>
<tr class="alt" >

<td width="111" >4
</td>

<td width="541" >Mit der Station wiederverbinden, die zuletzt getrennt wurde
</td>
</tr>
<tr class="" >

<td width="111" >*
</td>

<td width="541" >Gibt die Kennung des Relais und die Uhrzeit aus
</td>
</tr>
<tr class="alt" >

<td width="111" >#
</td>

<td width="541" >Verbindung zu trennen (Üblich nach einem QSO)
</td>
</tr>
<tr class="" >

<td width="111" >##
</td>

<td width="541" >Trennt mehrere Stationen gleichzeitig
</td>
</tr>
</tbody>
</table>
Falls ein QSO beendet wurde, ohne die Echolink Verbindung zu trennen, dann wird diese automatisch nach 5 Minuten unterbrochen.

Der Sysop (System Verwalter) ist Simon IN3FQQ.

Ich wünsche allen viel Spaß und gute Verbindungen!

73! Simon, IN3FQQ

---
author: IN3FQQ
comments: false
date: 2018-11-17 13:51:00+00:00
layout: page-fullwidth
link: https://drc.bz/betriebsarten/digitalfunk/codeplugs/
slug: codeplugs
title: Codeplugs
wordpress_id: 17570
---

# 


In dieser Rubrik werden Codeplugs für verschiedene digitalfähige Funkgeräte gesammelt. Die Codeplugs sind auf den Gebrauch für Südtiroler OMs ausgelegt, aber können natürlich weiterverwendet und den eigenen Bedürfnissen angepasst werden.

Inhaltsverzeichnis dieser Seite:



 	
  1. AnyTone D868UV (DMR Dualband)

 	
  2. TYT MD-2017 (DMR Dualband)





* * *





# 





# 1. AnyTone D868UV (DMR Dualband)


Aktuelles Codeplug/Programmierfile: [868_drc](https://drc.bz/wp-content/uploads/2018/12/868_drc.zip)


## Tastenbelegung


![Bildergebnis für anytone 868 keys](https://www.f5uii.net/wp-content/uploads/2018/07/img_5b387ee2e8cc2.png)



**P1**: Umschalten zwischen oberem und unterem VFO

**P1 lang**: umschalten zwischen Single/Dual VFO Betrieb

**P2**: umschalten zwischen VFO und Memory

**P2 lang**: Modus umschalten (ANA,A+D,D+A,DIG)



**PF1**: Digital Monitor (1x = aktueller TS, 2x = beidenTS)

**PF1 Lang**: GPS Position anzeigen

**PF2**: Analog Squelch öffnen

**PF3**: Sendeleistung

**PF3 lang**: Batteriekapazität anzeigen







Über die beiden Tasten in der Mitte (Aufwärts und Abwärts) kann zwischen den Zonen gewechselt werden. Der Kanalwahlschalter oben in der Mitte wechselt zwischen den Kanälen.

Die Farbe der LED oben am Gehäuse hat folgende Bedeutung:
Grün: Analog RX
Cyan: Digital RX
Konstant Rot: TX
Blinkt Rot: niedriger Batteriepegel


## Zusatzfunktionen




#### Rufzeichen, QTH und TG Anzeige


Beim DMR Empfang wird nicht nur die DMR-ID des OMs sondern auch sein Name, sein Rufzeichen und bei einigen OMs auch das QTH angezeigt. Außerdem wird die Sprechgruppe (Talkgroup, TG) angezeigt, welche der OM ruft.


#### Talk Permit Tone


Bei der Benutzung von einem DMR Kanal gibt das Funkgerät nach dem Drücken der PTT Taste einen Ton aus, sobald der Gesprächskanal mit dem Umsetzer aufgebaut ist.

Der Ton gibt also an, ab wann man beim DMR Funken sprechen darf und gehört wird.


#### Digitales APRS


Sobald ein GPS Signal empfangen wird (Symbol in der Mitte der oberen Leiste leuchtet rot) und man ein QSO auf einem DMR Relais führt, wird alle 2 Minuten beim Auslassen der PTT Taste die eigene GPS Position über das DMR Netzwerk ins APRS Netz gesendet. Dies wird auch durch eine Meldung am Bildschirm angezeigt. Alle DMR Kanäle im Codeplug haben diese Funktion aktiviert.

Wer die APRS Sendungen deaktivieren möchte, kann einfach im Menü unter "GPS"->"GPS On/Off" die Einstellung "Off" wählen. Dann verschwindet in der oberen Leiste das Symbol und es werden keine GPS Daten mehr gesendet.

**Achtung: Damit APRS funktioniert muss mindestens Firmware version 2.32 installiert sein! Das kann im Menü unter "Settings" -> "Device Info" geprüft werden. Der Wert "Firmware Ver" sollte mindestens "Ver 2.32" sein.**




## Einspielen aufs Funkgerät


Von der [Webseite des Herstellers](http://www.connectsystems.com/software/software%20D868UV.htm) wird die aktuellste Programmiersoftware heruntergeladen und auf dem eigenen PC installiert. Damit das Funkgerät vom PC korrekt erkannt wird, muss der Treiber für das USB-Programmierkabel installiert werden. Dieser befindet sich ebenfalls im heruntergeladenen ZIP-Archiv.

Sobald die Softwareinstallation abgeschlossen ist, kann das Funkgerät programmiert werden. Dazu öffnet man die Programmiersoftware "D868UVE" und öffnet darin die Codeplug-Datei.



Im Codeplug muss nun das eigene Rufzeichen und die eigene DMR-ID eingegeben werden. Dies geschieht über den Punkt "Digital"->"Radio ID List" in der linken Spalte. Dort ist nur ein einziger Eintrag MYCALL mit einer Nummer vorhanden. Dieser wird durch das eigene Rufzeichen und die eigene DMR-ID ersetzt.

Nach diesem Schritt kann der Codeplug auf das Funkgerät geladen werden. Dazu wird im Menü "Program" der Punkt "Write to Radio" angeklickt und bestätigt. Beim ersten Programmieren muss auch die "Digital Contact List" auf das Funkgerät geladen werden. Dieser Vorgang dauert einige Minuten.

Zum Beginn der Seite



* * *





# 





# 2. TYT MD-2017 (DMR Dualband)


Aktuelles Codeplug/Programmierfile: [2017_drc](https://drc.bz/wp-content/uploads/2018/12/08.12.2018_MD-2017_Codeplug-für-Amateurfunker.rdt_.zip)

ID und Call sind einzutragen! Sollten Fehler bemerkt werden bzw. wollen Extrawünsche eingearbeitet werden, dann bitte bei mir melden [drc@drc.bz](mailto:drc@drc.bz)

Grüße Stefan IW3BSO 73

![](https://drc.bz/wp-content/uploads/2018/12/Erklärung-Display-TYT-MD-2017.jpeg) ![](https://drc.bz/wp-content/uploads/2018/12/Erklärung-TYT-MD-2017.jpeg)

**Verfahrensanweisung zum Programmieren des DMR Geräts TYT MD2017**



 	
  1. Auf einem Windows Pc zuerst den Treiber [USB Driver for digital radio ](http://www.tyt888.com/uploadfile/upfiles/20180425144149.zip) installieren

 	
  2. Anschliessend [CPS 2017 V1.22](https://drc.bz/wp-content/uploads/2018/12/TYT.zip) am PC installieren

 	
  3. Danach bei ausgeschaltenem Handfunkgerät das Programmierkabel am Funkgerät anschließen und mit einer USB Schnittstelle am PC verbinden und das Funkgerät einschalten.

 	
  4. Das Programm starten

 	
  5. Menü „General Settings“ auswählen

 	
  6. Dort bei „Radio Name“ sein Rufzeichen eintragen und bei „Radio ID“ die  zugewiesene ID eintragen

 	
  7. Weiter unten bei „Intro Screen Line 1“ den eigenen Namen z.B. Sepp eintragen

 	
  8. Bei „Intro Screen Line 2“ das eigene Rufzeichen nochmals eintragen


So jetzt sollte dann alles passen und man kann „On Air“ gehen

**Kurzbeschreibung zum Codeplug für TYT MD 2017 Version 0.1 Vinschgau 2018**

Bei dieser Beschreibung versuche ich die Vorgehensweise zum richtigen Bedienen des Gerätes in kurzen Schritten zu erklären. Dabei werde ich größtenteils auf die DMR relevanten Bedienungen einzugehen, die anderen sind ja mehr oder weniger jedem bekannt.

Die Codeplug ist ein erster Anfang um überhaupt mit diesem Gerät funken zu können und ist mit Sicherheit verbesserungswürdig, deswegen bin ich offen für Verbesserungsvorschläge und werde versuchen, diese so weit als möglich einzubauen. Nichts desto trotz soll niemand davon abgehalten werden, sich selbst im Codeplug schreiben zu versuchen.

Zum besseren Verständnis habe ich noch **2 Bilder mit Beschreibung** einmal über die **Tastenbelegung** (fast jede Taste hat 2 Funktionen) und einmal die einzelnen **Symbole im Display** beigelegt, mit der Bitte diese gut einzustudieren, da sehr wichtig für eine richtige Bedienung!

Nach dem Einschalten des HFG (= Handfunkgerät) sollte zuerst über die Menu Taste die Zone in der man sich befindet ausgewählt werden. Z.B: Piz Chavalatsch, Plose, Kronplatz usw…

Bemerkung: nach einem Ein– und Ausschalten des HFG kommt die zuletzt gewählte **Zone**.

Hat man die **Zone** ausgewählt dann befinden sich in der oberen Zeile alle in der Zone erreichbaren DMR TG`s  (TG= **TalkGroup** = Sprechgruppe) an erster Stelle habe ich immer die  **Sprechgruppe TG 23207 D-LS T2** dies ist sozusagen unsere Stammgruppe und heißt also in der Langversion gesagt **D**igital- **L**ink**S**üdtirol auf Timeslot 2 (Timeslot = Zeitschlitz).

Die üblich verwendete Bezeichnung wie von den meisten OM s verwendet wäre: IR3EB 2-23207 aber zum Einstieg für uns sind die Zahlen vielleicht etwas wenig aussagekräftig.

IR3EB = das Call von Piz Chavalatsch, 2 steht für den Zeitschlitz 2 und 23207 ist die Sprechgruppe Südtirol.

Die einzelnen TG`s können über den Trackball oder mit der Pfeil nach oben bzw. unten Taste ausgewählt werden. Z.B: TG DL -T1 für Deutschland, TG TAA-TS2 für Trentino AltoAdige usw.

Es ist auch immer der **Timeslot** angegeben, dies deswegen um besser zu verstehen welcher gerade besetzt ist. Wenn z.B. also jemand ein Gespräch gerade auf TG TAA-TS2 führt so kann nicht gleichzeitig ein Gespräch auf TG 23207 D-LS T2 geführt werden da dieser Zeitschlitz schon besetzt ist. Es ist aber möglich ein Gespräch auf TG DL-T1 zu führen da dieser TS ja frei ist.

Wenn also in der oberen Zeile IR3EB = die Bezeichnung für Piz Chavalatsch neben dem D für Digital ein grünes **Lautsprechersymbol** erscheint und man hört nichts, dann sieht man das über den DMR von Piz Chavalatsch gefunkt wird, aber möglicherweise auf einem anderen Zeitschlitz mit einer anderen TG. Man kann nun versuchen mal die anderen TG` s durch zu testen und wenn sie in der Empfangsliste der Codeplug eingetragen sind dann kann man das Gespräch mithören ansonsten nicht!

Nun machen wir den ersten Versuch eine **Verbindung auf TG 23207 D-LS T2**, welche wir ausgewählt haben, aufzubauen; dazu drücken wir die Sendetaste und es sollte bei hergestellter Verbindung die TG 23207 mit **Telefonsymbol** erscheinen. Wenn das so ist dann kann man wie gewohnt ein QSO aufbauen und hoffen dass jemand antwortet.  Das wäre also ein klassisches Gespräch in der Gruppe von TG 23207 D-LS T2 wo sich dann auch jeder der QRV ist wie bei üblichen FM Verbindungen beteiligen kann.

Wenn kein **Telefonsymbol** erscheint erreicht man den Umsetzer nicht! (Also Antenne oder Position wechseln)

Beim DMR gibt es dann noch persönliche **Einzelrufe**, dazu wähle ich über die Menu Taste „Contacts“ aus und gehe zum erwünschten Call des zu rufenden Teilnehmer, schaue dass sein Call blau hinterlegt, also ausgewählt ist und drücke die PTT Taste und z.B. IN3FQQ Simon wird dann auf der ausgewählten TG gerufen.

Zweite Möglichkeit: Menu, „**contacts**“,auswählen mit „**confirm**“  bestätigen und dann auswählen ob z.B. **Rufalarm** (Call Alert), **Radio Check** usw. durchgeführt werden soll.

Bei „**Call Alert**“ „läutet“ das angerufene HFG und man kann das Gespräch einfach mit PTT Taste drücken annehmen.

Bei „**Radio Check**“ ist es möglich zu schauen ob ein auf gleicher TG eingeschaltenes HFG welches z.B. ohne Bediener irgendwo im Haus angeschaltet ist auch erreichbar wäre. Also eine einfache **Erreichbarkeitskontrolle**.

Weiters kann eine **SMS** gezielt an einzelne Kontakte gesendet werden.

Man geht über das Menu zu „Massages“ und wählt aus ob man schreiben also „Write“ oder vorgefertigte Nachrichten „Quick Text“ versenden will, bestätigt jeweils mit „Confirm“ dann „Send“ und „Confirm“ wählt den Kontakt unter „Contacts“ aus und bestätigt mit „Confirm“ und schon wird die Nachricht an gewünschten Kontakt in der zuvor gewählte TG versendet. Wichtig ist natürlich zu wissen dass sich gewünschter Teilnehmer eben in dieser befindet. Wenn es also funktioniert hat bekommt man eine Bestätigung zurück ansonsten „ Message Send Fail“ ( Nachricht versenden fehlgeschlagen)

Des weiteren habe ich an 7. Position z.B. bei der Zone Piz Chavalatsch   **IR3EB Lokal TS2** eine **Lokale Sprechgruppe  auf Zeitschlitz 2** programmiert um z.B. bei Ausfall des Netzwerkes hin zu anderen Umsetzern lokal im Einzugsbereich des Umsetzers zu kommunizieren.

In dieser TG habe ich zudem die **GPS Datenübertragung** aktiviert, so würde man dann die Position jedes Einzelnen OM`s bei einem QSO angezeigt bekommen. Dies dass jeder mal testen kann. Voraussetzung ist natürlich dass Gerät einen „GPS Fix“ gemacht hat, dies erkennt man wenn kein „Verbotsschild“ mehr die winzige grüne Erdkugel oben im Display ziert.

Die Gegenkontrolle unter Menu „**GPS/BeiDou Info**“ auswählen und die Koordinaten werden angezeigt unter „RX GPSInfo“

Zusätzlich habe ich die **rote Taste oben am Gerät** so programmiert dass sie bei langem drücken einen Alarm in diese Sprechgruppe sendet, die GPS Daten mitteilt und das Mikrofon für 10 sec. Freigeschalten wird. Dies ist momentan nur für Testzwecke so gemacht und man kann ohne weiteres bessere Konfigurationen machen.

Zur **„P1“ Taste**: dort habe ich eine erweiterte Sprachverschlüsselung, wird durch langes drücken der Taste aktiviert und das Symbol im Display wechselt von blau/rot zu blau/gelb. Habe dies so gemacht dass unsere OMs dies mal untereinander  testen können; aber wichtig bei normalen Gesprächen zwischen OM`s ist die Sprache bitte nicht verschlüsselt zu machen, also im Display blau/rot ( blau/rot= nicht verschlüsselt)!! Sonst wundert man sich dann wenn einem keiner eine Antwort gibt!!

Ebenso ist genau darauf zu achten dass nicht „**Direkt Betrieb**“ eingeschalten ist, dort kommt natürlich immer sofort das Telefonzeichen weil ja nicht auf eine Antwort vom Umsetzer gewartet wird. Direktbetrieb würde nur dann Sinn machen wenn der Umsetzer ausfällt und sich die OM`s auch ohne Umsetzer hören können.

Wenn man ein Gespräch empfängt/mithört so lassen sich sämtliche Positionen nicht mehr verstellen/umschalten ! Einzige Abhilfe: die „**Back**“ Taste drücken somit wird der Gegenkanal stumm geschaltet.

In der unteren Zeile befinden sich die in der Zone empfangbaren **Analogkanäle.**

Wichtig: In der Zone "**manuell**" befinden sich 16 leere DMR Kanäle zum Teil mit eingestellten  TG`s und 20 leer FM Kanäle die alle unter Menu, „Utilities“ „Program Radio“ einstellbar sind.

Das heißt jeder kann dort seine „**privaten QRG`s**“ oder Lokale Runden nach belieben ablegen bzw. wenn er verreist die am Urlaubsort vorhandenen DMR Repeater eintragen und dann benützen.

**Nachtrag zu VFO mit TYT MD 2017**

**VFO - MODE** mit TYT MD2017 funktioniert. Alle, die meine Codeplug verwenden, könnten z. B. Zuerst die Zone "manuell" auswählen dann Menu - Utilities - Radio Settings - Mode - auf MR Mode wechseln ... und dann die BACK-Taste lang gedrückt halten bis neben der Frequenz anstatt der Kanalnumner ein "V" steht. Nun kann man die QRG über die Zifferntasten direkt eingeben und danach mit den Pfeil nach oben oder unten die Frequenz aufwärts oder abwärts schalten. Weit praktischer aber ist den Scanmodus einzuschalten.Diese habe ich den blauen Knopf 3 sec. drücken programmieirt. Der Suchlauf bleibt dann bei jeder besetzten Frequenz stehen. Wieder auf Kanalanzeige umstellen, alles in umgekehrter Richtung.

TYT MD2017 alle Sprechgruppen hören, ohne dass man eine spezielle Firmware installieren muss. Folgendes muss am Funkgerät eingestellt werden:



 	
  * **Menü** Taste drücken

 	
  * Menüpunkt **Utilities** wählen

 	
  * **Radio Settings** wählen

 	
  * **PrivateCallMatch** wählen

 	
  * **Turn off** wählen

 	
  * **GroupCallMatch** wählen

 	
  * **Turn off** wählen


Nun sind alle Sprechgruppen zu hören, auch wenn die entsprechende Sprechgruppe nicht erfasst und in der RX Group List ist. Ich muss sagen habe es leider noch nicht getestet, aber das könnt ja Ihr dann machen und schauen ob es wirklich funktioniert

So, zu schreiben wäre noch einiges aber für den ersten Einstieg sollte es reichen.

Best 73 von IW3BSO Stefan

Zum Beginn der Seite

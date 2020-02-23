---
author: IW3AMQ
comments: false
date: 2018-04-03 08:03:05+00:00
layout: page-fullwidth
link: https://drc.bz/technik/analog-digitaltechnik/svxlink-mit-orange-pi-zero/
slug: svxlink-mit-orange-pi-zero
title: SVXlink mit Orange Pi Zero
categories:
- Analog-Digitaltechnik
wordpress_id: 16141
---

<div class="row">
<div class="medium-4 medium-push-8 columns" markdown="1">
<div class="panel radius" markdown="1">
**&Uuml;bersicht**
{: #toc }
*  TOC
{:toc}
</div>
</div>


<div class="medium-8 medium-pull-4 columns" markdown="1">

**H2 Prozessor**  
**Betriebssystem: Armbian Buster**  
IN3FQQ - Simon / IW3AMQ - Thomas 

<blockquote>Last update: 08. Februar 2020 </blockquote>


![](/images/OrangePiZero.jpg)

### Vorbereitung Hardware

Es braucht beim Orange Pi Zero wirklich wenig, es ist praktisch so gut wie alles schon auf dem Board, auch die Soundkarte! Für die Minimalausführung braucht insgesamt nur 4 Bauteile (2 Elektrolytkondensatoren zu 1 uF, einen Widerstand mit einem NPN Transistor), die auch fliegend im Gehäuse des Orange Pi Zero gelötet werden können.


![](/images/PinoutOrangePiZero.jpg)

![](/images/OrangePi-ZeroPinout.jpg) Die GPIO Numerierung ist besser aus diesem Bild ersichtlich 

Für den PTT einfach einen NPN Transistor verwenden, Basis mit einem 1 kohm Widerstand zum I/O Pin (Pin 11, PA01, GPIO1) vom I/O Port des Orange Pi Zero verbinden. Den Emitter des Transistors auf Masse legen. Der Kollektor kommt zum PTT des Funkgerätes. 

**In vielen Fällen kann auch auf den Transistor verzichtet werden, wenn der hohe Pegel der PTT-Leitung die 5 V nicht übersteigt.**

![](/images/SchematicInterfaceOPZ.webp)

Für den Audioeingang (MIC1N oder MIC1P) das Signal vom Diskriminatorausgang des RX über einen Kondensator zu 1 uF verbinden. Falls das NF-Signal zu hoch ist, vor dem Kondensator einen Spannungsteiler einsetzen. Dieser kann durch einen Widerstand mit 33 kohm in Serie, danach einen Widerstand zu 1,5 kohm Parallel zur Masse realisiert werden oder durch einen 10 kohm Drehwiderstand, dann ist der Pegel regelbar. Im Schaltplan ist der Drehwiderstand eingezeichnet. Dann in Serie den Kondensator zu 1 uF zum MIC Eingang des Orange PI Zero.

Den rechten Audioausgang über einen Kondensator zu 1 uF mit dem Modulatoreingang des TX verbinden. Sollte der NF-Pegel zu hoch sein, einen 1 kOhm Trimmer zum Regeln einsetzen, danach folgt wieder 1 uF in Serie. Natürlich kann auch hier statt dem Drehwiderstand ein Spannungsteiler eingesetzt werden. 

**In vielen Fällen kann auf die Schaltung mit den variablen Widerständen verzichtet werden. Wichtig ist aber auf jeden Fall einen Elektrolytkondensator zu 1 uF im RX und einen im TX Zweig in Serie zu schalten, um die Soundkarte des OrangePiZero gleichstrommäßig vom RTX zu trennen!**

![](/images/Mini-360_2.webp)

Die Spannungsversorgung von 12 V kann mit einem kleinen Switchingboard zu ein paar Euro auf 5 V für den Orange Pi Zero geregelt werden (min. 1 A). Dieses Board bringt 2 A und kann innen auf die Oberseite des Gehäuses geklebt werden oder direkt auf die zweireihige Steckerleiste. Ich habe dazu das "Mini 360 DC" bei [www.aliexpress.com](https://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20180402220942&SearchText=Mini+360) gekauft. Fünk Stück kosten inklusive Versand 1,50 € ! 


![](/images/Mini-360_1.webp)

Als Verbindungsstecker zum Funkgerät(e) habe ich eine MiniDIN Buchse mit 6 Pin verwendet.  


**Beispiel der Pinbelegung MiniDIN Buchse zum RTX:**

![](/images/MiniDinPinout.jpg)


  1 = TX NF  
  2 = PTT  
  3 = GND  
  4 = /  
  5 = RX NF  
  6 = + 12 Volt


**Pinbelegung Motorola GM900:**


DB15 TX: DB15 RX:


10 = GND 10 = GND  
14 = + 12 Volt 21 = PTT  
25 = RX NF 24 = TX NF  
9 = zu Pin 4 9 = zu Pin 4  
4 = zu Pin 9 4 = zu Pin 9


![](/images/20180610_235839.webp)


Im Bild erkennt man die Lochrasterplatine, die auf den Orange Pi Zero direkt aufgesteckt ist und den Spannungswandler "Mini 360 DC" und die Bauteile der NF mit dem PTT Transistor trägt. Die nötigen Verbindungen für +5V, GND, TX Nf, RX Nf und PTT gehen direkt über die Steckerleisten zum Orange Pi Zero. Vom linken Klemmpfosten führen nur 3 Kabel (GND, TX Nf und PTT) zum TX, vom rechten Klemmpfosten führt nur einer (RX Nf) zum RX und die anderen zwei sind + 12 V und GND für die Stromversorgung. 


![](/images/20180610_235756.webp)


Hier wurden 2 Mobilfunkgeräte von Motorola, GM900 verwendet. **Später stellte sich allerdings heraus, dass die GM900 von Motorola im TX - Betrieb sich nach einiger Zeit nicht mehr auf Sendung tasten lassen. Ein bug in der Software! Ein Aus- und Einschalten bringt den TX dann wieder zum Laufen ... äh Senden. **



Alles hat zusammen mit einem Schaltnetzteil zu 12 V / 10 A (ganz links) in einem Rackgehäuse mit 1 HE ([Höheneinheit](https://de.wikipedia.org/wiki/H%C3%B6heneinheit) = 44,45 mm) Platz! Ein Ventilator aus einem Servernetzteil sorgt zuverlässig für die nötige Kühlung, wenn der Thermoschalter (auf dem linken GM900 in weiss, rechteckig mit weißem Kabel) am Kühlblech des TX die 50°C überschreitet. Eine weitere Möglichkeit ist es, den Ventilator direkt durch einen I/O des Orange Pi Zero softwaregesteuert zu schalten. Dabei wird die Temperatur des uP berücksichtigt, die individuell eingestellt werden kann, siehe Ventilator weiter unten. 



![](/images/blue-raspberry-pi-heatsinks-1.jpg)


Für eine **Passivkühlung** reicht ein großzügig bemessener  Kühlkörper, der auf den uP des Orange Pi Zero angebracht wird. Für  natürliche Luftzirkulation ist zu sorgen. Einen Kühlkörper der größeren  Art findet man z.B. bei [Aliexpress.com](http://www.aliexpress.com)  mit den Stichworten “Blue Raspberry Pi Heatsinks”. Mit diesem bleibt  die Temperatur unter 50 °C. Der Kühler ist 15 mm x 14 mm x 13 mm groß. 



![](/images/kuehlkoerper-opz.jpg)



### Betriebssystem installieren


Am Besten eine microSD Karte der Klasse 10 (Class10) mit mindestens 4 GB
einsetzen.



  * Auf der SD-Karte die neueste Version (zur Zeit 5.91) Armbian Buster auf Orange Pi Zero installieren, siehe [https://www.armbian.com/orange-pi-zero/](https://www.armbian.com/orange-pi-zero/)
  * Image auf die SD-Karte mit dem Programm „**Win32DiskImager“** brennen
  * Die SD-Karte in den Orange Pi Zero stecken
  * Den Orange Pi Zero mit dem Netzwerk verbinden und Strom geben
  * Auf dem Windows PC einen Netzwerkscanner starten (ca. 3 Minuten warten, bis der Orange Pi gebootet hat) und feststellen, welche IP Adresse der Orange Pi Zero vom DHCP Server bekommen hat
  * Auf dem Windows PC das Programm „Putty“ starten, die festgestellte IP Adresse und **Port 22** angeben
  * Originale Zugangsdaten sind => User: **root ** Password: **1234**
  * Sollte kein ssh Zugang mit “root” auf port 22 möglich sein, muss der Zugang aktiviert werden (beim ITX Intel mit Debian). Dazu folgenden Befehl ausführen: **nano /etc/ssh/sshd_config** und den Parameter “PermitRootLogin” auf “yes” setzen.
  * Warten …
  * Neues Password für root vergeben, zum Beispiel: **1234abcd **…
  * … und ein zweites Mal eintippen
  * Neuen Usernamen vergeben: **svxlink **(obligatorisch)
  * Neues Unix Password vergeben, zum Beispiel: **1234abcd**
  * Userinformationen eingeben, zum Beispiel: **IR3UHF**
  * Den Namen des PC ändern: mit WinSCP oder **nano /etc/hostname** im Ordner **/etc** in der Datei **hostname** den Namen ändern und speichern 
  * Falls man das Password ändern möchte, folgenden Befehl tippen: **sudo passwd root**
  * Den Befehl **armbian-config** eintippen, dann im Menü **System** den Punkt **Hardware** auswählen und folgende Parameter mit der Leertaste aktivieren: **Analog-codec** Nun ist die interne Audiokarte aktiviert.
  * Neu starten mit** reboot**


**Armbian updaten**



  * Armbian udaten: **sudo apt-get update**
  * Updates von Armbian installieren: **sudo apt upgrade**
  * Firmware updaten: **sudo apt dist-upgrade**


### SVXLink installieren



  1. **apt install gcc g++ make cmake groff gzip doxygen tar git libsigc++-2.0-dev** **libjsoncpp-dev** **libcurl4-openssl-dev** **libqt4-dev libpopt-dev tcl8.6-dev** **libgcrypt20-dev** **libasound2-dev libgsm1-dev libopus-dev libspeex-dev librtlsdr-dev** **alsa-utils**
  2. **git clone [https://github.com/sm0svx/svxlink.git](https://github.com/sm0svx/svxlink.git)**


Danach kann in das von GIT geklonte Verzeichnis gewechselt und der /src/build Ordner erstellt werden:



  1. ** ****cd svxlink/src**
  2. ** mkdir build**
  3. ** cd build**



Nun starten wir cmake mit den folgenden beiden wichtigen Switches:  
**-DUSE_QT=OFF** sorgt dafür, dass die User-Anwendung _qtel_ nicht gebaut wird und daher auch die QT Bibliotheken beim Kompilieren nicht gebraucht werden

**-DWITH_SYSTEMD=yes** sorgt dafür, dass anstelle der früher üblichen init-files (/etc/init.d/svxlink) die entsprechenden systemd-Units generiert werden


  1. **cmake -DCMAKE_INSTALL_PREFIX=/usr -DSYSCONF_INSTALL_DIR=/etc -DLOCAL_STATE_DIR=/var -DUSE_QT=OFF -DWITH_SYSTEMD=yes ..**


Dann kann mit der Kompilierung begonnen werden. Diese dauert auf dem Orange Pi je nach verwendeter SD Karte gute 15-30 Minuten


  1. ** make**  


Sobald die Kompilierung abgeschlossen ist, können die Resultate ins System "Installiert" werden (Befehl [1]). Genauer gesagt werden dabei die ausführbaren Dateien und generierten Unit-Files an die richtigen stellen im System verschoben und aktiviert.


Am Ende wird dann (Befehl [2]) systemd angewiesen, nach neuen Unit-Files zu suchen. Hier sollten nun die neuen Unit-Files von svxlink gefunden werden

  1. ** make install**   
  2. ** systemctl daemon-reload**


Abschließend wird mit dem folgenden Befehl die Systemd-Unit "svxlink" beim Booten aktiviert:

  1. **systemctl enable svxlink**


**Installation der Audiodateien**


  * Kontrollieren, ob nur eine Instanz von Svxlink läuft mit **pidof svxlink**
  * Audiodateien kontrollieren, ob die Ordner (Core, Default; DtmfRepeater      usw.) in folgendem Ordner sind: **/usr/share/svxlink/sounds/en_US**
  * Falls keine vorhanden sind, mit dem PC diese Datei herunterladen:   
[https://github.com/sm0svx/svxlink-sounds-en_US-heather/releases/download/19.09/svxlink-sounds-en_US-heather-16k-19.09.tar.bz2](https://github.com/sm0svx/svxlink-sounds-en_US-heather/releases/download/19.09/svxlink-sounds-en_US-heather-16k-19.09.tar.bz2)
  * Diese Datei mit dem Windows PC mit dem Programm „7-zip“ entpacken und den gesamten Ordner mit Unterordnern mit dem Programm „WinSCP“ in den  Ordner **/usr/share/svxlink/sounds/en_US/** kopieren


### SVXLINK konfigurieren


  * Mit WinSCP die Datei **svxlink.conf** konfigurieren. Dazu siehe auch deutsche Anleitung im Netz (Test Zuordnung Soundkarte: **aplay -l** und **arecord -l** im Putty eingeben)
  * wenn GPIO Pins für PTT verwendet werden, können diese in **/etc/svxlink/gpio.conf** konfiguriert werden
  * Mit WinSCP wenn nötig auch die Datei **ModuleEchoLink.conf** im Ordner **/etc/svxlink/svxlink.d/** anpassen
  * Svxlink starten für Test: **svxlink** , mit **Q** beenden        
     
  * Svxlink als Service starten: **service svxlink start**
  * Svxlink als Service stoppen: **service svxlink stop**
  * Svxlink Status abfragen: **service svxlink status**

### Svxlink Audiopegel, Squelch und CTCSS justieren



**Abgleich NF TX**


  * Zweites Putty öffnen
  * Alsamixer starten: **alsamixer -c0 **(auch** alsamixer -c1 **bei externer Soundkarte, ev. Mit **F6** Soundkarte auswählen)
  * Damit alle Ein- und Ausgänge angezeigt werden **F5** drücken. 
  * Mit **TAB** weiterschalten, mit **Pfeil oben**, **unten**, **rechts**, **links** bzw. mit Taste **M** oder **Leertaste** für Ein/Aus.


**Voreinstellungen für Alsamixer:**  
„Line Out“ = **50** und mit M Taste auf ON setzen  
"Line Out": **Stereo**  
„Mic1“ = 0 und mit Leertaste - L R Caputure auf ON setzen  
"Mic1 Boo" = 38  
„DAC“ = **51** und mit M Taste auf ON setzen 



Alle anderen ausschalten bzw. auf 0 stellen.



  * Zum ersten Puttyfenster wechseln
  * Abgleichbefehl starten:  
     **devcal -t -f 1000 -d 5000 -m 5000 /etc/svxlink/svxlink.conf Tx1  
     **Achtung: Befehl selbst neu eintippen, NICHT kopieren und einfügen!!!      Das Kopieren/Einfügen hat einige Male Fehler gegeben.  
     oder**  
     devcal -t -f 1000 -d 5000 -m 5000 -a alsa:plughw:1 /etc/svxlink/svxlink.conf Tx1  
     **Achtung: ev. Auch …** -a alsa:plughw:0 **(je nach Soundkarte)
  * Mit Taste **T **Ptt einschalten
  * Mit den Tasten + und – den Pegel so einstellen, dass **5 kHz** Modulation erreicht sind
  * Falls nötig, im zweiten Puttyfenster den Regler “**Lineout**” verstellen (nicht über 90% gehen, Verzerrungsgefahr bzw. Verzerrung der NF im Testset prüfen)
  * Den Wert merken und in die Datei **svxlink.conf** unter „**MASTER_GAIN=**“      schreiben
  * Das erste Puttyfenster mit **Q** beenden



**Abgleich NF RX**


  * Mit dem Signalgenerator auf der RX Frequenz dem Empfänger ein      rauschfreies Signal mit einem 1 kHz Ton und 5 kHz Frequenzhub geben
  * Abgleichbefehl starten:  
     **devcal -r -f 1000 -d 5000 -m 5000 /etc/svxlink/svxlink.conf Rx1  
     **oder**  
     devcal -r -f 1000 -d 5000 -m 5000 -a alsa:plughw:1 /etc/svxlink/svxlink.conf Rx1  
     **Achtung: ev. auch …** -a alsa:plughw:0 **(je nach Soundkarte)
  * Mit **+** und **–** den Pegel so einstellen, dass **5 kHz** Modulation erreicht sind
  * Falls nötig, im zweiten Puttyfenster den Regler “**Mic1 Boo**” verstellen (nicht über 90% gehen, Verzerrungsgefahr). Falls das nicht reichen sollte, dann erst mit "ADC Gain" probieren
  * Den angezeigten Wert von **Preamp** merken und in die Datei **svxlink.conf**      unter „**PREAMP=**“ schreiben
  * Mit **Q** beenden
  * Im zweiten Puttyfenster mit **ESC** das Programm Alsamixer beenden
  * Parameter von Alsamixer mit dem Befehl **alsactl store** speichern
  * Damit die Parameter der Soundkarte in einem File erhalten bleiben und dieses dann kopiert werden kann, folgenden Befehl ausführen: **alsactl store -f /etc/svxlink/alsa_icom_rp4020** (als Beispieldatei)
  * Um diese Daten von der Datei wieder zu laden:  **alsactl restore -f /etc/svxlink/alsa_icom_rp4020**
  * Svxlink starten mit **svxlink –daemon** und mit **killall svxlink** wieder beenden


**Signalpegel einstellen**




  * Signalgenerator für S9 + 30 db auf -63 dbm einstellen, ohne Ton, nur      Träger
  * Abgleichbefehl starten:  
     **siglevdetcal /etc/svxlink/svxlink.conf Rx1**
  * Die angegebenen Werte für **SIGLEV_SLOPE**, **SIGLEV_OFFSET **und      **CTCSS_SNR_OFFSET** in **svxlink.conf** schreiben



**Abgleich CTCSS TX**


  * Das Programm Svxlink mit dem Befehl **svxlink** starten.
  * Den Umsetzer mit einem Handfunkgerät auftasten und den Pegel des Subaudiotones CTCSS messen.
  * Im File **svxlink.conf** den Parameter „**CTCSS_LEVEL=**“ in der Rubrik **[TX1]** so lange verändern, dass der Hub des Subaudiotones **500 Hz** beträgt. Dazu mit einem RTX den Umsetzer auf Sendung bringen.
  * Dazu bei jeder Änderung File speichern und dann Svxlink mit dem Befehl **svxlink** neu starten.
  * Am Ende den PC rebooten mit dem Befehl **reboot** und kontrollieren, ob alles läuft.


### Statische IP Adresse setzen



  * Die IP Adressen in der Datei **interface**s bearbeiten: **nano /etc/network/interfaces**   

  * Beispiel:  
**     source /etc/network/interfaces.d/*  
    auto lo  
    iface lo inet loopback  
  
    auto eth0  
    allow-hotplug eth0  
    iface eth0 inet static  
         address 44.134.190.115/28  
         gateway 44.134.190.112 **


Subnetmask ist meistens 255.255.255.240 bzw. /28 




Die DNS server in der Daten **resolv.conf** bearbeiten: **nano /etc/resolv.conf**


**nameserver 44.134.190.76  
nameserver 44.134.190.126**


(44.134.190.76 für Rittnerhorn und 44.134.190.126 für Kronplatz – den netzwerkmäßig näheren als erstes angeben)



Achtung! Wird eine SD Karte auf einem PC konfiguriert und dann in einen anderen PC genutzt, wird automatisch für die neue LAN Schnittstelle mit der neuen MAC Adresse ein DHCP Zugang konfiguriert. Die alten Einstellungen bleiben im Programm **nmtui** als "Wired connection 2" erhalten. Die ursprüngliche statische IP ist aber nicht mehr zugänglich, da diese auf einer "fremden" MAC Adresse lautet!


### Infotext bei Anmeldung ausgeben



Um einen Infotext nach dem Login auszugeben, im Ordner **/etc/profile.d** die Datei **info.sh** neu einrichten (sie ist meist noch nicht vorhanden, die Datei mit **nano /etc/profile.d/info.sh** oder WinSCP neu einrichten und bearbeiten). In dieser kann einfacher Test wie folgt eingegeben werden:



echo " R2 Kronplatz – Motorola MC Compact"  
echo ""  
echo "Niedere Leistung (1 W): echo 1 > /sys/class/gpio/gpio7/value"  
echo "Hohe Leistung (10 W): echo 0 > /sys/class/gpio/gpio7/value"  
echo ""  
echo "Kanal 1 (145,650 MHz): echo 0 > /sys/class/gpio/gpio0/value"  
echo "Kanal 2 (145,700 MHz): echo 1 > /sys/class/gpio/gpio0/value"  
echo ""



### Installation von setQRG auf dem MB45 mit OrangePiZero


  * Alle Dateien von [setQRG](https://drc.bz/wp-content/uploads/2020/02/setqrg-mb45-1.zip) entpacken und in den Ordner /opt kopieren
  * Mit **cd /opt** In den Ordner      /opt wechseln
  * Den Compiler Python-pip mit folgendem Befehl installieren: **apt-get      install python-pip**
  * Das GPIO Handling für den Orange Pi Zero herunterladen: **pip install Opi.GPIO**
  * Im Ordner **/usr/bin** die Datei **setQRG** anlegen z.B. mit **nano /usr/bin/setQRG** und folgenden Text einfügen:  
     **#!/bin/bash  
     python /opt/setQRG.py $@**
  * Die Datei speichern
  * Damit setQRG ohne Python Aufruf ausgeführt werden kann, folgenden Befehl ausführen: **chmod +x /usr/bin/setQRG**
  * Mit **cd .. **in das Hauptverzeichnis wechseln
  * Damit der Befehl setQRG beim reboot ausgeführt wird, muss in der Datei /etc/init.d/svxlink der Befehl (siehe fett gedruckt) ab Zeile 94 hinzugefügt werden:



        _case      “$1” in_ _       _  
        _start)_  
        **## Starte setQRG**  
        **log_daemon_msg "Setting QRG" "svxlink"**  
        **setQRG**  
        _Log_daemon_msg „Starting SVXLINK server“ „svxlink“_

        


  * Mit folgendem Befehl kann man schon testen, ob der Befehl korrekt ausgeführt wird: **setQRG**
  * Mit folgendem Befehl ruft man die Hilfe auf: **setQRG –h**


### Installation von Read Only Modus SD Karte
Orange Pi Zero**



In der Datei **/etc/fstab** mit WinSCP  oder mit dem Befehl **nano /etc/fstab** folgende 5 Zeilen am Ende einfügen und eine Leerzeile dazwischen lassen:



**tmpfs /tmp tmpfs nodev,noatime,nosuid,mode=1777,size=64m
0 0**


**tmpfs /var/tmp tmpfs
nodev,noatime,nosuid,mode=1777,size=64m 0 0**


**tmpfs /var/log tmpfs
nodev,noatime,nosuid,mode=1777,size=64m 0 0**

**tmpfs /var/lib/logrotate tmpfs
nodev,noatime,nosuid,mode=1777,size=12k 0 0**

**tmpfs /var/lib/dhcp tmpfs
nodev,noatime,nosuid,mode=1777,size=16k 0 0**


Danach, ohne
die anderen bestehenden Angaben in der ersten Zeile zu verändern, den Parameter
**/
ext4 defaults, noatime,…** in **/ ext4 ro,defaults,noatime,…**
ändern.


Mit Cntl-X Programm beenden, mit Y Dateiname und speichern bestätigen.  
Den Befehl **mount –a** ausführen.  
Mit **reboot** den Orange Pi Zero neu starten.  
Mit **touch test** prüfen, ob nun das System „read only“ ist.  
Mit dem Befehl **mount –o remount,rw /** kann der Status in „read / write“ umgestellt werden.  
Mit dem Befehl **mount –o remount,ro /** kann der Status in „read only“ umgestellt werden.


Sollte sich die Änderung der IP Adresse trotz des Befehls  **mount –o remount,rw /** nicht speichern lassen, die Änderungen rückgängig machen. Nicht vergessen, nach dem abspeichern der Datei den Befehl **mount -a** auszuführen und rebooten. Dann IP Adresse ändern und **/etc/fstab** wieder ändern.



### Ventilator für Orange Pi Zero’s Prozessor


Da doch der
Prozessor etwas heiß wird (> 55 °C), kann zusätzlich zum Kühlkörper (desto
größer, desto besser) auch ein Ventilator temperaturgesteuert angebracht
werden. Die Schaltung ist recht einfach, ein BC879 (NPN Darlington Transistor)
steuert über den GPIO 0 den Ventilator. Die Software ist schnell geschrieben.



Zur Abfrage
der Temperatur und anderer Parameter kann der folgende Befehl verwendet werden:
**armbianmonitor –m**



Die Ausgabe
erfolgt alle 5 Sekunden, sie kann mit **Ctrl-C**
beendet werden.



![](/images/fan.jpg)



Anstatt “Load” wird der Ventilator angeschlossen, Polarität beachten! Als Transistor kann auch ein NPN Darlington verwendet werden, der braucht weniger Basisstrom, z.B. ein BC879. Der Widerstand in Serie ist bei einem NPN Darlington 15 kohm. Ich habe den GPIO0 (pin 13) verwendet.



Software:



Im Ordner **/etc/opt**
wird eine einfache Textdatei mit dem Namen **fun-control.sh**
angelegt. Diese Zeilen dort einfügen:


    **_#!/bin/bash_**  
    **_echo
    0 > /sys/class/gpio/export_**  
    **_echo
    out > /sys/class/gpio/gpio0/direction_**  
    **_temperature=$(<
    /sys/devices/virtual/thermal/thermal_zone1/temp)_**  
    **_if
    [ $temperature -gt 45 ]_**  
    **_then_**  
    **_echo
    “1” > /sys/class/gpio/gpio0/value_**  
    **_else_**  
    **_echo
    “0” > /sys/class/gpio/gpio0/value_**  
    **_fi_**


In der 5. Zeile kann die Schalttemperatur geändert werden (momentan auf 45 °C).  
Die Datei speichern.  
Im selben Ordner dann den Befehl **chmod +x fan-control.sh** ausführen, um die Datei auszuführen.



Im Ordner **/etc**
die Datei **crontab**
bearbeiten. Die fett gedruckte Zeile einfügen und speichern.

    SHELL=/bin/sh
    PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin_
    # m h dom mon
    dow user command_  
    17 * * * *
    root cd / && run-parts –report /etc/cron.hourly  
    _25 6 * * *
    root test -x /usr/sbin/anacron || ( cd / && run-parts –report
    /etc/cron.daily )_  
    47 6 * * 7
    root test -x /usr/sbin/anacron || ( cd / && run-parts –report
    /etc/cron.weekly )_  
    52 6 1 * *
    root test -x /usr/sbin/anacron || ( cd / && run-parts –report
    /etc/cron.monthly )_  
    **_*
    * * * * root /etc/opt/fan-control.sh_**  
    #




Mit **reboot**
neu starten. Die Temperatur kann mit folgendem Befehl abgefragt werden: **cat
/sys/devices/virtual/thermal/thermal_zone0/temp**



## Parallel Port LPT1 bei einem ITX Pc  ansteuern

Das Programm
zur Steuerung der Ausgangspin der parallelen Schnittstelle kann hier
heruntergeladen werden: [https://bigasterisk.com/projects/parallel/](https://bigasterisk.com/projects/parallel/)

Alternativ
kann die Datei auch von der DRC Homepage heruntergeladen werden: [parcon.c](https://drc.bz/wp-content/uploads/2018/04/parcon.c)

Die Datei **parcon.c**
in den Ordner **/root/parcon/**
kopieren.

Zum Kompilieren der Datei “parcon.c” folgenden Parameter im Ordner von “parcon.c” schreiben:

**gcc -O parcon.c -o parcon**

Der manuelle
Befehl für die Ausführung lautet:

**./parcon/parcon 1h 2l 3l 4h 6l 8l**

h = high, l (kleines L) = low

Damit stellt
man Ausgang 1 auf high, Ausgang 2 auf low, Ausgang 3 auf low, Ausgang 4 auf
high usw. Achtung: D0/Pin2 in der Zeichnung entspricht Ausgang 1, D1/Pin3 =
Ausgang 2, D2/Pin4 = Ausgang 3 usw.

![](https://drc.bz/wp-content/uploads/2018/04/Parallel_port_pinouts.jpg)

Um den
gewünschten Befehl beim Start des Pc’s automatisch zu starten, folgende Zeile
im Programm “crontab” einfügen:

**crontab
-e** 
# start des Programmes zum Einfügen der parcon Befehlszeile


Editor
auswählen, z.B. **1** für nano  

Folgene Zeile ganz unten hinzufügen (Portnummer und high-low Level wie
gewünscht verändern):


**@reboot /root/parcon/parcon 1h 2l 3l 4h**

Unbedingt
eine Leerzeile nach dem Befehl einfügen! Beenden mit **Cntl-x**
und mit **j**
für ja Speicherung bestätigen  

PC mit **reboot**
neu starten.


Ausgang 1
habe ich mit der Kanalumschaltung und Ausgang 2 mit der
Sendeleistungsumschaltung verbunden (bei Motorola MC Compact)


</div> <!-- -->
</div> <!-- -->
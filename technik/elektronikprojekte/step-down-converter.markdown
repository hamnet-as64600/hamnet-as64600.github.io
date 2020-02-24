---
author: IW3AMQ
comments: false
date: 2018-08-24 07:35:06+00:00
layout: page
link: https://drc.bz/technik/analog-digitaltechnik/step-down-converter-mini-360-test/
slug: step-down-converter-mini-360-test
title: Step down converter MINI-360 - Test
wordpress_id: 17064
---

Viele verwenden den inzwischen legendär gewordenen switching down converter MINI-360, der von vielen Online-Shops vertrieben wird. Es gibt auch hier "gute" und "schlechte". Bei den "schlechten" macht sich das beim "ripple"-Wert bemerkbar, der Restwelligkeit der Ausgangsspannung. Diese kann auch ziemlich hoch sein und die Funktionsfähigkeit des angeschlossenen Gerätes negativ beeinflussen.

Ich habe also nun 3 verschiedene Versionen einem einfachen Test unterzogen, die Restwelligkeit bleibt bei allen, sei es bei keiner Last, wie unter Last, identisch.


 ![](https://drc.bz/wp-content/uploads/2018/08/10-HX-MINI-360.jpg) ![](https://drc.bz/wp-content/uploads/2018/08/11-HX-MINI-360.jpg)


Der verwendete IC ist der [MP2307DN](http://pdf1.alldatasheet.com/datasheet-pdf/view/189149/MPS/MP2307DN.html), er verträgt bis zu 23 Volt (max. 26 V) im Eingang und kann bis zu 3 A Strom liefern. Die Schaltfrequenz ist fix und beträgt ca. 340 kHz.

Ausschlaggebend für die unterschiedliche Restwelligkeit könnte die Qualität des Ferritkernes der Induktanz zu 10 uH sein, die bei den 3 getesteten Modellen auch unterschiedlich aussieht. Es könnten aber auch die Kondensatoren sein, die vielleicht nicht den vorgeschriebenen "low ESR" Werten ([Equivalent Series Resistance](https://en.wikipedia.org/wiki/Equivalent_series_resistance)) laut [Datenblatt](http://pdf1.alldatasheet.com/datasheet-pdf/view/189149/MPS/MP2307DN.html) entsprechen. Laut Datenblatt sollte die Restwelligkeit bei 10 mV liegen, ich habe aber Werte von 60 mV bis 320 mV gemessen.

Unterschiedlich ist daher auch die Ruhestromaufnahme, die beim "guten" Modell HX-MINI-360 nur ca. 10 mA beträgt, bei den anderen mit höherer Restwelligkeit aber ca. 40 mA.

Gespeist wurden die Module mit ca. 13,9 V, Ausgangsspannung wurde mit dem Drehwiderstand auf ca. 5 V eingestellt.

Ich lasse Bilder sprechen ...

73! Thomas, IW3AMQ



**HX-MINI-360 (ripple = 65 mV)**

![](https://drc.bz/wp-content/uploads/2018/08/10-HX-MINI-360.jpg) ![](https://drc.bz/wp-content/uploads/2018/08/11-HX-MINI-360.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/12-HX-MINI-360-1024x699.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/14-HX-MINI-360-1024x576.jpg) ![](https://drc.bz/wp-content/uploads/2018/08/13-HX-MINI-360-1024x576.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/15-HX-MINI-360-1024x758.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/16-HX-MINI-360-1024x576.jpg)



**MINI-360 mit Logo (ripple = ca. 320 mV)**

![](https://drc.bz/wp-content/uploads/2018/08/20-MINI-360_CloneA.jpg) ![](https://drc.bz/wp-content/uploads/2018/08/21-MINI-360_CloneA.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/23-MINI-360_CloneA-1024x905.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/24-MINI-360_CloneA-1024x576.jpg) ![](https://drc.bz/wp-content/uploads/2018/08/33-MINI-360_CloneB-1024x576.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/25-MINI-360_CloneA-1024x753.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/26-MINI-360_CloneA-1024x576.jpg)



**MINI-360 ohne Logo (ripple = ca. 300 mV)**

![](https://drc.bz/wp-content/uploads/2018/08/30-MINI-360_CloneB.jpg) ![](https://drc.bz/wp-content/uploads/2018/08/31-MINI-360_CloneB-1024x629.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/32-MINI-360_CloneB-1024x749.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/34-MINI-360_CloneB-1024x576.jpg) ![](https://drc.bz/wp-content/uploads/2018/08/22-MINI-360_CloneA-1024x576.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/35-MINI-360_CloneB-1024x705.jpg)

![](https://drc.bz/wp-content/uploads/2018/08/36-MINI-360_CloneB-1024x576.jpg)



---
title: PCB-k és áramköri rajzok
---

A DNMS építésének legjobb módja az egyik nyomtatott áramköri lapunk használata.
Ma már elég sok NYÁK-gyártó van, aki képes áramköri lapokat gyártani néhány dollárért, minimális mennyiség nélkül. Például a [JLCPCB](https://jlcpcb.com/).
Csak töltse le az alábbi áramköri rajzainkat és/vagy Gerber-fájljainkat, töltse fel őket a gyártó weboldalára, és rendelje meg a NYÁK-okat.

<br>
A nyomtatott áramköri lapok utolsó változatait itt ismertetjük. További információkért és a KiCad-fájlok eléréséhez lásd [Helmut Bitter Github](https://github.com/hbitter/DNMS/tree/master/PCBs).

### AIRROHR V1.4
<img src="../docs/dnms/airrohr-PCB.jpg" style="display: block; width:40%;margin: 1em 0" loading="lazy"/>
NYÁK a NodeMCU ESP8266 CPUWLAN számára, I2C busz kiterjesztéssel a DNMS és más érzékelők (SDS011, BME280...) csatlakoztatásához.


##### Letöltés:
* [Áramköri diagram](..docsdnmsairrohr-PCB-circuit-diagram.pdf)
* [Gerber fájl a nyomtatott áramkör gyártójának weboldalára való feltöltéshez](../docs/dnms/airrohr-PCB-circuit-diagram-gerber.zip)

---

### DNMS - T4 V1.4
NYÁK a DNMS Teensy 4.0-hoz, amely közvetlenül csatlakoztatható egy NodeMCU ESP8266-ra vagy a fenti AIRROHR NYÁK-ra.


##### Letöltés:
* [Áramköri diagram](..docsdnmsdnms-noise-measuring-teensy-40-circuit-diagram.pdf)
* [Gerber fájl a nyomtatott áramkör gyártójának weboldalára való feltöltéshez](..docsdnmsdnms-noise-measuring-teensy-40-circuit-gerber.zip)

---
title: Sestavite
---

> ⚠️ **POMEMBNA OPOMBA**
Pred sestavljanjem namestite vdelano programsko opremo!
Glejte razdelek __firmware flasher__.

### NodeMCU v3
Opomba: Naša navodila veljajo za različico 3 enote NodeMCU. To lahko prepoznate po priključkih VU in G (glejte risbo).

<img src="../docs/airrohr/airrohr-wiring-sds011-bme280.jpg" style="width:40%; margin-top: 3em" loading="lazy"/>
<small>Copyright: roman-minyaylov, licenca MIT</small>


<img src="../docs/airrohr/nodemcu-v3-bme280.jpeg" style="margin-top: 1em" loading="lazy"/>

##### Ko končate, mora biti videti takole


#### Ožičenje SDS011
Čepi so oštevilčeni od desne proti levi, zato pri povezovanju pazite, da kabli ležijo na čepih, saj se večina kablov Dupont prilega tudi med čepi.
```bash
SDS011 Pin 1 -> Pin D1 / GPIO5
SDS011 Pin 2 -> Pin D2 / GPIO4
SDS011 Pin 3 -> GND
SDS011 Pin 4 -> unused
SDS011 Pin 5 -> VU (NodeMCU v3) / VIN (NodeMCU v1,v2)
SDS011 Pin 6 -> unused
SDS011 Pin 7 -> unused
```

<br>

💡 Našli boste seznam [senzorjev, ki jih podpira naša vdelana programska oprema](https://github.com/opendata-stuttgart/sensors-software/blob/master/airrohr-firmware/Readme.md)



#### Spajkajte skupaj BME280
<img src="../docs/airrohr/solder-a-bme-280.jpeg" style="width:49%; padding-right: 0.5em" class="items-center" loading="lazy"/>
<img src="../docs/airrohr/solder-bme-280.jpeg" style="width:49%;" loading="lazy"/>

Povežite glavo z nožicami s ploščo BME280. Spajkate ga s hrbtne strani. Razmiki med nožicami so zelo majhni, zato bodite potrpežljivi in previdni.

Trik je v tem, da konico spajkalnika pritisnete na zatič, ga nekoliko segrejete in nato rahlo nanesete spajko.


#### Ožičenje BME280
Stiki so oštevilčeni od leve proti desni.
```bash
VIN -> Pin 3V3 (3.3V)
GND->  GND/G
SDA -> PIN D3
SCL -> Pin D4
```

### Povežite vse skupaj

 ##### NodeMCU in SDS011 povežite skupaj
<img src="../docs/airrohr/tie-air-quality-sensor-together.jpeg" loading="lazy"/>
S kabelsko kravato povežite NodeMCU (ESP8266) in senzor SDS011 tako, da je antena Wifi usmerjena stran od senzorja.

 ##### Priključite gibljivo cev
<img src="../docs/airrohr/sds011-with-tube.jpeg" style="width:49%; padding-right: 0.5em" loading="lazy"/>
<img src="../docs/airrohr/bme280-tied-to-tube.jpeg" style="width:49%;" loading="lazy"/>

* priključite upogljivo cev na senzor SDS011
* Za pritrditev temperaturnega senzorja BME280 na cevko uporabite drugo kabelsko kravato.
* Kabel USB speljite skozi cev. SDS011 namestite tako, da je NodeMCU obrnjen navzgor, ventilator pa navzdol.
 
##### Senzor potisnite v cev
* Dele potisnite v cev, tako da so zataknjeni v notranjosti.
* Kabel USB, upogljiva cev in BME280 morajo gledati iz konca cevi
* Drugo cev potisnite na prvo.

<img src="../docs/airrohr/sds011-jammed-into-tube.jpeg" loading="lazy"/>

##### Zaključna obdelava
* Temperaturni senzor namestite na gibljivo cev, tako da je na robu cevi.
* Odrežite gibljivo cev na koncu cevi
* Po želji: odprte konce cevi lahko prekrijete s fino mrežo. Tako lahko zrak kroži, žuželke pa ostanejo zunaj.

<img src="../docs/airrohr/position-bme280.jpeg" loading="lazy"/>

#### Umestitev
Idealno mesto bi bilo 1,5 do 3,5 metra nad cesto in dobro prezračevano. Vendar tega ni mogoče storiti za vse ljudi, zato se ob registraciji zahtevajo informacije, kot sta višina nad tlemi in položaj do ulice.

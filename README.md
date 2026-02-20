### Výpočet dosahu – 20 dBm TX + 14 dBi anténa

---

### Najprv EIRP (efektívny vyžiarený výkon):

```
EIRP = TX power + Antenna gain
EIRP = 20 dBm + 14 dBi = 34 dBm (2.5W)
```

⚠️ **Toto je mimo EU limit!** Legálne max EIRP na 2.4 GHz je 20 dBm. S 14 dBi anténou by si musel znížiť TX na **6 dBm** aby si bol legálny.

---

### Link budget (čo ťa reálne zaujíma):

| Parameter | Hodnota |
|---|---|
| EIRP (AP) | 34 dBm |
| Citlivosť mobilu (802.11b 1Mbps) | -95 dBm |
| Citlivosť mobilu (802.11n) | -85 dBm |
| Link margin (rezerva) | 10 dB |
| **Max path loss** | **119 dB** |

---

### Odhadovaný dosah podľa prostredia:

| Prostredie | Odhadovaný dosah |
|---|---|
| Voľné priestranstvo (ideál) | 5–8 km |
| Otvorená krajina s prekážkami | 1–2 km |
| Riedky les | 300–600 m |
| **Hustý listnatý les** | **100–300 m** |
| Hustý mokrý les (dážď) | 50–150 m |

---

### Prečo les tak veľmi skracuje dosah:

Listnatý les pridáva **20–40 dB útlmu** podľa hustoty a vlhkosti – mokré listy sú prakticky špongia na 2.4 GHz signál. Každých 10 dB útlmu = dosah sa zmenší na tretinu.

---

### Kritický detail – asymetria spojenia:

AP má výkon 34 dBm EIRP a "ďaleko vidí". Ale **mobil ti odpovie len s ~20 dBm a 0 dBi anténou** = 20 dBm EIRP. To znamená že AP bude mobil počuť ďalej ako mobil AP. Reálny dosah je teda limitovaný **slabším smerom = mobilom**.

Táto asymetria sa čiastočne kompenzuje tým, že sektorová anténa **prijíma aj lepšie** (14 dBi gain platí aj pre príjem).

---

### Praktické odporúčanie:

V hustom lese reálne počítaj s **150–300 metrami** spoľahlivého spojenia pre mobilný telefón. Pre väčší dosah by pomohlo skôr **umiestniť AP vyššie** (nad koruny stromov) ako zvyšovať výkon.
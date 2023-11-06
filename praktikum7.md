# Praktikum 7

Selles praktikumis uurisin kuidas lokaalseid ja võrgukettaid Windowsi ja Linuxi keskkonnas kasutada. 
Haakisin nii võrgukettaid kui ka lokaalseid kettaid enda loodud kataloogidesse. Lisaks kasutasin USB mälupulka Ubuntu virtuaalmasinal.

### Ülesanne 7.1

Andmekandjaid tuleb lähtestada erinevatel põhjustel, sealhulgas konkreetsete operatsioonisüsteemidega ühilduvuse tagamiseks, andmete kustutamiseks, rikutud failisüsteemide parandamiseks, partitsioonistruktuuride ümberkorraldamiseks, pahavara eemaldamiseks ja jõudluse parandamiseks.
Lähtestamine hõlmab seadme ettevalmistamist andmete salvestamiseks, kuid see kustutab kõik olemasolevad andmed, seega tuleks seda teha ettevaatlikult ja teha olulistest asjadest koopia.
### Ülesanne 7.2
Suurte kõvaketaste toetamine: GPT võimaldab suuremaid partitsioone ja kõvakettaruumi, võrreldes MBR-iga.
MBR-l on piirang, mis lubab ainult kuni 2 terabaiti (TB) suuruseid partitsioone, samas kui GPT toetab kõvakettaid, mille suurus ulatub kuni 9,4 zetabaidini (ZB). See teeb GPT-st sobiva valiku suurte andmete hoidmiseks ja haldamiseks.

Parem andmete usaldusväärsus ja turvalisus: GPT sisaldab varukoopiaid partitsioonitabelist, mis paiknevad erinevates kohtades kõvakettal. See muudab selle vastupidavamaks kettavigade ja andmekaotuse suhtes, kuna kui üks tabel on kahjustunud, saab süsteem kasutada varukoopiaid.
Lisaks toetab GPT andmete autentimist ja krüptimist, mis tugevdab andmete turvalisust. MBR ei paku neid lisaturvalisuse funktsioone.

Parandatud tugi mitme operatsioonisüsteemi jaoks: GPT toetab rohkem partitsioone kui MBR, mis muudab selle atraktiivseks mitme operatsioonisüsteemi kasutajatele. MBR võimaldab ainult nelja peamist partitsiooni, samas kui GPT võimaldab tuvastada tuhandeid partitsioone.
See teeb GPT-st hea valiku mitme operatsioonisüsteemi või mitme käivituslaaduri haldamiseks samal kõvakettal

### Ülesanne 7.3 

[TÜ võrguketta haakimine Windowsis](https://kodu.ut.ee/~rhn/hdd.png)


### Ülesanne 7.4

![ül4](https://github.com/RobinHenrik/opsys23/assets/144727763/934aed2e-da26-417f-9b7a-e361c760d90f)

### Ülesanne 7.5

-o ro: See parameeter tähendab "read-only". Partisioon haagiti ainult lugemisrežiimis, sellele partisioonile ei saa andmeid kirjutada.

-t auto: See parameeter määrab failisüsteemi tüübi, kuid kasutab automaatset tuvastamist, mis võimaldab süsteemil ise kindlaks teha partitsiooni failisüsteemi tüübi.


### Ülesanne 7.6

Ubuntu asendas auto-parameetri parameetriga fuseblk

### Ülesanne 7.7

![ül7](https://github.com/RobinHenrik/opsys23/assets/144727763/91b41c1d-34d1-4f37-bcab-e5f2c0c115e1)


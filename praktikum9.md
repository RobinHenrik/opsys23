|  Küsimus |  Linux |  Windows |  Linuxis kasutatud käsklus	 |  Windowsis kasutatud tööriist |
|---|---|---|---|---|
| 1. Mitu protsessi kokku arvutis käib? |   |  120 |   |  Tegumihaldur -> Jõudlus |
| 2. Milline on kõige esimesena käivitatud protsess? |   | smss.exe  |   | process explorer -> start time  |
| 3. Milliste kasutajate protsesse arvutis käib? |   | DWM-1, LOCAL SERVICE, NETWORK SERVICE, Robin, SYSTEM, UMFD-0, UMFD-1  |   | Tegumihaldur -> Üksikasjad -> Kasutajanimi |
|4. Kui kaua on arvuti järjest töötanud (up time)? (Alternatiivselt võib vastata ka, millal (kuupäev ja kellaaeg) arvuti viimati käima pandi.)  |   | 1h55min  |   | Tegumihaldur -> Jõudlus -> CPU -> Tööaeg  |
|5. Milline protsess käivitati kõige hiljem (viimasena)? |   | svchost.exe  |   |  process explorer -> start time |
|6. Milline on kõige rohkem protsessoriaega võttev protsess?  |   | svchost.exe  |   |  process explorer -> CPU time |
|7. Milline on kõige rohkem virtuaalmälu (aadressiruumi, commit, Virtual Size) võttev protsess?  |   | msedge.exe  |   | process explorer -> virtual size  |
| 8. Milline on kõige rohkem füüsilist mälu (working set) võttev protsess? |   | SearchHost.exe |   | process explorer -> working set  |
|9. Kui palju füüsilisest mälust (Physical Memory) on vaba?  |   |  1.8GB |   | Tegumihaldur -> jõudlus -> mälu |
| 10. Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt? |   | 33,38GB;53%  |   | Kettahaldus  |
|11. Milline on kõige suurem kõvakettal olev fail ja kõige suurem alamkaust?  |   | suurim fail: pagefile.sys     suurim alamkaust: C:\Windows  |   |  WinDirStat |
|12. Uurige, millisele CPU alamtegevusele us, sy, id, wa, st jne kulub enim protsessori aega ja mitu protsenti kulub kummagi käsu korral.  |   | -  |   | -  |
|13.1. Milline protsess kõige rohkem salvestusseadmele kirjutab?  |  - | msedge.exe  | -  | resource monitor -> disk -> write (B/sec)   |
|13.2. Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab?  |  - |  C:\ $LogFile (NTFS Volume Log) |  - |  resource monitor -> disk -> file |
| 13.3. Milline protsess kõige rohkem salvestusseadmelt loeb? |  - | msedge.exe  | -  | resource monitor -> disk -> write (B/sec)   |
| 13.4 Millisest failist eelmise küsimuse protsess kõige rohkem loeb? | -  | C:\Windows\Fonts\malgun.ttf  |  - | resource monitor -> disk -> file  |
|14. Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga?  |   |  msedge.exe |   |  resource monitor -> network -> total(B/sec) |
|15. Sõber kurdab, et tema arvuti on oluliselt aeglasemaks muutunud. Milliseid konkreetseid programme või käsureakäske kasutad põhjustaja tuvastamiseks. Mõlemal juhul kirjuta, mida konkreetselt jälgid (nt mis aken, veerud, numbrid jne).  |   |   |   |   |



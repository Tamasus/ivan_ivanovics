- Az imperatív nyelvekkel a vezérlés menetét manipuláljuk
	- Tedd ezt ezzel, utána ezt stb
	- FORTRAN, C, Pascal, Basic
- Ezért az imperatív programozási paradigma jól megfelel a Neumann gépnek
  *Imperatív paradigma: teljesen specifikált lépések teljesen specifikált adatokon*
# Hiba és eseménykezelés a Neumann gépen
- Az eseményekhez kezelő (handler) instrukciófolyam tartozik 
- Az esemény bekövetkezésekor a vezérlés menete megváltozik "ugorjon a kezelőre" (a CPU állapot a kontextus "lementése" után)
- A kezelés után (ha lehetséges) a vezérlés menete térjen vissza a "normál" instrukció folyamra folytatódjon a processz futása (az állapot a kontextus vissza-emelése után persze)
- Összegezve: **a hiba és eseménykezelés a vezérlés menetének manipulálásával történik**

# Egy más elvű gép: adatfolyam gép
A Daraflow Machine (kontrasztként) ideája:
- Szeparált processzorok minden operációra (operáció lehet: aritmetikai, logikai, függvényhívás stb.)
- Az operációk (processzorok) várnak míg operandusok értéke előáll utána adják eredményüket
- A processzorok (operációk) függetlenek. A legkorábbi lehetséges pillanatban adják az eredményüket
- Az operációk végrehajtásának sorrendje az adatfolyamból folytatódik.
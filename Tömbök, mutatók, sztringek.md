# A C típusszerkezete
![[Pasted image 20251101145352.png]]
# Elemi / leszármazott típusok
- Az elsődleges(elemi) típusú változók egyetlen érték tárolására alkalmasak
- A leszármaztatott típusok az elsődleges típusok kiterjesztéseként értelmezhetők
- Tömb: azonos típusú adatok fix méretű sorozata. A tömbelemek típusas a void és az enum típus kivételével tetszőleges lehet 
- Pointer (mutató): speciális típus, ami egy változó memóriacímét képes tárolni
# Tömb adatszerkezet
- Létrehozása: típus tömbnév [*méret*];
- Típus: char, int, float, double, pointer, struct, union
- Méret:
	- Tetszőleges egésze kiértékelődő kifejezés
	- Egész konstans
![[Pasted image 20251101150026.png]]
- A tömb méretére szükség lesz a tömb adatainak eléréséhez, ezért érdemes nevesíteni
![[Pasted image 20251101154845.png]]
# Tömb tárolása
- A tömb létrehozásakor a fordító a memóriában egymás melett lefoglal "méret" darab megadott típusú érték tárolására elegendő memóriaterületet. Például 10 elemű char tömb esetén 10 darab 1 byte-os memóriaterületet
- A tömb által lefoglalt memóriaterület mérete byte ban 
  **sizeof(tömbnév)**
- A tömb mérete (elemek száma):
  **sizeof(tömbnév) / sizeof(tömbelemek típusa)**
- A tömb mérete futási időben NEM változtathazó meg (fix méretű tároló)
# Tömbelemek elérése
- A tömb nevével azonosított változó tárolja a tömb első elemének memóriacímét
- A kezdőcímtől kiindulva az elemek sorozatszámozva érhetők el az indexelés operátorral
- Érvényes tömbindexek:0 ... méret -1
- Figyelem! A C szabvány nem rögzíti, hogy mi történjen a tömbindextúllépésekor. A fordító implementációjától függ, hogy ilyen esetben futási időben hibaüzenetet vagy "memóriaszemetet" kapunk eredményül.
![[Pasted image 20251102150322.png]]
# Tömb inicializálása
- Inicializációs lisitával:
![[Pasted image 20251102150410.png]]
- Figyelem! Inicializációs lista használata mellett a tömb méretét vagy simbolikus konstansal kell megadni, vagy a szögletes zárójelek közé írt egész kifejezéssel
- Ha az inicializáció lista elemszáma nagyobb mint a tömb mérete akkor fordítási időben hibát kapunk
- Ha az inicializáció lista elemszáma kissebb mint a tömb mérete a nem inicializált elemek a típusnak megfelelő "null" értékkel inicializálódnak.
- Ezek a hibák elkerülhetők ha iniciaéizációs lista használatakor nem rögzítjük a méretet (a fordító a lista elemszáma alapján kiszámítja)
![[Pasted image 20251102151447.png]]
# Tömb bejárása
- A tömb bejárásához for ciklust szokás használni ahol a ciklusváltozó használható a tömbelemek indexeléséhez
- A vezérlőfeltételben a tömb méretét szokás megadni
![[Pasted image 20251102151635.png]]
# Tömbök használata
- A C nyelvben a tömb adatszerkezetre vonatkozóan indexelés operátoron kívül nincs más művelet definiálva.
  Következmény: a tömb csak elemenként kezelhető
- A tömbökre vonatkozóan a szükséges műveleteket függvényben tudjuk definiálni
- Tömb lehet függvény argumentuma de visszatérési értéke nem
- Ökölszabály: ne használjunk tömböt ha nincs rá szükség. Akkor használjunk tömb adatszerkezetet, ha
	- emlékezni kell az összes elemre (például átlagnál kissebb elemek kiválasztása), vagy
	- a tömbelemeket nem a megadás sorrendjében kell feldolgozni
# Pointer típus
**Mutató (pointer):** olyan speciális változó ami egy másik változó címét tárolja.
A 'p' mutató egy pointer változó tehát van aktuális értéke és van címe. A pointer értéke az általa mutatott változó memória címe. A pointer címe az a memóriacím, ahol a pointer változó memóriacíme. A pointer címeaz a memóriacím ahol a pointer változó elhelyezkedik a memóriában.
![[Pasted image 20251102152536.png]]
![[Pasted image 20251102152544.png]]
![[Pasted image 20251102152726.png]]
# Pointer arimetika
- Pointereken elvégezhető műveletek:
	- Mutató léptetése a következő memóriacímre:
	  ![[Pasted image 20251102152855.png]]
	- Mutató léptetése az előző memóriacímre:
	  ![[Pasted image 20251102152928.png]]
	- Két azonos típusú mutató különbsége (a memóriában közöttük elhelyezkedő megegyező típusú elemek száma)
	  ![[Pasted image 20251102153046.png]]
	- 
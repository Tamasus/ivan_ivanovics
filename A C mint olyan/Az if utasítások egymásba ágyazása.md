![[Pasted image 20251004130306.png]]
Figyelem! A C nyelvben a behúzásnak nincs szintaktikai szerepe. a fordító minden **if** utasításhoz a hozzá legközelebb lévő első **else** utasítást rendeli
# 1.megoldás
Minden **if** utasításhoz megadjuk az **else** párját(üres utasítással ha szükséges)
![[Pasted image 20251004135635.png]]
# 2.megoldás
Jelöljük az **if** és az **else** ágak utasblokkjait ({} zárójelek között adjuk meg)
![[Pasted image 20251004135759.png]]
# Többirányú elágazás
- Kiértékelődik az első kifejezés
- Ha igaz, a hozzákapcsolt utasítás végrehajtódik és a program at if utáni utasításal folytatódik
- Ha hamis akkor kiértékelődik a következő kifejezés
- Ha egyik feltétel kifejezés sem teljesül akkor az utolsó else utasítás kerül végrehajtásra
- Az utolsó else utasítás elhagyható ha nincs szükség alapértelmezés szerinti tevékenység végrehajtására
- Az elágazások lehetséges száma implementáció függő
![[Pasted image 20251004140314.png]]
# Egymásba ágyazott if / többirányú elágazás
- Az if utasítások egymásba ágyazása nehezen olvasható kódot eredményez
![[Pasted image 20251004140428.png]]
- Érdemes átírni összetett feltételre vagy if-else if-else utasításra
![[Pasted image 20251004140548.png]]
# A switch utasítás
Többirányú programozást tesz lehetővé olyan esetekben amikor egy egész kifejezés értékét több konstans értékkel kell összehasonlítani.
![[Pasted image 20251004140748.png]]
- A megadható esetek száma implementációfüggő
- MInden konstans kifejezésének egyedi értékkel kell rendelkeznie
- A **default** megadása nem kötelező egyébként bárhol elhelyezkedhet a **switch** utasításon belül
- A **case** és a **default** a címkézett utasítások közé tartozik 
- Több esethez hozzárendelhető ugyanaz a program rész
![[Pasted image 20251004141139.png]]
# A switch utasítás kiértékelése
1. Kiértékelődik a **switch** utáni kifejezés
2. A vezérlés átadódik arra a **case** címekre amelyben a konstans kifejezés értéke megegyezik a kiértékelt kifejezés értékével. A program futása ettől a ponttól folytatódik azaz ettől a ponttól kezdve a megadott utasítások sorban végrehajtásra kerülnek!
3. Ha egyik **case** konstans sem egyezik meg a kifejezés értékével a program futása a **default** címkével megjelölt utasítással folytatódik
4. Ha nincs **default** címke a vezérlés a **switch** blokkját záró } zárójel utáni utasításra adódik![[Pasted image 20251004141803.png]]
Általában egy adott esethez tartozó programréslet végrehajtása után ki szeretnénk lépni a **switch** utasításból ( nem folytatni ettől a ponttól kezdve az utasítások végrehajtását)
***Alkalmazható vezérlésátadó utasítások:*
- **break:** hatására a vezérlés a **switch** {} után következő utasításra kerül
- **return:** a vezérlés a hívó függvényhez kerül ha a main függvnényényben használjuk a program befejezi futását ( a vezérlés az operációs rendszernek adódik vissza)
![[Pasted image 20251004142954.png]]

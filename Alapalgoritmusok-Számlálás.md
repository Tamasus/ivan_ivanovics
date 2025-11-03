- A feladat egy tetszőleges típusú elemeket tartalmazó sorozat összes vagy azon belüll egy T tulajdonsággal rendelkező elemeinek megszámlálása
- **Megoldási terv:**
Egy számláló változót deklarálunk és beállítjuk a kezdőértéket 0-ra. Végignézzük a sorozat összes elemét és:
- teljes leszámlálás esetén a számláló változóhoz hozzáadunk egyet
- feltételes számlálás esetén akkor adunk hozzá a számláló változóhoz egyet ha az adott elemre teljesül a feltétel (azaz T tulajdonsággal rendelkezik)
![[Pasted image 20251012104738.png]]
![[Pasted image 20251012104753.png]]
# Összegzés
- A feladat egy számsorozat összeges elemének vagy azon belül egy T tulajdonsággal rendelkező elemek összegének kiszámítása.
- **Megoldási terv:**
Létrehozunk egy gyűjtő változóz és beálítjuk a kezdőértéket 0-ra. Végignézzük a sorozat elemeit és:
	- minden elemet egyesével hozzáadunk a gyűjtő változóhoz; vagy
	- feltételes összegzés esetén akkor adjuk hozzá a gyűjtó válozóhoz a vizsgált elem értékét ha az adott elemre teljesül a feltétel (azaz T tulajdonsággal rendelkezik)
![[Pasted image 20251012105208.png]]
![[Pasted image 20251012105220.png]]

# Számlálás-gyakorlati példák
- Intervallumba első elemek megszámolása. Pl.: adottak a hallgatók ZH pontszámai. Hány dolgozat lett ötös a (40-50 pont között)
- Prímszám vizsgálat: egy szám valódi osztóinak megszámolása. Ha az osztók száma 0 akkor a szám prímszám
- Gyakoriság / realatív gyakoriság számítás PL.: fej vagy írás játékot szimulálunk. Véletlenszerűen állítunk elő adott hosszúságú sorozatot 0-ákból és 1-esekből. Hányszor volt fej(0) / írás (1) a sorozatban? Mennyi az egyes esetek relatív gyakorisága

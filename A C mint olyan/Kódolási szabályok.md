Forrás:Mats Henricson, Etik nyquist: C kódolási szabvány
- Minden forrásfájl elején szerepelnie kell az adott fájlra vonatkozó általános információkat tartalmazó megjegyzés blokknak
![[Pasted image 20251004153613.png]]
- A programon belül a megjegyzések nyelve azonos legyen
# Forrásfájlok
- A C forrásfájlok kiterjesztése mindig ".c" a header fájlok kiterjesztése mindig ".h"
- Az összetartozó C és header fájlok neve a kiterjesztéstől eltekintve azonos
- Egy forrásfájlba csak a logikailag szorosan összetartozó függvények kerülhetnek 
- A forrásfájlok mérete nem lépheti túl az 500 sort
- Header fájlokon kívül más fájl include-olása tilos. csak a szükséges header fájlokat include-oljuk. MInden header file-ban léteznie kell egy többszörös include-olgatást gátló mechanizmusnak
# Azonosítók
- **Általános elv:** a program olvashatóságát áttekinthetőségét biztosítani kell. Az azonosító név mindig utaljon egyértelműen az általa azonosított elem funkciójára
- A makrók (#define) neve mindig csupa nagybetűkből álljon
- A több szóból álló azonosító neveket egybe kell írni de a szóhatárokat nagybetűvel kell jelölni (myVariable). A makrók nevében a szóhatárokat a _  karakterrel kell jelölni
- Ne használjunk olyan neveket amelyek csak a kis- és nagybetűs írásmódban vagy az aláhúzás meglétében illetve a hiányában térnek el . Bár a C azonosítók tetszőleges hosszúságúak lehetnek a fordító csak az első 31 karaktert veszi figyelembe
# Függvények
- Függvény definíciójában alkalmazandó megjegyzés
![[Pasted image 20251004160608.png]]
- Egy függvény hossza nem haladhatja meg a 100-150 sort.
- Törekedjünk minnél kevesebb fv argumentum használatára
- A függvény deklaráció megadásánál az argumentumok típusai mellett mindig adjuk meg azok nevét is 
- Mindig adjuk meg a függvény visszatérési értékének típusát
- Tömböket és (nagy méretű) struktúrákat mindig mutatón keresztül adjunk át
- Tömböket és nagy méretű struktúrákat mindig mutatón keresztül adjuk vissza
# Utasítítások
- A változókat a lehető legkissebb hatáskörrel deklaráljuk
- A feltételes blokkot / ciklusmagot nyitó kapcsos zárójelet { az utasítással egy oszlopba de az azt közvetlenül követő sorba kell írni. A blokkot záró kapcsos árójel szintén ebbe az oszlopba kell hogykerüljön. A blokkban szereplő összes utasítás egy bekezdéssel beljebb kerül.
- A switch kifejezésben mindig legyen default ág a váratlan esetek kezelésére
- Ha egy kifejezés kiértékelési sorrendje nem triviális akkor használjunk zárójeleket még abban az esetben is ha a fordító szempontjából fölöslegesek
# Helyközök
- Mindig helyközt kell tenni:
	- Az unáris (egy operandusú) operátorok kivételével minden operátor elé és mögé
	- A vessző után
	- A pontos vessző után
	- Az if utasítás és a nyitó zárójel közé
- Sohasem szabad helyközt tenni
	- Vessző és pontosvessző elé
	- Az unáris operátorok és az operandusok közé
	- A ciklus utasítás vagy a függvény neve és a nyitó zárójel közé
	- A tömb neve és a nyitó szögletes zárójel közé

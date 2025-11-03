# Programvezérlés
- A C program lefordítása után előáll a program futtatható kódja (gépi kód)
- A futtatható C program végrehajtása a main függvény első utasításával indul, majd sorban hajtódik végre a függvény többi utasítása
- A többi függvény definíciójában szereplő utasítások csak az adott függvény meghívása esetén hajtódnak végre
- A függvényhívás kitérőt jelent a végrehajtási folyamatban. Ahelyett, hogy a következő utasításra kerülne a  vezérlés átkerül a meghívott függvény első sorára. Lefutnak a függvényen belül álló utasítások majd visszakerül a vezérlés a hívás helyére és onnan folytatódik tovább a program végrehajtása
- A futtató környezet programszámlálója nyílvántartja hogy hol tart a program végrehajtása. Valahányszor befejeződik egy függvény a program vezérlése mindig pontosan oda tér vissza ahonnan a függvényt meghívták. Ha pedig eléri a program végét, akkor a program befejezi működését.
- A program nyomonkövetéséhez a kódot ne lefelé olvassuk hanem a végrehajtás folyamatának megfelelően
- A fejlesztőeszköz nyomonkövető (debugger) funkciója segít a végrehajtás folyamatának követésében.
![[Pasted image 20251101104207.png]]
# Függvényhívások beágyazása
[[Függvények]]
- Függvények is hívhatnak függvényeket
- Ha nem használunk függvény deklaráviókat, számít a függvény definíciók sorrendje!
![[Pasted image 20251101104408.png]]
- Függvény argumentuma lehet függvényhívás aminek az értéke helyettesítődik be.
![[Pasted image 20251101104457.png]]
- DE a void nem érvényes függvény érték ezért void függvény hívás kifejezés nem lehet függnény argumentuma.
# Programtervezés
- A programtervezés lényege a probléma részfeladatokra bontása és lépésenkénti megoldása 
- A három vezérlési szerkezet(szekvencia, szelekció, ciklus) felhasználásával egyszerű utasításokból összetett utasítások, összetett utasításokból program egységek (blokkok, függvények) és program egységekből egy program modul épül fel
- A feladatot megoldó algoritmus megadható egyetlen main függvényben (spagetti-kód). DE a feladat egyetlen egységként kezelése csak kissebb problémák esetén eredményez átadható programot
# Programtervezési alapelvek
- Struktúrált programozás alaptétele:
  Bármely algoritmust leírhatunk három alapstruktúra (szekvencia, iteráció, szelekció) véges számú kombinációjával
- Procedúrális programozás: a részfeladatok végrehajtására eljárásokat írunk:
	- Top-down programtervezés: A megoldandó feladatból indulunk ki. Lépésenmként bontjuk részfeladatokra, amíg végrehajtható lépéshez jutunk
	- Bottm-down programtervezés: Először a legelemibb részeket és azok megoldó algoritmusát készítjük el, majd ezek felhasználásával oldjuk meg az összetett feladatokat.
- Modularitás: 
  A komplex feladatokat több , egymástól függetlenül elkészíthető/ tesztelhető részre (modulra) bontjuk. A teljes program az összekapcsolt modulokból áll
# Moduláris programozás
- Az egy modulban megírt program monolitikus
- Nagy programok fejlesztésekor a feladat bonyolultsága a csapatmunka támogatása szükséggessé teszi a probléma részekre (modulokra) bontását
- Minden modul önálló, névvel rendelkező,önnmagában értelmezhető fordítási egység. Önállóan tervezhető kódolható tesztelhető.
- Minden midulnál meg kell határozni a bemenő, kimenő paramétereket és azokat a függvényeket amelyeken keresztül a többi modullal kapcsolatot tart
# Top-down programtervezés
- A problémamegoldás során a lépésenkénti finomítás elvét alkalmazzuk, azaz afeladat megoldását először átfogóan végezzük el. Ezután a feladatot részekre bontjuk, és a továbbiakban ezeket a részfeladatokat oldjuk meg (funkcionális dekompozíció)
- Az egyes részeket egymástól függetlenül (de illesztve egymáshoz) írhatjuk, tesztelhetjük, javíthatjuk.
- Az egyes részeket addig kell továbbítani, amíg eljutunk az elemi utasítások szintjére.
# LNKO algoritmus
Az Euklédeszi LNKO algoritmus a legrégebbi nem triviális algoritmus amit ma is használunk
![[Pasted image 20251101145006.png]]

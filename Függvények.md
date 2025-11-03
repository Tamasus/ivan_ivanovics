### Függvények fogalma
Függvémy: a program olyan névvel (azonosítóval) ellátott egysége (alapprogramja) amely a program más részeiből annyiszor meghívható, ahányszor szükség van a függvényben definiált tevékenység sorozata

### Procedűrális programozás:
- A program sok kisméretű adott (jól körülhatárolt) feladatot végrehajtó, jól kézben tartható függvényekből épül fel
- A gyakran használt függvények kódját könyvtárakba rendezhetjük amelyekből a szerkesztőprogram a hivatkozott függvényt beépíti a programunkba
# Függvény dokumentációja
A függvények olyan kis programrészek amelyek egy jól körülhatárolt részfeladatot hajtanak végre. A forráskódban a függvények előtt megjegyzés (comment) formályában meg kell adni:
- milyen feladatot hajt végre
- milyen bemenetet vár, a bemeneti tartomány leírása (pl. a négyzetgyököt vonó függvény nem kaphat negatív számot paraméterenként)
- milyen kimenetet állít elő a futása során
# Függvények definíciója
![[Pasted image 20251030111608.png]]
- Saját függvényeinek mindig definiálni kell 
- Egy függvény definició csak egyszer szerepelhet a programban
- A programon belül bárhol elhelyezkedhet, kivéve egy másik függvény törzsében.
# Függvény fejléce
- ANSI C-ben: ha a függvény definícióban nem adtuk meg a visszaértési típust, **alapértelmezés szerint int** volt. NE használjuk ezt az inplicit feltételezést! Mindig adjuk meg a függvény visszatérési típusát
- A függvény neve programszinten ismert azonosító (a program összes forrásfálját tekintve egyedinek kell lennie). Érvényes, kisbetűs C azonosító és em lehet foglalt kulcsszó. A szóösszetételnél camelCase írásmódot használunk
- A függvény neve után kötelező szintaktikai elem a (). A zárójelben a paraméterlista szerepel ami lehet üres
- A fejléc megadása után {} között következik a függvény törzse
# Függvény váltózói
- A függvény törzsében definiált változók a függvény saját lokális változói futási időben a függvénybe belépéskor jönnek létre
- Csak a függvényen belül láthatók -> a láthatóságuk (scope) csak a függvényen belülre terjed ki
- Mivel minden függvény csak a saját lokális változóit látja, nincs névütközés
- A függvény futásának végén a lokális változók megszűnnek (törlődnek a memóriából) -> a változó élettartama (lifetime, storage duration) csak a függvény végrehajtási idejére terjed ki
![[Pasted image 20251030113018.png]]
# Függvény definíció
- A függvénynek neve van, amivel a programban több helyen is hivtkozhatunk rá (hívhatjuk) azaz többször elvégezhetjük ugyan azt a részfeladatot (különböző argumentumokon)
- A függvény olyan, mint egy program: van bemenete és kimenete is. A függvény bemenete az argumentumlista (a paraméterek aktuális értékei), kimenete a visszatérési érték
- A függvény visszatérési értékét (függvényértén) a return utasítással adjuk meg. Ezzel eggyúttal vissza is térünk a függvényhívás helyére! Tehát az utána következő utasítások nem hajtódnak végre 
# Függvény visszatérési értéke és típsusa
- A függvény visszatérési típusa a függvény által előállított konstans érték (függvény érték) típusa
- A függvény visszatérési típusa tetszőleges típus lehet kivéve tömb
- Ahhoz hogy egy függvény visszaadjon egy értéket, a függvény törzsében ki kell adni a *return* utasítást. **A függvény által visszaadott érték a return utasításban szereplő kifejezés értéke.**
- A return utasítás feldolgozásakor (a kifejezés kiértékelésekor) a fordító, ha szükséges, implicit típuskonverziót végez: kiértékelt kifejezés típusát a visszatérési típusra konvertálja
![[Pasted image 20251030120818.png]]
# A main függvény visszatérési értéke és típusa
- A C programban kötelezően szerepel egy main függvény (ez a program belépési pontja)
- A main függvény visszatérési típusa int
- A függvény visszatérési értéke pozitív egész szám vagy 0, aminek hibajelző szerepe van. A 0 azt jelenti hogy hiba nélkül lefutott a program.
![[Pasted image 20251030121209.png]]
# A return utasítás 
- Vezérlésátadó utasítás
- A return utasítást egy függvény törzsében adhatjuk meg. Ez a függvény végrehajtásának a végét jelenti, azaz az utána következő utasítások nem hajtódnak végre 
- Működése: 
  A returnutasítás utáni kifejezés kiértékelődik, a függvény visszatér a hívás helyére és visszadaja a kifejezés értékét
- Egy függvényben több return utasítás is szerepelhet.
- C specifikumok
	- A return utáni kifejezés bármilyen típusú lehet, kivéve tömb
	- A return utasítás maximuim egy értéket állít elő
- Ha a return utasítás után nem áll kifejezés akkor a függvény nem ad vissza értéket. Ilyenkor a függvény visszatérési típusa **void** (üres)
- Ha egy függvényben nincs return utasítás, akkor a függvény végrehajtása az utolsó utasítással ér véget. A függvénynek így nem lesz visszatérítési értéke a visszatérési típusnál a **void** jelölést használjuk
- Konvencionálisan minden függvényben van legalább egy return utasítás
![[Pasted image 20251030122323.png]]
# A függvény paraméterei
- A függvény bizonyos belső változóinak a függvény hívás során akarunk értéket adni ezeket a változókat a függvény paraméterlistájában adjuk meg
- A függvény definícióban a (formális) **paraméterlista a paraméterek típusát és a nevét tartalmazza** (ezeket space választja el). A listában szereplő paramétereket vessző választja el
- A paraméterek **tetszőleges típusúak** lehetnek, és a függvényen belül mint a függvény lokális változói használhatók de a függvényen kívül nem érhetők el
- A függvény paraméterlista egy változó deklarációs lista. Az itt szereplő változók a függvényen kívülről inicializált lokális változói. Ezeket nem kell ujradeklarálnia függvény törzsében!
![[Pasted image 20251030123000.png]]
- Igyekezzünk többször felhasználható (általános) függvényeket írni!
- Ez a függvény nem használható általánosan
![[Pasted image 20251030123126.png]]
- Ha a függvény nem vár paramétert akkor a paraméterlista vagy üres vagy a void kifejezést tartalmazza 
- Ilyenkor a függvény mindig ugyanúgy fut le kimenete nem függ a bemenettől
![[Pasted image 20251030123259.png]]
- A függvény hivatkozásában (híváskor) megadott aktuális paraméterlistát **argumentumlistának** nevezzük
- A függvény paraméterlistája és argumentumlistája között típuseggyezés történik, ezért a paraméterek megadási sorrendje rögzített. A fordító ellenőrzi a paraméterek számának típusának egyezését (a nevüket nem!)
![[Pasted image 20251030123554.png]]
# A függvény deklarációja
- A függvény deklarációja a függvény visszatérési típusát, nevét és a paramétereke típúsát tartalmazza.
  Pl.: double add( double, int)
- Ha a függvény deklarációja a paraméterek nevét is tartalmazza akkor ezt a függvény prototípusának nevezzük. Ezt javasolt használni!
  Pl.: double add(double a, int b)
- Ezt mindig a függvény hívás előtt kell elhelyezni a programban (nem hiba ha többször szerepel)
- Ha egy függvény definíciója megelőzi a hívás helyét akkor nincs szükség a prototípus külön megadására
# Függvény deklarációk és header állományok
- A függvény deklarációjának a hívás előtt kell szerepelnie a programban azért hogy a fordító a hívás helyén már ismerje a függvény azonosító "jelentését" és fordítási időben el tudja végezni a formális és az aktuális paraméterlista közötti egyezést
- A header állományok a függvény könyvtárakban definiált függvények deklarációit (és konstans makrókat) tartalmaznak. Ha külső ( nem adott programban definiált) függvényt akarunk hívni a deklarációját tartalmazó header állományt indukálni kell a forrásfájl elején.
- A header állományok a függvény könyvtárakban definiált függvények deklarációit (és konstans makrókat) tartalmaznak. Ha külső ( nem adott programban definiált) függvényt akarunk hívni a deklarációját tartalmazó header állományt indukálni kell a forrásfájl elején.
![[Pasted image 20251030141324.png]]
![[Pasted image 20251030141313.png]]
# Függvény hívása
- A függvény hívás olyan kifejezés amely átadja a vezérlést és az argumentumokat a hívott függvénynek.
  Pl.: 
  double result= add(2,3.14);
  print_multiplication_table();
- Ha a függvény prototípusban a paraméterlista helyén a void kulcszó áll (vagy üres) akkor a függvény argumentumlistája üres de híváskor a zárójeleket így is ki kell tenni
- Függvény híváskor az argumentumok sorrendben, érték szerint adódnak át a hívott függvényeknek. Azaz nem az argumentum adódik át hanem az értéke. A paraméter a hívott függvény saját változója, értéke az argumentum aktuális értékének másolata lesz
![[Pasted image 20251030142055.png]]
# Függvényhívás hatása
- A függvényhívás kifejezés kiértékelése azt jelenti, hogy a függvény lefut és a hívás helyén lévő kifejezésbe a visszatérési értéke behelyettesíthető. Ez a függvényhívás főhatása (a függvény értékének kiszámítása)
![[Pasted image 20251030150326.png]]
- A függvényhívás mellékhatásának azt nevezzük ha a függvény a program állapotában változást okoz. Mellékhatás például egy nem lokális változó módosítása vagy egy I/O művelet. A void visszatérési értékű függvénynek nincs értelme ha nincs mellékhatása (ez a célja).
# Command-querv sepatration elv
- Kétféle függvény létezik. A parancsfüggvényeket azért használjuk, hogy mellékhatásuk legyen. a query típusú függvény egy kérdésre válaszol, kiszámol valamit és az eredményt visszaadja
- Ha a függvény értéke csak a paraméterektől függ azonos bemenete mindig ugyanaz kell legyen az eredmény. Ha van mellékhatása is, ez nem biztos hogy teljesül!
- Igyekezzünk olyan függvényeket írni amelyeknek csak főhatása vagy csak mellékhatása van (ne keverjük a kettőt)!
![[Pasted image 20251030151111.png]]
![[Pasted image 20251030151119.png]]
![[Pasted image 20251030151131.png]]
# Miért írunk függvényeket?
- Kód újrahasznosítás: A függvényben definiált utasítássorozat többször elvégezhető
- Az ismétlődő programrészek függvénybe írásával rövidebb lesz a program
- Olvashatóság és karbantarthatóság javítása:
  A függvények képesek leírni egy feladat megoldása során meghatározott részproblémákat azaz egy összetett művelet (utasításcsoport) egyetlen függvényhívás utasítás mögé rejthető
- Információrejtés:
  A függvény saját hatáskört definiál; a változói kívülről nem érhetők el
- Memóriagazdálkodás:
  A függvény után lokális változók által foglalt memóriaterületek automatikusan felszabadításra kerülnek

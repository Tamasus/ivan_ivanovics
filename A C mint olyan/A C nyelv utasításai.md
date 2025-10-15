# Kifejezés utasítás
Tetszőleges kifejezés utasítás lesz ha utána ;-t teszünk. Egy kifejezés utasítás végrehajtása a kifejezés kiértékelését jelenti.
![[Pasted image 20251001172711.png]]
# Üres utasítás
Akkor van rá szükség amikor logikailag nem kívánunk semmilyen tevékenységet végrehajtani vagy az adott kódrészt még nem dolgoztuk ki de a szintaktikai szabályok szerint a program adott pontján utasytásnak kell szerepelnie
![[Pasted image 20251004122512.png]]
# Összetett utasítás
- A logikailag összetartozó deklarációk és utasítások egyetlen összetett utasításba (blokkba) csoportosítására szolgál. Mindenhol használható ahol szintaktikaillag utasítás megadása szükséges
- Általános formálya:
![[Pasted image 20251004122718.png]]
- **Fontos: nincs utána pontos vessző**
### Mikor használjuk?
- Amikor több logikailag összefüggő utasítást egyetlen utasításként kell kezelni
- Függvények törzseként
- Szelekciós blokk és ciklus utasítástörzs megadására
- Definíciók és deklarációk érvényességének lokalizálására.
# Szelekciós utasítások
![[Pasted image 20251004123017.png]]
- **Az if utasítás:**
	- Valamely utasítás végrehajtását egy feltétel kifejezés értékétől teszi függővé
- Az if utasításai csak akkor hajtódnak végre ha a feltétel igaz 
- A feltétel kifejezés egészre konvertálandó logikai kifejezés
- A feltétel kifejezés igaz ha értéke nem nulla. A kifejezés akkor hamis ha értéke nulla
![[Pasted image 20251004123250.png]]
![[Pasted image 20251004123311.png]]
![[Pasted image 20251004123327.png]]
# Szelekciós feltétel
- A C nyelvben nincs logikai adattípus 
- A szelekciós feltétel olyan kifejezés amelynek értéke egészre konvertálható (*char, int, float , double, enum*)
- A szelekciós feltétel hamis ha a kifejezés 0-ra értékelődik ki, egyébként igaz
- Feltétel kifejezésekben általában az összehansonlító operátorokat használjuk
- Mivel a szelekciós feltétel kifejezésnek egészre konvertálhatónak kell lennie ezért írható ilyen feltétel
![[Pasted image 20251004123705.png]]
# Feltételek láncolása
- A szelekciós feltételek láncolhatók de mivel nincs logikai típus a feltételek 0ra vagy 1 re értékelődnek ki 
- Próbáljuk ki a különböző "a" értékre! Mi az eredmény és miért?
![[Pasted image 20251004123842.png]]
- Hogyan írjuk át hogy az elvárt eredményt adja?
![[Pasted image 20251004124001.png]]
# Logikai tagadás / olvashatóság
 - A logikai tagadás használata nehezen olvashatóvá teszi a programot
 - A szelekciós feltételben a logikai tagadás elkerülehtő ha felcsréljük az if és az else ágat
 - **Például:**
	 - "Ha még nem vagy 17 éves nem lehet jogsid"
![[Pasted image 20251004124932.png]]
- A szelekciós feltételben a logikai tagadás úgy is kiküszöbölhető ha a logikai feltétel ellentétét fogalmazzuk meg
![[Pasted image 20251004125036.png]]
- **Például**:
	- " Ha még nem vagy 17 éves nem lehet jogosítványod"
![[Pasted image 20251004125136.png]]
# Összetett szelekciós feltétel 
- Bonyolultabb feltételek írásához a feltételek összekapcsolásáhozszükség van logikai operátorokra: *&& ,|| ,!*
![[Pasted image 20251004125350.png]]
- Az összetett logikai kifejezések kiértékeléséhez használt igazság tábla:
![[Pasted image 20251004125436.png]]
# Összetett feltétel szétbontása
- Az összetett logikai feltételek támogatása egyszerűbben megadható a De Morgan azonosságok alkalmazásával
![[Pasted image 20251004125541.png]]
- **például**
	- 2-vel és 5-el nem osztható számok
![[Pasted image 20251004125634.png]]
[[Az if utasítások egymásba ágyazása]]
# Címkézett utasítások
A **case** és a **default** utasítások. Használatukat lásd a **switch** utasításnál
# Vezérlésétadó utasítások
- **break:** utasításblokkból való kifejezésre szolgál, a vezérlés az utasításblokk utáni utasításblokk utáni utasításra adódik
- **continue:** iterációs utasítások törzében használva a program működése a soron következő iterációval folytatódik
- **return**: 
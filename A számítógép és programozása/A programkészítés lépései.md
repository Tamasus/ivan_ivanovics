![[Pasted image 20250919152933.png]]

## Specifikáció és algoritmus
#### Specifikáció:
Feladatleírás (deklaratívan adott) Mit kell csinálnia a programnak? Mi lessz a bemenete mi a kimenete mi ezek között az összefüggés?
#### Algoritmus:
A megoldás *Lépésről lépésre* történő leírása imperatív módon (utasítások sorozatonként). Hogyan hajtsa végre a számítógép a feladatot? *Ezt a programozónak kell kitalálnia!*

## Példa:
Specifikáció:
írjunk programot amelyik kiszámítja egy téglalap kerületét és területét! A program kérdezze meg a két oldalhosszt a felhasználótól és ezután írja ki az eredményt

Algoritmus:
![[Pasted image 20250919153534.png]]

C-program:
![[Pasted image 20250919153606.png]]

## Tesztelés, hibakeresés
Programhibák fajtái:
![[Pasted image 20250919153654.png]]
### Fordítási idejű hibák:
A C fordító csak akkor tudja lefordítani a programot ha az a formai szabályoknak eleget tesz.
**Szintaktikai hiba:** a nyelvtani szabályok szerint hibás
![[Pasted image 20250919153841.png]]
**Szemantikai hiba:** nincs értelme az utasításnak
![[Pasted image 20250919153919.png]]

### Futási idejű hibák:
A program futásakor(működése közben) tapasztaljuk. *Bug*-ok amik helyes programozással elkerülhetők
*Bug:* Apró méretű nehézség (T.Edison 1889)
pl.:
- Végtelen ciklus (a program nem terminál)
- hibás adatbevitel típushiba
- nullával való osztás
- érvénytelen sorozatindex
Futási idejű hibák detektálása: **Debuggolás**

### Logikai hibák:
A program látszólag helyes de nem az elvárt outputot szolgáltatja. Nehéz detektálni . Lehetséges okok:
- Algoritmus hibás implementálása 
- Szelekciós interációs blokk vége hibásan jelölt 
- Nem megfelelő paraméterek átadása
Példa: Két szám átlagának kiszámítása (hibás)
![[Pasted image 20250919154449.png]]

## Dokumentálás:
- A kódot emberek is olvassák!Biztosítani kell a kód :
	- Olvashatóságát (kódolási szabályok betartása)
	- Karbantarthatóságát (dokumentálás)
**Dokumentálás:**
- Tesztelési dokumentáció: hibakeresés körülményeiről a progtóram működőképességéről
- Fejlesztői dokumentáció: a program felépítése, működése
- Felhasználói dokumentáció: használati utasítás

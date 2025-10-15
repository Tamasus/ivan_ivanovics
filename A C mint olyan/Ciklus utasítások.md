- Utasítások autómatikus ismétlését biztosító programszerkezet. Az ismétlés addig tart, amíg az ismétlési feltétel igaz (nem nulla).
- A ciklus befejezi működését amikor a vezérlő feltétel hamissá válik (nulla lesz). Az a ciklus amelynek vezérlő feltétele soha sem lesz hamis a végtelen ciklus
- Ciklusból kilépni a vezérlő feltétel hamissá válása előtt a break vagy return utasítással lehet
- A ciklus utasításblokkjának (törzsének) vége előtt a következő iterációra lépni a continue utasítással lehet.
- A vezérlőfeltétel-kifejezés egészre konvertálódó, logikai kifejezés kell legyen
- A vezérlőfelület-kifejezés kiértékelésének helye alapján lehet ciklus:
	- Elöltesztelő ciklus: a vezérlőfeltétel a ciklustörzs végrehajtása előtt kiértékelődik
	- Hátulteszetlő ciklus: a vezérlő feltétel a ciklustörzs végrehajtása után értékelődik ki (vagyis az utasítás legalább egyszer mindig végrehajtódik)

# A while utasítás
- Addig ismétli az utasításokat (a ciklus törzsét) amíg a vezérlő feltétel kifejezés értéke igaz (nem nulla)
- Elöltesztelő ciklus
![[Pasted image 20251010133720.png]]
![[Pasted image 20251010133728.png]]
# A vezérlő feltétel
-Általában a relációs és logikai operátorok használatával írt logikai kifejezés de lehet más egészre konvertálódó kifejezés is . Például:
![[Pasted image 20251010133934.png]]
- Figyelem! Ha a vezérlőfeltételben tesztelt változó értékét nem módosítjuk a ciklustörzsben a vezérlőfeltétel mindig ugyanarra értékelődik ki!

# Végtelen ciklus elkerülése
1. A vezérlő feltételben tesztelt változó értékét a ciklustörzsben úgy kell módosítani hogy a vezérlőfeltétel véges számú lépés után hamissá váljon
![[Pasted image 20251010134216.png]]
2. Kigrás a ciklustörzsből
![[Pasted image 20251010134243.png]]
![[Pasted image 20251010134314.png]]
![[Pasted image 20251010134326.png]]
# A for ciklus
- Akkor használjuk ha a ciklusmagban megadott utasítást adott számszor kívánjuk végrehajtani (az ismétlések száma ismert)
- Elöltesztelő ciklus
- A kifejezések opcionálisak ; -vel elválasztva 
![[Pasted image 20251010134514.png]]
![[Pasted image 20251010134522.png]]

## A for ciklus működése
1. Az iterációs lépések számlálásra használt ciklusváltozó inicializálásával indul a ciklus (init_kif kiértékelése). A kifejezés megadása opcionális int
2. A feltétel_kif kiértékelése. Megadása opcionális, típusa egésre konvertálódó logikai kifejezés
	- Ha a feltétel_kif igaz (értéke nem nulla), végrehajtódnak a ciklustörzs utasításai ; majd kiértékelődik a léptető_kif (ciklusváltozó léptetése) és vissza 2.
	- Ha a feltétel_kif nincs megadva akkor annak értékét igaznak tételezi fel a fordító
	- Ha a feltétel_kif hamis (értéke 0) a for utasítás befejeti a működését
![[Pasted image 20251010135138.png]]
## A for ciklus - tömörítési lehetőségek
- Több inicializáló kifejezés is szerepelhet a for utasítás fejlécében
![[Pasted image 20251010135245.png]]
- A ciklusmagban szereplő kifejezés utasítások felvihetők a for utasítás fejlécébe a léptető_kif elé. Léptetéshez a postfix és a prefix alak is használható.
![[Pasted image 20251010135412.png]]
- Példákban a végrehatandő utasítás és a léptető_kif összevonható.Ekkor a léptetés csak postfix alakban írható
![[Pasted image 20251010135518.png]]

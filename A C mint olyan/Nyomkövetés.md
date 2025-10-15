- Nyomkövetés: az utasítások végrehajtásának követése minden állapotának és az összes generált kimenetnek a feljegyzése
	1. Megközelítés: manuális nyomkövetés papíron
	   Problémák: lassú unalmas nagy a hibázás valószínűsége
	2. Megközelítés: a program kritikus pontjain kiíratjuk a változók értékét.
	   Probléma: a kód olvashatósága romlik, hosszabb lesz a kód a hibajavítás után ki kell törölni a felesleges utasításokat
	3. Megközelítés: a fejlesztőkörnyezet debug funkciójának használata
- A program nyomkövetését a programhibák feltárása és javítása érdekében végezzük , ezért debuggolásnak nevezzük
- Lépései:
	1. A követni kívánt változókat megjelöljük (a kódsor elejére kattintva egy piros pont jelenik meg)
	2. A programot debug módban futtatjuk
	3. A debug konzol használatával a programot lépésenként hajtjuk végre követve a változók értékeinek alakulását
	4. A szükséges módosításokat a debug módból kilépve tudjuk elvégezni a kódon

- A while és a for elöltesztelő ciklusok. Azaz a ciklus elején tesztelik az ismétlést szabályozó feltételt. Előfordulhat, hogy a teszt soha nem lesz igaz azaz a ciklustörzs utasításai egyszer sem futnak le
- Bizonyos feladatoknál először le kell futtatni a ciklustörzs utasításait ahhoz hogy a program tudjon dönteni az utasítások ismétlődéséről. Például:
	- Hibás input újbóli beolvasása (input ellenőrzés)
	- A program futásának igény szerinti folytatása vagy leállítása (folyamatos működésű program)
- Az ilyen típusú feladatokat hátultesztelő ciklussal oldjuk meg

# Ellemőrzött adatbevitel
- Az adatok beolvasásakor ellenőrizni kell:
	- A beolvasott érték típúsát
	- A beolvasott érték helyességét
- A program addig nem folytathatja a működését amíg nem biztosítottuk a bemenet helyességét
- A scanf függvény működése
	- A sikeresen beolvasott adatok számát adja vissza
	- Az OS az enter billentyű lenyomásakor egy ideiglenes tároló területre (bufferba) tölti a szabványos inputon megadott karaktereket. Innen csak annyi karaktert dolgoz fel a függvény amennyit értelmezni képes a többi bennmarad a bufferban. -> Hibás adatbevitel esetén ki kell üríteni az input buffert
	- Karakter beolvasása: %c használatával a nem látható karakterek is (pl. új sor) feldolgozásra kerülnek. Ezek figyelmen kívül hagyásához a %c elé spacet kell tenni.
![[Pasted image 20251010143733.png]]
# Folyamatos működésű program 
- Folyamatos működésű egy program ha csak a felhasználó kérésére áll le.
![[Pasted image 20251010143851.png]]
![[Pasted image 20251010143901.png]]

# A break uatsítás
![[Pasted image 20251010143922.png]]
![[Pasted image 20251010143934.png]]

# A continue utasítás
A continue utasítással átugrunk utasításokat és új iterációt indítunk.
![[Pasted image 20251010144033.png]]
![[Pasted image 20251010144051.png]]
![[Pasted image 20251010144102.png]]
A feltétel átfogalmazásával a használata legtöbbször elkerülhető
# Végtelen ciklus
- A vezérlő feltétele mindig igaz.
![[Pasted image 20251010144213.png]]
- Általában akkor használjukk amikor nem tudunk (vagy túl bonyolult lenne) vezérlési feltételt megfogalmazni
- A végtelen ciklus megszakításáról (a ciklusból való kitörésről) a programozónak kell gondoskodnia vezérlésleadó utasítás használatával

# Választás a for és a while között
- A for utasítás használata biztonságosabb (mert az iteratív változó léptetése az utasítás fejlécének része azaz nehezebb véletlenül végtelen ciklust írni), ezért ahol lehet ezt használjuk
- Használjunk for ciklust ha már az ismétlés előtt tudjuk hogy maximum hányszor kell végrehajtani a ciklustörzset!
  Ha például elemek egy listáját (egy megadott tartományt) kell bejárni akkor tudjuk hogy maximum hány ismétlés szükséges az összes elem feldolgozásához
- Használjunk while ciklust ha egy feltétel bekövetkeztéig kell ismételni egy számítást és nem tefjuk előre kiszámolni hogy ez hány lépérd után következhet be!
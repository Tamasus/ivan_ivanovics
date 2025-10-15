- Az IDE (Integrated Development Environment) olyan allkalmazás ami a szoftverfejlesztők munkáját hatékonyan támogatja
- **Funkciói:**
	- Kódszerkesztő: kódszínezés, inteligens kódkiegészítés, refaktorálás
	- Build funkciók: fordítás automatikus tesztelés
	- Változók nyomonkövetése, hibakeresés (debugger)
	- Verziókövetés, csoportmunka támogatás
	- Dokumentáció készítés
# A C program szerkezete:
- A C nyelven megírt program egy vagy több forrásfájlban (fordítási egységben) található, melyek kiterjesztése .c
- A programhoz csatlakozó header fájlokat a # include utasítással építjük be melyek kiterjesztése .h
- A header fájlok az adott forrásfájlon kívül definiált függvények dekralációt tartalmazzák és konstans makrókat
- A C program mindig a main függvény első végrehajtható utasításával indul ( ez a függvény a program belépési pontja és csak egy példányban létezhet).
## Standard I/O kezelése
- A szabványso bemenetet/kimenetet könyvtári függvényekkel kezdjük. Deklarációjuk a stdio.h standard header állományban található:
![[Pasted image 20250928145137.png]]
- Formázott adatbevitel (input):
![[Pasted image 20250928145213.png]]
A szabványos bemenetről olvas karaktereket majd a formátumsztring specifikációi szerint értelmezi és konvertálja azokat. A konverzió eredményét a soron következő argumentum által kijelölt változóba tölti.
### A scanf() függvény működése:
- Space/újsor kategóriáig olvas
- Az input adatokat az operációs rendszer az Enter billentyű lenyomásakor egy ideiglenes tároló területre (bufferba ) tölti. Innen a scanf() fv csak annyi karaktert dolgoz fel amennyit értelmezni képes a megadott formátum szerint a többi bennmarad a bufferban.
- A c szabványban nincs definiálva eljárás az input buffer kiürítésére
- Karakter beolvasása helyesen:
![[Pasted image 20250928145926.png]]
- Formázott adatkiírás (output):
![[Pasted image 20250928150008.png]]
A formátum sztring meghatározza az argumentum értelmezésének módját valamint a megjelenítés formályát.
- A formátum sztringben használható helyettesítő karakterek beolvasásánál és kiirásáánál is:
![[Pasted image 20250928150157.png]]
![[Pasted image 20250928150212.png]]

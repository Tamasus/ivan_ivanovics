## A C nyelv jelkészlete:
![[Pasted image 20250926155600.png]]
### Azonosítók:
- Betűk, számjegyek és az aláhúzás karakter kombinációjaként hozható létre
- Nem kezdődhet számjeggyel 
- Kis- és nagybetű érzékeny
![[Pasted image 20250926162134.png]]

### Literálok (nyelvi konstansok):
##### Egész konstansok:
- Számjegyek sorozata, ahol a számjegyek decimális , oktális vagy hexadecimális számrendszerbeli jegyek
- Pozitív értéket jelöl ha nincs előtte negatív előjel
- Decimális Egész konstans első számjegye nem lehet 0
- Oktális egész konstans első számjegye 0 , majd ezt oktális számjegyek (0-tól 7-ig) követik (például :0,-01,040)
- Hexadecimális egész konstans előtagja 0x vagy 0X majd ezt Hexadecimális számjegyek követik (0-tól 9-ig, a vagy A, b vagy B , c vagy C, d vagy D, e vagy E, f vagy F) (Például:0x20, -0x7cA)

## Literálok
### Lebegőpontos konstans
Olyan decimális szám, amely előjeles valós számot reprezentál. A valós szám általában egészrészéből, tizedes törtrészből és kitevőből tevődik össze.
![[Pasted image 20250926163319.png]]
### Karakter konstans
Egyszeres idézőjelek (aposztrófok) közé zárt egyetlen karakter, vagy egy karaktert reprezentáló szekvencia.
![[Pasted image 20250926163516.png]]
A karakter konstansok a C-ben int típusúnak, 1byte helyet foglalnak és az általuk képviselt számérték a karakter ASCII kódja.
![[Pasted image 20250926163644.png]]
![[Pasted image 20250926163720.png]]
### Sztring konstans
- Kettős idézőjelek közé zárt karaktersorozat. Például:"ez egy szting konstans".
- Tárolásuk: a karaktereket tartalmazó byte-sorozat végén van egy 0 értékű byte (lezáró karakter:'\0')
- Tartalmazhat escape szekvenciát is amik szabványos vezérlő-és speciális karakterek megadására szolgálnak.
![[Pasted image 20250926164651.png]]
- A maximális hossza implementáció függő. Hosszú szövegeket több programsorba is széttördelhetünk a \ jellel.

### Szimbolikus konstans:
![[Pasted image 20250926164945.png]]
Előfordítónak szóló direktívában adjuk meg a pr.kód elején. Értékbehelyettesítésre szolgál. A forráskódban az AZONOSITO minden előfordulása kicserélődik a megadott értékre. Csupa nagybetűvel szokás megadni.
![[Pasted image 20250926165242.png]]
## Kulcsszavak
Előre definiált jelentésű, másra nem használható, fenntartott szavak. Kisbetűsek.
![[Pasted image 20250926165354.png]]
## Megjegyzés sorok:
![[Pasted image 20250926165426.png]]
Használatával a forráskód jól dokumentált jól olvasható lesz.Lehetővé teszi hogy egyes programrészeket ideiglenesen eltávolítsunk a kódból (pl. hibakeresés céljából). A megjegyzések nem ágyazhatók egymásba!
![[Pasted image 20250926165855.png]]
## Írásjelek, elválasztók:
Csak szintaktikai szerepük van, műveletet nem definiálnak.
![[Pasted image 20250926170010.png]]
## Operátorok:
Egy vagy több karakterből álló műveleti jelek feladatuk meghatározni az operandusokon végrehajtandó műveletet.
A C nyelv szabályos operátorai:
![[Pasted image 20250926170202.png]]

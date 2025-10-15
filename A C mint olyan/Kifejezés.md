- Operandus: a C nyelv azon eleme amelyen az operátor kifejti a hatását.
- Kifejezés: vagy egyetlen operandusból vagy operandusok és műveleti jelek (operátorok) kombinációjából épűl fel. Fajtái:
	- Elsődleges kifejezés: literál azonosító függvényhívás, tömbindex kifejezés vagy struktúra tagkiválasztó kifejezés.
	- Összetett kifejezés, amely zárójelezett vagy zárójel nélküli operátorokkal összekapcsolt operandusokból (elsődleges kifejezésekből) áll.
- Egy **kifejezés kiértékelésének** eredménye lehet
	- egy érték kiszámítása (főhatás)
	- függvényhívás
	- mellékhatás (Side effect) (vagy ezek kombinációja)
- **Mellékhatás:** amikor a kifejezés kiértékelése a program valamely változójában (azaz a program állapotában) változást idéz elő. Például: a=2+3
	- főhatás: a 2+3 kifejezés kiszámítása
	- mellékhatás 'a' értéke 5-re változik
Transzparensnek nevezzük azt a kifejezést amelynek nincs mellékhatása.
## Csoportosításuk az operandusok száma szerint:
- **Egyoperandusú** operátor esetén a kifejezés alakja:
	- Prefix/előrevetett alak: operátor operandus
	- Postfix/hátravetett alak: operandus operátor
- **Kétoperandusú** operátor esetén a kifejezés alakja:![[Pasted image 20250928121001.png]]
- **Háromoperandusú** (feltételes) operátor feltételes kifejezés alakja:![[Pasted image 20250928121104.png]]
## Elsődleges operátorok 
- Azok az egyoperandusú (unary) operátorok, amelyekkel elsődleges kifejezések hozhatók létre ( () ,[] , . , ->)
	- fv(argumentumok): függvényhívás operátor 
	- tomb[index]: tömb indexelés operátor
	- str.tag vagy pstr->tag:
	  struktúra illetve struktúra mutató pointer adattagjára hivatkozás operátorai
- Zárójel () operátor: kifejezések csoportosítása, műveletek kiértékelési sorrendjének előírása
## Arimetikai operátorok
- A négy alapművelet ( + , - , * , / ) és a maradékképzés (%) kétoperandusú (bináris) operátorai
![[Pasted image 20250928122114.png]]
- Az egyopernadusú mínusz (-) operátor amelynek csak prefix alakja létezik és az utána álló operandus értékét negálja (ellentétes előjelűre változtatja).
![[Pasted image 20250928122249.png]]
## Összehasonlító és logikai operátorok
- **A C nyelvben nincs külön logikai adattípus!** Vannak azonban olyan utasítások amelyekben feltételeket kell definiálni. Ezen kifejezések nulla vagy nem nulla értéke szolgáltatja a logikai hamis illetve igaz eredményt.
- Feltétel kifejezésekben használt bináris **Összehasonlító operátorok: < , <=, <, <=, == , !=**
![[Pasted image 20250928123543.png]]
![[Pasted image 20250928123559.png]]
![[Pasted image 20250928123611.png]]
- Mindhárom esetben a FALSE és a TRUE szimbolikus konstansok melyek értéke 0 illetve 1
- Bonyolultabb feltételek írásához a feltételek összekapcsolásához szükség van logikai operátorokra:
![[Pasted image 20250928123759.png]]
![[Pasted image 20250928123822.png]]
## Logikai operátorok rövidzár tulajdonsága
Ha az operátor bal oldalán szereplő kifejezés kiértékelésekor eldől az eredmény a jobboldali kifejezés ki sem értékelődik!
-  A && B : ha A hamis akkor a kifejezés biztosan hamis 
- A II B : ha A igaz akkor a kifejezés biztosan igaz
![[Pasted image 20250928124808.png]]
Következtetés: Ne hasnáljunk olyan kifejezést && és II operátorok operandusában aminek mellékhatása van!!

## Léptető operátorok:
- Unáris operátorok amelyek csak balérték operandussal használhatók de prefix és profix alakban is
- Egy változó értékét eggyel növelik (++) illetve eggyel csökkentik(--).
![[Pasted image 20250928133800.png]]
Az egy sorban lévő utasítások egymással ekvivalensek, de a léptető operátor használata gyorsabb kód létrehozását eredményezi.
![[Pasted image 20250928133901.png]]
## Értékadó operátor:
- Az értékadás olyan kifejezés amely a baloldali operandus által kijelölt változónak (balérték) adja meg a jobboldalon megadott kifejezés értékét (jobbérték). Ez az érték egyben az értékadó kifejezés értéke is. Ezért értékadás tetszőleges kifejezésben szerepelhet!
![[Pasted image 20250928134455.png]]
![[Pasted image 20250928134515.png]]
- Az értékadó operátorok kiértékelése jobbról ballra töörténik ezért használható a többszörös értékadás.
			a=b=25;
## Öszetett értékadás:
Értékadáskor gyakran egy változó értékét módosítjuk, majd az újj értékettároljuk a változóban.
a = a+ 2 ;
Ez tömörebb formában is megadható: a+= 2;
Az alábbi felírások egyenértékűek (kivéve ha összetett értékadáskor a bal oldali kifejezés csak egyszer értékelődik ki így ez gyorsabb kódot eredményez):
![[Pasted image 20250928135944.png]]
Öszetett értékadásban az alábbi kétoperandusú operátorok használhatóak:
![[Pasted image 20250928140025.png]]
### Egyéb operátorok:
- Bitműveletek operátorai
- Pointer operátorok
- **sizeof**: fordítási időben kiértékelésre kerülőegyoperandusú operátor amely megadja egy változó vagy típus méretét byte-ban (az eredmény egész típusú)
- **Vessző:** egy kifejezésen belüll lehet több kifejezést megadni vesszővel elválasztva.Az ilyen kifejezés balról jobbra kerül kiértékelésre; és a kifejezés értéke és típusa a jobboldali operandus értékével és típusával egyezik meg.
**x= (y = 3, y+2);  -> x=5**
- Több változó definiálása egyetlen utasításban vesző operátorral:
**int x=2, y =3, z= 5;**
## A feltételes operátor:
- Háromoperandusú operátor (?:), általában a feltételes utasítást helyettesítjük vele. Alakja:
![[Pasted image 20250928140704.png]]
- Először a kif1 kerül kiértékelésre. ha ennek értéke nem nulla (igaz) akkor a feltételes kifejezés értéke kif2, egyébként kif3. Tehát a? utáni kifejezések közül mindig csak az egyik értékelődik ki.
- A feltételes kifejezés típusa a nagyobb pontosságú részkifejezés (kif2 vagy kif3) típusával eggyezik meg
![[Pasted image 20250928140937.png]]
## Precedencia és asszocivitás
- Precedencia szabály: a kifejezésekben szereplő operátorok kiértékelésének sorrendjét írja elő.
Megjegyzés:
A művrletek kiértékelési sorrendje zárójelezéssel megváltoztatható!
- Asszociativitási szabály: a kifejezésekben szereplő azonos precedenciájú műveletek kiértékelésének sorrendjét határrozza meg
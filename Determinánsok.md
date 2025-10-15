## Definició
Az 1,2,....,n elemek egy permutációban két elem inverzióban áll ha közülük a nagyobbik megelőzi a kissebbiket. Egy permutáció *inverziószám*án az inverzióban álló elempárok számát értjük.

## Definíció
Egy permutáció aszerint páros illetve páratlan hogy inverziószáma páros illetve páratlan

# Tétel:
1. Ha egy permutációban két szomszédos elemet felcserélünk akkor az inverziószám 1-gyel változik (nő vagy csökken)
2. Ha egy permutációban két tetszőleges elemet felcserélünk akkor az inverziószám páratlannal változik
## Bizonyítás:
1. A két felcserélt elem viszonya megváltozott azaz ha eredetileg inverzióban álltak akkor a csere után már nem állnak inverzióban és fordítva. Mivel szomszédosak voltak, ezért a többi elemhez képest az elhelyezkedésük nem változott és természetesen a többi elem egymáshoz viszonyított helyzete sem módosult.
2. Ha két elem, *b* és *c*  között k darab másik áll akkor először a hátrébb álló *c*-t sorra megcseréljük a mindig éppen előtte állóval, amíg közvetlenül *b* mögé nem kerül ez szomszédos elemek közötti *k* cserét jelent. 
   Ezután megcseréljük ( a most egymás melett lévő) *b*-t és *c*-t. Végül ujabb  *k* cserével *b*-t rendre megcseréljük a mögötte álló elemekkel amíg végül a *b* elem a *c* eredeti helyére nem kerül. Ez összesen *2k + 1* , szomszédos elemek közötti csere volt, amelyek mindegyikénél 1-gyel változott (nőtt vagy csökkent) az inverziószám
# Tétel
Ha *n>1* akkor *n* elemnek ugyanannyi páros és páratlan permutációja van.
## Bizonyítás:
Tekintsük az 1, 2,......*n* számok összes páratlan permutációját, és mindegyikben cseréljük fel az első és a második helyen álló elemet. Ekkor csupa páros permutációhoz jutunk amelyek mind különbözők. Ebből azt kaptuk hogy legalább annyi páros permutáció van mint páratlan.
Ha ugyanezt az eljárást a páros permutációkból kiindulva hajtjuk végre akkor az adódik hogy legalább annyi páratlan permutáció van mint páros. Így a páros és páratlan permutációk száma valóban megegyezik (=n!/2)
### A determináns definíciója:
Legyen *n* rögzített pozitív egész. A determinánst első közelítésében úgy tekinthetjük mint egy számot amelyen *n^2* darab számból bizonyos bonyolult szabályok szerint számítunk ki.
A determináns definícióját számok helyett általánosságban egy tetszőleges *T* kommutatív test elemeire fogjuk kimondani. (megtalálható a [[Test]] pontaban) röviden összefoglalva ez azt jelenti hogy a "négy alapművelet" (a nullával való osztás kivételével) elvégezhető és a szokásos műveleti azonosságok érvényesek.
Legfontosabb példák: **R,C** illetve **Q** a valós a komplex illetve a racionális számok teste, valamint *Fp* a modulo *p* maradékos teste ahol *p* prímszám. Azt is megjegyezzük hogy a determináns definíciójához és az ebben a fejezetben tárgyalt tulajdonságaihoz osztásra nincs is szükség és így pl. egész számokból vagy poloniumokból képzett determinánsról beszélhetünk.
**Lényeges információ:** 
hogy n^2 darab *T* -beli elemet egy *n x n*-es négyzet alakú táblázatba rendezzünk. Az ilyen és az ennél általánosabb téglalap alakú táblázatokat **mátrix**oknak nevezzük.

## Definíció:
Legyen *T* egy kommutatív test és *k,n* adott pozitív egészek. Ekkor a *T* test feletti *k x n*-es mátrixon egy olyan téglalap alakú táblázatot értünk amelynek *k* sora és *n* oszlopa van és amelynek elemei *T*-ből vannak.
**Jelölések:** 
![[Pasted image 20251001164028.png]]
A továbbiakban sima gömbölyű ( ) zárójelet fogunk használni, de szokásos a szögletes [ ] zárójel használata is.

Egy általános A mátrix *i*-edik sorának *j*-edik elemét *aij*-vel fogjuk jelölni. Az első index tehát azt jelzi hogy a szóban forgó elem a táblázat hányadik sorában áll a második index pedig azt hogy hányadik oszlopban. Az előző példában a23=4. Ennek megfelelően egy *k x n*-es mátrix általános alakja
![[Pasted image 20251001164443.png]]
n x n -s négyzetes mátrix általános alakja
![[Pasted image 20251004164728.png]]

### Determináns fogalma az A mátrix determinánsán
(ezt det *A* val jelőljük majd) egy olyan *T*-beli elemet értünk amelyet a következőképpen határozunk meg. Először is *n*-tényezős sorozatokat képzünk minden lehetséges módon úgy hogy a mátrix minden sorából és minden oszlopából pontosan egy tényezőt veszünk (összesen *n!* ilyen sorozat képezhető). A következő lépésben minden egyes szorzatot "+" bóvagy "-" előjellel látunk el:
Ez azt jelenti hogy vagy magát a szorzatot tekintjük vagy pedig a negatívját (ellentetjét). Az előjelzési szabályt a következő bekezdésben részletezzük. Végül ezeket az előjeles szorzatokat összeadjuk (azaz az összeg minden tagja vagy egy ilyen sorozat vagy pedig a sorozat negatívja). Az így kapott  (n! tagú) összeget (amely tehát egy *T*-beli elem) nevezzük A mátrix determinánsának vagy más szóval *aij* elemekből képzett (*n*-edrendű vagy *n x n*-es vagy *n* méretű determinánsnak)
Egy sorozat "előjelezése" a következőképp történik. A sorozat tényezőit írjuk fel olyan sorrendben hogy az első helyen az **1**. sorból vett elem álljon a második helyen a **2**. sorból vett elem stb . Ha itt rendre megnézzük hogy a szorzat tényezői hányadik oszlopból valók akkor ezek az oszlopindexek is valamilyen sorrendben az 1, 2 . . . ,n számokat futják be ( hiszen minden oszlopból pontosan egy elem szerepel), tehát ezek az oszlopindexek az 1, 2, . . .,n számok egy permutációját adják. A szorzatot aszerint látjuk el pozitív illetve negatív előjellel , hogy ez a permutáció páros illetve páratlan.
![[Pasted image 20251004170750.png]]
soeok szerint vannak rendezve és ezeket a tényezőket rendre a 2., a 3., majd az 1. oszlopból vettük.
Az oszlopindexek permutációja tehát 231 amelyben két inverzió van. Így ez páros permutáció a szorzat előjele tehát pozitív (vagyis maga ez a sorozat nem pedig az ellentetje fog szerepelni a determinánst megadó összegben)

#### Figyelem!
A szorzat előjelezésének semmi köze sincs a szorzótényezőlnek az értékéhez ez kizárólag az *n* tényezőnek a mátrixon belüli elhelyezkedésétől függ. Az előjel meghatározásánál csakis az oszlopindexek imént említett permutációjának paritása számít ez a permutáció pedig mindig az 1, 2 , . . .,n természetes számokra vonatkozik függetlenül attól hogy a mátrix elemei (valós komplex stb.) számok vagy sem (pl. maradékosztályok)
A determinánst úgy jelöljük hogy a táblázatot (a zárójelek nélkül) két függőleges vonal közé tesszük.
### Definíció 
![[Pasted image 20251004172144.png]]
A jobb oldalon álló ∑ összegzést az 1, 2, . . .,n számok minden lehetséges σ permutációjára el kell végezni . Az összegben az *n!* tagnak pontosan a felét láttuk el negatív előjelzéssel (azaz ennyiszer szerepel a sorozat helyett az ellentetje), hiszen ugyanannyi páratlan és páros permutáció van (az *n = 1* triviális esettől eltekintve)
![[Pasted image 20251004172506.png]]
A definíció alapján meglehetősen nehézkes egy determináns kiszámítása.

## Tétel
Tekintsünk egy determináns  definíciójában szereplő *n*-tényezős szorzatot, ahol tehát minden sorból és minden oszlopból egy elem szerepel. Ez a sorozat (a tényezőket tetszőleges sorrendben felírva)  *αρ(1)π(1) . . . αρ(n)π(n)* alakú ahol *p* a sorindexeknek , *π* az oszlopindexeknek megfelelő permutáció. Ekkor az előjelet (−1)^(ρ)+I(π) határozza meg.
### Bizonyítás
Ha *p* természetes sorrendekk megfelelő permutáció,akkor az éppen a determináns definíciójában szereplő előjelezés hiszen *I(p)=0* . 
Könnyen látható, hogy a tényezőknek ebből a sorrendjéből kiindulva cserék egymásutánjával bármelyik másik sorrendhez eljuthatunk. Így elég azt megmutatnunk hogy ha a szorzatban két tényezőt felcserélünk akkor az *I(ρ) + I(π)* összeg paritása nem változik. Ez valóban igaz: egy ilyen csere ugyanis mind a *p* mind a *π* permutációjában két elem cseréjét jelenti ezért mindkét permutációban az inverziószám páratlannal változik,, tehát az inverziószámok összegének paritása változatlan marad.

# Elemi tulajdonságok
A determináns definíciójából azonnal adódnak az alábbi egyszerű állítások:
## Tétel
I. Ha a főátló (azaz a bal felső sarkot a jobb alsó sarokkal összekötő egyenes) alatt avgy fölött minden elem 0 akkor a determináns a főátlóbeli elemek szorzata.
II. Ha valamelyik sor vagy oszlop minden eleme 0 akkor a determináns is 0 
III. Ha valamelyik sor vagy oszlop minden elemét λ-val megszorozzuk akkor a determináns is λ-val szorzódik.
### Bizonyítás
I. és II. lényegében szerepelt az 1.2.3 feladatban. III. esetében a determináns definíció szerinti felírásában minden szorzat λ-val szorzódik, hiszen minden szorzatban pontosan egy tényező van az adott sorból, illetve oszlopból. Mivel az előjelezés nem módosult, így a λ-t minden tagból kiemelve kapjuk, hogy a determinánst adó előjeles összeg is λ-szorosára változott.
#### Megjegyzés
A II. állítás a III.-nak a * λ = 0* speciális esete. A következő tulajdonság hasonlóan igazolható

## Tétel
Ha valamelyik sor vagy oszlop minden eleme egy kéttagú összeg, akkor a determináns két determináns összegére bomlik ahol az egyikben az adott sorban illetve oszlopban rendre az összegek rgyik tagja szerepel a másikban pedig a másik tag a többi elem pedig mind a két determinánsban ugyanaz, mint az eredetiben volt.Azaz 
![[Pasted image 20251005104605.png]]
## Tétel
Ha két sor egyenlő (azaz a megfelelő elemek megegyeznek), akkor a determináns 0.
### Bizonyítás:
Megmutatjuk hogy a determináns definíció szerinti felírásban a szorzatok párba állíthatók úgy hogy bármely két összetartozó szorzat ugyanaz azonban az előjelezésükk ellentétes. Mivel minden pár összege 0 ezért a determináns is 0.
A bizonyítást az egyszerűség kedvéért arra az esetre mondjuk el amikor az első két sor egyenlő: *a1j = a2j* minden *j*-re.
A bizonyítás gondolatát először egy konkrét példán illusztráljuk. Legyen *n = 5* és tekintsük a determináns definíciójában az
![[Pasted image 20251005110553.png]]
szorzatot. Mivel a feltétel szerint ![[Pasted image 20251005110625.png]] ezért a determinánsban szintén szereplő
![[Pasted image 20251005110701.png]]
szorzat egyenlő *S*-sel.
Vizsgáljuk most meg az *S*, illetve* S ′* szorzatok előjelezését. Ehhez az oszlopindexekből képezett *35412*, illetve *53412* permutáció inverziószámát kell tekintenünk. Az utóbbi permutációt az előzőből úgy nyertük, hogy az első két elemet felcseréltük. Ennek alapján az inverziószám páratlannal változott (jelen esetben 1-gyel, mert a felcserélt elemek szomszédosak voltak). Ez azt jelenti, hogy a két permutáció ellentétes paritású, és így az *S* és *S ′* szorzatok előjelezése is ellentétes (jelen esetben a determinánst adó összegben *−S* és *+S* ′ fog szerepelni). Pontosan ugyanígy kell végiggondolni az általános esetet is. A determináns definíciójában szereplő szorzatok általános alakja
![[Pasted image 20251005111016.png]]
Ugyanez a szorzat még egyszer előfordul mint 
![[Pasted image 20251005111049.png]]
hiszen *α1σ(1) = α2σ(1) és α2σ(2) = α1σ(2)*. Könnyen látható, hogy ezzel a szorzatokat valóban párba állítottuk. Végül igazoljuk, hogy *S* és *S ′* ellentétes előjelű lesz. *S* előjelét a *σ(1)σ(2)σ(3). . . σ(n)* permutáció paritása, *S ′* -ét pedig a *σ(2)σ(1)σ(3). . . σ(n)* permutáció paritása adja. Mivel az utóbbi permutáció az előbbiből (az első) két elem cseréjével keletkezett, így a paritás valóban az ellenkezőjére változott.
# Tétel
Ha valamelyik sor egy másik sor λ-szorosa akkor a determináns 0

# Tétel
Ha egy sorhoz hozzáadjuk a másik sor λ-szorosát akkor a determináns nem változik
## Bizonyítás:
![[Pasted image 20251012110136.png]]
# Tétel 
Ha a két sort felcserélünk akkor a determináns a negatívjára változik.
## Bizonyítás
Többször egymás után alkalmazzuk a tételt. Elősör a második sort kivonjuk az elsőből majd az új első sort hozzáadjuk a második sorhoz , végül az új második sort kivonjuk az új első sorból. Eközben a determináns nem változik az első sor *j*-edik eleme pedik a következőképp módosul:
![[Pasted image 20251012110500.png]]
Végül az első sorból -1 et kiemelve a kapott determináns egyrészt az eredeti determináns -1szerese másrészt az eredetiből éppen az első két sor felcserélésével keletkezett.
# Tétel
Ha az elemeket a főátlóra tükrözzük akkor a determináns nem változik
## Bizonyítás
Megmutatjuk, hogy a két determináns definíció szerinti felsorolásban ugyan azok a sorozatok szerepelnek és az előjelzésük is azonos.
Az eredeti determinánsban szereplő szorzat általános alakját most az 1.2.3 Tételben szereplő módon, αρ(1)π(1) . . . αρ(n)π(n) formában írjuk fel, ahol ρ a sorindexek, π az oszlopindexek permutációja. Ugyanez a szorzat a főátlóra történő tükrözés után is szerepelni fog, éspedig βπ(1)ρ(1) . . . βπ(n)ρ(n) alakban. A két szorzat előjelezése is megegyezik, hiszen az előjelet az 1.2.3 Tétel szerint az eredeti determinánsban (−1)I(ρ)+I(π) , a tükrözés utániban pedig (−1)I(π)+I(ρ) határozza meg.
# Kifejezés
## Definíció
Tekintsünk egy n-eredetű determinánst Hagyjuk el az i-edik sort és a j-edik oszlopot, így egy (n − 1) × (n − 1)-es determináns keletkezik. Az αij elemhez tartozó Aij előjeles aldeterminánson ennek a determinánsnak a (−1)i+j -szeresét értjük.
![[Pasted image 20251012120839.png]]
**Figyelem:**
Az aldetermináns előjelzésének semmi köze sincs a determináns definíciójában az egyes szozatok előjelzéséhez itt semmiféle permutáció vagy inverziószám nem szerepel. Az aldetermináns előjelét kizárólag az határozza meg, hogy melyik sort és oszlopot hagytuk el: ha ezerk indexe azonos paritású (tehát ha páratlanadik sort és oszlopot hagytuk el), akkor az előjel "+" ellentétes paritás esetén "-" . Az előjelezést így az úgynevezett "sakktáblaszabály" adja:
![[Pasted image 20251012121621.png]]
# Tétel(Kifejtési tétel)
Ha egy sor minden elemét megszorozzuk a hozzá tartozó előjeles aldeterminánsal az így kapott szorzatoknak az összege a determinánssal egyenlő:
![[Pasted image 20251012121830.png]]
Ezt hívjuk a determináns *i*-edik sor szerinti kifejezésének. Természeteseb hasonló állítás érvényes sorok helyett oszlopokra is.
![[Pasted image 20251012122004.png]]
## Bizonyítás:
Tekintsük a detA= D determináns definíció szerinti felírását. Az *n*-tényezős szorzatokat csoportosítjuk aszerint hogy az *i*-edik sorból melyik elem szerepel bennük. Ezt a közös elemet kiemelve a determináns *D = αi1β1 + αi2β2 + . . . + αinβn* alakban írható. Megmutatjuk hogy bármely *j*-re *βj = Aij .*
Tekintsük most a D determinánsban (rögzített j-re) az αij -t tartalmazó szorzatoknak egy olyan felírását, amikor az αij tényező áll elől. Egy ilyen szorzat általános alakja:
![[Pasted image 20251012122534.png]]
Itt ρ a sorindexeknek, π az oszlopindexeknek megfelelő permutáció (tehát ρ(1) = i, π(1) = j). Ennek a szorzatnak az előjele (a D determinánst definíció szerint előállító összegben) az 1.2.3 Tétel szerint (−1)I(ρ)+I(π) (ahol I(ρ), illetve I(π) az i, ρ(2), . . . , ρ(n), illetve j, π(2), . . . , π(n) permutáció inverziószámát jelöli). Az αij kiemelése után így βj -re az alábbi összeg adódik:
![[Pasted image 20251012122649.png]]
Itt az összegben minden olyan n − 1-tényezős szorzatot kell venni, ahol a tényezők az i-edik sor és j-edik oszlop elhagyásával keletkezett D′ determináns definíciójában szerepelnek. Hasonlítsuk most össze az (1.4.2) jobb oldalán álló összeget (amely βj -vel egyenlő) a D′ determinánst definíció szerint előállító összeggel. Mindkét öszszegben ugyanazokról az n − 1-tényezős szorzatokról van szó. Vizsgáljuk meg, hogy egy ilyen szorzatot milyen előjellel kellene venni a D′ determináns kiszámításához. Ismét az 1.2.3 Tétel szerint ehhez meg kell nézni, hány inverzió fordul elő a sorindexek, valamint az oszlopindexek permutációjában együttvéve. Ezeket az inverziókat nem befolyásolja, ha a sorok és oszlopok számozásánál megtartjuk az eredeti, D-beli sor-, illetve oszlopszámokat (vagyis a sorokra 1, 2, . . . , i−1, i+ 1, . . . , n-et, az oszlopokra pedig 1, 2, . . . , j −1, j + 1, . . . , n-et). Ennek megfelelően a sorindexeknél a ρ ′ = ρ(2)ρ(3). . . ρ(n) permutáció inverziószámát, I(ρ ′ )-t, az oszlopindexeknél pedig a π ′ = π(2)π(3). . . π(n) permutáció inverziószámát, I(π ′ )-t kell tekinteni. (Tehát ρ ′ az 1, 2, . . . , i − 1, i+1, . . . , n számoknak a sorindexek szerinti permutációja, π ′ pedig az 1, 2, . . . , j − 1, j + 1, . . . , n számoknak az oszlopindexek szerinti permutációja.) Az (1.4.1)-ben szereplő eredeti ρ permutációt úgy nyerjük, ha ρ ′ = = ρ(2)ρ(3). . . ρ(n) elé ρ(1) = i-t írunk. Ezért I(ρ) annyival nagyobb I(ρ ′ )-nél, ahány elemmel ρ(1) = i inverzióban áll. Ezek az elemek nyilván éppen az i-nél kisebb számok, tehát I(ρ) = I(ρ ′ ) + (i − 1). Ugyanígy I(π) = I(π ′ ) + (j − 1). Az előzőkből I(ρ) +I(π) = i+j −2 +I(ρ ′ ) +I(π ′ ) adódik. Ezt (1.4.2)-be behelyettesítve kapjuk, hogy: 
![[Pasted image 20251012122748.png]]
# Tétel (ferde kifejezés)
Ha egy sor elemeit rendre egyik másik sorhoz tartozó előjeles aldeterminánsokkal szorozzuk meg az így kapott szorzatoknak az összege mindig 0:
![[Pasted image 20251012122959.png]]
**FIGYELEM!**
A kifejezés szó itt megtévesztő mert az összeg értékének semmi köze sincs az eredeti determinánshoz ez az összeg  mindig 0 függetlenül attól hogy maga a determináns 0 vagy sem
## Bizonyítás:
Egy másik determinánst fogunk készíteni és arra alkalmazzuk majd a kifejezési tételt. Tekintsük azt az A' mátrixot amelynek a *k*-adik sora ugyan az mint az eredeti determináns *r*-edik sora, a többi eleme pedig azonos az eredeti determináns megfelelő elemével. Azaz:
![[Pasted image 20251012123523.png]]
A'-ben a *k*-adik és az *r*-edik sor egyenéő (mindkettő az eredeti determináns *r*-edik sora) ezért det A'=0. Ha most ezt a determinánst a *k*-adik sora szerint kifejtjük akkor felhasználva hogy A-ban és A' ben a *k*-adik sorhoz tartozó Akj és A'kj előjeles aldeterminánsok minden *j*-re megegyeznek éppen a tételbeli összeget kapjuk:
![[Pasted image 20251012123947.png]]
# Definíció
Legyen γ1, γ2, . . . , γn tetszőleges. A γ1, γ2, . . . , γn elemek által generált Vandermonde-determináns
![[Pasted image 20251012124108.png]]
A Vandermonde-determináns i-edik sorában tehát rendre γi-nek 0, 1, . . . , n − 1-edik hatványa áll. Ha két generáló elem azonos, akkor két egyforma sor van, és így a determináns 0. Az alábbi szorzatalakból kiderül, hogy ennek a megfordítása is igaz.
# Tétel
![[Pasted image 20251012124228.png]]
## Bizonyítás:
Vonjuk ki jobról balra haladva minden oszlopból az őt megelőző oszlop *γ1*-szerzését:
![[Pasted image 20251012124400.png]]
Most vonjuk le minden sorból az első sort ezzel az első oszlop utolsó n-1 eleme is 0 lesz, a többi elem nem változott. A második , harmadik, stb. sorból rendre γ2 − γ1-et, γ3 − γ1-et stb. kiemelhetünk. Ezzel a
![[Pasted image 20251012124633.png]]
alakra jutottunk.  Ígya a feladatot egy eggyel kissebb rendű Vandermonde determinánsra vezettük vissza. A fenti eljárást megismételve (vagy teljes indukcióval) adódik a tétel.

##### forrás: 
https://freud.web.elte.hu/linalkonyv24.pdf (11-39)
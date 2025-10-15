A mátrixok szorosan kapcsolódnak a determinánsok illetve a lineáris egyenletrendszerek elméletéhez de ezektől függetlenül id számos alkalmazásuk van. Különösen érdekes és fontos a mátrixszámolás és annak néhány "szokatlan" tulajdonsága. Ezeknek a "furcsaságoknak" az egyik "igazi" magyarázatát majd a lineáris leképezésekkel való kapcsolat adja.
## Mátrixműveletek
## Definíció
Legyen *T* egy kommutatív test és *k,n* adott pozitív egészek. Ekkor a *T* test feletti *k x n*-es mátrixon egy olyan téglalap alakú táblázatot értünk, amelyeknek *k* sora és *n* oszlopa van amelynek elemei *T*-ből valók.
A mátrixot úgy jelöljük, hogy a táblázatot gömbölyű zárójelek közé foglaljuk. (Ismét felhívjuk a figyelmet arra, hogy a két függőleges határolóvonal a determinánst jelenti.) Egy általános A mátrix i-edik sorának j-edik elemét αij -vel fogjuk jelölni. Ennek megfelelően egy k × n-es (vagy k × n méretű) mátrix általános alakja
![[Pasted image 20251012151936.png]]
A T feletti k × n-es mátrixok halmazát T k×n-nel jelöljük. Itt is megjegyezzük, hogy általános T test helyett első közelítésben legtöbbször nyugodtan gondolhatunk pl. a valós, a racionális vagy a komplex számokra. Emellett azonban — különösen az alkalmazások szempontjából — nagyon fontosak a véges testek is. Ezek legegyszerűbb fajtája Fp, a modulo p maradékosztályok teste, ahol p prímszám. Most két mátrix összeadását, illetve egy mátrixnak egy T-beli elemmel való szorzását definiáljuk. Ezeknek a műveleteknek az értelmezése a ,,természetes módon”, elemenként történik a T-beli összeadás és szorzás segítségével:
## Definíció
Legyen A, B ∈ T k×n, λ ∈ T. Ekkor A + B-t illetve λA-t úgy kapjuk meg, hogy a megfelelő helyeken álló elemeket összeadjuk, illetve minden elemet e λ-val megszorozzuk:
![[Pasted image 20251012152206.png]]
és
![[Pasted image 20251012152222.png]]
A *T* test elemeit szokás skalároknak nevezni és így egy mátrixnak egy *T*-beli elemmel vett szotzatát a mátrix skalárszorzatának hívjuk. Az imént definiált műveletekre a megszokott tulajdonságok érvényesek.
# Tétel
A *kxn*-es mátrixok körében az összeadás asszociatív, kommutatív, létezik nullaelem és minden elemnek létezik ellentetje. Ez részletesen kifejtve a következőket jelenti:
![[Pasted image 20251012153133.png]]
Az összeadásra nézve egy kommutatív csoportot alkotnak. A két együttesen T^kxn felett
## Bizonyítás:
Valamennyi tulajdonság azonnal adódik a műveletek definíciójából és a *T*-beli megfelelő tulajdonságból. Például a 0 mátrix (nullmátrix) az lesz, amelynek minden eleme (a *T*-beli) nulla stb.
(41.oldal)

##### forrás: 
https://freud.web.elte.hu/linalkonyv24.pdf (39-56)
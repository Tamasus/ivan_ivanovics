#Def: A valós számsorozat (sorozat) a természetes számok halmazán értelmezett valós értékű függvény
Megjegyzés:    f:IN -> IR
jelölés:
an -> általános eleme a sorozatnak.
![[Pasted image 20250929181638.png]]
## Sorozatok megadása:
### a.) Általános elemmel:
![[Pasted image 20250929185042.png]]
### b.) Rekurzív módon:
(néhány elemet rögzítünk)
Az általános elemet a rögzített elemek felhasználásával adjuk meg

**Példa:**
Fibonachi-sorozat:
a=1,a2=1
an=an-1+an-n ha n>=3

### c.)  Szöveges utasítás
**Példa**: A sorozat n-edik eleme legyen az n-edik prímszám négyzetgyöke

#Def: Legyen
![[Pasted image 20250929185537.png]]
adott sorozat azt mondjukk hogy an alulról korlátos ha létezik k E IR amelyre k=<3 ha n E IN esetén.
Felülről korlátos ha létezik k E IR amelyre an =< k  ha n E IN
Azt mondjuk hogy korlátos ha alulról és felülről is korlátos

#### Megjegyzés:
1. Ha van alsókorlát akkor abból megszámlálhatatlanul végtelen van
2. Ha felülről korlátos akkor megszámlálhatatlanul végtelen felsőkorlátja van
3. A korlátosság vizsgálata során legalább egy alsó és legalább egy felső korlát megadása a cél ha van ilyen

#Def:Legyen {an}
1. Alulról korlátos sorozat. A sorozat alsó korlátai közül a legnagyobbat a sorozat legnagyobb alsó korlátjának (pontos alsó korlátjának, infinumának) nevezzük
Jele: inf{an}
2. Felülről korlátos sorozat. A sorozat felső korlátjai közül a legkissebbet a sorozat legkissebb felső korlátjának (pontos felső korlátjának supremumának) nevezzük
Jele: sup{an}

#Def: Azokat a sorozatokat amelyekben az elemek váltakozva követik egymást alternáló sorozatnak nevezzük

#Def: A {bn} sorozatot az {an} sorozat rész sorozatának nevezzük ha az eredeti sorozatból a {bn} sorozat véges vagy megszámlálhatóan végtelen eleme törlésével előálítható úgy hogy a nem törölt elemek sorrendjét nem változtatjuk meg

#Def: A T E IR számot az {an} sorozat torlódási pontjának nevezzük ha tetszőlegesen kicsiny sugarú környezetében a sorozat megszámlálhatóan végtelen eleme megtalálható

Megjegyzés:
1. Van olyan sorozat aminek nincs torlódási pontja pl.: {n}
2. Vannak olyan sorozatok amelyeknek több torlódási pontjuk is van
![[Pasted image 20250930191132.png]]

#Def:
1. Legyen {an} adott sorozat {an} monoton növekvő ha n,m E IN esetén ha n=< m akkor an=< am
   Szigorúan monoton nő ha an < am
2. Monoton csökkenő ha n,m E IN re ahol n=<m fennáll hogy an >=am
   Szigoruan monoton csökken ha an > am
Megjegyzés:
A monotonítás vizsgálatakor (an-an+1) két egymás melletti elem különbségének előjelét vizsgáljuk (an+1-an)

#Def: Vizsgáljuk monotonitás szempontjából az:
#füzet 
Megjegyzés: vannak olyan sorozatok amik nem rendelkeznek monotonitási tulajdonsággal
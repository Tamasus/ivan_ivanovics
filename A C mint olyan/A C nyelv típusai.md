Típus: 
A változótárolásához szükséges memóriaterületet méretet és tárolt értéket értelmezédét hstározzs mrg.
![[Pasted image 20250927163828.png]]
**Enum:** Olyan adattípus melynek értékei egy konstanshalmazból kerülnek ki.
- Ezek int típusú szimbilokus konstansok: alapértelmezés szerint balról jobbra nulláról kezdve egész értéket reprezentálnak
**enum answer {NO, YES, MAYBE};**
	A konstansok értéke a megadott sorrendben 0,1,2
- Ha a felsorolásban az egyik konstans értéke meg van adva (ez lehet negatív érték is), a tőle jobbra esők ettől a kiindulási értéktől kezdődően kapnak egyesével növekvő értéket. Azonos érték többször is szerepelhet!
**{enum ansver {NO=10, YES, MAYBE=10};**
	A konstansok értéke itt balrol jobbra 10, 11, 10
![[Pasted image 20250928103848.png]]
## Típuselőírások:
- Típusnevek:
**char,int,float,double,enum,struct,union**
- Üres típus (csak függvényekkel): void
## Típusmódosítók:
 - A tárolási hosszra vanatkozó : short, long
 - Az előjel értelmezését határozza meg: signed, unsigned
### Miért van szükség a típusmódosítókra?
A **char** és az **int** típus értelmezése függ a C nyelv implementációjától (HW+OS). Típusmódosítókkal olyan programok írhatók amelyek ugyanúgy futnak a különböző típusu számítógépeken.
![[Pasted image 20250928114529.png]]
## Típusminősítők:
- A **const** kulcsszóval olyan változót deklarálhatunk amelynek értéke futási időben nem változtatható meg (csak olvasható, konstans változó).
![[Pasted image 20250928114722.png]]
- A **volatile** típusminősítővel olyan változó hozható létre, amelynek értékét a programtól független kód is megváltoztathatja.

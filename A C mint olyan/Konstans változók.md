#### Konstans változó:
Olyan változó amelynek értéke futás időben nem változtatható meg (állandó).
**Konstans változó létrehozása:**
1. A **const** típusminősítő megadásával a változó definíciójában. DE az ilyen változó értéke indirekt módon (mutatók segítségével) megváltoztatható!
2. **Konstans makrók** (szimbolikus konstansok) használatával. CSak abban a forrásfájlban láthatók ahol definiáljuk őket.
3. Az **enum** típus használatával. Csak egész (int) típusú konstansok esetén alkalmazható. Igazi konstansok, mert a fordító nem tárolja ezeket a memóriában (így nem változtatható meg az értékük).

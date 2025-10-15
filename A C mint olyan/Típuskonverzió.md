**Mikor van rá szükség?**
- Kifejezések kiértékelésekor ha kétoperandusú operátor különböző típúsú operandusokkal rendelkezik ( a művelet elvégzéséhez azonos típúsúnak kell lenniük).
- Függvények megfelelő argumentummal történő meghívásához.
**Típusai:**
- Implicit(automatikus): a fordító végzi, rögzített szabályok alapján.
- Explicit(kikényszerített): a programoző írja elő a típuskonverziós operátor (cast) segítségével.
![[Pasted image 20250928143529.png]]
Magyarázat: a és b egészek ezért az osztás eredménye is egész mivel a c double (valós) típúsú, értékadáskor implicit típuskonverziót végez a C fordító
![[Pasted image 20250928143656.png]]
Magyarázat: 'a' típúsát explicite valósta változtatjuk így az osztás művelet eredménye is valós. Értékadáaskor nincs szükség konverzióra.
## Implicit típuskonverzió szabályai:
#### Általános szabály:
"Szűkebb" adattípus információvesztés nélkül konvertálódik "szélesebb" adattípusra.
- Az ekész típusuk int-re konvertálódnak
- Az egész típus mindig átalakítható leebegőpontos típussá
- Lebegőpontos típus egész típusra alakításakor a törtrész elvész
- A kétoperandusú műveletek többsége az operandusait és az eredményt a legnagyobb közös típusra konvertálja
- 
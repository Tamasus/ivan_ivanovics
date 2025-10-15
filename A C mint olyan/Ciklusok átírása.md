[[Ciklus utasítások]]
- A while ciklus speciális esete ezért a for és a while ciklusok egymásba átírhatók
- DE a ciklustörzsben kiadott continue utasírás hatása eltérő lehet:
	- While ciklusban : a köv iteráció a feltétel_kif kiértékelésével kezdődik
	- for ciklusban: a köv.iteráció megkezdése előtt kiértékelődik a következő iteráció megkezdése előtt kiértékelődik a léptető_kif majd a következő iteráció a feltétel_kif feldolgozásával kezdődik
# A continue hatása
Csak páros számokat írjuk ki 10 től visszafelé
![[Pasted image 20251010140135.png]]
![[Pasted image 20251010140157.png]]
# A do-while ciklus
Az utasítás végrehajtását követi a vezérlőfeltétel kiértékelése ezért legalább egyszer mindig végrehajtódik a ciklusmag (hátultesztelő ciklus). Ha a feltétel igaz (értéke nem nulla), új iteráció kezdődik; ha hamis a ciklus befejeződik
![[Pasted image 20251010140427.png]]
![[Pasted image 20251010140434.png]]

![[Pasted image 20251010140448.png]]


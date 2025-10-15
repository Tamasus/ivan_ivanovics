**A ciklus utasítások egymásba ágyazhatók**
1. A külső ciklus vezérlőfeltétele kiértékelődik
2. Kiértékelődik a belső ciklus vezérlő feltétele és amíg igaz ismétlődnek a belső ciklus utasításai
3. Amikor a belső ciklus vezérlő feltétele hamissá válik a külső ciklus vezérlő feltétele újból kiértékelődik. Ha igaz új iteráció kezdődik
4. Amikor a külső ciklus vezérlő feltétele hamissá válik a beágyazott ciklus befejezi a működését
![[Pasted image 20251012095918.png]]
- Legyen a külső ciklus iterációk száma N, a belső cikluss iterációk száma M. A külső ciklus egy iterációja alatt a belső ciklus M iterációja fut le, és ez ismétlődik N-szer. Így az összes iterációk száma NxM
![[Pasted image 20251012100158.png]]
![[Pasted image 20251012100212.png]]
![[Pasted image 20251012100226.png]]
- Háromszoros beágyazás. Az összes iterációk száma: KxNxM
![[Pasted image 20251012100311.png]]

## Vegyük észre e következő absztakciókat
- A *soron következő instrukció* koncepció egy instrukció folyam (instruction stream) képzetet ad
- Ezen folyamon egy mutató mutathatja a soron következő elemet Ez a mutató a programszámláló regiszter 
- Az instrukció folyam instrukcióinak hészlete vezérlési állapotteret határoz meg. Ebből egy állapotot az ad meg hogy az i edik lépésben mely instrukciót hajtja végre a processzor
- Létezik számunkra egy adatfolyam is: a memória rekesznek és regisztereknek az a sora mely az egymás utáni instrukciókban operandusként szerepelnek
- Az adatfolyam elemei adat állapotteret határoznak meg
- egy-egy instrukció végrehajtása állapot válltozást hoz
## Az instrukció folyam végrehajtása
- A program(az instrukció folyam kód) futása állapot-átmenetek láncolatát hozza
- A vezérlés állapot-átmenet láncolat kulcsjellemzője a programszámláló regiszter egymás utáni értékei:
	- A vezérlés menete(Flow of control) (processz vagy thread szál fogalom)ű
- A Neumann elvű gépekre jellemző ez az egy vezérlésmenet (Single Instruction Stream) egy adatfolyamon (on Single Data Stream) SISD
## Állapotfüggés
- Hogy egy instrukció milyen állapotba "billent" az függ az előző állapottól
- Állapot érzéken a Neumann gép
- El tudunk-e képzelni állapot független gépet?

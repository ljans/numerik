## FPI
Programm zur Durchführung von Fixpunktiterationen.

### Eingabe
- Y<sub>1</sub>: Fixpunktiteration *&varphi;(x)*
- Startwert *x<sub>0</sub>*
- Anzahl Iterationen *n*

### Ausgabe
- Alle Iterierten *x<sub>k</sub> = &varphi;(x<sub>k-1</sub>)* für *k = 1, ..., n*
- Konvergenzordnung *p*
- Schätzung der Lipschitzkonstanten *L*
- A posteriori Fehlerschätzer *e = ||x<sub>k</sub> - x&ast;||*
- Aitken-Beschleunigung *x&ast;*

### Beispiel
- Y<sub>1</sub> = (6+X)^(1/3)
- x<sub>0</sub> = 6
- n = 3

## LGSITER
Programm zur iterativen Lösung linearer Gleichungssysteme der Form *Ax=b*.
Zur Auswahl stehen die folgenden Verfahren:
- Gauß-Seidel / Einzelschritt
- Jacobi / Gesamtschritt

### Eingabe
- [A]: Matrix *A*
- [B]: Rechte Seite *b*
- [C]: Startwert *x<sub>0</sub>*

### Ausgabe
- Berechnung der Iterationsmatrix *M*
- Berechnung des Vektors *d*
- Konvergenztest und Berechnung der Lipschitz-Konstanten *L* in Zeilensummennorm *|| &middot; ||<sub>&infin;</sub>* oder Spaltensummennorm *|| &middot; ||<sub>1</sub>*
- Erste Iterierte *x<sub>1</sub> = Mx<sub>0</sub> + d*

### Modus: Iteration
Zusätzliche Ausgabe
- Nächste Iterierte *x<sub>k+1</sub> = Mx<sub>k</sub> + d*

### Modus: A priori
#### Zusätzliche Eingabe
- Toleranz *||x<sub>k</sub> - x&ast;|| &leq; &varepsilon;*

#### Zusätzliche Ausgabe
- Mindestanzahl an Schritten *k* zum Erreichen der Toleranz

### Modus: A posteriori
#### Zusätzliche Ausgabe
- Fehlerschätzung *||x<sub>k</sub> - x&ast;||* auf Grundlage der letzten beiden Iterierten *x<sub>k</sub>* und *x<sub>k-1</sub>*

### Modus: Wechseln
Ermöglicht, das Verfahren zwischen Iterationsschritten zu wechseln.

### Beispiel
- `[A] = [[100,1,1,1,1][1,100,1,1,1][1,1,100,1,1][1,1,1,100,1][1,1,1,1,100]]`
- `[B] = [[96][97][98][99][100]]`
- `[C] = [[1][1][1][1][1]]`

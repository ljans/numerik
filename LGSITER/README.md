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
- Neue Iterierte *x<sub>k+1</sub> = Mx<sub>k</sub> + d*

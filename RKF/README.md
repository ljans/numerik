## RKF
Runge-Kutta-Fehlberg-Verfahren zur Lösung von Anfangswertproblemen der Form *y'(t) = f(t,y(t))* mit *y(t<sub>0</sub>)=y<sub>0</sub>*.

### Eingabe
- Y<sub>1</sub>: *f*(T,Y)
- Startzeitpunkt *t<sub>0</sub>*
- Startwert *y<sub>0</sub>*
- Schrittweite *h*
- Anzahl Schritte *m*
- Optional: Butcher-Tableau *a=*[A], *B*=[B], *c*=[C]

### Ausgabe
- Optional: Bedingungsgleichungen der Konvergenzordnung für *p=1,2,3*
- Alle Iterationsschritte mit Formeln und Zwischenergebnissen

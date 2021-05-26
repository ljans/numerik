## RKF
Runge-Kutta-Fehlberg-Verfahren zur Lösung von Anfangswertproblemen der Form *y'(t) = f(t,y(t))* mit *y(t<sub>0</sub>)=y<sub>0</sub>*.
Grundlage des Verfahrens ist ein Butcher-Tableau, das in den Matrizen [A], [B] und [C] gespeichert wird.

### Modus: Konvergenzordnung analysieren
Prüft die Bedingungsgleichungen der Konvergenzordnung *p = 1* bis *p = 4*.

### Modus: Runge-Kutta
#### Eingabe
- Y<sub>1</sub>: *f*(T,Y)
- Startzeitpunkt *t<sub>0</sub>*
- Startwert *y<sub>0</sub>*
- Schrittweite *h*
- Anzahl Schritte *m*

#### Ausgabe (für jeden Iterationsschritt *n = 1, ..., m*)
- Funktionsauswertungen *k<sub>i</sub>*
- Verfahrensfunktion *&varphi;<sub>c</sub>*
- Neue Iterierte *y<sub>n</sub>*

### Modus: Runge-Kutta mit Fehlberg-Trick
#### Zusätzliche Eingabe
- [D]: Integrationsgewichte für den Fehlberg-Trick

#### Zusätzliche Ausgabe (für jeden Iterationsschritt)
- Verfahrensfunktion *&varphi;<sub>d</sub>*
- Neue Iterierte *z<sub>n</sub>*
- Fehlerschätzer *e = |1 - z<sub>n</sub>/y<sub>n</sub>|*

### Beispiel
- `[A] = [[0][.5][.75]]`
- `[B] = [[0,0,0][.5,0,0][0,.75,0]]`
- `[C] = [[2/9,1/3,4/9]]`
- `[D] = [[7/24,1/4,1/3,1/8]]`
- *t<sub>0</sub> = 0*
- *y<sub>0</sub> = 1*
- *h = 0.2*
- *m = 1*

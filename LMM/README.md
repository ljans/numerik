# LMM
Explizite lineare Mehrschrittmethoden zur iterativen Lösung von Differenzialgleichungen der Form *y'(t) = f(t,y(t))* mit gegebener Vorlaufsrechnung.


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Belegung
----- | --------
`Y₁`  | Funktion *f*(`T`,`Y`)


## Ablauf
- Das Programm fordert zur Eingabe der folgenden Werte auf:
	- Startzeitpunkt *t<sub>0</sub>*
  - Schrittweite *h*
  - Stufenzahl *m*
  - Parameter *&alpha;<sub>0</sub>* bis *&alpha;<sub>m</sub>*
  - Parameter *&beta;<sub>0</sub>* bis *&beta;<sub>m-1</sub>*
  - Vorlaufwerte *y<sub>0</sub>* bis *y<sub>m-1</sub>*
- Die Funktionsauswertungen *f<sub>0</sub>* bis *f<sub>m-1</sub>* werden ausgegeben.
- Das Programm fordert zur Wahl einer der im Folgenden beschriebenen Aktionen auf.


### Aktion: Zeitschritt
- Der nächste Wert *y<sub>m</sub>* und die Funktionsauswertung *f<sub>m</sub>* werden ausgegeben


### Aktion: Konsistenzord.
- Die Prüfung der Konsistenzordnung wird ausgegeben.


### Aktion: Stabilitaet
- Das erste charakteristische Polynom wird geplottet.


## Beispielsetup
- Y<sub>1</sub>(T,Y)=T+Y
- t<sub>0</sub>=0.4
- h=0.05
- m=2
- &alpha;<sub>0</sub>=0
- &alpha;<sub>1</sub>=-1
- &alpha;<sub>2</sub>=1
- &beta;<sub>0</sub>=-0.5
- &beta;<sub>1</sub>=1.5
- y<sub>0</sub>=4.509822
- y<sub>1</sub>=4.755313


## Arbeitsspeicher
Feld   | Belegung
------ | -------
`A`    | Startwert *t<sub>0</sub>*
`B`    | Zwischenspeicher
`H`    | Schrittweite *h*
`I`    | Schleifenindex
`J`    | Schleifenindex
`M`    | Stufenzahl *m*
`P`    | Konsistenzordnung *p*
`R`    | *&beta;*-Summe
`S`    | *&alpha;*-Summe
`T`    | Funktionsparameter *t*
`Y`    | Funktionsparameter *y*
`Z`    | Zwischensumme
`[G]`  | *f*-Vektor
`[H]`  | *&alpha;*-Vektor
`[I]`  | *&beta;*-Vektor
`[J]`  | *y*-Vektor
`Str1` | Zwischenspeicher
`Str0` | Zwischenspeicher
`Y₀`   | Charakteristisches Polynom

# EIGNWERT
Ermittelt die (reellen) Eigenwerte *&lambda;* einer Matrix *A* &in; &reals;<sup>*n*&times;*n*</sup>.


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Belegung
----- | --------
`[A]` | Matrix *A*


## Ablauf
Folgende Schritte werden für alle *n* Eigenwerte wiederholt:

1. Der Graph des charakteristischen Polynoms wird angezeigt.
2. Das Programm wartet, bis der Cursor in die Nähe einer Nullstelle bewegt und der Punkt mit <kbd>ENTER</kbd> bestätigt wird.
3. Der entsprechende Eigenwert wird ausgegeben.


## Beispielsetup
- A=`[[.5,1,1.5][0,2,2.5][0,0,3]]`


## Arbeitsspeicher
Feld   | Belegung
------ | -------
`K`    | Index
`L`    | Eigenwert *&lambda;*
`N`    | Dimension *n*
`[I]`  | Einheitsmatrix
`Y₀`   | Charakteristisches Polynom
`∟DIM` | Dimensionsliste {*n,n*}

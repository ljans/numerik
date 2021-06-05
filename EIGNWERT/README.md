# EIGNWERT
Ermittelt die (reellen) Eigenwerte *&lambda;* einer Matrix *A* &in; &reals;<sup>*n*&times;*n*</sup>.


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Typ    | Belegung
----- | ------ | --------
`[A]` | Matrix | *A*


## Ablauf
Folgende Schritte werden für alle *n* Eigenwerte wiederholt:

- Der Graph des charakteristischen Polynoms wird angezeigt.
- Das Programm wartet, bis der Cursor in die Nähe einer Nullstelle bewegt und der Punkt mit <kbd>ENTER</kbd> bestätigt wird.
- Der entsprechende Eigenwert wird ausgegeben.

## Beispiel
```
A=[[.5,1,1.5][0,2,2.5][0,0,3]]
```

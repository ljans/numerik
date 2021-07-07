# GRAD
Gewöhnliches und konjugiertes Gradientenverfahren zur iterativen Lösung linearer Gleichungssysteme der Form *Ax = b* mit *A* &in; &reals;<sup>*n*&times;*n*</sup>.


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Belegung
----- | --------
`[A]` | Matrix *A*
`[B]` | Rechte Seite *b*
`[C]` | Startwert *x<sub>0</sub>*


## Ablauf
Zunächst wird die Berechnung des anfänglichen Residuums *r<sub>0</sub>* ausgegeben.
Zu Beginn jedes Iterationsschritts fordert das Programm dann zur Wahl zwischen gewöhnlichem oder konjugiertem Gradientenverfahren auf und führt anschließend durch die folgenden Berechnungen:
1. Suchrichtung
1. Line search
1. Neue Iterierte
1. Neues Residuum


## Beispielsetup
- A=`[[1,-1][-1,2]]`
- b=`[[1][1]]`
- x<sub>0</sub>=`[[1][0]]`


## Arbeitsspeicher
Feld   | Belegung
------ | -------
`C`    | 0 = gewöhnlich, 1 = konjugiert
`K`    | Iteration *k*
`N`    | Dimension *n*
`Q`    | Line search Parameter *&alpha;* bzw. *&lambda;*
`R`    | Vorheriges Skalarprodukt des Residuums
`S`    | Aktuelles Skalarprodukt des Residuums
`[D]`  | Arbeitsvektor *x*
`[G]`  | Nullvektor
`[H]`  | Produkt von Matrix *A* und Suchrichtung
`[I]`  | Suchrichtung *d*
`[J]`  | Residuum *r*
`Str8` | Index *<sub>k-2</sub>*
`Str9` | Index *<sub>k-1</sub>*
`Str0` | Index *<sub>k</sub>*
`∟DIM` | Dimensionsliste {*n,n*}

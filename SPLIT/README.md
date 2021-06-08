# SPLIT
Löst lineare Gleichungssysteme der Form *Ax = b* durch Splitting der Matrix *A* &in; &reals;<sup>*n*&times;*n*</sup> in *A = D + L + R*.
Zur Auswahl stehen die folgenden Verfahren:

- Gauß-Seidel / Einzelschritt
- SOR (Successive Over-Relaxation)
- Jacobi / Gesamtschritt


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Belegung
----- | --------
`[A]` | Matrix *A*
`[B]` | Rechte Seite *b*
`[C]` | Startwert *x<sub>0</sub>*


## Ablauf
- Das Programm fordert zur Wahl eines Verfahrens auf.
- Die Berechnung der Matrizen *M* und *N* wird ausgegeben.
- Um die Konvergenz des Verfahrens nachzuweisen, wird eine Lipschitz-Konstante *L < 1* gesucht.
  1. Zunächst wird getestet, ob die Zeilensummennorm *||M||<sub>&infin;</sub>* geeignet ist.
  1. Falls nicht, wird die Spaltensummennorm *||M||<sub>1</sub>* getestet.
  1. Sind beide ungeeignet, fordert das Programm zur Eingabe der Spektralnorm *||M||<sub>2</sub>* auf.
- Die Berechnung der ersten Iterierten *x<sub>1</sub> = Mx<sub>0</sub> + Nb* wird ausgegeben.
- Das Programm fordert zur Wahl einer der im Folgenden beschriebenen Aktionen auf.


### Aktion: iterieren
- Die Berechnung der nächsten Iterierten *x<sub>k</sub> = Mx<sub>k-1</sub> + Nb* wird ausgegeben.


### Aktion: a-priori
- Das Programm fordert zur Eingabe einer Toleranz *&varepsilon; &geq; ||x<sub>k</sub> - x&ast;||* auf.
- Eine hinreichende Anzahl an Iterationsschritten *k* zum Erreichen der Toleranz wird ausgegeben.


### Aktion: a-posteriori
- Eine Fehlerschätzung für *||x<sub>k</sub> - x&ast;||* auf Grundlage der letzten beiden Werte *x<sub>k</sub>* und *x<sub>k-1</sub>* wird ausgegeben.


### Aktion: beenden
- Das Programm wird beendet.


## Beispielsetup
- A=`[[100,1,1,1,1][1,100,1,1,1][1,1,100,1,1][1,1,1,100,1][1,1,1,1,100]]`
- b=`[[96][97][98][99][100]]`
- x<sub>0</sub>=`[[1][1][1][1][1]]`
- &varepsilon;=0.0001


## Arbeitsspeicher
Feld   | Belegung
------ | --------
`C`    | Zwischensumme
`D`    | Zwischenergebnis
`E`    | Toleranz *&epsilon;*
`I`    | Schleifenindex
`J`    | Schleifenindex
`K`    | Iteration *k*
`N`    | Dimension *n*
`P`    | Index der *p*-Norm *&#124;&#124; &middot; &#124;&#124;<sub>p</sub>*
`S`    | Spaltensumme
`W`    | Relaxationsparameter *&omega;*
`Z`    | Zeilensumme
`[D]`  | Wert *x<sub>k</sub>*
`[E]`  | Wert *x<sub>k-1</sub>*
`[F]`  | Iterationsmatrix *M*
`[G]`  | Matrix *N*
`[H]`  | Matrix *D*
`[I]`  | Matrix *L*
`[J]`  | Matrix *R*
`Str9` | Index *<sub>k-1</sub>*
`Str0` | Index *<sub>k</sub>*
`∟DIM` | Dimensionsliste {*n,n*}

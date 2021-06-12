# FAKTOR
Matrixfaktorisierungen zur direkten Lösung linearer Gleichungssysteme der Form *Ax = b* mit *A* &in; &reals;<sup>*n*&times;*n*</sup>.


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Belegung
----- | --------
`[A]` | Matrix *A*
`[B]` | Rechte Seite *b*


## Ablauf
- Das Programm fordert zur Wahl einer der folgenden Faktorisierungen auf:
  - **LR (Gauß)** mit linker unterer Dreiecksmatrix *L* und rechter oberer Dreiecksmatrix *R*
  - **LL<sup>T</sup> (Cholesky)** mit linker unterer Dreiecksmatrix *L*
  - **QR (GS)** mit orthogonaler Matrix *Q* und rechter oberer Dreiecksmatrix *R*
- Je nach Faktorisierung werden die erforderlichen Umformungen mit Zwischenergebnissen ausgegeben.
- Die Berechnung der Lösung *x* wird ausgegeben.


## Arbeitsspeicher
Feld   | Belegung
------ | -------
`I`    | Zeilenindex
`J`    | Spaltenindex
`K`    | Zeilenindex
`N`    | Dimension *n*
`S`    | Zwischensumme
`[G]`  | Lösungsvektor
`[I]`  | Arbeitsmatrix
`[J]`  | Arbeitsmatrix
`Str9` | Gleichungsindex
`Str0` | Gleichungsindex
`∟DIM` | Dimensionsliste {*n,n*}

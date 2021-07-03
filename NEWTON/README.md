# NEWTON
Newton-Verfahren zur iterativen Lösung von nicht-linearen Gleichungssystemen der Form *F*(*x*) = *0* mit *x* &in; &reals;<sup>2</sup>.


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Belegung
----- | --------
`Y₁`  | Erste Komponente *F<sub>1</sub>*(`X`,`Y`)
`Y₂`  | Zweite Komponente *F<sub>2</sub>*(`X`,`Y`)
`[A]` | Startvektor *x<sub>0</sub>*


## Ablauf
- Die folgenden Berechnungen werden zunächst für *k = 0* ausgegeben:
	- Funktionsauswertung *F*(*x<sub>k</sub>*)
  - Jacobi-Matrix &nabla;*F*(*x<sub>k</sub>*)
  - Inverse der Jacobi-Matrix &nabla;*F<sup>-1</sup>*(*x<sub>k</sub>*)
  - Korrektur *s<sub>k</sub>* = &nabla;*F<sup>-1</sup>*(*x<sub>k</sub>*) *F*(*x<sub>k</sub>*)
  - Norm der Korrektur *||s<sub>k</sub>||<sub>2</sub>*
  - Neue Iterierte *x<sub>k+1</sub> = x<sub>k</sub> - s<sub>k</sub>*
- Das Programm fordert zur Wahl einer der im Folgenden beschriebenen Aktionen auf.


### Aktion: iterieren
- Der Iterationszähler *k* wird um eins erhöht und die Berechnungen auf Grundlage der letzten Iterierten wiederholt.


### Aktion: Konvergenzord. (ab *k=2*)
- Das Programm prüft, ob *F* eine Kontraktion ist.
- Falls ja, wird eine Schätzung der Konvergenzordnung ausgegeben.


### Aktion: beenden
- Das Programm wird beendet.


## Beispielsetup
- F<sub>1</sub>(X,Y)=X^2+Y^2+0.6Y-0.16
- F<sub>2</sub>(X,Y)=X^2-Y^2+X-1.6Y-0.14
- x<sub>0</sub>=`[[-0.4][-0.4]]`


## Arbeitsspeicher
Feld   | Belegung
------ | -------
`K`    | Iterationszähler *k*
`R`    | Norm der letzten Korrektur *&#124;&#124;s<sub>k-1</sub>&#124;&#124;*
`S`    | Norm der aktuellen Korrektur *&#124;&#124;s<sub>k</sub>&#124;&#124;*
`X`    | Erste Komponente des Funktionsparameters
`Y`    | Zweite Komponente des Funktionsparameters
`[B]`  | Aktuelle Iterierte *x<sub>k</sub>*
`[G]`  | Korrektur *s*
`[H]`  | Funktionsauswertung *F*(*x<sub>k</sub>*)
`[I]`  | Inverse der Jacobi-Matrix &nabla;*F<sup>-1</sup>*(*x<sub>k</sub>*)
`[J]`  | Jacobi-Matrix &nabla;*F*(*x<sub>k</sub>*)
`Str8` | Index *<sub>k-1</sub>*
`Str9` | Index *<sub>k</sub>*
`Str0` | Index *<sub>k+1</sub>*

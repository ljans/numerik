# FPI
Iterative Lösung und Fehlerschätzung von Fixpunktgleichungen der Form *x = &varphi;(x)*.


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Belegung
----- | --------
`Y₁`  | Funktion *&varphi;(X)*
`L`   | *(optional)* Lipschitz-Konstante *L*


## Ablauf
- Das Programm fordert zur Eingabe des Startwerts *x<sub>0</sub>* auf.
- Die erste Iterierte *x<sub>1</sub> = &varphi;(x<sub>0</sub>)* wird berechnet.
- Das Programm fordert zur Wahl einer der im Folgenden beschriebenen Aktionen auf.


### Aktion: iterieren
- Eine neue Iterierte *x<sub>k</sub> = &varphi;(x<sub>k-1</sub>)* wird berechnet.


### Aktion: a-priori
- Das Programm fordert zur Eingabe einer Fehlertoleranz *&varepsilon; &geq; |x<sub>k</sub> - x&ast;|* auf.
- Eine hinreichende Anzahl an Iterationsschritten *k* zum Erreichen der Toleranz wird berechnet.


### Aktion: a-posteriori
- Eine Fehlerschätzung für *|x<sub>k</sub> - x&ast;|* auf Grundlage der letzten beiden Werte *x<sub>k</sub>* und *x<sub>k-1</sub>* wird berechnet.


### Aktion: beschleunigen
- Das Ergebnis einer Aitken-Beschleunigung auf Grundlage der letzten drei Werte *x<sub>k</sub>* bis *x<sub>k-2</sub>* wird berechnet.


### Aktion: L berechnen
- Die Lipschitz-Konstante wird auf Grundlage der letzten drei Werte *x<sub>k</sub>* bis *x<sub>k-2</sub>* näherungsweise berechnet.


### Aktion: p berechnen
- Die Konvergenzordnung wird auf Grundlage der letzten vier Werte *x<sub>k</sub>* bs *x<sub>k-3</sub>* näherungsweise berechnet.


### Aktion: beenden
- Das Programm wird beendet.


## Beispielsetup
- &varphi;(X)=(6+X)^(1/3)
- x<sub>0</sub>=6


## Arbeitsspeicher
Feld   | Belegung
------ | -------
`A`    | Wert *x<sub>k-3</sub>*
`B`    | Wert *x<sub>k-2</sub>*
`C`    | Wert *x<sub>k-1</sub>*
`D`    | Wert *x<sub>k</sub>*
`E`    | Toleranz *&varepsilon;*
`K`    | Iteration *k*
`L`    | Lipschitz-Konstante *L*
`Str8` | Index *<sub>k-2</sub>*
`Str9` | Index *<sub>k-1</sub>*
`Str0` | Index *<sub>k</sub>*
`Y₁`   | Funktion *&varphi;(X)*

## FPI
Programm zur Durchführung von Fixpunktiterationen.

### Eingabe
- Y<sub>1</sub>: Fixpunktiteration *&varphi;(X)*
- Startwert *x<sub>0</sub>*

### Ausgabe
- Erste Iterierte *x<sub>1</sub> = &varphi;(x<sub>0</sub>)*

### Aktionen
#### Iterieren
Berechnet eine neue Iterierte *x<sub>n</sub> = &varphi;(x<sub>n-1</sub>)*.

#### *p* berechnen
Berechnet die Konvergenzordnung *p* auf Grundlage von *x<sub>n</sub>*, *x<sub>n-1</sub>*, *x<sub>n-2</sub>* und *x<sub>n-3</sub>*.

#### *L* schätzen
Schätzt die Lipschitz-Konstante *L* auf Grundlage von *x<sub>n</sub>*, *x<sub>n-1</sub>* und *x<sub>n-2</sub>*.

#### *L* eingeben
Ermöglicht die manuelle Eingabe der Lipschitz-Konstanten *L*.

#### A priori
Berechnet die minimal notwendige Anzahl Iterationsschritte *k* zu einer angegebenen Toleranz *&varepsilon;* auf Grundlage von *x<sub>n</sub>* und *x<sub>n-1</sub>*.

#### A posteriori
Berechnet eine Fehlerschätzung *|x<sub>n</sub> - x&ast;|* auf Grundlage von *x<sub>n</sub>* und *x<sub>n-1</sub>*.

#### Aitken
Berechnet die Aitken-Beschleunigung auf Grundlage von *x<sub>n</sub>*, *x<sub>n-1</sub>* und *x<sub>n-2</sub>*.

### Beispiel
- Y<sub>1</sub> = (6+X)^(1/3)
- x<sub>0</sub> = 6

# RKF
Explizite Runge-Kutta-Verfahren zur iterativen Lösung von Differenzialgleichungen der Form *y'(t) = f(t,y(t))* mit Anfangswert *y(t<sub>0</sub>) = y<sub>0</sub>*.
Grundlage der Verfahren bildet ihr jeweiliges Butcher-Tableau, das in einen Spaltenvektor *a*, die Matrix *B* und den Zeilenvektor *c* aufgeteilt wird.
Für den Fehlberg-Trick kommt optional noch ein weiterer Zeilenvektor *d* hinzu.


## Setup
Folgende Felder können im Voraus belegt oder beim Start des Programms eingegeben werden:

Feld  | Belegung
----- | --------
`Y₁`  | Funktion *f*(`T`,`Y`)
`[A]` | Vektor *a*
`[B]` | Matrix *B*
`[C]` | Vektor *c*
`[D]` | *(optional)* Vektor *d*

Die Butcher-Tableaus der folgenden Verfahren sind bereits hinterlegt und können direkt verwendet werden:

1. **Euler1&#9656;Heun2** ([Euler-Verfahren][Euler1] eingebettet im [Verfahren von Heun][Heun2])
2. **Euler2** ([Mittelpunktsregel][Euler2])
3. **BS2&#9656;Ralston3** ([Verfahren von Bogacki-Shampine][BS2] eingebettet im [Verfahren von Ralston][Ralston3])
4. **Heun2&#9656;SSPRK3** ([Verfahren von Heun][Heun2] eingebettet im ["Strong Stability Preserving" Runge-Kutta-Verfahren][SSPRK3])
5. **RK4 klassisch** ([Klassisches Runge-Kutta-Verfahren][klassisch])
6. **RK4 3/8-Regel** ([3/8 Regel][3/8])

[Euler1]: https://en.wikipedia.org/wiki/List_of_Runge%E2%80%93Kutta_methods#Forward_Euler "In Wikipedia öffnen"
[Heun2]: https://en.wikipedia.org/wiki/List_of_Runge%E2%80%93Kutta_methods#Heun's_method "In Wikipedia öffnen"
[Euler2]: https://en.wikipedia.org/wiki/List_of_Runge%E2%80%93Kutta_methods#Explicit_midpoint_method "In Wikipedia öffnen"
[BS2]: https://en.wikipedia.org/wiki/List_of_Runge%E2%80%93Kutta_methods#Bogacki%E2%80%93Shampine "In Wikipedia öffnen"
[Ralston3]: https://en.wikipedia.org/wiki/List_of_Runge%E2%80%93Kutta_methods#Ralston's_third-order_method "In Wikipedia öffnen"
[SSPRK3]: https://en.wikipedia.org/wiki/List_of_Runge%E2%80%93Kutta_methods#Third-order_Strong_Stability_Preserving_Runge-Kutta_(SSPRK3) "In Wikipedia öffnen"
[klassisch]: https://en.wikipedia.org/wiki/List_of_Runge%E2%80%93Kutta_methods#Classic_fourth-order_method "In Wikipedia öffnen"
[3/8]: https://en.wikipedia.org/wiki/List_of_Runge%E2%80%93Kutta_methods#3/8-rule_fourth-order_method "In Wikipedia öffnen"


## Ablauf
1. Das Programm fordert zur Eingabe der Anfangswerte *t<sub>0</sub>* und *y<sub>0</sub> = y(t<sub>0</sub>)* auf.
1. Das Programm fordert zur Eingabe der ersten Schrittweite *h* auf.
1. Die erste Funktionsauswertung *k<sub>1</sub> = f(t<sub>0</sub>, y<sub>0</sub>)* wird ausgegeben.
1. Die Berechnung der weiteren Stützstellen gemäß dem Butcher-Tableau sowie die zugehörigen Funktionsauswertungen *k<sub>i</sub>* werden ausgegeben, wobei *i* von *2* bis zur Stufe *s* des Verfahrens läuft.
1. Die Verfahrensfunktion *&varphi; = ck* wird ausgegeben.
1. Das Update *y<sub>n+1</sub> = y<sub>n</sub> + h&varphi;* zum nächsten Schritt *t<sub>n+1</sub> = t<sub>n</sub> + h* wird ausgegeben.
1. Eine weitere Funktionsauswertung *k<sub>s+1</sub> = f(t<sub>n+1</sub>, y<sub>n+1</sub>)* wird berechnet.
1. Das Programm fordert zur Wahl einer der im Folgenden beschriebenen Aktionen auf.


### Aktion: fortschreiten
1. Das Programm fordert zur Eingabe einer neuen Schrittweite *h* auf.
1. Der Wert *k<sub>s+1</sub>* wird im nächsten Schritt als *k<sub>1</sub>* verwendet.
1. Die Schritte 4.-8. des vorherigen Abschnitts werden wiederholt.


### Aktion: Fehlberg-Trick
1. Mit dem um *k<sub>s+1</sub>* erweiterten Vektor *k* wird eine weitere Verfahrensfunktion *&varphi; = dk* ausgegeben.
1. Ein weiterer Wert *z<sub>n+1</sub> = y<sub>n</sub> + h&varphi;* wird ausgegeben.
1. Eine Fehlerschätzung auf Grundlage von *y<sub>n+1</sub>* und *z<sub>n+1</sub>* wird ausgegeben.


### Aktion: p(c) bestimmen
1. Die Prüfung der Konvergenzordnung *p = 1* bis *p = 4* für das Verfahren zum Vektor *c* wird ausgegeben.


## Beispielsetup
- f(T,Y)=Y^2e^(-T)
- a=`[[0][.5][.75]]`
- B=`[[0,0,0][.5,0,0][0,.75,0]]`
- c=`[[2/9,1/3,4/9]]`
- d=`[[7/24,1/4,1/3,1/8]]`
- t<sub>0</sub>=0
- y<sub>0</sub>=1
- h=0.2


## Arbeitsspeicher
Feld   | Belegung
------ | -------
`A`    | Wert *t<sub>n</sub>*
`B`    | Wert *y<sub>n</sub>*
`C`    | Zwischensumme
`H`    | Schrittweite *h*
`K`    | Wert *k<sub>s+1</sub>*
`N`    | Schritt *n*
`P`    | Verfahrensfunktion *&varphi;*
`S`    | Stufe *s*
`T`    | Funktionsparameter *t*
`Y`    | Funktionsparameter *y*
`Z`    | Wert *z<sub>n</sub>*
`[H]`  | Diagonalmatrix von *a*
`[I]`  | Einsmatrix
`[J]`  | Vektor *k*
`Str8` | Index *<sub>n-1</sub>*
`Str9` | Index *<sub>n</sub>*
`Str0` | Index *<sub>i</sub>*
`Y₁`   | Funktion *f*(`T`,`Y`)
`∟DIM` | Dimensionsliste {*s,1*}



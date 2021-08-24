# Numerik
In diesem Projekt werden Programme für die Taschenrechner TI-83 Plus und TI-84 Plus zur Lösung numerischer Fragestellungen gesammelt.
Verfügbar sind die folgenden Verfahren, sortiert nach Anwendungsbereich:

- Direkte Lösung linearer Gleichungssysteme
  - **[Matrix-Faktorisierungen](FAKTOR)**
    - LR (Gauß)
    - LL<sup>T</sup> (Cholesky)
    - QR (Gram-Schmidt)
- Iterative Lösung linearer Gleichungssysteme
  - **[Splitting-Verfahren](SPLIT)**
    - Gauß-Seidel / Einzelschritt
    - SOR (Successive Over-Relaxation)
    - Jacobi / Gesamtschritt
  - **[Gradientenverfahren](GRAD)**
    - Gewöhnliches Gradientenverfahren
    - Konjugiertes Gradientenverfahren
- Iterative Lösung von (nicht-linearen) Gleichungen
  - **[Fixpunktiteration](FPI)**
  - **[Newton-Verfahren](NEWTON)** (im *&reals;<sup>2</sup>*)
- Iterative Lösung gewöhnlicher Differenzialgleichungen
  - **[Explizite Runge-Kutta-Verfahren](RKF)** (für Anfangswertprobleme)
    - Euler-Verfahren
    - Verfahren von Heun
    - Mittelpunktsregel (verbessertes Euler-Verfahren)
    - Verfahren von Bogacki-Shampine (ode23)
    - "Strong Stability Preserving" Runge-Kutta-Verfahren
    - Klassisches Runge-Kutta-Verfahren
    - 3/8-Regel
    - Jedes weitere Verfahren unter Angabe seines Butcher-Tableaus
  - **[Explizite lineare Mehrschrittmethoden](LMM)**
- Sonstiges
  - **[Bestimmung von Matrix-Eigenwerten](EIGNWERT)**

## Haftungsausschluss
Die vorliegenden Programme wurden mit Sorgfalt erstellt, für deren Richtigkeit und Vollständigkeit wird jedoch keinerlei Gewähr übernommen.
Eine Haftung für Schäden jeglicher Art, die durch die Nutzung oder Nichtnutzung der Programme entstehen, ist grundsätzlich ausgeschlossen.
Insbesondere wird ausdrücklich darauf hingewiesen, dass die Nutzung im Rahmen von Prüfungsleistungen nur mit expliziter Genehmigung zulässig ist.

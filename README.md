# Numerik
In diesem Projekt werden Programme für die Taschenrechner TI-83 Plus und TI-84 Plus zur Lösung numerischer Fragestellungen gesammelt.
Verfügbar sind die folgenden Verfahren, sortiert nach Anwendungsbereich:

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
- Sonstiges
  - **[Bestimmung von Matrix-Eigenwerten](EIGNWERT)**

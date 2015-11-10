# 4. Übungsblatt
## Aufgabe 12 Schwellenwertelemente: Darstellung Boolescher Funktionen
**Geben Sie einen Algorithmus an, der zu einer beliebigen gegebenen Booleschen Funktion f : {0, 1}n → {0, 1} ein Netz aus Schwellenwertelementen mit höchstens drei Schichten liefert, das diese Funktion berechnet! (Das Netz soll konstruiert, nicht durch Beispiele trainiert werden! Hinweis: vgl. Aufgaben des letzten Übungsblatts)**

---
## Aufgabe 13 Trainieren von Schwellenwertelementen
**In der Vorlesung wurde der Lernvorgang eines Schwellenwertelementes für das logische AND behandelt. Hier soll nun die logische Negation betrachtet werden. Geben Sie anhand einer anschaulichen Darstellung der Fehlerfunktion an, wie der Lernvorgang verläuft für**

a) **Startwerte $w = 2$ und $\Theta = -2$, Lernrate $\frac{1}{3}$**

b) **Startwerte $w = 1$ und $\Theta = 2$, Lernrate $\frac{1}{2}$**

c) **Startwerte $w=2$ und $\Theta = 1$, Lernrate $\frac{1}{10}$**

**Geben Sie eine geometrische Interpretation der Lernergebnisse an!**

---
## Aufgabe 14 Trainieren von Schwellenwertelementen
**Geben Sie den Ablauf des Lernvorgangs (Delta-Regel) eines Schwellenwertelementes für die Boolesche Funktion x1 ∧ ¬x2 an! (Am besten mithilfe einer Tabelle, die Spalten für die Werte von x1, x2, d = x1 ∧¬x2, x·w, y, e (Fehler), ∆w1, ∆w2, ∆θ, w1, w2 und θ enthält.) Verwenden Sie als Anfangsbelegung des Gewichtsvektors w = (0, 0, 0) und als Lernrate 1. Geben Sie eine geometrische Interpretation des Lernergebnisses an!**

| $x_1$ | $x_2$ | $d=x_1 \land \neg x_2$ | $x*w$ | $y$ | $\epsilon$ | $\Delta w_1$ | $\Delta w_2$ | $\Delta \Theta$| $w_1$| $w_2$| $ \Theta$ |
| :---: | :---: | :---: | :---: |
| 0 | 0 | 0 |  0 | 0 | 1 |

---
## Aufgabe 15 Gradientenabstieg
**Wie in der Vorlesung erläutert, werden neuronale Netze durch Gradientenabstieg trainiert. D.h., man berechnet den Gradienten der Fehlerfunktion bzgl. der Parameter des neuronalen Netzes (Gewichte und Biaswerte) und bewegt sich dann ein kleines Stück (durch die Lernrate und die Größe des Gradienten bestimmt) in die dem Gradienten entgegengesetzte Richtung. (Der Gradient gibt ja die Richtung der stärksten Steigung der Funktion an, wir wollen aber den Fehler minimieren, daher müssen wir uns in die Gegenrichtung bewegen.) In dieser Aufgabe veranschaulichen wir uns dieses Verfahren anhand der Minimierung einer einstelligen Funktion. Der Gradient ist in diesem Fall einfach die Ableitung der Funktion nach ihrem Argument. Wir betrachten die Funktion**
$$ f(x) = \frac{(x + 4)(x + 2)(x + 1)(x - 3)}{20} + 2 $$
**Versuchen Sie, das Minimum dieser Funktion durch Gradientenabstieg zu bestimmen!**
a) mit Startwert x0 = 3 und Lernrate η = 0.05,
b) mit Startwert x0 = −0.5 und Lernrate η = 0.95,
c) mit Startwert x0 = −2 und Lernrate η = 0.2.
**Veranschaulichen Sie den Vorgang durch eine Skizze! Welche Probleme treten auf?**

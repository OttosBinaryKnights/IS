# 7. Übungsblatt
*found on [github.com/OttosBinaryKnights/IS](https://github.com/OttosBinaryKnights/IS)*
## Aufgabe 23 Bedingte Wahrscheinlichkeiten
a) **Vier Kugeln werden der Reihe nach auf vier Kästen verteilt, wobei alle $4^4$ Reihenfolgen gleichwahrscheinlich sein mögen. Wie groß ist die Wahrscheinlichkeit, dass ein Kasten genau drei Kugeln enthält, wenn die ersten beiden Kugeln in verschiedene Kästen gelegt werden?**

* Die ersten Beiden in verschiedene Kästen: $\frac34$
* dritte Kugel in eines der BEIDEN belegten Kästchen $\frac24$
* vierte Kugel ins doppelt belegte Kästchen $\frac14$
$P(A \cap B) = \frac34 * \frac24* \frac14 = \frac{6}{64}$

$P(B|A) = \frac{P(A\cap B)}{P(A)} = \frac18$

b) **Über eine bestimmte Familie sei bekannt, dass sie zwei Kinder hat. Wie groß ist die Wahrscheinlichkeit, dass beide Kinder Mädchen sind, wenn bekannt ist, dass mindestens ein Kind ein Mädchen ist?**

*abhängig von Geschlechtsverteilung (50% angenommen)*

$$X: \text{Beide Kinder Maedchen}$$
$P(X) = 50$%

*kommt auf Interpreatation der Aufgabe an:*

 * nur Richtig wenn Reihenfolge der Kinder egal, sonst angeblich $ \frac13$

c) **Wie groß ist die Wahrscheinlichkeit in Teilaufgabe b), wenn bekannt ist, dass das jüngere Kind ein Mädchen ist?**

ändert sich nichts?
$P(X) = 50$% (unabhängig?!)

formal: $P(B|A) = \frac14 / \frac12 = 0.5$

---
## Aufgabe 24 Stochastische Unabhängigkeit
a) **Ein Glücksrad habe 36 numerierte Sektoren (Zahlen 1 bis 36). Die Sektoren seien folgendermaßen rot (R) oder blau (B) gefärbt:**

|   1   |   2   |   3   |   4   |   5   |   6   |   7   |   8   |   9   |   10  |   11   |   12   |   13   |   14   |   15   |   16  |   17   |   18   |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   R   |   R   |   R   |   R   |   R   |   B   |   B   |   B   |   B   |   R   |   R   |   R   |   R   |   B   |   B   |   B   |   B   |   B   |
|   36  |   35  |   34  |   33  |   32  |   31  |   30  |   29  |   28  |   27  |   26  |   25  |   24  |   23  |   22  |   21  |   20  |   19  |

 **Wir betrachten die drei Ereignisse**
* $A:$ **das Glücksrad hält in einem roten Sektor,**
* $B:$ **das Glücksrad hält in einem Sektor mit einer geraden Zahl,**
* $C:$ **das Glücksrad hält in einem Sektor mit einer Zahl ≤ 18.**

**Zeigen Sie, dass die Ereignisse paarweise, aber nicht vollständig$^1 $ unabhängig sind!**
$P(A) = \frac12$;
$P(B) = \frac12$;
$P(C) = \frac12$;
* $P(A \cap B) = \frac9{36} = \frac14 = P(A)*P(B)$
-> paarweise unabh.
* $P(A \cap C) = \frac9{36} = \frac14 = P(A)*P(C)$
-> paarweise unabh.
* $P(B \cap C) = \frac9{36} = \frac14 = P(B)*P(C)$
-> paarweise unabh.

* $P(A \cap B \cap C) = \frac4{36} = \frac19 \neq \frac18 = P(A)*P(B)*P(C)$
-> nicht vollständig unabh.


b) **Zwei faire Würfel, ein roter und ein weißer, werden geworfen. Wir betrachten die drei Ereignisse**
 * $A:$ **der rote Würfel zeigt eine 1 oder eine 2,**
 * $B:$ **der weiße Würfel zeigt eine 3, 4 oder 5,**
 * $C:$ **die Summe der Augenzahlen ist 4, 11 oder 12.**
**Zeigen Sie, dass die Ereignisse vollständig, aber nicht paarweise unabhängig sind!**

|   | 1 | 2 | 3 | 4 | 5 | 6 |
| :---: |:---: | :---: | :---: | :---: | :---: | :---: |
| **1** | 2 | 3 | 4 | 5 | 6 | 7 |
| **2** | 3 | 4 | 5 | 6 | 7 | 8 |
| **3** | 4 | 5 | 6 | 7 | 8 | 9 |
| **4** | 5 | 6 | 7 | 8 | 9 | 10|
| **5** | 6 | 7 | 8 | 9 | 10| 11|
| **6** | 7 | 8 | 9 | 10| 11| 12|

$P(A) = \frac13$;
$P(B) = \frac12$;
$P(C) = \frac{6}{36}$;
* $P(A \cap B) = \frac6{36} = \frac16 = P(A)*P(B)$
-> paarweise unabh.
* $P(A \cap C) = \frac1{18} \neq \frac{1}{18} = P(A)*P(C)$
-> paarweise unabh.
* $P(B \cap C) = \frac2{36} \neq \frac{1}{12} = P(B)*P(C)$
-> nicht paarweise unabh.

* $P(A \cap B \cap C) = \frac1{36} = \frac1{36} = P(A)*P(B)*P(C)$
-> vollständig unabh.

*$^1$Als vollständig unabhängig sei hier nur der Fall $P(A\cap B\cap C)=P(A)P(B)P(C)$ verstanden.*

---

## Aufgabe 25 Der Bayessche Satz

$$P(A|B) = \frac{P(A \cap B)}{P(A)} = \frac{P(B|A)P(A)}{P(B)}$$

a) **In einer gegebenen Population leiden 2 % aller Menschen an einer bestimmten Krankheit. Ein Test habe die Eigenschaft, dass er bei Kranken in 95 % und bei Gesunden in 99 % aller Fälle die richtige Diagnose stellt. Wie groß ist die Wahrscheinlichkeit dafür, dass eine Person, bei der auf Grund des Tests die Krankheit (nicht) diagnostiziert wird, auch tatsächlich (nicht) an dieser Krankheit leidet?**

|   | Krank K | Gesund !K |
| --- | --- | --- |
| Pos T | 0.019 | 0.0098 |
| Neg !T | 0.001 | 0.9702 |

$P(!K|!T) = \frac{P(!K|!T) P(!K)}{P(!T)} 0.999$
$P(K|T) = \frac{P(T|K) P(K)}{P(T)} = 0.6597$

b) **Etwa 5 von 100 Männern und etwa 25 von 10 000 Frauen sind farbenblind. Eine farbenblinde Person werde zufällig ausgewählt. Wie groß ist die Wahrscheinlichkeit, dass diese Person ein Mann ist?**

|   | Mann | Frau |
| --- | --- | --- |
| FBlind | 0.025 | 0.00125 |
| Norm | 0.475 | 0.49875 |
|  | 0.5 | 0.5 |

$P(\text{Mann unter Farbenblinden})= \frac{0.025}{0.025+0.00125} = 0.9523...$

c) **Gegeben seien zwei Urnen. Urne 1 enthalte zwei weiße und eine rote Kugel, Urne 2 eine weiße und zwei rote. Es werde zuerst zufällig eine Kugel aus Urne 1 gezogen und in Urne 2 gelegt. Anschließend wird zufällig eine Kugel aus der Urne 2 gezogen.**

**Angenommen, die aus Urne 2 gezogene Kugel sei rot: Wie groß ist die Wahrscheinlichkeit, dass die aus Urne 1 in Urne 2 überführte Kugel weiß war?**

$A: $Es wurde eine weiße Kugel aus Urne 1 in 2 gelegt

$P(A) = \frac23$

$B: $Es wurde ROT aus Urne 2 gezogen

$P(B|A) = \frac12$

$P(B|!A) = \frac34$

$P(B) = P(B|A) * P(A) + P(B|!A) * P(!A)$
$= \frac12 * \frac23 + \frac34 * \frac13$
$= \frac26 + \frac14 = \frac{7}{12}$

$P(A|B) = \frac{P(B|A)P(A)}{P(B)}$
$= \frac{\frac12 * \frac23}{\frac{7}{12}}$
$= \frac47 = 0.5714...$


---
## Aufgabe 26 Ameisenkolonieoptimierung

a) **Zeigen Sie am Beispiel des Doppelbrückenexperiments, dass die Ameisen nicht den kürzesten Pfad finden, wenn Sie nur auf dem Hinweg zur Futterquelle oder auf dem Rückweg von der Futterquelle Pheromon ablegen!**

Wenn die langsamere Ameise beim Futter ankommt dann ist nicht der kürzere Rückwege stärker pheromonisiert, sondern der eigene Weg -> tilt!


b) **Zeigen Sie am Beispiel des Doppelbrückenexperiments, dass die Ameisen, wenn sie mit einem Gedächtnis ausgestattet werden, das es ihnen erlaubt, ihren Weg vom Nest zur Futterquelle zurückzuverfolgen (backtrace), auch dann den kürzesten Pfad finden, wenn Sie nur auf dem Rückweg Pheromon ablegen!**
Wenn noch kein Pheromon ausgelegt ist, dann sprühe und gehe den eigenen Weg zurück, ansonsten dem ausgesprühtem Weg folgen.

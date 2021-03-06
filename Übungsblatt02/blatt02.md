# 2. Übungsblatt

## Aufgabe 4 Stimulus-Response-Agent
#### Wir betrachten den in der Vorlesung behandelten S-R-Agenten, der sich in einem durch ein Gitter in Felder eingeteilten Raum bewegt und den Umriss des Raumes oder den Umriss eines im Raum stehenden Objektes abfahren soll.
**a) In der Vorlesung wurde vorausgesetzt, dass es keine „engen Zwischenräume“ (engl. tight spaces) gibt, d.h. keine Durchgänge zwischen Wänden des Raumes und Objekten, die nur ein Feld breit sind. Warum ist diese Voraussetzung wichtig? Was kann passieren, wenn man diese Voraussetzung fallen lässt?**

 Bsp.:
$
\begin{bmatrix}
 & \Box & \leftarrow   & 2    & \Box         & \Box & \\
 & \Box & \blacksquare & \Box & \blacksquare & \Box & \\
 & \Box & \blacksquare & \Box & \blacksquare & \Box & \\
 & \Box & \Box         & 1    & \rightarrow  & \Box &
\end{bmatrix}
$

 Lässt man "enge Zwischenräume" zu, so erfüllt er seine Aufgabe nicht mehr, wie das Beispiel zeigt. Wir nehmen an, dass der Agent auf Position 1 startet. Den Regeln entsprechend bewegt sich der Agent von diesem Punkt aus nach Osten, umfährt das rechte Objekt und gelangt dann zu Punkt 2. Um das Objekt nun zu umfahren müsste der Agenz nun nach Süden fahren. Den Regeln lassen ihn jedoch nach Westem fahren, so dass er nun beide Objekte umfährt.  

 Bsp.2:

$
\begin{bmatrix}
 & \Box & \Box          & \Box    & \Box         & \Box & \\
 & \Box & \blacksquare  & \Box    & \blacksquare & \Box & \\
 & \Box & \Box & 1      & \Box    & \Box & \\
 & \Box & \Box          & \blacksquare    & \blacksquare  & \Box &
\end{bmatrix}
$

Bot kann sich in engen Zwischenräumen verfangen. ($x_1$ bis $x_4$ = 0)

**b) Kann man ein Regelsystem — ggf. unter Verwendung weiterer aus den Sensordaten abgeleiteter Merkmale $(x_i)$ oder auch der Sensordaten $(s_1 ... s_8)$ selbst — angeben, das den Agenten in die Lage versetzt, seine Aufgabe auch dann zu erfüllen, wenn es „enge Zwischenräume“ gibt? Begründen Sie Ihre Antwort!**

*Tobys Kurzform: Nein, weil er ein Gedächnis bräuchte um sich zu merken in welcher Richtung er in enge Zwischenräume eingetaucht ist.*

 Bsp.:
$
\begin{bmatrix}
& \Box & \Box         & 1               & \Box         & \Box & \\
& \Box & \blacksquare & 2               & \blacksquare & \Box & \\
& \Box & \blacksquare & 3               & \blacksquare & \Box & \\
& \Box & \blacksquare & \blacksquare    & \blacksquare & \Box & \\
& \Box & \Box         & \Box            & \Box         & \Box
\end{bmatrix}
$

 Es ist nicht möglich, eine entsprechende Regelbasis wie man an den folgenden Beispielen leicht zeigen kann. Im nebenstehenden Beispielraum 2 mußte sich ein S-R-Agent, um das uförmige Objekt zu umfahren, am Punkt nach Suden bewegen, um uber das Feld 2 schließlich Feld 3 zu erreichen. Anschließen müßte er auf umgekehrtem Wege wieder zu Punkt 1 fahren. An den Punkten 1 und 2 fuhrt dies zu widersprüchlichen Regeln, denn beim Einfahren in das uförmige Objekt mußte er sich an beiden Punkten nach Süden, beim Ausfahren jedoch am Punkt 2 nach Norden und am Punkt 1 nach Westen (oder Osten, je nach Richtung, aus der dieser Punkt ursprunglich erreicht wurde) bewegen. Das Reizmuster ist aber in beiden Fällen, d.h. beim Ein- und beim Ausfahren, gleich.

 Bsp.:
$
\begin{bmatrix}
& \blacksquare & \Box  & \blacksquare  & \Box & \blacksquare & \Box \\
& \Box         & \Box  & \Box          & 2    &\Box          & \Box \\
& \blacksquare & \Box  & \blacksquare  & \Box & \blacksquare & \Box \\
& \Box         & \Box  & \Box          & 1    & \Box         & \Box\\
& \blacksquare & \Box  & \blacksquare  & \Box & \blacksquare & \Box
\end{bmatrix}
$

 Betrachten wir nun den nebenstehenden Beispielraum 3. Der S-R-Agent möge am Punkt 1 starten. Wir nehmen o.B.d.A. an, dass er sich von diesem Punkt aus nach Norden bewegt (bewegt er sich in eine andere Richtung, so drehe man die Abbildung). Er erreicht schließlich den Punkt 2. Da an diesem Punkt das gleiche Reizmuster vorliegt wie an Punkt 1, muß sich der S-R-Agent auch in die gleiche Richtung bewegen wie an Punkt 1, also nach Norden. Damit entfernt er sich aber von den beiden Objekten, die er (ausgehend von Punkt 1 mit einem Schritt nach Norden) hätte umfahren können, nämlich die beiden Objekte, die nordwestlich und nord östlich von Punkt 1 liegen. Um sie zu umfahren, musste er sich an Punkt 2 nach Osten oder nach Westen bewegen, was aber zu widerspruchlichen Regeln führt.

 Die Beispiele zeigen, dass ein Agent die Aufgabe, den Umriss eines Objektes oder die Begrenzung des Raumes abzufahren, im allgemeinen Fall, d.h. bei Vorliegen "Zwischenräume", nur lösen kann, wenn er über ein z.B. merken kann, welche Aktion er zuvor ausgefuhrt hat oder aus welcher Richtung er gekommen ist. Durch ein solches Gedächtnis lässt sich die Widerspruchlichkeit der Regeln aufheben, aber der Agent ist dann natürlich kein reiner S-R-Agent mehr.

---
## Aufgabe 5 Stimulus-Response-Agent
#### Der schon in Aufgabe 4 betrachtete S-R-Agent aus der Vorlesung werde wie folgt verändert: Statt der Aktionen „Gehe nach Norden, Osten, Süden, Westen“ stehen dem Agenten die Aktionen „Gehe vorwärts“ (in Richtung des Sensors s2), „Drehe nach links“ (um 90° gegen den Uhrzeigersinn) und „Drehe nach rechts“ (um 90° im Uhrzeigersinn) zur Verfügung.
**a) Geben Sie ein Regelsystem an, das den Agenten den Umriss des Raumes oder den Umriss eines im Raum stehenden Gegenstandes abfahren lässt! Setzen Sie dabei voraus, dass es keine „engen Zwischenräume“ gibt.**

 $
\begin{matrix}
 & s_1 &            & s_2          &             & s_3  \\
 &     & \nwarrow   & \uparrow     & \nearrow    &      \\
 & s_8 & \leftarrow & \blacksquare & \rightarrow & s_4  \\
 &     & \swarrow   & \downarrow   & \searrow    &      \\
 & s_7 &            & s_6          &             & s_5
\end{matrix}
$

### DIESE REGEL FÜHRT WRSL ZU EINER ENDLOSSCHLEIFE

 $x_1 = 1 \leftrightarrow s_2 = 1 \lor s_3=1$

 $x_2 = 1 \leftrightarrow s_4 = 1 \lor s_5 = 1$

 $x_3 = 1 \leftrightarrow s_6 = 1 \lor s_7 = 1$

 $x_4 = 1 \leftrightarrow s_8 = 1 \lor s_1 = 1$

 Mit diesen Zwischengrößen lassen sich die Regeln folgendermaßen formulieren:

 $x_1 = 1 \land x_4 = 1 \rightarrow \text{"Drehe nach rechts"}$

 $x_1 = 0 \land x_4 = 1 \rightarrow \text{"Gehe vorwaerts"}$

 $x_1 = 0 \land x_3 = 1 \land x_4 = 0 \rightarrow \text{"Drehe nach links"}$

 $x_1 = 1 \land x_2 = 0 \land x_4 = 0 \rightarrow \text{"Drehe nach rechts"}$

 $x_1 = 0 \land x_2 = 0 \land x_3 = 0 \land x_4 = 0 \rightarrow \text{"Gehe vorwaerts"}$

 ---

 ---
 *Alternative Lösung*

 $x_1 = 1 \leftrightarrow s_2 = 1$ (Weg versperrt)

 $x_2 = 1 \leftrightarrow s_1 = 1 \lor s_8 = 1$ (Wand links oder linksvorne)

 $x_3 = 1 \leftrightarrow s_1 = 0 \lor s_8 = 0 \lor s_7 = 1$ (Wand hintenlinks)

 Mit diesen Zwischengrößen lassen sich die Regeln folgendermaßen formulieren:


 $x_1 = 1 \rightarrow rechts$

 $x_2 = 1 \rightarrow$ vorwärts

 $x_3 = 1 \rightarrow links$

 ($1 \rightarrow$ vorwärts)


**b) Kann man ein Regelsystem angeben, das den Agenten in die Lage versetzt, seine Aufgabe auch dann zu erfüllen, wenn es „enge Zwischenräume“ gibt? Begründen Sie Ihre Antwort!**

 Wie in Aufgabe 1 kann der Agent seine Aufgabe nur dann erfüllen, wenn er über ein Gedächtnis verfügt, also kein reiner S-R-Agent mehr ist.

---
## Aufgabe 6 Boolesche Algebra
**a) Zeigen Sie, dass die aus den Operationen Konjunktion, Disjunktion und Negation bestehende Operationenmenge $\{\land ,\lor ,\neg \}$ eine Verknüpfungsbasis (oder vollständige Operationenmenge) ist, d.h., dass alle Funktionen $\{0,1\}^n \rightarrow \{0,1\}$ mit den Operationen dieser Menge konstruiert werden können!**

 Jede boolsche Funktion lässt sich in KNF und DNF darstellen. Da in diesen Normalformen nur die Operationen Konjunktion, Disjunktion und verwendet werden, ist die aus diesen Funktionen bestehende Menge eine Verknüpfungsbasis.

Noch zu zeigen, dass mehrstellige Operationen (n>2) auch durch die Operationsmenge darzustellen ist. 
Dazu einfach einsetzen f(a1, f(a2, a3)). 

**b) Zeigen Sie, dass die nur aus der Peircefunktion (NOR) bestehende Operationenmenge $\{\downarrow\}$ eine Verknüpfungsbasis ist!**

Beweis unter Punkt 2.4.1 im Dokument: http://student.cosy.sbg.ac.at/~vhorak/Bakk-Arbeit/MathSem.pdf
Beweis: Es genügt zu zeigen, dass sich $\{0,1\}n \rightarrow \{0,1\}$ durch $\{\downarrow\}$ darstellen lassen.

 $\neg: \neg A = \neg (A\lor A) = A \downarrow A$

 $\lor: A\lor B = (A\lor B)\land (A\lor B) $

 $= \neg \neg ((A\lor B)\land (A\lor B))$

 $= \neg (\neg (A\lor B)\lor \neg (A\lor B))$

 $ = \neg ((A\downarrow B)\lor (A\downarrow B))$

 $ = (A\downarrow B)\downarrow (A\downarrow B)$

 $\land: A\land B = \neg \neg (A\land B) = \neg (\neg A\lor \neg B) = \neg A\downarrow \neg B = (A\downarrow A)\downarrow (B\downarrow B)$

**c) Zeigen Sie, dass die nur aus der Shefferfunktion (NAND) bestehende Operationenmenge $\{\uparrow\}$ eine Verknüpfungsbasis ist!
Beweis: Es genügt zu zeigen, dass sich $\{\land ,\lor ,\neg \}$ durch $\{\uparrow\}$ darstellen lassen.**

Beweis unter Punkt 2.4.2 im Dokument: http://student.cosy.sbg.ac.at/~vhorak/Bakk-Arbeit/MathSem.pdf

 $\neg: \neg A = \neg (A\land A) = A\uparrow A$

 $\land : A\land B = (A\land B)\lor (A\land B)$

 $ = \neg \neg ((A\land B)\lor (A\land B)) $

 $= \neg (\neg (A\land B)\land \neg (A\land B))$

 $= \neg ((A\uparrow B)\land (A\uparrow B))$

 $ = (A\uparrow B)\uparrow (A\uparrow B)$

 $\lor : A\lor B = \neg \neg (A\lor B) = \neg (\neg A\land \neg B) = \neg A\uparrow \neg B = (A\uparrow A)\uparrow (B\uparrow B)$

 **d) Zeigen Sie, dass die aus den Operationen Implikation und Negation bestehende Operationenmenge $\{\rightarrow , \neg \}$ eine Verknüpfungsbasis ist!**

 $\land : A \land B = \neg \neg (A \land B) = \neg (\neg A \lor \neg B) = \neg (A \rightarrow \neg B)$

 $\lor : A \lor B = \neg \neg A \lor B = \neg A \rightarrow B$

---
## Aufgabe 7 Darstellung Boolescher Funktionen
  **Stellen Sie die Operationen Konjunktion, Disjunktion, Negation, Implikation und exklusive Disjunktion (exklusives Oder, XOR) nur unter Verwendung der vier Grundrechenarten Addition, Subtraktion, Multiplikation und Division dar.**

*Hinweis: Verwenden Sie keine Restbildung, also nicht die Modulo-Operation.*


 * Konjunktion:
 $$ f(a,b) = a*b = ab $$

 * Disjunktion:
 $$ f(a,b) = \neg (\neg a \land \neg b) = 1 - ((1-a)*(1-b)) = 1- (1-b-a+ab) = b+a-ab $$

 * Negation:
 $$ f(a) = 1 - a $$

 * Implikation (a → b):
 $$ f(a,b) = \neg a \lor b = (1-a) + b -(1-a)*b = 1-a+b-b+ab = 1-a+ab $$

 * exklusive Disjunktion:
 $$ f(a,b) = (a \lor b) \land \neg (a\land b) = (a+b - ab) * (1-ab) = a+b-ab-a^2b-ab^2 + a^2b^2 $$
Da a,b element aus {0,1} ist a^2=a und b^2 = b daraus folgt
$$ a+b-ab-ab-ab+ab = a+b-2ab $$


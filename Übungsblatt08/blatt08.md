# Übungsblatt 8
## Aufgabe 1 The Legend of Zelda und Netze von Schwellenwertelementen
**Ganondorf hatte Zelda und Link in einen magischen Käfig 4 eingesperrt. Die Situation schien ausweglos, doch plötzlich erschallte ein leisen „Hey!“und die Fee Navi meldete sich zu 3 Wort. „Ihr müsst die Kräfte des Triforce aktivieren um das Böse zu bannen. Nur so könnt ihr den bösen Mächten ent- 2 kommen! “**

**Geben Sie ein neuronales Netz aus Schwellenwertelementen an, das für Punkte (x1,x2) innerhalb des in der nebenstehen- den Skizze gezeigten grau markierten Bereichs den Wert 1 und für Punkte außerhalb den Wert 0 liefert!**
![Abbildung](Abbildung1.png)

---
## Aufgabe 2 Die Zwerge und die Wahrscheinlichkeitsrechnung
**Die Berichte des kleinen Hobbits Bilbo und seiner Gefolgschaft wurden in den letzten Jahren zahlreich wiedergegeben. Viele kennen die Zwerge als Gemeinschaft, denn von ihren Streitig- keiten wurde nur selten berichtet. So kam es, das die sich sonst so einigen Bifur, Bofur und Bombur in einen Streit um das letzte Fass Bier gerieten.**

**Ihre Trefferchance ist mittlerweile stark eingeschränkt: Bifur, der betrunkenste der Drei, konnte sein Ziel nur noch mit einer geschätzten Wahrscheinlichkeit von 0.3 treffen. Bofur schwankte nur wenig, aber sah seine Gegner bereits doppelt. Mit einer Chance von 0.5 sollte er also seinen Gegner treffen können. Bombur der kräftigste unter Ihnen prahlte wie viel er doch vertragen konnte. Zur Demonstration warf er einen Krug in die Luft und zerschmetterte ihn mit seiner Axt. Mit einer Treffsicherheit von 1.0 war er so Zielgenau wir immer.**

**Die drei einigten sich nacheinander zuzuschlagen. Wer einmal getroffen wurde scheidet sofort aus. In der Reihenfolge Bifur, Bofur, Bombur, Bifur, ... konnten sie nun wählen wen sie jeweils angreifen. Was wäre die beste Strategie für Bifur, wenn Bofur und Bombur jeweils den verbleibenden Zwerg mit der höchsten Zielgenauigkeit angreifen würden? Wie hoch ist Bifurs Chance zu gewinnen?**

---
## Aufgabe 3 Mario Kart und Mehrwertige Logiken
**Betrachten Sie die n-wertigen Logiken $L_n(n\leq 2)$ mit den Wahrheitswerten**
$$T_n=\{0=\frac{0}{n-1}, \frac{1}{n-1}, \frac{2}{n-1}, ..., \frac{n-2}{n-1}, \frac{n-1}{n-1} = 1\}$$

**Die logischen Verknüpfungen in $L_n$ seien wie folgt definiert:**
![Formeln](Formeln.png)
**Offensichtlich entspricht die Logik $L_2$ mit den Wahrheitswerten $T_2 = \{0,1\}$ der klassischen, zweiwertigen Aussagenlogik.**

**Christian, Christoph und Alex spielen eine Party Mario-Kart. Nach vielen Runden sind sie sich unsicher unter welchen Bedingungen einer von ihnen gewinnt. Folgende Beziehungen lassen sich aufstellen:**

a) **Alex ist sich sicher, dass gilt: „Wenn ich einen blauen Panzer erhalte und einen Turbo Pilz einsetzen kann, dann werde ich gewinnen.“
Stellen sie den im Text beschriebenen Ausdruck für B (blauer Panzer), T (Turbo Pilz) und A (Alex gewinnt) auf. Berechnen sie anschließend die Wahrheitswerte für alle Kom- binationen von T3 der logischen Variablen B, T und A.**

b) **Christian und Christoph sind der Meinung, dass dieser Ausdruck viel zu einfach sei und geben folgende Alternative an.**
$$((B \rightarrow A)\land (T \rightarrow A))\land (B \land T).$$
**Berechnen sie erneut die Wahrheitswerte für alle Kombinationen von $T_3$ der logischen Variablen B, T und A.**

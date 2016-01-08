# Übungsblatt 09
## Aufgabe 27 Zustandsautomaten: Stimulus-Response-Agent
*Auf dem 2. Übungsblatt haben wir gesehen, dass man für einen reinen Stimulus-Response- Agenten kein Regelsystem angeben kann, das ihn den Umriss eines Objektes oder des Raumes abfahren lässt, wenn es „enge Zwischenräume“ gibt, d.h. Zwischenräume zwischen einer Wand und einem Objekt oder zwischen zwei Objekten, die nur ein Feld breit sind.
Agenten mit inneren Zuständen können dagegen auch in Gitterwelten mit engen Zwischen- räumen ihre Aufgabe erfüllen. Definieren Sie geeignete innere Zustände und geben Sie ein Regelsystem für einen solchen Agenten an!*

---
## Aufgabe 28 Zustandsautomaten: Türme von Hanoi
*Das Problem der Türme von Hanoi ist sicherlich aus einer der Grundvorlesungen bekannt. Auf einem von drei Stäben liegt eine Anzahl verschieden großer Scheiben, jede Scheibe auf der nächstgrößeren. Diese Scheiben sollen auf einen anderen der Stäbe umgelagert werden (wobei der dritte Stab als Zwischenlager dienen kann), ohne dass die folgenden Bedingungen verletzt werden:*

* a) *Es darf immer nur eine Scheibe bewegt werden.*
* b) *Scheiben dürfen nur auf Stäben abgelegt werden.*
* c) *Es darf nie eine größere Scheibe auf eine kleinere gelegt werden.*

![Hanoi](Hanoi.png)

*Wir betrachten hier das Problem der Türme von Hanoi für drei Scheiben $S_1$ bis $S_3$, wie in der obigen Skizze gezeigt. Der rekursive Algorithmus zur Lösung dieses Problems ist sicher bekannt. Es gibt aber auch einen iterativen: Man bewege stets die größte Scheibe, die bewegt werden kann, ohne den im Schritt vorher gemachten Zug rückgängig zu machen. Man bewege die Scheibe nach rechts (wobei ein Zug von C nach A auch als „nach rechts“ gilt), wenn die Zahl der von der Ausgangsposition an ausgeführten Züge ungerade ist, und man bewege sie nach links (wobei ein Zug von A nach C auch als „nach links“ gilt), wenn diese Zahl gerade ist. Sollte der so bestimmte Zug nicht erlaubt sein oder den vorhergehenden Zug rückgängig machen, bewege man die Scheibe in die andere Richtung.*

*Geben Sie ein Produktionssystem für einen Agenten an, der das Problem der Türme von Hanoi auf die beschriebene Weise löst. Nehmen Sie als mögliche Aktionen die sechs Züge bewege(Scheibe, Richtung) an. Als Sensoreingaben stehen $G_1, G_2$ und $G_3$ zur Verfügung, wobei $G_i$ dann 1 (wahr) ist, wenn die Scheibe Si die größte Scheibe ist, die bewegt werden kann. (Binäre) Zustandsvariablen sind $B_1, B_2, B_3$ und R, für die es die folgenden Zustandsänderungsfunktionen gibt: durch bewegt($B_i$) werden $B_i$ auf 1 und alle $B_j, j\neq i$, auf 0 gesetzt, durch umdrehen wird der Wert von R negiert (ist er 1, so wird er 0 und umgekehrt). Überlegen Sie, ob es (mindestens in natürlicher Sprache) nicht noch eine einfachere Beschreibung des iterativen Algorithmus gibt.*

---
## Aufgabe 29 Zustandsautomat: Kaffeeautomat
*Ein Getränkeautomat verfügt über einen Knopf k für Kaffee und einen Knopf c für Cappuccino, mit denen das gewünschte Getränk gewählt werden kann. Ein Kaffee kostet 40 Cent, ein Cappuccino 50 Cent. Nachdem ein Getränk gewählt wurde, können Münzen der Werte 5 Cent, 10 Cent oder 20 Cent eingeworfen werden. Der Automat verfügt über Sensoren $m_5, m_{10}$ und $m_{20}$, die den Einwurf einer entsprechenden Münze anzeigen. Ist der zu zahlende Betrag erreicht oder überschritten, wird das Getränk ausgegeben (Aktionen Ausgabe(Kaffee) und Ausgabe(Cappuccino)). Der Automat gibt kein Wechselgeld aus. Münzen, die eingeworfen werden, bevor ein Getränk gewählt wurde, werden sofort zurückgegeben. Außerdem kann, solange das gewählte Getränk noch nicht voll bezahlt ist, der Geldrückgabeknopf r gedrückt werden, was zur Rückgabe der eingeworfenen Münzen führt (Aktion Rückgabe).*

*Geben Sie ein Regelsystem für einen Agenten an, der diesen Automaten steuert!*

---
## Aufgabe 30 Zustandsautomaten: Ampelsteuerung
*Gegeben sei eine Straßenkreuzung, wie sie die Abbildung rechts zeigt. Straße 1 soll gegenüber Straße 2 bevorrechtigt sein. D.h., es gibt in Straße 2 Induktionsschleifen (siehe Abbildung), von denen der Steuerungsagent die Sensoreingaben $i_1$ und $i_2$, jeweils mit den Werten 0 und 1, erhält. Der Wert 1 zeigt an, dass an der entsprechenden Stelle ein Fahrzeug vor der Ampel 2 wartet.*

![Kreuzung](Kreuzung.png)

*Nur wenn ein Fahrzeug wartet, soll Ampel 2 auf grün schalten. Außerdem soll für Straße 1 eine gewisse Mindestlänge der Grünphase und eine Maximallänge der Rotphase eingehalten werden. Entwickeln Sie eine Ampelsteuerung für die gegebene Kreuzung.*

# 2. Übungsblatt

## Aufgabe 4 Stimulus-Response-Agent
**Wir betrachten den in der Vorlesung behandelten S-R-Agenten, der sich in einem durch ein Gitter in Felder eingeteilten Raum bewegt und den Umriss des Raumes oder den Umriss eines im Raum stehenden Objektes abfahren soll.**
### a) In der Vorlesung wurde vorausgesetzt, dass es keine „engen Zwischenräume“ (engl. tight spaces) gibt, d.h. keine Durchgänge zwischen Wänden des Raumes und Objekten, die nur ein Feld breit sind. Warum ist diese Voraussetzung wichtig? Was kann passieren, wenn man diese Voraussetzung fallen lässt?
### b) Kann man ein Regelsystem — ggf. unter Verwendung weiterer aus den Sensordaten abgeleiteter Merkmale (xi) oder auch der Sensordaten (s1 bis s8) selbst — angeben, das den Agenten in die Lage versetzt, seine Aufgabe auch dann zu erfüllen, wenn es „enge Zwischenräume“ gibt? Begründen Sie Ihre Antwort!

---
## Aufgabe 5 Stimulus-Response-Agent
**Der schon in Aufgabe 4 betrachtete S-R-Agent aus der Vorlesung werde wie folgt verändert: Statt der Aktionen „Gehe nach Norden, Osten, Süden, Westen“ stehen dem Agenten die Aktionen „Gehe vorwärts“ (in Richtung des Sensors s2), „Drehe nach links“ (um 90° gegen den Uhrzeigersinn) und „Drehe nach rechts“ (um 90° im Uhrzeigersinn) zur Verfügung.**
### a) Geben Sie ein Regelsystem an, das den Agenten den Umriss des Raumes oder den Umriss eines im Raum stehenden Gegenstandes abfahren lässt! Setzen Sie dabei voraus, dass es keine „engen Zwischenräume“ gibt.


### b) Kann man ein Regelsystem angeben, das den Agenten in die Lage versetzt, seine Aufgabe auch dann zu erfüllen, wenn es „enge Zwischenräume“ gibt? Begründen Sie Ihre Antwort!

---
## Aufgabe 6 Boolesche Algebra
### a) Zeigen Sie, dass die aus den Operationen Konjunktion, Disjunktion und Negation bestehende Operationenmenge {∧,∨,¬} eine Verknüpfungsbasis (oder vollständige Operationenmenge) ist, d.h., dass alle Funktionen {0,1}n → {0,1} mit den Operationen dieser Menge konstruiert werden können!
### b) Zeigen Sie, dass die nur aus der Peircefunktion (NOR) bestehende Operationenmenge {↓} eine Verknüpfungsbasis ist!
Beweis unter Punkt 2.4.1 im Dokument: http://student.cosy.sbg.ac.at/~vhorak/Bakk-Arbeit/MathSem.pdf
### c) Zeigen Sie, dass die nur aus der Shefferfunktion (NAND) bestehende Operationenmenge {↑} eine Verknüpfungsbasis ist!
Beweis unter Punkt 2.4.2 im Dokument: http://student.cosy.sbg.ac.at/~vhorak/Bakk-Arbeit/MathSem.pdf
### d) Zeigen Sie, dass die aus den Operationen Implikation und Negation bestehende Opera- tionenmenge {→, ¬} eine Verknüpfungsbasis ist!

---
## Aufgabe 7 Darstellung Boolescher Funktionen
  **Stellen Sie die Operationen Konjunktion, Disjunktion, Negation, Implikation und exklusive Disjunktion (exklusives Oder, XOR) nur unter Verwendung der vier Grundrechenarten Addition, Subtraktion, Multiplikation und Division dar.**

*Hinweis: Verwenden Sie keine Restbildung, also nicht die Modulo-Operation.*


 * Konjunktion:
 $$ f(a,b) = a*b = ab $$

 * Disjunktion:
 $$ f(a,b) = a + b $$

 * Negation:
 $$ f(x) = 1 - x $$

 * Implikation (a → b):
 $$ f(a,b) = (1-a) + b $$

 * exklusive Disjunktion:
 $$ f(a,b) = (1-a) * (1-b) $$

# 1. Übungsblatt (ungeprüft)
Aufgabenblatt: (http://fuzzy.cs.uni-magdeburg.de/wiki/uploads/Lehre.IS1516/is2015_ue01.pdf)
## 1.1 Der Touring Test
_Quelle:_ (http://www.beneu.de/privat/archiv/turing/tur2.html)
### Was ist das Imitationsspiel?
Fragesteller C muss herausfinden welcher seiner beiden "Chatpartner" (A und B) weiblich, welcher männlich ist. Ein Chatpartner (B) soll den Fragesteller unterstützen die richtige Antwort zu finden, der Andere (A) versucht den Fragesteller zu einer falsche Antwort zu bewegen.

### Wie wird es von Turing beschrieben? Wie wird es von einem Rechner gespielt?
Bei Touring wird ein Chatpartner A durch eine Maschine ersetzt, die versucht das der Fragesteller die Maschine für den menschlichen Chatpartner

### Wann besteht ein Rechner/Programm den Turing-Test?
Wenn der Fragesteller mit midestens gleicher Häufigkeit die Maschine für menschlich hält, mit der er den menschlichen Chatpartnern das falsche Geschlecht zuordnete.

### Gibt es bereits Rechner/Programme, die den Turing-Test bestehen?
Nein. Loebner-Preis wurde noch nicht verliehen. (gäbe die Silbermedaille - erweiterter Test für Goldmedaille)

---
## 1.2 Weizenbaums ELIZA
### Welche Funktion hat das Programm „ELIZA“?
Soll Kommunikation zwischen einen Menschen und einem Computer über natürliche Sprache demonstrieren.

_Funktionsweise:_
 * in einem strukturiertem Wörterbuch wird die Frage nach Schlüsselwörtern durchsucht
 * Bei einem Treffer wird nach Synonymen oder Oberbegriffen gesucht und für dieses (passend zum Themengebiet) eine Folgefrage gestellt ("oberflächliche Simulation eines Psychotherapeuten")
 * kein Schlüsselwort auffindbar -> Ausweichphrasen

### Welche Bedeutung hat „ELIZA“ im Zusammenhang mit dem Turing-Test?
Kann als frühe Umsetzung des Turing-Tests gesehen werden.

### Besteht „ELIZA“ den Turing-Test?
Nein - Benutzer findet schnell heraus, das es sich um ein Programm handelt:
 * Versteht keine Metaphern (Mutter Natur != Familie)
 * oben genannte Ausweichphrasen
---
## 1.3 Das chinesische Zimmer
### Worin besteht das Gedankenexperiment?
In einem Raum sitzt ein Person und erhält durch einen Schlizt eine Geschichte und zugehörige Fragen in Chinesischen Schriftzeichen, ist selbst jedoch nicht des Chinesischen mächtig. Mithilfe eines Handbuchs in seiner Muttersprache ist er jedoch in der Lage durch stumpfes Befolgen der darin enthaltenen Regeln anhand der eingehenden Zettel die korrekte Antwort, ebenfalls in chinesischen Schriftzeichen zu geben.
Der draußen stehende Muttersprachler, der ihm die Geschichte und Fragen zusteckte kommt hierbei zum dem Schluss das innen ebenfalls jemand sitzen müsse, der Chinesisch spricht.

### Wofür/Wogegen wird es als Argument benutzt?
Es soll beweisen, dass ein Computer **nicht** allein dadurch Bewusstsein erlangt, indem es ein passendes Programm ausführt.

### In welchem Zusammenhang steht es mit dem Turing-Test?
 Autor wollte zeigen, dass das Bestehen des Turing-Test für eine Rechenmaschine nicht ausreicht um als Intelligent zu gelten. Die Maschine **erscheint** nur intelligent

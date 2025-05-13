### 📋 Aufgabenstellung

Schreibe ein Java-Programm, das ein **Tic Tac Toe**-Spiel gegen die KI simuliert. Der Benutzer spielt gegen den Computer und versucht, als Erster drei Felder in einer Reihe zu haben.

#### Schritte:

1. Erstelle ein Spielfeld als **2D-Array** mit einer Größe von 3x3 (3 Reihen und 3 Spalten).
2. Der Benutzer gibt nacheinander seine Züge ein (Reihe und Spalte, z.B. 1 1 für die obere linke Ecke).
3. Der Computer wählt seinen Zug automatisch aus und setzt ein „O“. Die Auswahl des Computerzugs kann zufällig erfolgen (z.B. durch Generierung einer zufälligen Zahl).
4. Das Spiel überprüft nach jedem Zug, ob ein Spieler gewonnen hat. Ein Spieler gewinnt, wenn er drei Felder in einer Reihe (horizontal, vertikal oder diagonal) hat.
5. Wenn das Spielfeld voll ist und niemand gewonnen hat, endet das Spiel mit einem Unentschieden.
6. Gib nach jedem Zug das aktuelle Spielfeld aus, um dem Spieler den Fortschritt anzuzeigen.
7. Zeige am Ende des Spiels an, wer gewonnen hat oder ob es ein Unentschieden war.
8. Der Spieler soll am Ende gefragt werden, ob er eine neue Runde spielen möchte.

#### Spielregeln:
- Das Spielfeld ist ein 3x3 Raster.
- Der Benutzer setzt „X“, der Computer setzt „O“.
- Das Spiel endet, wenn einer der Spieler drei Felder in einer Reihe, einer Spalte oder diagonal hat oder das Spielfeld voll ist (Unentschieden).
- Der Benutzer gibt in jeder Runde die Reihe und Spalte seines Zugs ein, wobei die Indizes von 1 bis 3 gehen.

---

### 🧩 Hinweise:

- Verwende für das Spielfeld ein **2D-Array**.
- Für den Benutzer kannst du `Scanner` verwenden, um die Eingabe zu lesen.
- Die KI kann ihre Züge zufällig auswählen, aber du kannst sie später auch optimieren.
- Das Spiel sollte nach jedem Zug den aktuellen Zustand des Spielfelds ausgeben, um dem Spieler eine Übersicht zu geben.
- Du kannst auch eine Klasse mit Methoden und Attributen erstellen, um das Spielfeld, die Spieler und die Logik des Spiels besser zu strukturieren.

---

### Optional:

> Erweitere das Programm um einen **Spieler-gegen-Spieler-Modus**. In diesem Modus spielen zwei Benutzer gegeneinander. Die Regeln bleiben die gleichen, aber beide Spieler machen abwechselnd ihre Züge.

---

### Console:

```plaintext
Willkommen zu Tic Tac Toe!

Du X gegen Computer O.

Aktuelles Spielfeld:

_ | _ | _
---------
_ | _ | _
---------
_ | _ | _

Gib die Position für deinen Zug ein:

Dein Zug: 1 1

Aktuelles Spielfeld:

X | _ | _
---------
_ | _ | _
---------
_ | _ | _

Computer Zug: 1 2

Aktuelles Spielfeld:

X | O | _
---------
_ | _ | _
---------
_ | _ | _

Dein Zug: 2 2

...
```

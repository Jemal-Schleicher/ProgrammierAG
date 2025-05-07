### 📋 Aufgabenstellung
Schreibe ein Java-Programm, das:

1. Den Benutzer nach einer Schätzung fragt, wie viele Würfe es braucht, um eine 6 zu würfeln.
2. Einen Würfel simuliert (Zahlen von 1 bis 6) und so lange würfelt, bis eine **6** erscheint.
3. Die tatsächliche Anzahl der Versuche zählt und mit der Schätzung vergleicht.
4. Die Würfe und das Ergebnis in der Konsole ausgibt.

Nutze dazu eine `while`-Schleife und `Math.random()`, um Zufallszahlen zu erzeugen.

---

### 🧩 Hinweise
- Ein Würfelwurf kann so simuliert werden: `(int)(Math.random() * 6) + 1`
- Verwende `Scanner`, um die Nutzereingabe zu lesen.
- Gib am Ende aus, ob die Schätzung richtig war oder wie sehr sie daneben lag.

---

### Optional

> Ändere das Programm so, dass es erst stoppt, wenn zweimal hintereinander eine 6 geworfen wurde.  
> Zähle weiterhin die Versuche und gib sie aus.

---

### Console

```plaintext
Wie viele Würfe denkst du, braucht es bis zur ersten 6?
Tipp eingeben: 4
Würfle...
Es wurde eine 3 geworfen.
Es wurde eine 4 geworfen.
Es wurde eine 2 geworfen.
Es wurde eine 6 geworfen.
Benötigte Versuche: 4
Deine Schätzung war genau richtig!

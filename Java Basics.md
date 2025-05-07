# Datentypen

---

| Datentyp   | Größe             | Wertebereich                                            | Beschreibung                                                    | Beispielwert      |
|------------|------------------|----------------------------------------------------------|------------------------------------------------------------------|-------------------|
| `boolean`  | 1 Bit (meist 1 Byte) | `true` / `false`                                     | Wahrheitswert, speichert nur zwei Zustände                      | `true`, `false`   |
| `char`     | 2 Byte (16 Bit)   | 0 bis 65.535 (Unicode)                                 | Einzelnes Unicode-Zeichen, intern als Zahl gespeichert           | `'A'`, `'1'`      |
| `byte`     | 1 Byte (8 Bit)    | -128 bis 127                                            | Sehr kleiner Ganzzahltyp (z. B. für Speicheroptimierung)        | `100`, `-50`      |
| `short`    | 2 Byte (16 Bit)   | -32.768 bis 32.767                                      | Kleiner Ganzzahltyp                                              | `32000`, `-1500`  |
| `int`      | 4 Byte (32 Bit)   | -2.147.483.648 bis 2.147.483.647                        | Standard-Ganzzahltyp                                             | `42`, `-1000000`  |
| `long`     | 8 Byte (64 Bit)   | -9.223.372.036.854.775.808 bis 9.223.372.036.854.775.807 | Sehr großer Ganzzahltyp                                          | `100000000000L`, `-5000L` |
| `float`    | 4 Byte (32 Bit)   | ca. ±1.4×10⁻⁴⁵ bis ±3.4×10³⁸ (7 Dezimalstellen genau)  | Gleitkommazahl mit einfacher Genauigkeit                         | `3.14f`, `-0.001f`|
| `double`   | 8 Byte (64 Bit)   | ca. ±4.9×10⁻³²⁴ bis ±1.8×10³⁰⁸ (15 Dezimalstellen genau)| Gleitkommazahl mit doppelter Genauigkeit                        | `3.14159265358979`, `-1.23e4` |
| `string`   | variabel          | abhängig von Länge und Inhalt                          | Zeichenkette, speichert Text, besteht intern aus `char`-Werten  | `"Hallo"`, `"12345"`|



\* `boolean` ist technisch oft 1 Bit, aber meist 1 Byte im Speicher (Implementierungsabhängig).

## Deklaration

Deklaration bedeutet, eine Variable mit einem bestimmten Typ zu **definieren**, aber noch **keinen Wert zuzuweisen**.
### Beispiel:
```java
int zahl;
String name;
float kommazahl;
char buchstabe;
```

## Initialisierung

Initialisierung bedeutet, eine Variable bei der Deklaration sofort mit einem Wert zu versehen.
### Beispiel:
```java
int alter = 25;
String stadt = "Berlin";
boolean istAngemeldet = true;
char symbol = '#';
```

## Wertzuweisung

Wertzuweisung bedeutet, einer bereits deklarierten Variable einen Wert zuzuweisen (oder den bisherigen zu überschreiben).
### Beispiel:
```java
alter = 7;
stadt = "Braum";
istAngemeldet = false;
symbol = '!';
```
# Operatoren

---
## Vergleichsoperatoren

| Operator | Bedeutung              | Beispiel            | Ergebnis         |
|----------|------------------------|---------------------|------------------|
| `==`     | gleich                 | `5 == 5`            | `true`           |
|          |                        | `5 == 4`            | `false`          |
| `!=`     | ungleich               | `3 != 4`            | `true`           |
|          |                        | `5 != 5`            | `false`          |
| `>`      | größer als             | `7 > 3`             | `true`           |
|          |                        | `3 > 7`             | `false`          |
| `<`      | kleiner als            | `2 < 1`             | `false`          |
|          |                        | `1 < 2`             | `true`           |
| `>=`     | größer oder gleich     | `4 >= 4`            | `true`           |
|          |                        | `3 >= 4`            | `false`          |
| `<=`     | kleiner oder gleich    | `5 <= 6`            | `true`           |
|          |                        | `7 <= 6`            | `false`          |

## Logische Operatoren

| Operator | Name            | Beschreibung                               | Beispiel                          |
|----------|-----------------|--------------------------------------------|-----------------------------------|
| `&&`     | logisches UND   | true, wenn **beide Bedingungen** true sind | `true && true` → `true`           |
|          |                 |                                            | `true && false` → `false`         |
|          |                 |                                            | `false && true` → `false`         |
|          |                 |                                            | `false && false` → `false`        |
| `\|\|`   | logisches ODER  | true, wenn **mind. eine Bedingung** true ist | `true \|\| true` → `true`         |
|          |                 |                                            | `true \|\| false` → `true`        |
|          |                 |                                            | `false \|\| true` → `true`       |
|          |                 |                                            | `false \|\| false` → `false`     |
| `!`      | logisches NICHT | kehrt den Wahrheitswert um                 | `!true` → `false`                 |
|          |                 |                                            | `!false` → `true`                 |

## Zahlen Operatoren

| Operator | Name              | Beschreibung                                                                 | Beispiel                    | Ergebnis |
|----------|-------------------|------------------------------------------------------------------------------|-----------------------------|----------|
| `+`      | Addition           | Zwei Werte werden addiert                                                    | `5 + 3`                     | `8`      |
| `-`      | Subtraktion        | Ein Wert wird von einem anderen abgezogen                                    | `10 - 4`                    | `6`      |
| `*`      | Multiplikation     | Zwei Werte werden multipliziert                                              | `7 * 2`                     | `14`     |
| `/`      | Division           | Ein Wert wird durch einen anderen geteilt                                    | `8 / 2`                     | `4`      |
| `%`      | Modulo (Rest)      | Gibt den Rest einer Division zurück                                          | `9 % 4`                     | `1`      |
| `++x`    | Präfix-Inkrement   | Erhöht `x` um 1 **vor der Verwendung**                                       | `x = 3; y = ++x;`           | `y = 4`  |
| `x++`    | Postfix-Inkrement  | Erhöht `x` um 1 **nach der Verwendung**                                      | `x = 3; y = x++;`           | `y = 3`, `x = 4` |
| `--x`    | Präfix-Dekrement   | Verringert `x` um 1 **vor der Verwendung**                                   | `x = 3; y = --x;`           | `y = 2`  |
| `x--`    | Postfix-Dekrement  | Verringert `x` um 1 **nach der Verwendung**                                  | `x = 3; y = x--;`           | `y = 3`, `x = 2` |

# Ein- und Ausgabe

---
In Java wird die Ein- und Ausgabe über die Konsole in der Regel mit den Klassen aus dem **`java.util.Scanner`** Paket (für die Eingabe) und der **`System.out`** Klasse (für die Ausgabe) durchgeführt.

## Ausgabe
### Beispiel:
```java
int planeten = 8;
// Ausgabe ohne Zeilenumbruch
System.out.print("Hallo, ");
System.out.print("Welt!");
        
// Ausgabe mit Zeilenumbruch
System.out.println("Hallo, Welt!");

// Ausgabe mit Variablen
System.out.println("Es gibt " + planeten + "Planeten in unserem Sommensystem!");
```
### Konsole:
```java
Hallo, Welt!Hallo, Welt!
Es gibt 8 Planeten in unserem Sommensystem!
```

## Eingabe
### Beispiel:
```java
import java.util.Scanner;

// Scanner-Objekt erstellen, um Benutzereingaben zu lesen
Scanner scanner = new Scanner(System.in);
// Liest die nächste ganze Zahl vom Datentyp (Int) aus Konsole und speichert sie in Variable alter
int alter = scanner.nextInt();

// Scanner bei Programmende deaktivieren, um Ressourcen freizugeben
scanner.close();
```

# Datentypen Umwandlung in Java

---
In Java gibt es zwei Hauptarten von Datentypen-Umwandlungen: **automatische (implizite)** und **manuelle (explizite)** Umwandlung.

## 1. Automatische Umwandlung

Bei der **automatischen Umwandlung** wird ein Datentyp in einen anderen größeren Datentyp umgewandelt, ohne dass der Entwickler dies explizit angeben muss. Diese Umwandlung geschieht automatisch, wenn der Wert in den Zieltyp passt.

### Beispiel:
```java
int zahl = 10;
double ergebnis = zahl; // int wird automatisch in double umgewandelt
```

## 2. Manuelle Umwandlung

Bei der manuellen Umwandlung muss der Entwickler explizit angeben, dass ein Datentyp in einen kleineren Datentyp umgewandelt werden soll. Diese Umwandlung kann zu einem Verlust von Informationen führen, insbesondere bei Gleitkommazahlen, die in Ganzzahlen umgewandelt werden.

### Beispiel 1:
```java
double zahl = 10.99;
int ergebnis = (int) zahl; // double wird manuell in int umgewandelt
System.out.println(ergebnis); // Ausgabe: 10
```
In diesem Beispiel wird der Dezimalteil der Zahl 10.99 abgeschnitten, und die Zahl wird als 10 gespeichert. Es findet ein Verlust der Nachkommastellen statt.
## 3. Umwandlung von String zu primitiven Datentypen

Ein häufiger Fall ist die Umwandlung von Strings in primitive Datentypen, z. B. bei Benutzereingaben. Dies kann durch die Verwendung von Wrapper-Klassen erfolgen, die die parse-Methoden bieten.
### Beispiel:
```java
String zahlString = "123";
int zahl = Integer.parseInt(zahlString);  // Umwandlung von String zu int

String doubleString = "3.14";
double pi = Double.parseDouble(doubleString);  // Umwandlung von String zu double
```

## 4. Umwandlung von primitiven Datentypen zu String

Um einen primitiven Datentyp in einen String zu konvertieren, kannst du entweder die String.valueOf()-Methode oder die +-Operator-Überladung verwenden.### Beispiel:

### Beispiel:
```java
int zahl = 42;
String zahlString = String.valueOf(zahl);  // Umwandlung von int zu String

double pi = 3.14;
String piString = pi + "";  // Eine weitere Möglichkeit, double zu String zu konvertieren
```

## 5. ASCII-Tabelle

Da char intern als Zahl gespeichert wird, kann man zwischen char und int umwandeln:

[ASCII-Tabelle auf ascii-code.com](https://www.ascii-code.com/)

### Beispiel:
```java
char buchstabe = 'A';
int buchstabenCode = buchstabe;
System.out.Println(buchstabenCode);
char buchstabeVonCode = (char) buchstabenCode;
System.out.Println(buchstabeVonCode);
```

### Console:
```text
65
A
```

# If-else Verzweigung

---
Die `if-else` Verzweigung ist eine grundlegende Kontrollstruktur in Java. Sie wird verwendet, um Entscheidungen zu treffen und verschiedene Code-Blöcke auszuführen – je nachdem, ob eine Bedingung **wahr (`true`)** oder **falsch (`false`)** ist.

```java
boolean bedingung = 1 > 2; // = false
if (bedingung){
    // Wird ausgeführt, wenn Bedingung true ist
} else {
    // Wird ausgeführt, wenn Bedingung false ist
}
```

# Switch-case Verzweigung

Die `Switch-case` Verzweigung ist eine Alternative zur `if-else`-Kette. Sie wird verwendet, wenn eine Variable mit **mehreren festen Werten** verglichen werden soll.

---

```java
switch (variable) {
        case Wert1:
        // Code, wenn variable == Wert1
        break;
        case Wert2:
        // Code, wenn variable == Wert2
        break; // Switch case wird verlassen

        case Wert3:
        // Code, wenn variable == Wert3
        // Code läuft weiter bis zum nächsten break

        case Wert4:
        // Code, wenn variable == Wert4
        break;

// Weitere Fälle können hier hinzugefügt werden

default:
        // Code, wenn kein anderer Fall passt
        }

```

## Aufgabe: Altersprüfung

**Ziel:** Lies das Alter einer Person über die Konsole ein und gib eine passende Nachricht aus.

### Anforderungen:
1. Nutze `Scanner`, um eine Zahl vom Benutzer einzulesen.
2. Wenn die Person:
    - **unter 18** ist, gib aus: `"Du bist noch minderjährig."`
    - **genau 18** ist, gib aus: `"Du bist gerade volljährig geworden!"`
    - **über 18** ist, gib aus: `"Du bist volljährig."`

### Beispielausgabe:

```text
Wie alt bist du?
18
Du bist gerade volljährig geworden!
```

## Aufgabe: Monat bestimmen

**Ziel:** Lies eine Zahl von 1 bis 12 über die Konsole ein und gib den entsprechenden Monatsnamen aus.

### Anforderungen:
1. Nutze `Scanner`, um eine Zahl (Monatsnummer) vom Benutzer einzulesen.
2. Verwende eine `switch-case`-Struktur, um die Zahl einem Monatsnamen zuzuordnen.
3. Wenn die Zahl außerhalb des Bereichs 1–12 liegt, gib aus: `"Ungültige Eingabe."`

### Beispielausgabe:

```text
Bitte gib eine Monatszahl ein: 3
Der gesuchte Monat ist März!
```

## Aufgabe: Durchschnitt berechnen mit Rundung

**Ziel:** Berechne den Durchschnitt von drei Ganzzahlen und gib das Ergebnis als Gleitkommazahl mit einer Dezimalstelle aus.

### Anforderungen:
1. Lies drei ganze Zahlen (`int`) von der Konsole ein.
2. Berechne den Durchschnitt.
3. Achte auf **korrekte Typumwandlung**, damit keine Ganzzahldivision entsteht.
4. Gib das Ergebnis als `double` mit **einer Nachkommastelle** aus.

### Beispiel:

```text
Gib drei ganze Zahlen ein:
5
8
7
Der Durchschnitt ist: 6.7
## 1. Datentypen

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

## 1.1 Deklaration

Deklaration bedeutet, eine Variable mit einem bestimmten Typ zu **definieren**, aber noch **keinen Wert zuzuweisen**.
### Beispiel:
```java
int zahl;
String name;
float kommazahl;
char buchstabe;
```

## 1.2 Initialisierung

Initialisierung bedeutet, eine Variable bei der Deklaration sofort mit einem Wert zu versehen.
### Beispiel:
```java
int alter = 25;
String stadt = "Berlin";
boolean istAngemeldet = true;
char symbol = '#';
```

## 1.3 Wertzuweisung

Wertzuweisung bedeutet, einer bereits deklarierten Variable einen Wert zuzuweisen (oder den bisherigen zu überschreiben).
### Beispiel:
```java
alter = 7;
stadt = "Braum";
istAngemeldet = false;
symbol = '!';
```
---
# 2. Operatoren

## 2.1 Vergleichsoperatoren

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
## 2.2 Logische Operatoren

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
## 2.3 Zahlen Operatoren

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

---
# 3. Ein- und Ausgabe in der Konsole

In Java wird die Ein- und Ausgabe über die Konsole in der Regel mit den Klassen aus dem **`java.util.Scanner`** Paket (für die Eingabe) und der **`System.out`** Klasse (für die Ausgabe) durchgeführt.

## 3.1 Ausgabe
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

## 3.2 Eingabe
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

---
# 4. Datentypen Umwandlung

In Java gibt es zwei Hauptarten von Datentypen-Umwandlungen: **automatische (implizite)** und **manuelle (explizite)** Umwandlung.

## 4.1 Automatische Umwandlung

Bei der **automatischen Umwandlung** wird ein Datentyp in einen anderen größeren Datentyp umgewandelt, ohne dass der Entwickler dies explizit angeben muss. Diese Umwandlung geschieht automatisch, wenn der Wert in den Zieltyp passt.

### Beispiel:
```java
int zahl = 10;
double ergebnis = zahl; // int wird automatisch in double umgewandelt
```

## 4.2 Manuelle Umwandlung

Bei der manuellen Umwandlung muss der Entwickler explizit angeben, dass ein Datentyp in einen kleineren Datentyp umgewandelt werden soll. Diese Umwandlung kann zu einem Verlust von Informationen führen, insbesondere bei Gleitkommazahlen, die in Ganzzahlen umgewandelt werden.

### Beispiel:
```java
double zahl = 10.99;
int ergebnis = (int) zahl; // double wird manuell in int umgewandelt
System.out.println(ergebnis); // Ausgabe: 10
```
In diesem Beispiel wird der Dezimalteil der Zahl 10.99 abgeschnitten, und die Zahl wird als 10 gespeichert. Es findet ein Verlust der Nachkommastellen statt.
## 4.3 Umwandlung von String zu primitiven Datentypen

Ein häufiger Fall ist die Umwandlung von Strings in primitive Datentypen, z. B. bei Benutzereingaben. Dies kann durch die Verwendung von Wrapper-Klassen erfolgen, die die parse-Methoden bieten.
### Beispiel:
```java
String zahlString = "123";
int zahl = Integer.parseInt(zahlString);  // Umwandlung von String zu int

String doubleString = "3.14";
double pi = Double.parseDouble(doubleString);  // Umwandlung von String zu double
```

## 4.4 Umwandlung von primitiven Datentypen zu String

Um einen primitiven Datentyp in einen String zu konvertieren, kannst du entweder die String.valueOf()-Methode oder die +-Operator-Überladung verwenden.### Beispiel:

### Beispiel:
```java
int zahl = 42;
String zahlString = String.valueOf(zahl);  // Umwandlung von int zu String

double pi = 3.14;
String piString = pi + "";  // Eine weitere Möglichkeit, double zu String zu konvertieren
```

## 4.5 ASCII-Tabelle

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

---
# 5. If-else Verzweigung

Die `if-else` Verzweigung ist eine grundlegende Kontrollstruktur in Java. Sie wird verwendet, um Entscheidungen zu treffen und verschiedene Code-Blöcke auszuführen – je nachdem, ob eine Bedingung **wahr (`true`)** oder **falsch (`false`)** ist.

```java
boolean bedingung = 1 > 2; // = false
if (bedingung){
    // Wird ausgeführt, wenn Bedingung true ist
} else {
    // Wird ausgeführt, wenn Bedingung false ist
}
```

---
# 6. Switch-case Verzweigung

Die `Switch-case` Verzweigung ist eine Alternative zur `if-else`-Kette. Sie wird verwendet, wenn eine Variable mit **mehreren festen Werten** verglichen werden soll.

```java
int zahl = 231

switch (zahl) {
        case 1:
        // Code, wenn variable == 1
        break;
        case 2:
        // Code, wenn variable == 2
        break; // Switch case wird verlassen

        case 3:
        // Code, wenn variable == 3
        // Code läuft weiter bis zum nächsten break

        case 4:
        // Code, wenn variable == 4
        break;

// Weitere Fälle können hier hinzugefügt werden

default:
        // Code, wenn kein anderer Fall passt
        }

```

---
# 7. While-schleifen

## 7.1 While-Schleife

>Eine while Schleife führt einen Anweisungsblock so lange aus, bis die Prüf**bedingung** nicht mehr wahr ist

Eine **Iteration** ist ein einzelner Durchlauf einer Schleife, bei dem der enthaltene Anweisungsblock einmal ausgeführt wird, solange die Bedingung erfüllt ist.

Wie oft wird der Schleifenblock (also eine Iteration) bei dieser Bedingung ausgeführt?

```java 
// Nachbau einer while-Schleife  
boolean bedingung = true;  
int zähler = 0;  
int iterationen = 9;  
  
while (bedingung == true) {  
    System.out.println("Wert von zähler: " + zähler);  
  
    if (zähler >= iterationen - 1) {  
         bedingung = false;  
    } else {  
        zähler++;  
    }  
}
```

### Console :
```Console
Wert von zähler: 0
Wert von zähler: 1
Wert von zähler: 2
Wert von zähler: 3
Wert von zähler: 4
Wert von zähler: 5
Wert von zähler: 6
Wert von zähler: 7
Wert von zähler: 8
```

## 7.2 Do-While-Schleife

> Eine **do-while** Schleife führt einen Anweisungsblock mindestens einmal aus, bevor die Prüfbedingung überprüft wird. Sie prüft die Bedingung nach der ersten Ausführung des Schleifenblocks, wodurch der Block immer mindestens einmal ausgeführt wird, auch wenn die Bedingung zu Beginn **falsch** ist.

Eine **Iteration** ist ein einzelner Durchlauf der Schleife, bei dem der Anweisungsblock ausgeführt wird, solange die Bedingung nach dem ersten Durchlauf wahr ist.

Wie oft wird der Schleifenblock (also eine Iteration) bei dieser Bedingung ausgeführt?

### Beispiel:
```java
// Nachbau einer do-while-Schleife, bei der die Bedingung von Anfang an falsch ist
int zähler = 10;  // Der Zähler beginnt bei 10
int iterationen = 5;  // Die Schleife sollte 5 Mal durchlaufen

do {  
    System.out.println("Wert von zähler: " + zähler);  
    zähler++;  
} while (zähler < iterationen);  // Die Bedingung ist von Anfang an falsch
```

### Console:
```Console
Wert von zähler: 10
```

### 7.2.1 Unterschiede zur While-Schleife:
- Bei einer **while**-Schleife würde der Schleifenblock nicht ausgeführt werden, wenn die Bedingung von Anfang an falsch ist.
- Bei einer **do-while**-Schleife wird der Schleifenblock **mindestens einmal** ausgeführt, selbst wenn die Bedingung nach dem ersten Durchlauf falsch ist.

---
# 8 Methoden in Java

Eine Methode in Java ist eine Funktion, die innerhalb einer Klasse definiert wird. Sie kann von anderen Methoden innerhalb derselben Klasse aufgerufen werden. Je nach den verwendeten Zugriffsmodifizierern, kann sie auch von außerhalb der Klasse aufgerufen werden.

### 8.1 Eigenschaften von Methoden:

1. **Scoop der Variablen**: Eine innerhalb einer Methode deklarierte Variable kann nur in dieser Methode verwendet werden.
2. **Übergeben von Variablen**: Beim Aufruf einer Methode können Variablen übergeben werden. Diese Variablen sind dann innerhalb der Methode verfügbar, ohne dass sie explizit dort deklariert werden müssen.
3. **Rückgabewert**: Methoden können einen Wert zurückgeben. Der Rückgabetyp wird dabei im Methodenkopf angegeben.
4. **Beendigung einer Methode**: Eine Methode kann auf verschiedene Arten beendet werden:
    - Sie wurde vollständig durchlaufen.
    - Sie hat einen Wert zurückgegeben.
    - Sie hat einen Fehler geworfen.

> `void` steht immer für "keinen Wert", d.h. die Methode gibt keinen Wert zurück.

### 8.2 Aufbau einer Methode:

Die Grundstruktur einer Methode sieht wie folgt aus:

####  8.2.1 Ohne Rückgabe- und Übergabewert/e

```java
public void methodeName() {
    // Code
}
```

#### 8.2.2 Mit Übergabewert

```java
public int berechneSumme() {
    return 42;
}
```

#### 8.2.3 Mit Rückgabewert

```java
public void druckeSumme(int zahl) {
    System.out.println(zahl);
}
```

#### 8.2.4 Mit Rückgabe- und Übergabewerten

```java
public int addiere(int a, int b) {
    return a + b;
}
```

### 8.3 Aufruf einer Methode:

Je nachdem, wie eine Methode deklariert wurde, muss sie entsprechend aufgerufen werden. Es gibt verschiedene Arten des Aufrufs

#### 8.3.1 Ohne Rückgabe- und Übergabewert/e

```
methodeName();
```

#### 8.3.2 Mit Übergabewert

```
druckeSumme(5);
```

#### 8.3.3 Mit Rückgabewert

```
int summe = berechneSumme();
```

#### 8.3.4 Mit Rückgabe- und Übergabewerten

```
int ergebnis = addiere(5, 7);
System.out.println(ergebnis); // Ausgabe: 12
```

---
# 9. Arrays

Ein **Array** ist eine Sammlung von **gleichen Datentypen**, die unter einem gemeinsamen Namen gespeichert sind. Arrays bieten eine Möglichkeit, mehrere Werte gleichzeitig zu speichern und über Indizes darauf zuzugreifen. Der Index eines Arrays beginnt immer bei **0**.

### 9.1 Deklaration und Initialisierung eines Arrays

Ein Array muss zunächst deklariert und anschließend mit Werten initialisiert werden. Die Deklaration erfolgt mit dem Datentyp des Arrays und der Anzahl der Elemente, die es speichern soll.

```java
int[] zahlen = {1, 2, 3, 4, 5}; 
```

### 9.2 Zugriff auf Array-Elemente

Um auf die Elemente eines Arrays zuzugreifen, verwendet man den Index des jeweiligen Elements. Der Index beginnt bei 0 für das erste Element, 1 für das zweite Element usw.

```java
int[] zahlen = {1, 2, 3, 4, 5};
System.out.println(zahlen[0]);  // Ausgabe: 1
System.out.println(zahlen[3]);  // Ausgabe: 4
```

### Console:
```plaintext
1
4
```
### 9.3 Iteration über ein Array

Man kann auch eine Schleife verwenden, um über alle Elemente eines Arrays zu iterieren und diese zu verarbeiten.

```java
int[] zahlen = {1, 2, 3, 4, 5};

for (int i = 0; i < zahlen.length; i++) {
    System.out.println("Element " + i + ": " + zahlen[i]);
}
```

### Console:
```Console
Element 0: 1
Element 1: 2
Element 2: 3
Element 3: 4
Element 4: 5
```

### 9.4 Array mit `for-each`-Schleife

In Java gibt es auch eine vereinfachte Möglichkeit, über Arrays zu iterieren: die **`for-each`-Schleife**. Sie ist besonders nützlich, wenn man auf jedes Element eines Arrays zugreifen möchte, ohne den Index manuell zu handhaben.

```java
int[] zahlen = {1, 2, 3, 4, 5};
for (int zahl : zahlen) {
    System.out.println(zahl);
}
```

### Console:
```Console
1
2
3
4
5
```

### 9.5 Ändern von Werten in einem Array

Da Arrays veränderbar sind, kannst du die Werte eines Arrays auch ändern, indem du den entsprechenden Index angibst.

```java
int[] zahlen = {1, 2, 3, 4, 5};
zahlen[2] = 99;
System.out.println(zahlen[2]); 
```

### Console:
```plainText
99
```

### 9.6 Mehrdimensionale Arrays

In Java kannst du auch Arrays mit mehreren Dimensionen erstellen, wie z.B. ein **zweidimensionales Array** (eine Matrix).

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

System.out.println(matrix[0][1]);  // Ausgabe: 2
System.out.println(matrix[2][0]);  // Ausgabe: 7
```

### Console:
```Console
2
7
```

---

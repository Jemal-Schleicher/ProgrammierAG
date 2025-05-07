>Eine while Schleife führt einen Anweisungsblock so lange aus, bis die Prüf**bedingung** nicht mehr wahr ist

>Eine **Iteration** ist ein einzelner Durchlauf einer Schleife, bei dem der enthaltene Anweisungsblock einmal ausgeführt wird, solange die Bedingung erfüllt ist.

>Wie oft wird der Schleifenblock (also eine Iteration) bei dieser Bedingung ausgeführt?

Code:
```java 
// Nachbau einer for-Schleife mit while  
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

Ausgabe :
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

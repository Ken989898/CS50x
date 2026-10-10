# CS50x — Problem Set 1

Meine Lösungen zu **CS50x: Introduction to Computer Science** (HarvardX).
Programmiersprache: C. Alle hier abgelegten Lösungen sind mit `check50`
geprüft.

Ich arbeite den Kurs parallel zum Abitur durch, als Vorbereitung auf ein
duales Studium der Angewandten Informatik.

\---

## Problem Set 1

### `credit` — Kreditkartenvalidierung mit dem Luhn-Algorithmus

**Aufgabe:** Eine Kartennummer einlesen, mit dem Luhn-Algorithmus auf
Gültigkeit prüfen und den Kartentyp bestimmen (VISA, MASTERCARD, AMEX)
oder `INVALID` ausgeben.

**Der Algorithmus:** Jede zweite Ziffer von rechts wird verdoppelt. Ergibt
die Verdopplung eine zweistellige Zahl, werden deren Ziffern einzeln addiert.
Diese Summe wird zu der Summe der übrigen Ziffern addiert. Ist das Ergebnis
durch 10 teilbar, ist die Nummer gültig.

**Mein Ansatz:** Statt die Nummer als Zeichenkette zu behandeln, arbeite ich
rein arithmetisch. Einzelne Ziffern hole ich über `input % modulo / divisor`
heraus und erhöhe `modulo` und `divisor` pro Schritt um den Faktor 100 —
so trifft eine Schleife genau jede zweite Stelle. Die Stellenzahl bestimme
ich über eine Schleife, die die Zahl so lange durch 10 teilt, bis sie 0 ist.
Der Kartentyp ergibt sich aus den führenden Ziffern in Kombination mit der
Stellenzahl.

\---

### `cash` — Wechselgeld mit minimaler Münzanzahl

**Aufgabe:** Einen Centbetrag einlesen und die kleinstmögliche Anzahl Münzen
(25, 10, 5, 1 Cent) ausgeben, die diesen Betrag ergibt.

**Der Ansatz:** Ein Greedy-Algorithmus — immer die größte Münze nehmen, die
noch in den Restbetrag passt, und den Rest entsprechend verringern. Für das
US-Münzsystem liefert Greedy nachweislich das Optimum.

\---

### `mario-more` — Pyramiden mit verschachtelten Schleifen

**Aufgabe:** Eine Höhe zwischen 1 und 8 einlesen und zwei gegenüberliegende
Treppenpyramiden aus `#` ausgeben, getrennt durch eine Lücke von zwei
Leerzeichen.

**Der Ansatz:** Verschachtelte `for`-Schleifen. Die äußere Schleife läuft über
die Zeilen, die inneren erzeugen pro Zeile die führenden Leerzeichen, den
linken Block, die Lücke und den rechten Block. Die Anzahl der Leerzeichen
nimmt pro Zeile ab, während die Blockbreite zunimmt.

\---

## Hinweis

Dieses Repository dokumentiert meinen eigenen Lernweg.

Meinen Code darf ich aufgrund der CS50x Regeln nicht hochladen.

Bei Interesse kann ich diesen aber gerne nachreichen.




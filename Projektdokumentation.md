# Spiele Api

# Projekt-Dokumentation

Müller und Jeanneret

## 1 Informieren

### 1.1 Ihr Projekt

In diesem Projekt entwickeln wir eine Anwendung, mit der man Binärcode ineinander umrechnen kann.

| US-№ | Verbindlichkeit | Typ           | Beschreibung                                                                                                                                                |
| ---- | --------------- | ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | Muss            | Funktional    | Als Benutzer möchte ich die Applikation starten können, um sie für meine Zwecke verwenden zu können.                                                        |
| 2    | Muss            | Funktional    | Als Benutzer möchte ich Binärcode in Dezimalzahlen umrechnen können, um verschiedene Codes miteinander vergleichen zu können.                               |
| 3    | Muss            | Funktional    | Als Benutzer möchte ich Dezimalzahlen in Binärcode umrechnen können, um effizient mit Binärdaten arbeiten zu können.                                        |
| 4    | Muss            | Funktional    | Als Benutzer möchte ich Dezimalzahlen mit Kommas in der Applikation in Binärcode umrechnen können, um präzise Daten verarbeiten zu können.                  |
| 5    | Muss            | Funktional    | Als Benutzer möchte ich sehen, welcher Binärcode für welche Dezimalzahl steht, um eine klare Zuordnung der Werte zu haben.                                  |
| 6    | Muss            | Funktional    | Als Benutzer möchte ich BCD-Code verwenden können in der Applikation, um spezielle binäre Darstellungen zu nutzen.                                          |
| 7    | Muss            | Funktional    | Als Benutzer möchte ich ASCII-Code verwenden können in der Applikation, um andere binäre Daten umrechnen zu können.                                         |
| 8    | Muss            | Funktional    | Als Benutzer möchte ich die verschiedenen Binärcodes ineinander umrechnen können, um flexibel zwischen den Darstellungen zu wechseln.                       |
| 9    | Muss            | Qualität      | Als Benutzer möchte ich, dass Fehleingaben abgefangen werden, um sicherzustellen, dass die Umrechnungen korrekt erfolgen.                                   |
| 10   | Muss            | Randbedingung | Als Benutzer möchte ich, dass die Applikation benutzerfreundlich ist, damit ich sie intuitiv und effizient nutzen kann.                                     |

### 1.3 Testfälle

| TC-№ | Ausgangslage | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1  | PC ist gestartet | Applikation öffnen | Applikation öffnet sich. |
| 2.1  | Applikation ist am laufen | Im Menü auf Umrechnen drücken. | Umrechnermenü öffnet sich. |
| 3.1  | Umrechnungsmenü ist offen | Im Menü bei Eingabe, Dezimalzahl auswählen und bei Ausgabe, BCD-Code auswählen.| Umrechner braucht Eingabedaten. |
| 3.2  | Umrechnungsmenü ist offen | In der Eingabe wird die Dezimalzahl 1 eingegeben. | In der Ausgabe wird 0001 ausgegeben. |
| 4.1  | Umrechnungsmenü ist offen | Im Menü bei Eingabe, Dezimal auswählen und bei der Ausgabe, ASCII-Code auswählen. | Umrechner braucht Eingabedaten. |
| 4.2  | Umrechnungsmenü ist offen | In der Eingabe, wird die Zahl 1 eingegeben. | In der Ausgabe steht 00110001. |
| 5.1  | Umrechnungsmenü ist offen | Im Menü bei Eingabe, ASCII-Code auswählen und bei Ausgabe, BCD-Code auswählen. |
| 5.2  | Umrechnungsmenü ist offen | In der Eingabe, wird 00110111	eingeben.| In der Ausgabe steht 0111. |
| 6.1  | Umrechnungsmenü ist offen | Im Menü bei Eingabe, BCD-Code auswählen und bei Ausgabe, Dezimalzahl auswählen. |
| 6.2  | Umrechnungsmenü ist offen | In der Eingabe, wird 0011 eingegeben. | In der Ausgabe steht 3. |


### 1.4 Diagramme

![Alt text](<Use Case Diagramm.png>)

## 2 Planen

| AP-№ | Frist      | Zuständig   | Beschreibung                  | geplante Zeit |
| ---- | ---------- | ----------- | ----------------------------- | ------------- |
| 1.A  | 05.02.2024 | Müller      | Schere Stein Papier           | 6\*45'        |
| 2.A  | 05.02.2024 | Sacher      | Russian Roulette              | 8\*45'        |
| 3.A  | 05.02.2024 | Müller      | Wahl bei Schere Stein Papier  | 45'           |
| 4.A  | 05.02.2024 | Hitz        | Spielauswahl                  | 45'           |
| 5.A  | 05.02.2024 | Sacher      | Multiplayer                   | 2\*45'        |
| 6.A  | 05.02.2024 | Sacher      | Computer Gegner               | 2\*45'        |
| 7.A  | 05.02.2024 | Hitz        | Waffenwahl Russian Roulette   | 2\*45'        |
| 8.A  | 05.02.2024 | Sacher      | Eine Kugel pro Waffe          | 45'           |
| 8.B  | 05.02.2024 | Hitz        | Schuss Sound                  | 45'           |
| 9.A  | 05.02.2024 | Hitz        | Itemwahl                      | 2\*45'        |
| 10.A | 05.02.2024 | Hitz        | Spielanleitungen              | 30'           |
| 11.A | 05.02.2024 | Müller      | Fehleingaben abfangen         | 45'           |
| 12.A | 05.02.2024 | Hitz        | Benutzerfreundliches Frontend | 45'           |
| 13.A | 05.02.2024 | Sacher      | API                           | 3\*45'        |
| 14.A | 05.02.2024 | Sacher      | Testen                        | 30            |
| 15.A | 05.02.2024 | Individuell | Portfolio                     | 4\*45'        |

Total:

## 3 Entscheiden

Wir haben uns dazu entschieden, den Modus für lokales Zusammenspielen weg zu lassen.
Ausserdem haben wir uns dazu entschieden, die Items in dem russischen Roulette Spiel weg zu lassen.

## 4 Realisieren

| AP-№ | Datum             | Zuständig   | geplante Zeit | tatsächliche Zeit |
| ---- | ----------------- | ----------- | ------------- | ----------------- |
| 1.A  |  23.02.24                 | Müller      | 6\*45         |   8*45                |
| 2.A  | 19.01. - 02.02.24 | Sacher      | 8\*45         | 12\*45'           |
| 3.A  | 26.01.24          | Müller      | 45            |   45                |
| 4.A  |  23.02.24                 | Hitz        | 45            |    2*45               |
| 5.A  | -                 | Sacher      | 2\*45         | -                 |
| 6.A  | 26.01.24          | Sacher      | 2\*45         | 30'               |
| 7.A  | 23.2.24                  | Hitz        | 2\*45         |  -                 |
| 8.A  | 26.01.24          | Sacher      | 45            | 15'               |
| 8.B |   26.01.24      |    Hitz        | 45            | 45
| 9.A  | 23.2.24                  | Hitz        | 2*45            |  -                 |
| 10.A |  23.2.24                 | Hitz        | 30        |  25                |
| 11.A | 23.2.24                  | Müller        | 45            |   45                |
| 12.A |   23.2.24                | Hitz      | 45            |    45               |
| 13.A |  23.2.24                 | Sacher        | 3*45            |     4*45              |
| 14.A | 19.01.24          | Sacher      | 30        | 45'               |
| 15.A   |  1.3.24                 | Individuell      | 4*45            |    4*45               |
 

## 5 Kontrollieren

### 5.1 Testprotokoll

| TC-№ | Datum      | Resultat | Tester |
| ---- | ---------- | -------- | ------ |
| 1.1  | 01.03.2024 | OK ✅    | Sacher |
| 1.2  | 01.03.2024 | OK ✅    | Sacher |
| 1.4  | 01.03.2024 | OK ✅    | Sacher |
| 1.5  | 01.03.2024 | OK ✅    | Sacher |
| 1.6  | 01.03.2024 | OK ✅    | Sacher |
| 1.7  | 01.03.2024 | OK ✅    | Sacher |
| 1.8  | 01.03.2024 | OK ✅    | Sacher |
| 1.9  | 01.03.2024 | OK ✅    | Sacher |
| 2.1  | 01.03.2024 | OK ✅    | Sacher |
| 3.1  | 01.03.2024 | OK ✅    | Sacher |
| 4.1  | 01.03.2024 | OK ✅    | Sacher |
| 5.1  | 01.03.2024 | NOK ❌   | Sacher |
| 6.1  | 01.03.2024 | OK ✅    | Sacher |
| 7.1  | 01.03.2024 | NOK ❌   | Sacher |
| 8.1  | 01.03.2024 | OK ✅    | Sacher |
| 8.2  | 01.03.2024 | OK ✅    | Sacher |
| 9.1  | 01.03.2024 | OK ✅    | Sacher |
| 10.1 | 01.03.2024 | NOK ❌   | Sacher |
| 11.1 | 01.03.2024 | OK ✅    | Sacher |
| 12.1 | 01.03.2024 | OK ✅    | Sacher |

Die Testfälle, die nicht erfüllt wurden, also die Items, der lokale Multiplayer und die Auswahl der verschiedenen Waffen in dem russischen Roulette Spiel, lassen sich sehr gut in der Zukunft als Erweiterungen oder Updates hinzufügen. Trotz diesen fehlgeschlagenen Tests, ist die SpieleApi voll funktionsfähig und funktioniert ohne Fehler.

## 6 Auswerten

- Portfolioeintrag Robin Sacher: https://portfolio.bbbaden.ch/view/view.php?t=d14ea1bf74539810c87b
- Portfolioeintrag Julian Hitz: https://portfolio.bbbaden.ch/view/view.php?t=36424a8005e4d8914a5b
- Portfolioeintrag Damian Müller: https://portfolio.bbbaden.ch/view/view.php?t=921690286c35cfb6bd6b

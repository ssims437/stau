# Stau

**Warum es steht, obwohl nichts passiert ist.** Kein Unfall, keine Baustelle — und trotzdem
Stillstand. Solche Staus entstehen aus dem Verkehr selbst. Dieses Blatt baut ihn aus vier Regeln
nach und misst nach, was sonst behauptet wird.

→ **[Blatt öffnen](https://ssims437.github.io/stau/)**

- **Weg-Zeit-Bild** einer Ringstraße: jede schräge Linie ein Auto, die dunklen Bänder die Staus —
  sie laufen sichtbar **gegen** die Fahrtrichtung
- **Fundamentaldiagramm** aus 60 eigenen Läufen, mit dem Umschlagpunkt und einer Vergleichskurve
  ohne Trödeln
- **Dichte, Trödelwahrscheinlichkeit und Höchsttempo** am Regler; „Einer bremst" setzt die
  Störung von Hand
- **Prüflauf** — acht Zeilen, darunter die kritische Dichte gegen ihre Herleitung

## Die vier Regeln

```
1 beschleunigen  wer langsamer als erlaubt fährt, wird um eins schneller
2 bremsen        wer dem Vordermann zu nahe kommt, geht auf dessen Abstand herunter
3 trödeln        mit Wahrscheinlichkeit p wird einer grundlos um eins langsamer
4 fahren         alle rücken gleichzeitig um ihre Geschwindigkeit vor
```

Mehr ist es nicht (Nagel und Schreckenberg, 1992). Ein Feld ist 7,5 m, ein Schritt eine Sekunde.
**Regel 3 ist die entscheidende**: Ohne sie fährt sich der Verkehr in einen völlig gleichmäßigen
Zustand ein. Mit ihr genügt ein einziges unnötiges Bremsen, und die Störung wandert rückwärts
durch die Kolonne.

## Was der Prüflauf zeigt

| Behauptung | Ergebnis |
|---|---|
| kein Auto verschwindet, keines fährt durch ein anderes | 18 Läufe · 5400 Zeitschritte · **0** Verstöße in drei Kategorien |
| der Durchsatz stimmt, egal wie man ihn misst | feste Zählstelle gegen Dichte × Tempo · Unterschied **9,9·10⁻³** Autos/s |
| ohne Trödeln gibt es keinen Stau — bis es nicht mehr geht | unterhalb der kritischen Dichte fahren nach 900 s **alle** mit Höchsttempo |
| **die kritische Dichte steht schon in den Regeln** | gemessen 50,0 / 33,3 / 25,0 / 16,7 % gegen **1/(v+1)** = 50 / 33,3 / 25 / 16,7 % |
| die Stauwelle läuft mit genau einem Feld je Sekunde zurück | 29 aufeinanderfolgende Sekunden, jedes Mal genau ein Feld |
| Staus entstehen aus dem Nichts — aber nicht überall | dünner Verkehr: **0** Staus · dichter: **57** — ohne jedes Hindernis |
| dieselbe Saat, dieselbe Straße | 18 000 Auto-Zeit-Felder, 0 Unterschiede · andere Saat: 98 % anders |
| **und wie schnell wandert der Stau wirklich** | sechs Dichten · alle rückwärts · im Mittel **−15,3 km/h** |

## Die zwei Zahlen, die man nicht verwechseln darf

| | Wert | was es ist |
|---|---|---|
| **Auflösungskante** | −27 km/h | ein *vollständig stehender* Pulk löst sich auf: je Sekunde fährt genau ein Auto ab, also rückt die Kante um genau ein Feld zurück. Folgt zwingend aus den Regeln |
| **Stauwelle im Verkehr** | **−15,3 km/h** | wie schnell ein echter Stau im laufenden Verkehr rückwärts wandert. Gemessen, nicht gerechnet |

Die zweite Zahl ist die schöne: Auf echten Autobahnen misst man etwa **−15 km/h**. Im ganzen Modell
steckt keine einzige Zahl aus der Wirklichkeit — nur vier Regeln, 7,5 m je Feld und eine Sekunde je
Schritt. Der Wert kommt heraus, er wird nicht hineingesteckt.

## Was mich das gekostet hat

**Ich hatte den Stau am falschen Ende gemessen.** Die Prüfzeile „die Stauwelle läuft ein Feld je
Sekunde zurück" meldete: *0 aufeinanderfolgende Sekunden*. Der Grund war ein Denkfehler über die
Richtung: Ein Stau löst sich **vorne** auf, nicht hinten. Ich hatte das hinterste stehende Auto
verfolgt — und das steht, wie es sich für ein Stauende gehört, minutenlang völlig unbewegt da.
Gemessen werden muss das **vorderste noch stehende** Auto; dessen Position rückt je Sekunde um
genau ein Feld zurück.

**Und dann hat mich der Ring eingeholt.** Nach der Korrektur stimmten 30 Sekunden lang alle Werte —
und danach standen Sprünge von −170 Feldern in den Daten. Ursache: Die vorne abgefahrenen Autos
waren **einmal um den Ring herum** und kamen dem Stau von hinten wieder in die Quere. Physikalisch
völlig richtig, für diese Messung aber Unsinn. Die Straße ist jetzt lang genug, dass das im
Messfenster nicht passieren kann.

**Meine Randnotiz war falsch, und der Prüflauf hat sie widerlegt.** Ich hatte hingeschrieben, das
Modell könne die real gemessenen 15 km/h nicht treffen — es liefere 27 km/h und brauche dafür eine
Zusatzregel fürs zögerliche Anfahren. Beim Nachmessen kam **−15,3 km/h** heraus. Der Fehler war,
zwei verschiedene Dinge für dasselbe zu halten: die Auflösungskante eines stehenden Pulks (die
tatsächlich exakt −27 km/h hat) und die Wanderung einer Stauwelle im laufenden Verkehr. Beides steht
jetzt nebeneinander im Blatt, mit dem Unterschied ausgeschrieben — und die Notiz, die das Gegenteil
behauptete, ist weg.

**Was das Blatt nicht kann:** eine Spur, keine Überholvorgänge, keine Lastwagen, keine Auffahrten
und Abfahrten, keine Ampeln, keine Netze. Kein zögerliches Anfahren (das „slow-to-start", mit dem
sich Hysterese und metastabile Zustände zeigen lassen), keine Reaktionszeiten, keine
Geschwindigkeitsanpassung an den Verkehr weiter vorne. Und die Ringstraße ist eine Idealisierung:
Auf ihr ist die Zahl der Autos konstant, auf einer echten Autobahn kommen sie an Auffahrten dazu.

## Technik

Eine einzelne HTML-Datei. Kein Build, keine Bibliothek, nichts verlässt den Browser.
Zellularautomat, xorshift-Zufall mit Saat, Canvas 2D, hell und dunkel.

## Die ganze Sammlung

Alle Blätter nach Feld geordnet, jedes mit eigenem Repo:
**[ssims437.github.io](https://ssims437.github.io/)**

## Lizenz

MIT

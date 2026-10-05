<!-- ELUCENIA technical documentation · conversao-de-acuidade-visual · de · no clinical/professional/rights approval -->

# Umrechnung der Sehschärfe

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/conversao-de-acuidade-visual)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Eingegebene Notation

`modo`

- `s20` — Snellen 20/x (Fuß)
- `s6` — Snellen 6/x (Meter)
- `dec` — Dezimal
- `log` — logMAR

### Wert (Snellen: nur der Nenner)

`valor`

Bereich: -0,4–2000

## Fassung der Methode

Snellen/Dezimalvisus/logMAR-Umrechnung; ETDRS 1982 0,02 je Buchstabe; Holladay-Konventionen 2004

## Dokumentierte Formel

Dezimalvisus = Snellen-Zähler ÷ Nenner (20/40 = 0,5). logMAR = −log10(Dezimalvisus) = log10(MAR), wobei MAR der minimale Auflösungswinkel in Bogenminuten ist. Jede ETDRS-Zeile entspricht 0,1 logMAR (5 Buchstaben à 0,02).

## Grenzen und Population

Die Umrechnung erfordert einen positiven Snellen-Bruch und bewahrt die ursprüngliche Messung; sie führt keine neue Untersuchung durch. Vergleichen Sie Ergebnisse nur mit dokumentierter Entfernung, Auge, optischer Korrektur und Sehprobentafel. Die Abstufung von 0,1 logMAR pro Zeile und 0,02 pro Buchstabe entspricht der ETDRS-Struktur, nicht jeder Tafel. Holladay 2004 empfiehlt Mittelwerte in logMAR statt des arithmetischen Mittels der Snellen-Brüche. Fingerzählen und Handbewegungen hängen von der Entfernung ab und dürfen durch diese Umrechnung keine festen Dezimaläquivalente erhalten.

## Referenzen

- [Holladay JT. Visual acuity measurements. J Cataract Refract Surg, 2004.](https://doi.org/10.1016/j.jcrs.2004.01.014)

- [Ferris FL et al. New visual acuity charts for clinical research. Am J Ophthalmol, 1982.](https://doi.org/10.1016/0002-9394(82)90197-0)

- [Organização Mundial da Saúde. Blindness and vision impairment (fact sheet).](https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment)

- [Holladay2004,JCRS30:287–290](https://www.hicsoap.com/__static/03b5dccbd2b603d4d234479004ca5de4/097-visual-acuity-measurements-jcrs-2004-_in-3426.pdf?dl=1)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

# Codebuch Anne Will, Ukraine, Folgen 500 bis 503 (2022)

## Überblick
Gerichtetes Two-Mode-Netzwerk aus Gästen, Sendungen und Parteien.
Quelle der Gästelisten: ARD, Sendungsarchiv Anne Will.
Erhebung durch: DEIN NAME, Datum.

## Edgelist (edgelist_anne_will.csv)

| Variable | Beschreibung |
|---|---|
| from | ID des Gastes (Initialen, klein geschrieben) |
| to | ID der Sendung (Nummer) oder der Partei (Kürzel) |
| relationship | 1 = Gast in Sendung, 2 = Mitglied in Partei |

Die Kanten zeigen immer vom Gast zur Sendung oder zur Partei.

## Nodelist (nodelist_anne_will.csv)

| Variable | Beschreibung |
|---|---|
| id | Eindeutige ID. Gäste = Initialen, Sendungen = Sendungsnummer, Parteien = Kürzel |
| name | Vollständiger Name bzw. Bezeichnung |
| type | 1 = Gast, 2 = Sendung, 3 = Partei |
| party | Parteizugehörigkeit des Gastes, leer wenn keine |
| sector | Bereich des Gastes, z. B. Politik, Journalismus, Wissenschaft |
| country | Herkunftsland des Gastes |

## Hinweise
Fehlende Werte bleiben leer. Es gibt keine Sonderzeichen in den IDs.

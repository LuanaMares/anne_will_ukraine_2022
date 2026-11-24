# Datensatz Anne Will Ukraine 2022 #
Codebuch Stand 2026-11
erstellt von Luana Mares Kiefer (lk278@hdm-stuttgart.de)

## Inhalt
- edgelist_anne_will.csv (Edgelist)
- nodelist_anne_will.csv (Nodelist)
- codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung
Ich habe die Gästelisten der Talkshow "Anne Will" (ARD) aus dem Jahr 2022 für die Sendungen 500 bis 503 erhoben, die sich mit dem Krieg in der Ukraine befassen. Quelle sind die Sendungsseiten der ARD (https://www.fernsehserien.de/anne-will/episodenguide, zuletzt abgerufen 24.11.26). Parteizugehörigkeiten wurden anhand der Angaben der Sendung bzw. öffentlicher Quellen ergänzt.

Das Netzwerk ist ein *gerichtetes two-mode Netzwerk* aus Gästen, Sendungen und Parteien. Es wurden zwei Beziehungsarten erhoben.

**Teilnahmenetzwerk**
Ein Gast nahm an einer Sendung teil. Die Kante geht vom Gast zur Sendung.

**Mitgliedschaftsnetzwerk**
Ein Gast ist Mitglied einer Partei. Die Kante geht vom Gast zur Partei. Gäste ohne Parteizugehörigkeit haben keine solche Kante.

Insgesamt gibt es ANZAHL GÄSTE Gäste, 4 Sendungen und ANZAHL PARTEIEN Parteien.


# EDGE-Attribute

**from**
ID des Ausgangsknotens. Immer ein Gast (Initialen in Kleinbuchstaben, z.B. lk für Lars Klingbeil).

**to**
ID des Zielknotens. Entweder eine Sendung (500, 501, 502, 503) oder eine Partei (übliches Kürzel, z.B. SPD).

**relationship**
Art der Beziehung zwischen den Knoten
1 = Teilnahme: Der Gast (erste Spalte) war in der Sendung (zweite Spalte) zu Gast.
2 = Mitgliedschaft: Der Gast (erste Spalte) ist Mitglied der Partei (zweite Spalte).


# NODE-Attribute

**id**
Eindeutige ID des Knotens, identisch mit den IDs in der Edgelist.
Gäste = Initialen aus Vor- und Nachname, Sendungen = Sendungsnummer, Parteien = Parteikürzel.

**name**
Vollständiger Name des Gastes, Bezeichnung der Sendung (z.B. Folge 500) oder der Partei.

**type**
Art des Knotens
1 = Gast
2 = Sendung
3 = Partei

**party**
Parteizugehörigkeit des Gastes (Kürzel). Leer bei Sendungen, Parteien und parteilosen Gästen.

**sector**
Berufsfeld, in dem der Gast auftritt (z.B. Politik, Journalismus, Wissenschaft). Leer bei Sendungen und Parteien.

**country**
Land, dem der Gast zugeordnet wird (z.B. Deutschland, Ukraine). Leer bei Sendungen und Parteien.

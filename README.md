# Eishockeyanalyse für den MEK

Dieses Projekt führt eine grafische Analyse von Eishockeydaten für den MEK (Muenchner Eishockey Klub) durch. Die Analyse basiert auf den Daten, die in der Datei `2023-bis-2025-Teamstatistiken-R.xlsx` enthalten sind.

## Daten

Die Daten für diese Analyse stammen aus der Datei `2023-bis-2025-Teamstatistiken-R.xlsx`. Sie enthalten Informationen über verschiedene Aspekte der Leistung des MEK in verschiedenen Eishockeyspielen:

Hier ist eine detaillierte Erklärung der Daten anhand des Codebuchs:

### `date`
- **Definition**: Datum des Spiels
- **Ausprägungen**: Datum im Format yymmdd

### `season`
- **Definition**: Saison
- **Ausprägungen**: Vierziffrige Saisonkennzahl (z.B. 2223 für die Saison 2022/23)

### `opp`
- **Definition**: Gegner
- **Ausprägungen**: Name der gegnerischen Mannschaft (z.B. `paf1b` für Pfaffenhofen 1B)

### `opptabelle`
- **Definition**: Tabellenplatz Gegner
- **Ausprägungen**: Welchen Tabellenplatz hatte der Gegner am Ende der Saison inne? (Natürliche Zahl zwischen 1 und Anzahl der Teams in der Gruppe)

### `heim`
- **Definition**: Heimspiel ja/nein
- **Ausprägungen**: 1, wenn es sich um ein Heimspiel handelt, 0, wenn es sich um ein Auswärtsspiel handelt

### `gf`
- **Definition**: Tore MEK (Mannschaft des Erfassenden)
- **Ausprägungen**: Element der natürlichen Zahlen

### `ga`
- **Definition**: Tore Gegner
- **Ausprägungen**: Element der natürlichen Zahlen

### `gd`
- **Definition**: Tordifferenz
- **Ausprägungen**: Element der ganzen Zahlen

### `pts`
- **Definition**: Punkte
- **Ausprägungen**: Element der natürlichen Zahlenmenge 0, 1, 2, 3 (Sieg = 3, Sieg nach Penaltyschießen = 2, Niederlage nach Penaltyschießen = 1, Niederlage = 0)

### `sf`
- **Definition**: Schüsse MEK
- **Ausprägungen**: Element der natürlichen Zahlen

### `sa`
- **Definition**: Schüsse Gegner
- **Ausprägungen**: Element der natürlichen Zahlen

### `sd`
- **Definition**: Schussdifferenz
- **Ausprägungen**: Element der ganzen Zahlen

### `spct`
- **Definition**: Schussquote
- **Ausprägungen**: Tore MEK durch Schüsse MEK, Element der reellen Zahlen zwischen 0 und 1

### `pp`
- **Definition**: Powerplays MEK
- **Ausprägungen**: Wie oft hat der MEK in dem Spiel Powerplay gespielt? (Element der natürlichen Zahlen)

### `ppg`
- **Definition**: Powerplaytore MEK
- **Ausprägungen**: Element der natürlichen Zahlen

### `pppct`
- **Definition**: Powerplayquote MEK
- **Ausprägungen**: Powerplaytore MEK durch Powerplays MEK, Element der reellen Zahlen zwischen 0 und 1

### `pk`
- **Definition**: Unterzahlspiele MEK
- **Ausprägungen**: Wie oft hat der MEK in dem Spiel Unterzahl gespielt? (Element der natürlichen Zahlen)

### `pkga`
- **Definition**: Unterzahlgegentore MEK
- **Ausprägungen**: Element der natürlichen Zahlen

### `pkpct`
- **Definition**: Unterzahlquote MEK
- **Ausprägungen**: 1 - (Unterzahlgegentore MEK durch Unterzahlspiele MEK), Element der reellen Zahlen zwischen 0 und 1

### `pdo`
- **Definition**: PDO
- **Ausprägungen**: Schussquote plus Fangquote, Maß des "Glücks" in einem Spiel (PDO > 1 = MEK hatte Glück, PDO < 1 = MEK hatte Pech)

### `pktopp`
- **Definition**: Punkte Gegner
- **Ausprägungen**: Die Punktzahl (absolut), die die gegnerische Mannschaft in der jeweiligen Saison erzielt hat



## Verwendung

Um diese Analysen durchzuführen, führen Sie das entsprechende R-Skript `analyze.qmd` aus und stellen Sie sicher, dass die Datei `2023-bis-2025-Teamstatistiken-R.xlsx` im Arbeitsverzeichnis vorhanden ist.

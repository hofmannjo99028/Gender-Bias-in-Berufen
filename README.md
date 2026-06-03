# Gender Bias in Wikidata: Vergleich von Berufsrepräsentationen und Geschlechterverteilungen

## 1. Einleitung

Digitale Wissenssysteme wie Wikidata spielen eine zentrale Rolle bei der Sammlung, Strukturierung und Bereitstellung von Informationen. Sie werden zunehmend als Datenbasis für wissenschaftliche Analysen, maschinelles Lernen und gesellschaftliche Entscheidungsprozesse genutzt. Gleichzeitig wird verstärkt diskutiert, ob solche Systeme tatsächlich neutrale Abbildungen der Realität darstellen oder bestehende gesellschaftliche Ungleichheiten reproduzieren.

Ein zentraler Aspekt ist dabei der sogenannte **Gender Bias**, also die systematische Verzerrung der Darstellung von Geschlechtern in Daten. Diese Verzerrungen können sich sowohl in der Sichtbarkeit von Personen als auch in der Darstellung bestimmter Berufsgruppen äußern.

Ziel dieses Projekts ist es, diese möglichen Verzerrungen anhand von Berufsdaten in Wikidata zu untersuchen und mit realen Arbeitsmarktdaten zu vergleichen.


## 2. Forschungsfrage

Die zentrale Forschungsfrage lautet:

**Inwiefern führt die Stuktur von Wikidata zu einer Überrepräsentation von Status Berufen und Unterrepräsentation von alltäglichen Berufen und welche geschlechtsspezifischen Verzerrungen ergeben sich daraus?**

Daraus ergeben sich folgende Teilfragen:

- Welche Berufe sind in Wikidata besonders stark repräsentiert?
- Wie unterscheidet sich die Geschlechterverteilung innerhalb dieser Berufe?
- Weicht der Männeranteil in Wikidata systematisch von realen Daten ab?
- Welche strukturellen Verzerrungen lassen sich daraus erkennen?


## 3. Datenbasis

Die Analyse basiert auf zwei unterschiedlichen Datenquellen:

### 3.1 Wikidata-Daten

- Extraktion von Berufsdaten mittels SPARQL-Abfragen
- Variablen:
  - Beruf (`occupation`)
  - Geschlecht (`genderLabel`)
  - Anzahl von Personen (`count`)
- Fokus auf Personen mit vorhandenen Wikidata-Einträgen

Wichtiger Punkt:
Wikidata erfasst nicht alle Personen, sondern primär solche mit öffentlicher Relevanz.


### 3.2 Reale Daten

- Statistische Daten zur tatsächlichen Geschlechterverteilung in ausgewählten Berufen
- Dienen als Referenz zur Bewertung der Wikidata-Ergebnisse

Beispielhafte Berufe:
- Ärzte
- Pflegefachkräfte
- CEOs
- Büroangestellte
- Lehrer
- Erzieher
- Politiker
- Beamte


## 4. Methodik

Die Analyse wurde in mehreren Schritten durchgeführt:


### 4.1 Auswahl der Berufe

Es wurden gezielt unterschiedliche Berufsgruppen ausgewählt, um verschiedene gesellschaftliche Bereiche abzudecken:

#### Prestigeträchtige und statusorientierte Berufe
- CEO
- Politiker
- Ärzte
- Beamte

#### Alltägliche sowie Care- und Sozialberufe
- Pflegefachkräfte
- Büroangestellte
- Lehrer
- Erzieher

Ziel:
Unterschiede zwischen hoch angesehenen und alltäglichen Berufen sichtbar machen.


### 4.2 Datenaufbereitung

- Einlesen der Daten mit **Python (pandas)**
- Bereinigung der Daten (z. B. numerische Formatierung)
- Zusammenführung von Wikidata- und realen Datensätzen


### 4.3 Berechnung der Anteile

Für jeden Beruf wurden berechnet:

- Anteil männlicher Personen (in %)
- Anteil weiblicher Personen (in %)

für:
- Wikidata

schon gegeben:
- reale Daten


### 4.4 Vergleichsanalyse

Die Analyse basiert auf einem direkten Vergleich:

- Wikidata vs. Realität
- Fokus auf Unterschiede im Männeranteil

Darstellung durch:
- Tabellen
- Balkendiagramme


### 4.5 Untersuchung der erfassten Personen

Um besser zu verstehen, welche Personen in Wikidata erfasst werden, wurden für ausgewählte Berufsgruppen beispielhafte Personen einschließlich Geschlecht und Geburtsjahr betrachtet.

Dadurch sollte untersucht werden, ob Wikidata eher historisch bedeutsame und gesellschaftlich sichtbare Personen enthält als eine repräsentative Auswahl aller Berufstätigen.


## 5. Ergebnisse


### 5.1 Allgemeine Beobachtungen

Die Analyse zeigt deutliche Unterschiede zwischen Wikidata und realen Daten:

- Wikidata enthält überproportional viele Einträge zu bestimmten Berufen
- Besonders betroffen sind:
  - Führungspositionen
  - politische Berufe
  - akademische Berufe


### 5.2 Geschlechterverteilung in Wikidata

In vielen untersuchten Berufen zeigt sich:

- ein sehr hoher Männeranteil in Wikidata
- besonders stark bei:
  - CEOs
  - Politikern
  - Beamten


### 5.3 Vergleich mit realen Daten

Der Vergleich zeigt:

- In der Realität sind viele Berufe deutlich ausgeglichener
- In Wikidata hingegen:
  - stärkere Dominanz männlicher Personen
  - geringere Sichtbarkeit weiblicher Personen


### 5.4 Vergleich des Männeranteils (zentraler Befund)

Ein zentrales Ergebnis ist der Vergleich des Männeranteils:

In nahezu allen untersuchten Berufen gilt:

> Der Männeranteil in Wikidata liegt deutlich über dem tatsächlichen Männeranteil in der realen Arbeitswelt.

Besonders auffällig:

- **Ärzte**
  - Wikidata: sehr hoher Männeranteil (~90%)
  - Realität: fast ausgeglichen

- **Politiker / Beamte**
  - Wikidata: extreme männliche Dominanz
  - Realität: weniger extrem, aber weiterhin ungleich

- **Care-Berufe**
  - In beiden Datensätzen weiblich dominiert
  - Wikidata zeigt jedoch teilweise verzerrte Intensitäten


### 5.5 Sichtbarkeit von Berufen

Ein weiteres wichtiges Ergebnis:

- Berufe mit hoher gesellschaftlicher Sichtbarkeit (z. B. CEO, Politiker)
  → stark in Wikidata vertreten

- Alltägliche Berufe
  → deutlich unterrepräsentiert


### 5.6 Wer wird in Wikidata erfasst?

Die Betrachtung einzelner Personen zeigt, dass Wikidata überwiegend historisch bedeutsame und gesellschaftlich sichtbare Persönlichkeiten enthält.

Viele der erfassten Personen stammen aus dem 19. oder frühen 20. Jahrhundert und sind überwiegend männlich.

Dies gilt sowohl für Statusberufe wie Politiker und CEOs als auch für Berufe wie Lehrer oder Ärzte.

Die Ergebnisse unterstützen die Annahme, dass Wikidata nicht die Gesamtheit aller Berufstätigen abbildet, sondern vor allem Personen mit öffentlicher Sichtbarkeit und historischer Relevanz.


### 5.7 Statistische Überprüfung

Zur statistischen Überprüfung der Unterschiede zwischen Wikidata und den realen Arbeitsmarktdaten wurde ein gepaarter T-Test durchgeführt.

Ergebnis:

- t-Wert = -3,88
- p-Wert = 0,006

Da der p-Wert deutlich unter dem Signifikanzniveau von 0,05 liegt, sind die Unterschiede zwischen Wikidata und den realen Arbeitsmarktdaten statistisch signifikant.

Die beobachteten Abweichungen können daher nicht allein durch Zufall erklärt werden.


## 6. Interpretation

Die Ergebnisse lassen sich durch mehrere Faktoren erklären:

### 6.1 Sichtbarkeitsbias

Wikidata erfasst vor allem:
- bekannte Personen
- öffentlich relevante Figuren

→ führt zur Überrepräsentation bestimmter Berufsgruppen

Viele der erfassten Personen stammen zudem aus historischen Zeiträumen, in denen Frauen in Politik, Wissenschaft oder Führungspositionen deutlich seltener vertreten waren.

Dadurch wird die männliche Dominanz in zahlreichen Berufsgruppen zusätzlich verstärkt.


### 6.2 Geschlechterbias

Da:
- gesellschaftliche Machtpositionen historisch stärker von Männern besetzt sind

→ werden in Wikidata:
- Männer häufiger dargestellt
- Frauen seltener sichtbar


### 6.3 Reproduktion gesellschaftlicher Strukturen

Wikidata bildet nicht nur Realität ab, sondern:

→ reproduziert bestehende Ungleichheiten

Beispiel:
- männliche CEOs → stark überrepräsentiert
- weibliche Arbeit in Care-Berufen → weniger sichtbar


## 7. Limitationen

Die Analyse hat mehrere Einschränkungen:

- Wikidata ist keine vollständige Datenbasis
- Fokus auf „relevante“ Personen
- Unterschiede zwischen Datenquellen
- Aggregation vereinfacht komplexe Realitäten
- Geschlecht wird meist binär erfasst


## 8. Fazit

Die Analyse zeigt deutlich:

- Wikidata stellt keine neutrale Abbildung der Realität dar
- bestimmte Berufsgruppen sind überrepräsentiert
- männlich dominierte Berufe erscheinen häufiger
- weiblich dominierte Tätigkeiten sind teilweise unterrepräsentiert

Besonders relevant ist der Befund, dass:

> der Männeranteil in Wikidata systematisch höher ist als in realen Daten.

Dies deutet auf einen strukturellen Gender Bias hin, der sowohl aus gesellschaftlichen als auch aus datenbedingten Faktoren entsteht.


## 9. Technologien

- Python
- pandas
- numpy
- scipy
- matplotlib
- SPARQL
- Wikidata Query Service


## 10. Reproduzierbarkeit

Alle Analyseschritte sind im Jupyter Notebook (`analysis.ipynb`) dokumentiert.

Die verwendeten Datensätze befinden sich im Repository und ermöglichen eine vollständige Reproduktion der Ergebnisse.
## Wie groß ist die derzeit jährlich erzeugte Datenmenge und wie verändert sie sich?
Verdoppelt sich alle 2 Jahre (Exponentiell)

## Was versteht man unter dem 3-V-Modell? Welche weiteren Dimensionen kennen Sie?
### 3-V-Modell
- Volume (große Datenmengen)
- Velocity (mit hoher Geschwindigkeit)
- Variety (Verschiedenheit)
### 5-V-Modell
- Volume
- Velocity
- Variety
- Veracity (Nicht immer vertrauenswürdig)
- Value (Datenauswertung soll Gewinn bringen)
## Grenzen Sie BigData zu traditionellen (relationalen) Datenhaltungssystemen ab!
Datensätze, deren Größe über die Fähigkeit typischer Datenbanksoftwaretools zum Erfassen, Speichern, Verwalten und Analysieren hinausgeht.
## Was versteht man unter strukturierten, unstrukturierten und semi-strukturierten Daten?
- **Strukturierte Daten**: Daten mit vorgegebenen Format/Schema => Speichereffizient (aber unfelxibel!)
	- Tabelle in einer relationalen Datenbank
- **Unstrukturierte Daten**: Keine formalisierte Struktur => sehr flexibel und gut geeignet für heterogene Daten
	- Bilder
	- Videos
	- Texte
- **Semistrukturierte Daten**: Haben "versteckte" Struktur, die aber nicht notwendigerweise immer eingehalten werden muss
	- XML-Dokument (ohne Schema/DTD)

## Vergleichen Sie BigData und DataWarehouses?
Big Data Anwendungen arbeiten (im Gegensatz zu Data Warehouse Systemen) in der Regel ohne aufwändige Aufbereitung der Daten

## Was versteht man unter unsicheren Daten und welche Konsequenz hat dies für die Speicherung/Auswertung von BigData?
Unsicherheit = Veracity, Falsche Messwerte/Daten können zu Abweichungen führen
   
## Nennen Sie einige Techniken und Ideen hinter BigData und erklären Sie diese kurz!
### MapReduce
Datenverarbeitungsparadigma im Bereich BigData. Vorgehensweise:
1. **Map**: Eingabedaten werden auf eine Menge von Prozessen verteilt, welche die vom Nutzer bereitgestellte Map-Funktion ausführen => Schlüssel-Wert-Paare
2. **Shuffle** & Sort: Werte eines Schlüssels zu Listen zusammenfassen und Schlüssel sortieren => Schlüssel-Wertlisten-Paare
3. **Reduce**: Die Werte der Wertlisten werden aggregiert ausgegeben
### Shared-Nothing-Architektur / verteilte (Datei-)Systeme / horizontale Skalierung
IT-Architektur, die aus mehreren autonomen Knoten besteht, die ein verteiltes System bilden. Jeder Knoten kann selbständig arbeiten.
#### Horizontale Skalierung
Hinzufügen zusätzlicher Rechner/Knoten
### NoSQL-Datenbanken
NoSQL = Not-only SQL
- Daten werden nicht normalisiert, kein starres Datenbankschema (Schemafreiheit)
- Fokus auf Skalierbarkeit und hoher Performance
	- Konsistenz der Daten (oft) nicht garantiert (ACID-Prinzip)
	- Transaktionen nur eingeschränkt oder gar nicht unterstützt
- Partition tolerant: Systeme funktionieren auch über physische Netzerwerkpartitionen
- In 4 Klassen unterteilt:
	- Spaltenorientiert
	- Schlüssel-Wert-orientiert
	- Dokumentorientiert
	- Graphenbasiert

## Was versteht man unter Stream- bzw Batch-basierter Verarbeitung von Daten?
**Batch**: Daten werden angesammelt und gemeinsam verarbeitet
**Stream**: Kontinuierliche Erfassung, Verteilung und Analyse von Daten

## Nennen und beschreiben Sie kurz die 4 logischen Schichten einer BigData-Architektur!
1. **Datenquellen (Auswahl/Aufbereitung)**: Daten werden geprüft, korreliert, aufbereitet und transformiert um sie “speicherbereit” zu machen
2. **Datenspeicherung**: Hier werden die gesammelten Daten abgelegt/persistiert
3. **Datenverarbeitung/-analyse**: Hier werden die Daten verarbeitet und analysiert
4. **Ausgabe/Präsentation**: Hier werden die gewonnenen Informationen in geeigneter Form (Diagramme, Berichte, …) für die jeweilige Zielgruppe dargestellt

## Nennen Sie 5 Anwendungsfelder für BigData!
- Marketing und Vertrieb
- Produktion und Logistik
- Medizin
- Finanzbereich
- Personaldatenmanagement

## Nennen Sie wesentliche Herausforderungen im Bereich BigData!
- Heterogene Daten
- Vermeidung von Redundanzen
- Priorisierung der Daten
- Datensicherheit und -schutz
- Energieeffizienz

## Erklären Sie das CAP-Theorem!
### 3 Garantien
- **Availability**: Jeder Client kann immer lesen und schreiben
- **Partition Tolerance**: Das System funktioniert trotz physischer Netzwerkpartitionen gut
- **Consistency**: Alle Clients haben stets die gleiche Sicht auf die Daten
**Es können nur 2 Garantien erfüllt sein (nach Eric Brewer)**
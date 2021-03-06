# Introduction

# Grundlagen
* GTFS-Datenformat
* GTFS-Realtime ? (Falls ich das noch mache)

# Related Work
* State of the art
* Boston MBTA viz
* Brosi Travic
	* Differences my work to Travic

# Probleme (und Lösungen)
* Einsatz von GPS Daten
	* Fehlende Verfügbarkeit
	* Aktualisierungsintervall
	* Verlässlichkeit & Verfügbarkeit

* GTFS-Realtime (keine Verfügbarkeit bei Stuttgart-VVS) -> deshalb nur Interpolation der statischen Fahrpläne. Fokus auf Visualisierung und nicht auf Echtzeitsystem.

* Datenanzahl (Trips pro Tag)
	* Bei Projekt beginn war bereits zu erwarten, dass viele Daten verarbeitet werden müssen 
	* Timeline aus dem Projekt anzeigen? -> Daten erfassen

* Tech choices
	* Postgresql
   * Mapbox
   * Nodejs
   * Docker & AWS

# Implementierung

## Backend 
  * Abschnitt / Gliederung des Abschnitts aufgreifen und erklären

### Optimieren von GTFS
  * gtfstidy -> simplify shapes, integer ids, etc

### Database optimization for GTFS format (normalization)

### Finetune the Database for GIS queries
  * Why optimize
  * What can be optimized
  * A-B Test
  * Test results

### Building an API for GTFS
  * Database queries
  * Endpoints

## Frontend
  * Client
  * Geojson format
  * Object access over trip id
  * Algorithm? (most important ones)

### Optimizing Frontend Performance
  * Alter FPS per Zoom Level
  * Split vehicles into 2 groups: Inside bbox and Outside
  * Optimizing algorithms
  * Save values to prevent their tedious recalculations

### Introduction of UI Components
  * Timeline + Time jump
  * Trip counter
  * Map (Zoom / Pan)
  * Vehicles
  * Vehicle states (getting active / inactive)
  * Filter mechanices of Lines + Vehicle type
  * Layer style switcher
  * Route finder
  * Bezier Easing 


# Ergebnisse
  * What did I wanted to achiev and what was the outcome

# Ausblick

# Fazit
  * Was wurde erreicht und was nicht
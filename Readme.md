# Frontend Dev Docker Umgebung
Kleine Umgebung zum Üben und Austesten. Hier ist noch keine Distribution BuildChain enthalten. Aber zum Entwickeln reicht es ;)


## Vorraussetzungen
- Docker ist installiert
- Powershell (Windows)

## Features
- Docker Container
- Makefile zum Bauen, Starten, Stoppen des Containers
- Developmemt im laufenden Container
- npm script BuildChain mit SASS, Livereload und ESlint

## Getting Started
1. Repo forken und/oder klonen
2. Ins Verzeichnis wechseln und `make build-dev` ausführen.
3. `make run-dev` ausführen

## Benutzung (Dev)
Im Dev-mode wird das Programm per Mount in den Server geladen - es kann also auf dem Hostsystem daran gearbeitet werden. Ein Neubauen bei Codeänderungen ist nicht notwendig.
- `make build-dev` buildet das Dev Image
- `make run-dev` startet den Dev Container und ruft *enter-dev* auf
- `make stop-dev` stoppt den Dev Container
- `make rebuild-dev` stoppt den Dev Container (falls er existiert), baut das Dev Image neu und startet den Container erneut
- `make enter-dev` wählt einen in den Dev Container ein

## Buildchain starten
Im Dev Container `npm run watch` ausführen. Falls hier etwas nicht klappt, im Container noch mal `npm install` ausführen. Danach dann noch mal `npm run watch` ausführen.

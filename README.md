## RageMP RP Basis (DE)

Minimale Roleplay-Basis fuer RageMP (NodeJS 22, ESM). Enthält einfache Authentifizierung, deutsche Befehle und Datei-Persistenz.

### Voraussetzungen
- Node.js 22+
- RageMP Server (Windows)

### Installation
1) Kopiere die Ordner `server-files`, `packages` und `client_packages` in deinen RageMP-Server.
2) Optional: `npm i` (aktuell nicht notwendig).
3) Der echte Start erfolgt ueber `ragemp-server.exe`. Das Script `npm start` laedt nur die Entry-Datei.

### Features
- **Authentifizierung vor Spawn**: Verpflichtende Login/Register vor dem Spielen
- **Vollständige UI-Suite**: Moderne CEF-Interfaces für alle Funktionen
- **Real-Sync System**: Echtzeit-Synchronisation aller Spieler, Fahrzeuge, NPCs und Objekte
- **60 Jobs**: Umfassendes Job-System mit Erfahrungspunkten und Karriere-Levels
- **Erweiterte Systeme**: Gangs, Tattoo, News, Wetter, Drogen, Schatzsuche
- **UI-Customization**: Vollständige Anpassung aller UI-Farben und -Positionen
- **Deutsche Commands**: `/register`, `/login`, `/hilfe`, `/me`, `/ooc`, `/id`, `/report`
- **Admin-Commands**: `/veh`, `/dv`, `/tp`, `/setmoney`, `/edituser`
- **JSON-Datei-Persistenz** unter `storage/`

### Konfiguration
Datei: `config/default.json`

```json
{
  "motd": "Willkommen auf dem RP-Server!",
  "spawn": [-425.517, 1123.62, 325.854],
  "adminIds": [1]
}
```

### Real-Sync System
Das **Real-Sync System** bietet professionelle Echtzeit-Synchronisation:
- **20 FPS Spieler-Sync** für flüssige Bewegungen
- **10 FPS Fahrzeug-Sync** für präzise Positionierung
- **Intelligente Optimierung** mit Distanz-basierten Updates
- **Performance-Monitoring** und automatische Optimierung
- **Admin-Commands**: `/realsync`, `/realsyncperf`, `/realsyncoptimize`

### Start (RageMP)
- Starte `ragemp-server.exe`.
- Achte darauf, dass `server-files/index.js` existiert und `type: module` aktiv ist.
- Das Real-Sync System startet automatisch beim Server-Start.

### Hinweis
Der Code prueft das Vorhandensein von `mp`, um lokale Node-Laeufe nicht scheitern zu lassen. Fuer den echten Serverbetrieb muss `mp` von RageMP bereitgestellt werden.

### Dokumentation
- **Core-Übersicht**: [docs/core.md](docs/core.md)
- **Admin-Guide**: [docs/admin_guide.md](docs/admin_guide.md)
- **Real-Sync Guide**: [docs/realsync_guide.md](docs/realsync_guide.md)
- **Installation**: [docs/install_checklist.md](docs/install_checklist.md)
- **Deployment**: [docs/deploy_guide.md](docs/deploy_guide.md)
- **Changelog**: [docs/changelog.md](docs/changelog.md)



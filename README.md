# HorizontCity - RageMP GTA 5 Roleplay Server

Ein umfassender RageMP GTA 5 Roleplay-Server mit moderner C#-Architektur und MongoDB-Integration.

## 🚀 Features

### Core Systems
- **Player Management** - Vollständiges Spieler-System mit Profilen, Statistiken und Verwaltung
- **Faction System** - Erweiterte Fraktions-Verwaltung mit Rängen und Berechtigungen
- **Gang System** - Umfassendes Gang-System mit Territorien, Kriegen und Drogenhandel
- **Job System** - Vollständiges Job-System mit Bewerbungen, Gehältern und Arbeitszeiten
- **Vehicle System** - Komplettes Fahrzeug-System mit Modifikationen und Verwaltung
- **Economy System** - Erweiterte Wirtschaft mit Märkten, Investitionen, Krediten und Versicherungen
- **Bank System** - Vollständiges Bankensystem mit ATMs, Tresoren und Sicherheit
- **Animation System** - Umfassendes Animations-System mit Presets und Gruppen
- **Emotion System** - Detailliertes Emotions-System mit Triggern und Effekten
- **Robbery System** - Komplettes Raub-System mit verschiedenen Typen und Schwierigkeiten
- **Housing System** - Vollständiges Immobilien-System mit Einrichtung und Möbeln
- **Phone System** - iPhone 16 und iPad mit Apps, Nachrichten und Einstellungen
- **Health System** - Umfassendes Krankheits-System mit Krankenhäusern und Medikamenten
- **Brand System** - Tattoo- und Branding-System mit Shops und Designs
- **Lumberjack System** - Baumfällen-System mit verschiedenen Baumtypen und Werkzeugen
- **Construction System** - Bauarbeiter-System mit Baustellen und Phasen
- **Alarm System** - Umfassendes Alarmsystem mit Sensoren und Zonen
- **Key System** - Schlüssel & Sicherheitskarten-System mit Zugangskontrolle
- **Parking System** - Parkplatz-System mit verschiedenen Typen und Preisen
- **Garage System** - Garage-System mit Mietplätzen und Features
- **Casino System** - Casino-System mit Spielen, Tischen und Maschinen
- **Sync System** - Vollständiges Sync-System für Echtzeit-Daten
- **Weather System** - Echtzeit-Wetter-System mit Berlin-Synchronisation
- **Ped System** - Ped-System mit Einsatz-Tieren und Missionen
- **Blip System** - Blip Maker mit Templates und Routen
- **NPC System** - NPC Maker mit Dialogen und Verhalten
- **Disability System** - Behinderungen-System mit Hilfsmitteln und Haustieren
- **Blip Maker** - Blip Maker mit Templates und Projekten
- **NPC Maker** - NPC Maker mit Dialogen und Verhalten
- **Agriculture System** - Landwirtschafts-System mit Verarbeitung
- **Drug System** - Drogen-System mit Verarbeitung und Nebenwirkungen
- **Alcohol System** - Alkohol-System mit Verarbeitung und Nebenwirkungen
- **Oil Pump System** - Ölpumpen-System mit Verarbeitung und Lieferung an Tankstellen
- **GPS System** - GPS-System mit Navigationssystem für alle Fahrzeuge
- **City Hall System** - Vollständiges Rathaus-System
- **City Center System** - Vollständiges City Center-System
- **Radio System** - Radio-System mit Stationen und Playlists
- **Cinema System** - Kino-System mit Filmen und Tickets
- **Sport Studio System** - Fitness-Studio-System mit Mitgliedschaften und Trainern
- **Crime System** - Verbrechens-System mit Polizei und Gefängnis
- **Power Production System** - Stromproduktions-System mit Kraftwerken
- **Tax System** - Steuer-System mit Steuerbehörden und Steuererklärungen
- **Tram System** - Straßenbahn-System mit Routen und Fahrplänen
- **Driver License System** - Führerschein-System mit Prüfungen und Verstößen
- **Shopping Center System** - Einkaufszentrum-System mit Shops und Loyalitätskarten
- **Disaster System** - Katastrophen-System mit Notdiensten und Warnungen
- **News System** - Nachrichten-System mit Artikeln und Kanälen
- **Moderator System** - Moderatoren-System mit Berechtigungen und Aktionen
- **Club System** - Club-System mit Mitgliedschaften und Events
- **Unemployment System** - Arbeitslosen-Geld-System mit Leistungen und Schulungen
- **Pension System** - Renten-System mit Beiträgen und Auszahlungen
- **Trading System** - An- und Verkaufssystem mit Märkten und Bewertungen
- **Digital Records System** - Digitale Akten-Systeme mit Verschlüsselung
- **Civil Registry System** - Einwohnermeldeamt mit Geburts- und Heiratsurkunden
- **Family Life System** - Familienleben-System mit Beziehungen und Events
- **Inventory System** - Umfassendes Inventar-System mit Items und Trading
- **Event System** - Turniere, Events und Wettbewerbe
- **Admin System** - Vollständiges Admin-Panel mit Commands und Verwaltung

### Technische Features
- **MongoDB Integration** - Moderne NoSQL-Datenbank für optimale Performance
- **REST API** - Vollständige Web-API für externe Tools und Integrationen
- **Logging System** - Umfassendes Logging mit Serilog
- **Configuration Management** - Flexible Konfiguration über JSON-Dateien
- **Dependency Injection** - Moderne .NET 6 Architektur
- **Async/Await** - Optimierte Performance durch asynchrone Programmierung

## 📋 Voraussetzungen

- **Visual Studio 2022** oder höher
- **.NET 6.0 SDK** oder höher
- **MongoDB Server** 4.4 oder höher
- **RageMP Server** (für die eigentliche Server-Integration)

## 🛠️ Installation

### 1. Repository klonen
```bash
git clone https://github.com/yourusername/horizontcity.git
cd horizontcity
```

### 2. MongoDB installieren und starten
```bash
# Windows
# MongoDB Community Server von https://www.mongodb.com/try/download/community herunterladen
# und installieren

# Linux (Ubuntu/Debian)
sudo apt-get install mongodb
sudo systemctl start mongodb

# macOS
brew install mongodb-community
brew services start mongodb-community
```

### 3. Projekt kompilieren
```bash
# Mit Visual Studio 2022
# HorizontCity.sln öffnen und Build Solution ausführen

# Oder mit .NET CLI
dotnet build
```

### 4. Konfiguration anpassen
Die `appsettings.json` Datei nach Ihren Bedürfnissen anpassen:

```json
{
  "ConnectionStrings": {
    "MongoDB": "mongodb://localhost:27017"
  },
  "MongoDB": {
    "DatabaseName": "horizontcity"
  },
  "Server": {
    "Name": "HorizontCity",
    "MaxPlayers": 100,
    "Port": 22005
  }
}
```

### 5. Server starten
```bash
# API starten
cd src/HorizontCity.API
dotnet run

# Oder mit Visual Studio
# HorizontCity.API als Startup-Projekt setzen und F5 drücken
```

## 🏗️ Projektstruktur

```
HorizontCity/
├── src/
│   ├── HorizontCity.Core/          # Hauptlogik und Services
│   │   ├── Commands/               # Admin Commands
│   │   ├── Configuration/          # Konfigurationsklassen
│   │   ├── Events/                 # Event System
│   │   └── Services/               # Business Logic Services
│   ├── HorizontCity.Data/          # Datenmodell und Repository
│   │   ├── Database/               # MongoDB Kontext
│   │   ├── Models/                 # Datenmodelle
│   │   └── Repositories/           # Datenzugriff
│   └── HorizontCity.API/           # Web API
│       └── Controllers/            # REST API Controller
├── tests/
│   └── HorizontCity.Tests/         # Unit Tests
├── appsettings.json               # Konfiguration
└── README.md                      # Diese Datei
```

## 🔧 Konfiguration

### Server-Einstellungen
```json
{
  "Server": {
    "Name": "HorizontCity",
    "MaxPlayers": 100,
    "Port": 22005,
    "Language": "de",
    "StreamDistance": 400.0
  }
}
```

### Economy-Einstellungen
```json
{
  "Economy": {
    "StartingMoney": 5000,
    "InterestRate": 0.01,
    "SalaryInterval": 24
  }
}
```

### Faction-Einstellungen
```json
{
  "Factions": {
    "MaxMembers": 50,
    "AllowWars": false,
    "WarCooldown": 72
  }
}
```

## 📚 API Dokumentation

### Player Endpoints
- `GET /api/players` - Alle Online-Spieler abrufen
- `GET /api/players/{id}` - Spieler nach ID abrufen
- `POST /api/players` - Neuen Spieler erstellen
- `PUT /api/players/{id}` - Spieler aktualisieren
- `DELETE /api/players/{id}` - Spieler löschen

### Faction Endpoints
- `GET /api/factions` - Alle Fraktionen abrufen
- `GET /api/factions/{id}` - Fraktion nach ID abrufen
- `POST /api/factions` - Neue Fraktion erstellen
- `POST /api/factions/{id}/invite` - Spieler einladen
- `POST /api/factions/{id}/kick` - Spieler kicken

### Event Endpoints
- `GET /api/events` - Alle Events abrufen
- `POST /api/events` - Neues Event erstellen
- `POST /api/events/{id}/join` - Event beitreten
- `POST /api/events/{id}/leave` - Event verlassen

## 🎮 Admin Commands

### Spieler-Verwaltung
- `/kick <spieler> [grund]` - Spieler kicken
- `/ban <spieler> [grund] [dauer]` - Spieler bannen
- `/unban <spieler>` - Spieler entbannen
- `/warn <spieler> <grund>` - Spieler verwarnen
- `/setlevel <spieler> <level>` - Admin-Level setzen

### Geld-Verwaltung
- `/give <spieler> <betrag>` - Geld geben
- `/setmoney <spieler> <betrag>` - Geld setzen

### Fahrzeug-Verwaltung
- `/spawnvehicle <modell>` - Fahrzeug spawnen
- `/deletevehicle <kennzeichen>` - Fahrzeug löschen
- `/repair` - Fahrzeug reparieren

### Fraktions-Verwaltung
- `/createfaction <name> <kurzname> <typ>` - Fraktion erstellen
- `/deletefaction <name>` - Fraktion löschen
- `/setfactionleader <fraktion> <spieler>` - Fraktionsleiter setzen

## 🔒 Sicherheit

- **Rate Limiting** - Schutz vor Spam und Missbrauch
- **Input Validation** - Validierung aller Eingaben
- **SQL Injection Protection** - Schutz durch MongoDB
- **Authentication** - JWT-basierte Authentifizierung (geplant)
- **Authorization** - Rollenbasierte Berechtigungen

## 📊 Monitoring

- **Structured Logging** - Detaillierte Logs mit Serilog
- **Health Checks** - API Health Monitoring
- **Performance Metrics** - Automatische Performance-Überwachung
- **Error Tracking** - Umfassende Fehlerverfolgung

## 🧪 Testing

```bash
# Unit Tests ausführen
dotnet test

# Mit Coverage
dotnet test --collect:"XPlat Code Coverage"
```

## 🤝 Contributing

1. Fork das Repository
2. Erstelle einen Feature-Branch (`git checkout -b feature/AmazingFeature`)
3. Committe deine Änderungen (`git commit -m 'Add some AmazingFeature'`)
4. Push zum Branch (`git push origin feature/AmazingFeature`)
5. Öffne einen Pull Request

## 📝 Lizenz

Dieses Projekt steht unter der MIT-Lizenz. Siehe `LICENSE` für Details.

## 🆘 Support

Bei Problemen oder Fragen:

1. Überprüfe die [Issues](https://github.com/yourusername/horizontcity/issues)
2. Erstelle ein neues Issue mit detaillierter Beschreibung
3. Kontaktiere das Entwicklerteam

## 🗺️ Roadmap

### Version 1.1
- [ ] JWT Authentication
- [ ] Real-time WebSocket API
- [ ] Advanced Admin Panel
- [ ] Mobile App Integration

### Version 1.2
- [ ] Advanced Anti-Cheat
- [ ] Custom Map Support
- [ ] Advanced Roleplay Features
- [ ] Multi-Server Support

### Version 2.0
- [ ] Microservices Architecture
- [ ] Kubernetes Deployment
- [ ] Advanced Analytics
- [ ] AI-Powered Features

## 🙏 Danksagungen

- RageMP Team für das großartige Framework
- MongoDB Team für die exzellente Datenbank
- .NET Team für das moderne Framework
- Alle Contributors und Community-Mitglieder

---

**HorizontCity** - Wo deine Geschichte beginnt! 🏙️

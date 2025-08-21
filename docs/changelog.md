# Changelog

Alle wichtigen Änderungen am RageMP RP Server werden in dieser Datei dokumentiert.

## [2.0.0] - 2024-12-19

### 🚀 Neue Features

#### Authentifizierung vor Spawn
- **Verpflichtende Authentifizierung**: Spieler müssen sich einloggen/registrieren bevor sie spawnen können
- **Automatische Auth-UI**: Auth-Interface öffnet sich automatisch beim Server-Join
- **UI-basierte Auth**: Modernes Login/Register-Interface statt Chat-Commands
- **Sicherheitsschutz**: Alle Commands erfordern jetzt Authentifizierung

#### Vollständige UI-Suite (CEF)
- **Login/Register UI** (F1/F2): Modernes Auth-Interface mit Tabs und Validierung
- **Charakter-Management UI** (F3/F4): Charaktere erstellen, auswählen, löschen mit Live-Vorschau
- **Job-Management UI** (F5/F6): Jobs durchsuchen, beitreten, arbeiten mit Grid-Layout
- **Vendor/Shop UI** (F7/F8): Händler durchsuchen, Artikel kaufen mit Mengenauswahl
- **Erweiterte bestehende UIs**: Settings, Inventar, Bank, Fraktionspanel, Adminpanel

#### Tastenkombinationen-System
- **F1/F2**: Login/Register UI
- **F3/F4**: Charakter-Management
- **F5/F6**: Jobs
- **F7/F8**: Vendor/Shops
- **F9**: Fraktionspanel
- **F10**: Admin Panel
- **I**: Inventar
- **B**: Bank
- **W**: Arbeiten (kontextuell)
- **ESC**: Alle UIs schließen

### 🔧 Verbesserungen

#### Server-Architektur
- **Neue Event-Struktur**: Getrennte Auth-Events für UI-basierte Authentifizierung
- **Erweiterte Player-Events**: Kein automatischer Spawn mehr beim Join
- **Auth-Schutz**: Alle wichtigen Commands prüfen Authentifizierungsstatus
- **Verbesserte Admin-Prüfung**: Admin-Commands erfordern zusätzlich Auth-Status

#### Client-Integration
- **Einheitliche UI-Controller**: Alle UIs haben konsistente Client-Controller
- **Tastenkombinationen-Bindung**: Serverseitige Tastenbindungen für alle UIs
- **CEF-Browser-Management**: Korrekte HUD/Radar-Behandlung bei UI-Öffnung
- **Event-Weiterleitung**: Nahtlose Server-Client-Kommunikation

#### User Experience
- **Moderne UI-Designs**: Einheitliches Design mit Glasmorphismus-Effekten
- **Deutsche Lokalisierung**: Alle UI-Texte und Nachrichten auf Deutsch
- **Tastenkombinationen-Hilfe**: Shortcuts in allen UIs angezeigt
- **Fehlerbehandlung**: Umfassende Validierung und Fehlermeldungen

### 🛠️ Technische Änderungen

#### Neue Dateien
```
server-files/src/events/auth.js          - Auth-Events für UI-System
client_packages/auth_client.js           - Auth-UI Controller
client_packages/characters_client.js     - Charakter-UI Controller
client_packages/jobs_client.js           - Job-UI Controller
client_packages/vendors_client.js        - Vendor-UI Controller
client_packages/ui/auth/index.html       - Login/Register Interface
client_packages/ui/characters/index.html - Charakter-Management Interface
client_packages/ui/jobs/index.html       - Job-Management Interface
client_packages/ui/vendors/index.html    - Vendor/Shop Interface
```

#### Geänderte Dateien
- `server-files/src/events/player.js`: Auth-UI beim Join, kein Auto-Spawn
- `server-files/src/commands/auth.js`: Legacy-Commands mit Spawn-Integration
- `server-files/src/commands/characters.js`: Auth-Prüfung hinzugefügt
- `server-files/src/commands/admin.js`: Auth-Prüfung für Admin-Commands
- `client_packages/index.js`: Alle neuen UI-Controller geladen
- Alle bestehenden UIs: Tastenkombinationen und verbesserte Shortcuts

### 🔒 Sicherheit
- **Verpflichtende Authentifizierung**: Keine Commands ohne Login möglich
- **Auth-Status-Prüfung**: Server prüft `player.authenticated` bei allen wichtigen Aktionen
- **UI-Validierung**: Client-seitige und Server-seitige Eingabevalidierung
- **Session-Management**: Korrekte Authentifizierungsstatusverwalting

### 📚 Dokumentation
- **Erweiterte Core-Übersicht**: Alle neuen Features und Events dokumentiert
- **Tastenkombinationen-Guide**: Vollständige Übersicht aller Shortcuts
- **Auth-Flow-Diagramme**: Visuelle Darstellung des neuen Auth-Systems
- **Admin-Guide-Updates**: Auth-Anforderungen für Admin-Funktionen

## [1.0.0] - 2024-12-18

### 🎯 Initial Release

#### Grundfunktionen
- **RageMP Server-Setup**: Node.js 22 basierte Server-Architektur
- **Authentifizierung**: Chat-basierte Login/Register-Commands
- **Charaktersystem**: Erstellung, Auswahl, Verwaltung
- **Fraktionssystem**: Erstellen, Einladen, Ränge, Chat
- **Job-System**: 30 vordefinierte Jobs mit Verdienst-System
- **Vendor-System**: Shops mit Artikel-Verkauf
- **Admin-Tools**: Fahrzeug-Spawn, Teleport, Geld-Management

#### Basis-UIs
- **Settings-Panel**: Benutzereinstellungen mit Theme-Unterstützung
- **Inventar-System**: Artikel-Verwaltung
- **Bank-System**: Ein-/Auszahlungen, Überweisungen
- **Fraktionspanel**: Mitgliederverwaltung
- **Admin-Panel**: Admin-Tools-Interface

#### Server-Architektur
- **Modulare Struktur**: Getrennte Services für Charaktere, Fraktionen, Jobs, Vendors
- **JSON-Persistierung**: Datei-basierte Speicherung für Benutzer und Fraktionen
- **Event-System**: Server-Client-Kommunikation über RageMP Events
- **Konfiguration**: Zentrale Config-Datei für alle Einstellungen

---

## Versionshinweise

### Semantic Versioning
Dieses Projekt folgt [Semantic Versioning](https://semver.org/):
- **MAJOR**: Inkompatible API-Änderungen
- **MINOR**: Neue Features (rückwärtskompatibel)
- **PATCH**: Bugfixes (rückwärtskompatibel)

### Upgrade-Hinweise
- **1.x → 2.x**: Authentifizierung ist jetzt verpflichtend vor Spawn. Bestehende Spieler müssen sich nach dem Update neu einloggen.

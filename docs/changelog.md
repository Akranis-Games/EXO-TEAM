# Changelog

Alle wichtigen Änderungen am RageMP RP Server werden in dieser Datei dokumentiert.

## [2.8.0] - 2024-12-19

### 🚀 Neue Features

#### Business-System
- **Verschiedene Geschäftstypen**: Shop, Restaurant, Bar, Club, Tankstelle, Autohaus, Werkstatt, Krankenhaus, Polizeiwache, Bank
- **Geschäfts-Management**: Erstellen, Löschen, Mitarbeiter einstellen/entlassen, Finanzen verwalten
- **Mitarbeiter-System**: Rollen, Gehälter, Einstellungen und Entlassungen
- **Finanz-Management**: Einnahmen, Ausgaben, Gehaltszahlungen und Statistiken
- **Geschäfts-Einstellungen**: Öffnungszeiten, Auto-Restock, Inventar-Limits
- **Admin-Verwaltung**: Umfassende Admin-Commands für Business-Management

#### Schwarzmarkt-System
- **6 Illegale Job-Typen**: Drogendealer, Waffenschmuggler, Geldwäscher, Autodiebin, Hacker, Menschenhändler
- **Job-System**: Level-basierte Jobs mit Cooldowns, Risiko-Bewertungen und Belohnungen
- **Schmuggelware**: 9 verschiedene illegale Items mit unterschiedlichen Werten
- **Polizei-Integration**: Automatische Benachrichtigungen bei fehlgeschlagenen Jobs
- **Location-System**: Verschiedene Standorte für jeden Job-Typ
- **Skill-System**: Level-basierte Job-Freischaltung und Erfahrungspunkte

#### Waffenmarkt-System
- **40+ Waffen**: Handfeuerwaffen, Gewehre, Schrotflinten, Maschinengewehre, Spezialwaffen, illegale Waffen
- **Waffenschein-System**: 4 verschiedene Lizenztypen mit Prüfungen
- **Prüfungs-System**: Multiple-Choice-Fragen für jeden Lizenztyp
- **Waffen-Kategorien**: 7 Kategorien mit unterschiedlichen Eigenschaften
- **Lizenz-Management**: Erstellen, Widerrufen und Überprüfen von Lizenzen
- **Admin-Integration**: Umfassende Admin-Commands für Waffenmarkt-Verwaltung

#### Akten-System
- **5 Akten-Typen**: Polizei-, Gerichts-, Medizin-, Arbeits- und Verkehrsakten
- **Berechtigungssystem**: Job-basierte Zugriffsrechte für verschiedene Akten-Typen
- **Akten-Management**: Erstellen, Bearbeiten, Notizen hinzufügen, Status ändern
- **Suchfunktion**: Volltext-Suche mit Filtern nach Typ, Status und Ersteller
- **Verlaufsprotokoll**: Vollständige Historie aller Änderungen und Aktionen
- **Admin-Verwaltung**: Umfassende Admin-Commands für Akten-Management

#### Laptop-System
- **6 Laptop-Typen**: Standard, Professional, Gaming, Police, Medical, Business
- **Job-spezifische Apps**: Verschiedene Apps je nach Beruf (Polizei, Medizin, Business, etc.)
- **App-Management**: Installieren, Deinstallieren und Verwalten von Apps
- **Anpassbare Einstellungen**: Helligkeit, Lautstärke, Benachrichtigungen, Auto-Save
- **Wallpaper-System**: Eigene Hintergrundbilder für Laptops
- **Berechtigungssystem**: Job-basierte Zugriffsrechte für spezielle Apps

#### Blip Creator System
- **Verschiedene Blip-Typen**: 16 vordefinierte Typen (Polizei, Krankenhaus, Tankstelle, etc.)
- **50 Blip-Farben**: Umfassende Farbpalette von Weiß bis Gold
- **Blip-Management**: Erstellen, Bearbeiten, Löschen, Duplizieren und Umschalten
- **Kategorisierung**: Blips nach Typ, Kategorie und Ersteller gruppieren
- **Vorschau-System**: Blip-Vorschau vor dem Erstellen mit allen Eigenschaften
- **Import/Export**: Vollständige Blip-Daten importieren und exportieren
- **Admin-Verwaltung**: Umfassende Admin-Commands für Blip-Management

#### NPC Creator System
- **10 NPC-Typen**: Fußgänger, Verkäufer, Wächter, Arbeiter, Fahrer, Polizist, Sanitäter, Feuerwehrmann, Mechaniker, Koch
- **Verschiedene Verhalten**: 10 verschiedene Verhaltensweisen (laufen, stehen, sitzen, patrouillieren, arbeiten, verkaufen, fahren, untersuchen, heilen, löschen)
- **Animationen**: 13 verschiedene Animationen für verschiedene Aktivitäten
- **NPC-Management**: Erstellen, Bearbeiten, Löschen, Duplizieren und Umschalten
- **Routen-System**: Definierte Routen für NPCs mit verschiedenen Verhalten
- **Zeitplan-System**: NPCs können nach Zeitplänen aktiv/inaktiv sein
- **Bereichs-Suche**: NPCs in bestimmten Bereichen finden
- **Import/Export**: Vollständige NPC-Daten importieren und exportieren
- **Admin-Verwaltung**: Umfassende Admin-Commands für NPC-Management

#### Gefängnis-System
- **Insassen-Management**: Spieler einsperren, freilassen, Haftstrafen verwalten
- **Zellen-System**: Standard- und Einzelhaft-Zellen mit Insassen-Verwaltung
- **Haftstrafe-Verwaltung**: Verlängern, verkürzen und Einzelhaft verhängen
- **Gefängnis-Regeln**: 5 Standard-Regeln mit Strafen für Verstöße
- **Automatische Freilassung**: Spieler werden automatisch freigelassen wenn Haftstrafe abgelaufen ist
- **Polizei-Integration**: Nur Polizisten können das Gefängnis-System nutzen
- **Gefängnis-Statistiken**: Auslastung, Insassen-Zahlen und tägliche Statistiken
- **Vollständiges Logging**: Alle Gefängnis-Aktionen werden protokolliert
- **Gefängnis-Orte**: Definierte Bereiche für verschiedene Aktivitäten (Arbeit, Hof, Kantine)

#### Tür-System
- **Tür-Management**: Türen erstellen, bearbeiten, löschen und verwalten
- **Verschiedene Tür-Typen**: Haus, Geschäft, Garage, Lagerhalle, Büro, Apartment
- **Schloss-System**: 5 Schloss-Typen (Schlüssel, Code, Karte, Fernbedienung, Biometrisch) mit 5 Sicherheits-Levels
- **Zugriffskontrolle**: Besitzer und berechtigte Spieler können Türen verwalten
- **Tür-Status**: Verschließen, öffnen, beschädigen und reparieren
- **Schloss-Upgrades**: Schloss-Level von 1-5 upgraden für höhere Sicherheit
- **Tür-Gesundheit**: Gesundheitssystem mit Reparatur-Funktion
- **Bereichs-Suche**: Türen in bestimmten Bereichen finden
- **Import/Export**: Vollständige Tür-Daten importieren und exportieren
- **Admin-Verwaltung**: Umfassende Admin-Commands für Tür-Management

#### Alarm-System
- **Alarm-Management**: Alarme erstellen, bearbeiten, löschen und verwalten
- **8 Alarm-Typen**: Einbruchsalarm, Feueralarm, medizinischer Notfall, Polizei-Notfall, Bankalarm, Gasalarm, Atomalarm, Wetteralarm
- **5 Alarm-Level**: Niedrig, Mittel, Hoch, Kritisch, Notfall mit verschiedenen Farben und Lautstärken
- **Automatische Auslösung**: Alarme können automatisch bei bestimmten Aktionen ausgelöst werden
- **Benachrichtigungssystem**: Spieler im Bereich werden über aktive Alarme informiert
- **Spezielle Benachrichtigungen**: Polizei und Feuerwehr erhalten spezielle Benachrichtigungen je nach Alarm-Typ
- **Alarm-Status**: Aktivieren, stummschalten und zurücksetzen von Alarmen
- **Berechtigungssystem**: Nur Besitzer, Polizei, Feuerwehr oder Admins können Alarme verwalten

#### Feuerwehr-System
- **Brand-Management**: Brände erstellen, verwalten und löschen mit 8 verschiedenen Brand-Typen
- **Brand-Level-System**: 5 Brand-Level (Klein, Mittel, Groß, Massiv, Katastrophal) mit verschiedenen Ausbreitungsraten
- **Feuerwehrmann-Management**: Registrierung, Ränge, Erfahrungspunkte und Zertifizierungen
- **Notruf-System**: Notrufe erstellen, beantworten und abschließen mit Prioritätsstufen
- **Feuerwachen-System**: 5 Feuerwachen mit Kapazitätsmanagement und Personalzuweisung
- **Werkzeug-System**: 5 verschiedene Löschmittel (Wasser, Schaum, Trockenpulver, CO2, Feuerdecke) mit Effektivität je nach Brand-Typ
- **Brand-Ausbreitung**: Realistische Brand-Ausbreitungssimulation mit Schadensberechnung
- **Erfahrungssystem**: Erfahrungspunkte für Feuerwehrmänner mit Statistiken und Karrierefortschritt
- **Tablet-App**: Umfassende Tablet-App für Feuerwehrmänner mit Dashboard, Brand-Management und Notruf-System
- **Automatische Benachrichtigungen**: Benachrichtigungen an alle Feuerwehrmänner im Dienst bei Notrufen
- **Brand-Schaden**: Schadensberechnung basierend auf Brand-Level und Ausbreitung
- **Cooldown-System**: Abklingzeiten zwischen Brand-Auslösungen und Notrufen
- **Cooldown-System**: Alarme haben Abklingzeiten zwischen Auslösungen
- **Trigger-Limits**: Maximale Anzahl von Alarmauslösungen pro Alarm
- **Bereichs-Suche**: Alarme in bestimmten Bereichen finden
- **Import/Export**: Vollständige Alarm-Daten importieren und exportieren
- **Admin-Verwaltung**: Umfassende Admin-Commands für Alarm-Management

### 🔧 Verbesserungen

#### Server-Architektur
- **Neue Services**: BusinessSystem, BlackMarket, WeaponMarket für zentrale Verwaltung
- **Event-System**: Umfassende Event-Integration für alle neuen Systeme
- **Command-System**: 100+ neue Commands für alle Business-, Schwarzmarkt- und Waffenmarkt-Funktionen
- **MongoDB-Integration**: Alle neuen Systeme sind vollständig MongoDB-kompatibel

#### Client-Integration
- **Event-Handler**: Vollständige Client-Server-Kommunikation für alle neuen Systeme
- **Real-time Updates**: Automatische Aktualisierung bei allen System-Änderungen
- **Error-Handling**: Umfassende Fehlerbehandlung und Benutzer-Feedback

### 🛠️ Technische Änderungen

#### Neue Dateien
```
server-files/src/services/business_system.js   - Business-System Service
server-files/src/services/black_market.js      - Schwarzmarkt-System Service
server-files/src/services/weapon_market.js     - Waffenmarkt-System Service
server-files/src/services/case_system.js       - Akten-System Service
server-files/src/services/laptop_system.js     - Laptop-System Service
server-files/src/services/blip_creator.js      - Blip Creator System Service
server-files/src/events/business_system.js     - Business-System Events
server-files/src/events/black_market.js        - Schwarzmarkt-System Events
server-files/src/events/weapon_market.js       - Waffenmarkt-System Events
server-files/src/events/case_system.js         - Akten-System Events
server-files/src/events/laptop_system.js       - Laptop-System Events
server-files/src/events/blip_creator.js        - Blip Creator System Events
server-files/src/commands/business.js          - Business-System Commands
server-files/src/commands/black_market.js      - Schwarzmarkt-System Commands
server-files/src/commands/weapon_market.js     - Waffenmarkt-System Commands
server-files/src/commands/case.js              - Akten-System Commands
server-files/src/commands/laptop.js            - Laptop-System Commands
server-files/src/commands/blip_creator.js      - Blip Creator System Commands
server-files/src/services/npc_creator.js       - NPC Creator System Service
server-files/src/events/npc_creator.js         - NPC Creator System Events
server-files/src/commands/npc_creator.js       - NPC Creator System Commands
server-files/src/services/prison_system.js     - Gefängnis-System Service
server-files/src/events/prison_system.js       - Gefängnis-System Events
server-files/src/commands/prison.js            - Gefängnis-System Commands
server-files/src/services/door_system.js       - Tür-System Service
server-files/src/events/door_system.js         - Tür-System Events
server-files/src/commands/door.js              - Tür-System Commands
server-files/src/services/alarm_system.js      - Alarm-System Service
server-files/src/events/alarm_system.js        - Alarm-System Events
server-files/src/commands/alarm.js             - Alarm-System Commands
```

#### Geänderte Dateien
- `server-files/src/commands/index.js`: Alle neuen System-Commands importiert
- `server-files/src/events/index.js`: Alle neuen System-Events importiert
- `server-files/src/commands/help.js`: Alle neuen Commands in Hilfe integriert
- `rp-server/docs/core.md`: Alle neuen Systeme dokumentiert

---

## [2.7.0] - 2024-12-19

## [2.7.0] - 2024-12-19

### 🚀 Neue Features

#### Haus-System
- **Verschiedene Haus-Typen**: Wohnung, Haus, Villa mit unterschiedlichen Preisen und Möbel-Limits
- **Haus-Management**: Kaufen, Verkaufen, Mieten mit realistischen Preisen
- **Möbel-System**: Umfassender Katalog mit 5 Kategorien (Wohnzimmer, Schlafzimmer, Küche, Bad, Dekoration)
- **Einrichtungsfunktion**: Möbel über Tablet platzieren und entfernen
- **Haus-Interior**: Teleport-System mit verschiedenen Innenräumen
- **Sicherheitssystem**: Alarmanlage und Schloss-Funktionen
- **Admin-Verwaltung**: Umfassende Admin-Commands für Haus-Management

#### Haus-System UI
- **Moderne CEF-Interface**: Übersichtliche Darstellung aller Häuser und Möbel
- **Navigation**: Separate Bereiche für Übersicht, eigene Häuser, verfügbare Häuser, Möbel-Katalog
- **Verwaltung**: Haus-Info, Schloss, Alarmanlage und Möbel-Platzierung
- **Möbel-Katalog**: Kategorisierte Anzeige aller verfügbaren Möbel
- **Keybind-Integration**: H-Taste zum Öffnen, ESC zum Schließen

#### Erweiterte Commands
- **Haus-Verwaltung**: `/haus [aktion] [hausId]` für alle Haus-Aktionen
- **Haus-Operationen**: `/hauskaufen`, `/hausverkaufen`, `/hausmieten` für Transaktionen
- **Haus-Zugang**: `/hausbetreten`, `/hausverlassen` für Haus-Interior
- **Möbel-Management**: `/hausmoebel` für Möbel-UI, `/moebelkatalog` für Übersicht
- **Haus-Status**: `/hausschloss`, `/hausalarm` für Sicherheit
- **Admin-Commands**: `/hauserstellen`, `/hausloeschen`, `/hausreset` für Admins

### 🔧 Verbesserungen

#### Server-Architektur
- **Neuer Service**: HouseSystem für zentrale Haus- und Möbel-Verwaltung
- **Haus-Persistenz**: Alle Haus-Daten werden in JSON-Dateien gespeichert
- **Möbel-System**: Vollständige Möbel-Verwaltung mit Position und Rotation
- **Event-System**: Umfassende Event-Integration für Haus-Änderungen

#### Client-Integration
- **Haus-System UI**: Vollständige CEF-Interface für Haus-Management
- **Keybind-Integration**: H-Taste für Haus-System, ESC zum Schließen
- **Real-time Updates**: Automatische Aktualisierung bei Haus-Änderungen

### 🛠️ Technische Änderungen

#### Neue Dateien
```
server-files/src/services/house_system.js      - Haus-System Service
server-files/src/events/house_system.js        - Haus-System Events
server-files/src/commands/house.js             - Haus-System Commands
client_packages/house_system.html              - Haus-System UI Interface
client_packages/house_system_controller.js     - Haus-System Client Controller
```

#### Geänderte Dateien
- `rp-server/config/default.json`: Umfassende Haus-System-Konfiguration hinzugefügt
- `server-files/src/commands/index.js`: Neue Haus-System-Commands importiert
- `server-files/src/commands/help.js`: Haus-System-Commands in Hilfe integriert
- `rp-server/docs/core.md`: Haus-System dokumentiert

---

## [2.6.0] - 2024-12-19

### 🚀 Neue Features

#### Rang- und Rechte-System
- **Umfassendes Rang-System**: Jobs, Gangs und Admin mit detaillierten Hierarchien
- **Berechtigungsverwaltung**: Granulare Berechtigungen für alle Aktionen
- **Job-Ränge**: 7 Ränge für Polizisten, 5 für Sanitäter, Mechaniker und Tuning
- **Gang-Ränge**: 6 Ränge von Anwärter bis Boss mit steigenden Berechtigungen
- **Admin-Ränge**: 5 Ränge von Moderator bis Owner mit umfassenden Rechten
- **Rang-basierte Aktionen**: Verhaften, Behandeln, Reparieren, Kicken basierend auf Berechtigungen

#### Rang-System UI
- **Moderne CEF-Interface**: Übersichtliche Darstellung aller Ränge und Berechtigungen
- **Navigation**: Separate Bereiche für Job-, Gang- und Admin-Ränge
- **Verwaltung**: Spieler befördern, degradieren und Ränge setzen
- **Berechtigungsanzeige**: Alle verfügbaren Berechtigungen übersichtlich dargestellt
- **Keybind-Integration**: R-Taste zum Öffnen, ESC zum Schließen

#### Erweiterte Commands
- **Rang-Verwaltung**: `/setrank`, `/promote`, `/demote` für alle Rang-Typen
- **Rang-Informationen**: `/ranks`, `/myrank`, `/permissions` für Spieler
- **Rang-Aktionen**: `/arrest`, `/heal`, `/repair`, `/kick` basierend auf Berechtigungen
- **Hilfe-System**: `/rankhelp` für umfassende Rang-System-Dokumentation

### 🔧 Verbesserungen

#### Server-Architektur
- **Neuer Service**: RankSystem für zentrale Rang- und Berechtigungsverwaltung
- **Berechtigungsprüfung**: Automatische Überprüfung aller Aktionen
- **Rang-Persistenz**: Ränge werden in Spieler-Variablen gespeichert
- **Event-System**: Umfassende Event-Integration für Rang-Änderungen

#### Client-Integration
- **Rang-System UI**: Vollständige CEF-Interface für Rang-Verwaltung
- **Keybind-Integration**: R-Taste für Rang-System, ESC zum Schließen
- **Real-time Updates**: Automatische Aktualisierung bei Rang-Änderungen

### 🛠️ Technische Änderungen

#### Neue Dateien
```
server-files/src/services/rank_system.js      - Rang-System Service
server-files/src/commands/ranks.js            - Rang-System Commands
client_packages/rank_system.html              - Rang-System UI Interface
client_packages/rank_system_controller.js     - Rang-System Client Controller
```

#### Geänderte Dateien
- `rp-server/config/default.json`: Umfassendes Rang- und Berechtigungssystem hinzugefügt
- `server-files/src/commands/index.js`: Neue Rang-System-Commands importiert
- `server-files/src/commands/help.js`: Rang-System-Commands in Hilfe integriert
- `rp-server/docs/core.md`: Rang-System dokumentiert

### 🔒 Sicherheit
- **Berechtigungsprüfung**: Alle Aktionen werden auf entsprechende Berechtigungen geprüft
- **Rang-Validierung**: Server-seitige Validierung aller Rang-Änderungen
- **Admin-Schutz**: Nur berechtigte Admins können Ränge ändern
- **Aktions-Überwachung**: Alle Rang-basierten Aktionen werden protokolliert

### 📚 Dokumentation
- **Erweiterte Core-Übersicht**: Rang-System und alle Commands dokumentiert
- **Berechtigungsübersicht**: Alle verfügbaren Berechtigungen aufgelistet
- **Rang-Hierarchien**: Detaillierte Beschreibung aller Rang-Stufen
- **System-Integration**: Dokumentation der Integration in bestehende Systeme

---

## [2.1.0] - 2024-12-19

### 🚀 Neue Features

#### Raub-System (Robbery System)
- **Verschiedene Raub-Typen**: Bank, Juwelier, Tankstelle, Kiosk mit unterschiedlichen Anforderungen
- **Team-basierte Raubzüge**: Mehrere Spieler können sich an einem Raub beteiligen
- **Cooldown-System**: Realistische Wartezeiten zwischen Raubzügen (10 Min - 1 Stunde)
- **Polizei-Benachrichtigungen**: Automatische Benachrichtigungen an alle Polizisten
- **Belohnungssystem**: Zufällige Belohnungen basierend auf Raub-Typ
- **Admin-Verwaltung**: Umfassende Admin-Commands für Raub-Management

#### Diebstahl-System (Theft System)
- **Skill-basiertes System**: 10 Skill-Level mit Erfahrungspunkten
- **Verschiedene Ziele**: Fahrzeuge, Häuser, Läden, Geldautomaten, Lager
- **Skill-bonus**: Höhere Skills geben bessere Belohnungen
- **Standort-Überprüfung**: Spieler müssen in der Nähe der Ziele sein
- **Polizei-Anforderungen**: Verschiedene Polizei-Anzahlen je nach Diebstahl-Typ
- **Skill-Entwicklung**: Spieler können ihre Diebstahl-Fähigkeiten verbessern

#### Tuning-System
- **20 Tuning-Items**: Verschiedene Kategorien (Performance, Optik, Sicherheit)
- **Job-Integration**: Tuning-Job mit Level- und Tool-Anforderungen
- **Workshop-UI**: Moderne CEF-Interface für Tuning-Operationen
- **Fahrzeug-Integration**: Direkte Anwendung auf RageMP-Fahrzeuge
- **Erfahrungssystem**: Tuning-Erfahrung für Karriere-Entwicklung

#### Admin Settings UI
- **Zentrale Verwaltung**: Alle Server- und User-Einstellungen in einem Interface
- **Modernes Dark Design**: Benutzerfreundliche Oberfläche mit Sidebar-Navigation
- **Umfassende Funktionen**: Jobs, Items, Händler, Tankstellen, Fraktionen, Gangs verwalten
- **Backup & Export**: Konfiguration und User-Daten exportieren/importieren
- **System-Status**: Echtzeit-Überwachung aller Server-Systeme
- **Admin-Befehle**: Schnelle Konfigurationsänderungen über Chat-Commands

### 🔧 Verbesserungen

#### Server-Architektur
- **Neue Services**: RobberyService, TheftService, TuningService
- **Erweiterte Commands**: Umfassende Command-Sets für alle neuen Systeme
- **Skill-Persistenz**: Diebstahl-Skills werden in User-Daten gespeichert
- **Cooldown-Management**: Server-seitige Cooldown-Verwaltung für alle Systeme

#### Client-Integration
- **Tuning Workshop UI**: Vollständige CEF-Interface für Tuning-Operationen
- **Keybind-Integration**: F9 für Tuning Workshop, ESC zum Schließen
- **Workshop-Location**: Blip und Marker für Tuning-Workshop-Standort

### 🛠️ Technische Änderungen

#### Neue Dateien
```
server-files/src/services/robbery.js      - Raub-System Service
server-files/src/services/theft.js        - Diebstahl-System Service
server-files/src/services/tuning.js       - Tuning-System Service
server-files/src/commands/robbery.js      - Raub-System Commands
server-files/src/commands/theft.js        - Diebstahl-System Commands
server-files/src/commands/tuning.js       - Tuning-System Commands
client_packages/ui/tuning/index.html      - Tuning Workshop Interface
client_packages/tuning_controller.js      - Tuning Client Controller
server-files/src/controllers/admin_settings.js    - Admin Settings Controller
server-files/src/events/admin_settings.js         - Admin Settings Event Handler
client_packages/admin_settings.html               - Admin Settings UI Interface
client_packages/admin_settings.js                 - Admin Settings UI JavaScript
client_packages/admin_settings_controller.js      - Admin Settings Client Controller
```

#### Geänderte Dateien
- `server-files/src/commands/index.js`: Neue Command-Imports
- `server-files/src/commands/help.js`: Neue Commands in Hilfe integriert
- `rp-server/docs/core.md`: Neue Systeme dokumentiert
- `rp-server/config/default.json`: Tuning-Items und Shop hinzugefügt

### 🔒 Sicherheit
- **Polizei-Überwachung**: Alle Raubzüge und Diebstähle werden überwacht
- **Standort-Validierung**: Spieler müssen an den richtigen Orten sein
- **Cooldown-Schutz**: Verhindert Spam von Raubzügen und Diebstählen
- **Skill-Überprüfung**: Diebstähle erfordern entsprechende Skill-Level

### 📚 Dokumentation
- **Erweiterte Core-Übersicht**: Alle neuen Systeme und Commands dokumentiert
- **Admin-Commands**: Neue Admin-Funktionen für alle Systeme
- **Hilfe-System**: Umfassende Hilfe für alle neuen Commands
- **System-Integration**: Dokumentation der Integration in bestehende Systeme

---

## [2.0.0] - 2024-12-19

### 🚀 Neue Features

#### Real-Sync System
- **Echtzeit-Synchronisation**: Alle Spieler, Fahrzeuge, NPCs und Objekte werden in Echtzeit synchronisiert
- **Performance-Optimierung**: Konfigurierbare Sync-Raten (20 FPS für Spieler, 10 FPS für Fahrzeuge)
- **Intelligente Optimierung**: Distanz-basierte Sync, Prioritäts-System, Chunk-basierte Übertragung
- **Erweiterte Features**: Bewegungs-Interpolation, Client-seitige Vorhersage, Datenkomprimierung
- **Performance-Monitoring**: Echtzeit-Statistiken, automatische Optimierung, Debug-Informationen
- **Admin-Commands**: Umfassende System-Verwaltung über Chat-Commands

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
server-files/src/services/realsync.js    - Real-Sync System Service
server-files/src/commands/realsync.js    - Real-Sync Admin Commands
server-files/src/services/fire_department.js - Feuerwehr-System Service
server-files/src/events/fire_department.js   - Feuerwehr-System Events
server-files/src/commands/fire.js            - Feuerwehr-System Commands
client_packages/auth_client.js           - Auth-UI Controller
client_packages/characters_client.js     - Charakter-UI Controller
client_packages/jobs_client.js           - Job-UI Controller
client_packages/vendors_client.js        - Vendor-UI Controller
client_packages/realsync_client.js       - Real-Sync Client Controller
client_packages/ui/auth/index.html       - Login/Register Interface
client_packages/ui/characters/index.html - Charakter-Management Interface
client_packages/ui/jobs/index.html       - Job-Management Interface
client_packages/ui/vendors/index.html    - Vendor/Shop Interface
client_packages/ui/fire_department_tablet.html - Feuerwehr Tablet-App
docs/realsync_guide.md                   - Real-Sync System Dokumentation
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


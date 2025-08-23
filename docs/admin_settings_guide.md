# Admin Settings UI - Benutzeranleitung

Das Admin Settings UI ist ein umfassendes Interface zur zentralen Verwaltung aller Server- und User-Einstellungen des RP-Servers.

## 🚀 Features

### 📋 Übersicht
- **Zentrale Verwaltung**: Alle Einstellungen in einem modernen Interface
- **Dark Design**: Benutzerfreundliche Oberfläche mit Sidebar-Navigation
- **Real-time Updates**: Sofortige Aktualisierung aller Änderungen
- **Backup & Export**: Vollständige Datensicherung und Wiederherstellung

### 🎯 Verwaltungsbereiche

#### 1. Server Einstellungen
- **Grundkonfiguration**: Server-Name, MOTD, Spawn-Position
- **Admin-Verwaltung**: Admin-IDs, Fraktionsrollen
- **Sofortige Anwendung**: Änderungen werden sofort gespeichert

#### 2. User Verwaltung
- **User-Liste**: Alle registrierten Benutzer anzeigen
- **Daten bearbeiten**: Geld, Bank, Job, Fraktion ändern
- **User löschen**: Benutzer und alle Daten entfernen
- **Suche**: Schnelle Benutzer-Suche nach verschiedenen Kriterien

#### 3. Jobs System
- **Job hinzufügen**: Neue Jobs mit Gehalt und Beschreibung
- **Job verwalten**: Bestehende Jobs bearbeiten oder löschen
- **Job-Integration**: Automatische Integration in alle Systeme

#### 4. Items System
- **Kategorien**: Nahrung, Werkzeuge, Waffen, Kleidung, Drogen, Materialien, Fahrzeuge, Dokumente, Verschiedenes, Tuning
- **Item hinzufügen**: Neue Items mit Eigenschaften und Effekten
- **Item verwalten**: Bestehende Items bearbeiten oder löschen
- **Tab-Navigation**: Einfache Navigation zwischen Item-Kategorien

#### 5. Händler System
- **Händler hinzufügen**: Neue Händler mit Items und Preisen
- **Item-Verwaltung**: Items zu Händlern hinzufügen/entfernen
- **Preis-Management**: Preise für alle Items verwalten
- **JSON-Format**: Einfache Import/Export-Funktionalität

#### 6. Tankstellen System
- **Tankstelle hinzufügen**: Neue Tankstellen mit Position und Marke
- **Preismultiplikator**: Individuelle Preisgestaltung pro Tankstelle
- **Standort-Management**: X, Y, Z-Koordinaten verwalten

#### 7. Fraktionen System
- **Fraktion hinzufügen**: Neue Fraktionen mit Beschreibung und Farbe
- **Mitglieder-Verwaltung**: Automatische Zählung der Mitglieder
- **Farben**: Hex-Farben für individuelle Gestaltung
- **Sicherheit**: Mitglieder werden bei Löschung automatisch entfernt

#### 8. Gang System
- **Gang hinzufügen**: Neue Gangs mit Gründer und Farbe
- **Mitglieder-Management**: Mitglieder-Liste verwalten
- **Farben**: Individuelle Gang-Farben für Erkennung

#### 9. Erweiterte Systeme
- **Nachrichten-System**: Nachrichten an alle Spieler senden
- **Wetter-System**: Wetter für alle Spieler setzen
- **Drogen-System**: Drogen-Systeme aktivieren/deaktivieren
- **Schatzsuche-System**: Schwierigkeit und Status verwalten

#### 10. Backup & Export
- **Konfiguration**: Server-Konfiguration exportieren/importieren
- **User-Daten**: Alle Benutzer-Daten sichern/wiederherstellen
- **Backup-Erstellung**: Vollständige Backups mit Zeitstempel
- **Daten-Löschung**: Alle Daten löschen (mit Bestätigung)

## 🎮 Bedienung

### Tastenkombinationen
- **F10**: Admin Settings UI öffnen
- **ESC**: UI schließen
- **Enter**: Formulare absenden

### Navigation
1. **Sidebar**: Links für alle Verwaltungsbereiche
2. **Hauptbereich**: Formulare und Listen für den gewählten Bereich
3. **Status-Nachrichten**: Erfolgs- und Fehlermeldungen oben im Bereich
4. **Modals**: Popup-Fenster für detaillierte Bearbeitung

### Formulare
- **Validierung**: Alle Eingaben werden automatisch validiert
- **Sofortige Speicherung**: Änderungen werden sofort gespeichert
- **Fehlerbehandlung**: Benutzerfreundliche Fehlermeldungen
- **Bestätigungen**: Gefährliche Aktionen erfordern Bestätigung

## 🔧 Admin-Befehle

### UI-Verwaltung
- `/adminsettings` - Admin Settings UI öffnen
- `/adminclose` - Admin Settings UI schließen

### Schnelle Konfiguration
- `/setmotd [message]` - Message of the Day setzen
- `/setweather [type]` - Wetter setzen
- `/broadcast [message]` - Nachricht an alle senden

### Server-Informationen
- `/serverinfo` - Server-Informationen anzeigen
- `/exportconfig` - Konfiguration exportieren
- `/importconfig [filename]` - Konfiguration importieren

### Backup & Wiederherstellung
- `/createbackup` - Backup erstellen
- `/restorebackup [filename]` - Backup wiederherstellen
- `/clearalldata` - Alle Daten löschen (VORSICHT!)

## 📁 Dateistruktur

```
rp-server/
├── server-files/src/
│   ├── controllers/
│   │   └── admin_settings.js          # Server-seitiger Controller
│   └── events/
│       └── admin_settings.js          # Event-Handler
├── client_packages/
│   ├── admin_settings.html            # UI-Interface
│   ├── admin_settings.js              # UI-JavaScript
│   └── admin_settings_controller.js   # Client-Controller
└── config/
    └── default.json                   # Server-Konfiguration
```

## 🚨 Sicherheitshinweise

### Admin-Berechtigung
- Nur Spieler mit Admin-IDs können das UI öffnen
- Alle Aktionen werden protokolliert
- Gefährliche Aktionen erfordern Bestätigung

### Daten-Sicherheit
- Regelmäßige Backups erstellen
- Export-Dateien sicher aufbewahren
- Vorsicht bei `/clearalldata` - alle Daten gehen verloren!

### Server-Neustart
- Nach großen Konfigurationsänderungen Server neu starten
- Backups vor wichtigen Änderungen erstellen
- Test-Umgebung für kritische Änderungen verwenden

## 🔄 Workflow-Beispiele

### Neuen Job hinzufügen
1. Admin Settings UI öffnen (F10)
2. "Jobs System" auswählen
3. Job-Name, Gehalt und Beschreibung eingeben
4. "Job Hinzufügen" klicken
5. Job ist sofort verfügbar

### User-Daten bearbeiten
1. "User Verwaltung" auswählen
2. Benutzer in der Liste finden
3. "Bearbeiten" klicken
4. Daten ändern
5. "Änderungen Speichern" klicken

### Backup erstellen
1. "Backup & Export" auswählen
2. "Backup Erstellen" klicken
3. Datei wird im `storage`-Ordner gespeichert
4. Datei sicher aufbewahren

## 📞 Support

Bei Problemen oder Fragen:
1. Server-Logs überprüfen
2. Admin-Commands für schnelle Hilfe verwenden
3. Backup vor Änderungen erstellen
4. Test-Umgebung für kritische Änderungen

## 🎯 Best Practices

### Regelmäßige Wartung
- Wöchentliche Backups erstellen
- Server-Status regelmäßig überprüfen
- User-Daten regelmäßig bereinigen
- Konfiguration dokumentieren

### Änderungen verwalten
- Kleine Änderungen schrittweise testen
- Große Änderungen in Test-Umgebung
- Änderungen dokumentieren
- Rollback-Plan bereithalten

### Performance
- Große Datenmengen vermeiden
- Regelmäßige Bereinigung alter Daten
- Monitoring der Server-Performance
- Optimierung bei Problemen

---

**Das Admin Settings UI bietet eine umfassende und benutzerfreundliche Lösung zur Verwaltung aller Server-Aspekte. Nutzen Sie es verantwortungsvoll und erstellen Sie regelmäßig Backups Ihrer Konfiguration.**

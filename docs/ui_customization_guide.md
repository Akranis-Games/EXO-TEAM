# UI-Anpassungsystem - Benutzerhandbuch

## Übersicht

Das RP-Server UI-Anpassungssystem ermöglicht es Benutzern, die Benutzeroberfläche vollständig nach ihren Wünschen anzupassen. Sie können Farben, Positionen, Größe und Verhalten aller UI-Elemente individuell einstellen.

## UI-Einstellungen öffnen

### Chat-Commands
- `/uieinstellungen` oder `/ui` - Öffnet das vollständige UI-Einstellungsfenster
- `F1` - Tastenkombination zum Öffnen der UI-Einstellungen

## Einstellungsoptionen

### 1. Allgemeine Einstellungen
- **Design**: Wählen zwischen Dunkel, Hell und Benutzerdefiniert
- **UI-Skalierung**: Größe aller UI-Elemente (0.8x - 1.5x)
- **Animationen**: UI-Übergangseffekte aktivieren/deaktivieren

### 2. Farbanpassung
Vollständige Kontrolle über alle UI-Farben:
- **Hintergrund**: Haupthintergrundfarbe
- **Vordergrund**: Text- und Icon-Farbe
- **Primärfarbe**: Buttons und Akzente
- **Akzentfarbe**: Highlights und Links
- **Karten-Hintergrund**: Panel-Hintergründe
- **Rahmenfarbe**: Umrandungen und Linien
- **Hover-Effekt**: Mouseover-Farbe
- **Status-Farben**: Erfolg, Warnung, Fehler

### 3. UI-Positionierung
Anpassbare Positionen für:
- **HUD-Elemente**: Minimap, Chat, Tachometer
- **UI-Panels**: Inventar, Bank, Handy, Tablet
- **Benutzerdefinierte Offsets**: Feinabstimmung der Position

### 4. HUD-Einstellungen
- **Sichtbarkeit**: HUD, Minimap, Tachometer
- **Transparenz**: Durchsichtigkeit aller HUD-Elemente

### 5. Chat-Einstellungen
- **Darstellung**: Größe, Transparenz, Breite
- **Verhalten**: Auto-Hide, Zeitstempel

### 6. Audio-Einstellungen
- **Lautstärke**: Master, UI-Sounds, Musik
- **Features**: UI-Sounds, Voice Chat

## Schnell-Commands

### UI-Verwaltung
- `/uireset` - Alle UI-Einstellungen zurücksetzen
- `/uiscale [0.8-1.5]` - UI-Skalierung schnell ändern
- `/uianim` - UI-Animationen ein/ausschalten

### HUD-Steuerung
- `/hud` - HUD ein/ausschalten
- `/minimap` - Minimap ein/ausschalten

### Positionierung
```
/uipos [ui-typ] [position]
```
**UI-Typen**: inventory, bank, phone, tablet, chat, minimap, speedometer  
**Positionen**: center, left, right, top-left, top-right, bottom-left, bottom-right

**Beispiele**:
- `/uipos inventory left` - Inventar links positionieren
- `/uipos chat top-right` - Chat oben rechts positionieren

### Farbänderung
```
/uicolor [farbtyp] [hex-farbe]
```
**Farbtypen**: bg, fg, primary, accent, card, border, hover, ok, warn, error

**Beispiele**:
- `/uicolor primary #ff0000` - Primärfarbe auf Rot setzen
- `/uicolor bg #1a1a1a` - Hintergrund dunkler machen

## Tastenkombinationen

### UI-Fenster
- `F1` - Authentifizierung/UI-Einstellungen
- `F2` - Registrierung
- `F3` - Charakterverwaltung (Liste)
- `F4` - Charakterverwaltung (Erstellung)
- `F5` - Jobs (Liste)
- `F6` - Jobs (Beitritt)
- `F7` - Händler (Liste)
- `F8` - Händler (Kauf)
- `F9` - Fraktion
- `F10` - Admin Panel

### Schnellzugriff
- `I` - Inventar
- `B` - Bank
- `P` - Handy
- `T` - Tablet
- `C` - Bürgerbüro
- `F` - Tankstelle
- `J` - Jobcenter
- `W` - Arbeit
- `H` - Hilfe (in UIs)
- `ESC` - UI schließen

## Technische Details

### UI-Positionierungsklassen
Das System verwendet automatisch CSS-Klassen für die Positionierung:
- `.pos-center` - Zentriert
- `.pos-left` / `.pos-right` - Links/Rechts
- `.pos-top-left` / `.pos-top-right` - Oben Links/Rechts
- `.pos-bottom-left` / `.pos-bottom-right` - Unten Links/Rechts

### Datenspeicherung
- Alle Einstellungen werden in der Benutzerdatei gespeichert (`storage/user_*.json`)
- Einstellungen werden bei der Anmeldung automatisch geladen
- Änderungen werden sofort angewendet und gespeichert

### Kompatibilität
- Das System ist kompatibel mit allen bestehenden UI-Elementen
- Neue UI-Elemente erben automatisch die Benutzereinstellungen
- Das System funktioniert mit allen Browsern (CEF)

## Problembehebung

### UI-Elemente verschwunden
1. `/uireset` ausführen
2. Server neu verbinden
3. UI-Einstellungen überprüfen

### Farben falsch dargestellt
1. Theme auf "Benutzerdefiniert" setzen
2. Farben manuell anpassen
3. `/uicolor` Commands verwenden

### Positionen nicht korrekt
1. `/uipos` Commands verwenden
2. HUD-Offsets zurücksetzen
3. UI-Skalierung überprüfen

## Tipps

1. **Backup**: Notieren Sie sich Ihre bevorzugten Einstellungen
2. **Schrittweise Anpassung**: Ändern Sie jeweils nur eine Einstellung
3. **Testen**: Testen Sie alle UI-Elemente nach Änderungen
4. **Skalierung**: Bei hohen Auflösungen höhere UI-Skalierung verwenden
5. **Kontrast**: Achten Sie auf ausreichenden Farbkontrast für die Lesbarkeit

## Support

Bei Problemen mit der UI-Anpassung wenden Sie sich an einen Administrator oder nutzen Sie:
- `/hilfe` - Für alle verfügbaren Commands
- `/uireset` - Für Problembehebung
- `/adminlogs` - Für Administratoren zur Fehlerdiagnose

# Installations-Checkliste

## Voraussetzungen prüfen
- [ ] Node.js 22.x installiert (`node --version`)
- [ ] npm installiert (`npm --version`)
- [ ] RageMP Server heruntergeladen und entpackt
- [ ] RageMP Client installiert
- [ ] Port 22005 (UDP) und 22006 (TCP) freigegeben

## Server-Setup
- [ ] In `rp-server/` Verzeichnis wechseln
- [ ] `npm install` ausführen
- [ ] `config/default.json` anpassen:
  - [ ] Admin-IDs eintragen
  - [ ] Spawn-Koordinaten setzen
  - [ ] MOTD anpassen
- [ ] `storage/` Ordner erstellen (falls nicht vorhanden)

## RageMP Integration
- [ ] `server-files/` in RageMP Server-Ordner kopieren
- [ ] `client_packages/` in RageMP Client-Ordner kopieren
- [ ] `packages/` in RageMP Packages-Ordner kopieren
- [ ] RageMP `conf.json` anpassen:
  - [ ] `packages` Array prüfen
  - [ ] `client_packages` Pfad setzen

## Test & Verifikation
- [ ] Server starten (`node index.js`)
- [ ] Client verbinden
- [ ] **Auth-UI öffnet sich automatisch** beim Join
- [ ] **Login/Register über UI funktioniert** (F1/F2)
- [ ] **Spawn erfolgt nach erfolgreicher Auth**
- [ ] `/hilfe` Befehl testen (nach Auth)
- [ ] CEF-UIs öffnen sich (F3-F10, I, B)
- [ ] Tastenkombinationen funktionieren
- [ ] Keine Fehler in Server-Konsole

## Troubleshooting
- [ ] Ports prüfen (Windows Firewall)
- [ ] Node.js Version kompatibel
- [ ] Alle Dateien korrekt kopiert
- [ ] Berechtigungen für `storage/` Ordner
- [ ] **Auth-UI lädt nicht**: Client-Packages korrekt kopiert?
- [ ] **Tastenkombinationen funktionieren nicht**: Alle Client-Controller geladen?
- [ ] **Commands nach Auth nicht verfügbar**: Server-Events korrekt importiert?

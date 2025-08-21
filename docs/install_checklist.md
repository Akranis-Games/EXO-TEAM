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
- [ ] `/hilfe` Befehl testen
- [ ] `/register` funktioniert
- [ ] CEF-UI öffnet sich (`/settings`)
- [ ] Keine Fehler in Server-Konsole

## Troubleshooting
- [ ] Ports prüfen (Windows Firewall)
- [ ] Node.js Version kompatibel
- [ ] Alle Dateien korrekt kopiert
- [ ] Berechtigungen für `storage/` Ordner

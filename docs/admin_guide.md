# Admin-Guide

## Zugriffssteuerung
- **Authentifizierung erforderlich**: Admins müssen sich einloggen bevor Admin-Befehle funktionieren
- Admin-IDs: `config/default.json` -> `adminIds: [1,2,...]`
- Adminpanel öffnen: `/admin` oder **F10-Taste** (CEF-UI)
- Befehle sind zusätzlich direkt per Chat verfügbar (siehe unten)
- **Auth-Status**: `player.authenticated` muss `true` sein für alle Admin-Funktionen

## Befehle (Server)
- `/veh [modell]`: Spawnt ein Fahrzeug beim Admin und setzt ihn auf den Fahrersitz.
- `/dv`: Zerstoert das Fahrzeug, in dem der Spieler sitzt.
- `/tp [SpielerID]`: Teleportiert Admin zu Zielspieler.
- `/setmoney [SpielerID] [Betrag]`: Setzt Geld (Variable `money`) beim Ziel.

Voraussetzung: Spieler muss in `adminIds` enthalten sein oder `player.isAdmin === true` (RAGE Flag).

## Admin-UI (CEF)
**Öffnen**: `/admin` oder **F10-Taste**  
Datei: `client_packages/ui/admin/index.html`

### Funktionen
- **Fahrzeug spawnen**: Dropdown auswählen → "Fahrzeug spawnen" (intern `/veh <modell>`)
- **Geld setzen**: Spieler-ID + Betrag eingeben → "Geld setzen" (intern `/setmoney <id> <betrag>`)

### Tastenkombinationen
- **F10**: Admin-Panel öffnen/schließen
- **ESC**: Admin-Panel schließen

**Hinweis**: Die UI nutzt clientseitig `mp.trigger('cmd', '/veh ...')` etc. Alternativ können dedizierte Remote-Events ergänzt werden, falls du Chat-Kommandos vermeiden möchtest.

## Moderation & Reports
- Spielerreports kommen ueber `/report [text]` bei allen Admins im Chat an.
- Empfehlung: eigenes Report-Panel (Queue, Status, Notizen).

## Logging & Sicherheit (Empfehlungen)
- Logge Adminaktionen serverseitig (z. B. `veh`, `setmoney`, `tp`), inkl. Admin-ID, Ziel, Zeitstempel.
- Pruefe Eingaben strikt (z. B. Modellnamen, IDs, Betraege).
- Schuetze Konfiguration (keine Weitergabe von `config/default.json`).

## Backups
- Nutzer-/Charakterdaten: `storage/user_*.json`
- Fraktionen: `storage/factions.json`
- Backup-Strategie: taeglicher Snapshot, 7-14 Tage Vorhaltezeit; vor Updates manuelles Backup erstellen.

## Erweiterungen (optional)
- Tempban/Kick/Freeze-Funktionen
- Admin-Report-Panel (Zuweisung, Status, Notizen, Historie)
- Fahrzeug-/Objekt-Editor (Spawning, Speichern, Laden)
- Rechte/Rollen-System fuer Unter-Admins

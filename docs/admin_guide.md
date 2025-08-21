# Admin-Guide

## Zugriffssteuerung
- Admin-IDs: `config/default.json` -> `adminIds: [1,2,...]`
- Adminpanel oeffnen: `/admin` (CEF-UI)
- Befehle sind zusaetzlich direkt per Chat verfuegbar (siehe unten).

## Befehle (Server)
- `/veh [modell]`: Spawnt ein Fahrzeug beim Admin und setzt ihn auf den Fahrersitz.
- `/dv`: Zerstoert das Fahrzeug, in dem der Spieler sitzt.
- `/tp [SpielerID]`: Teleportiert Admin zu Zielspieler.
- `/setmoney [SpielerID] [Betrag]`: Setzt Geld (Variable `money`) beim Ziel.

Voraussetzung: Spieler muss in `adminIds` enthalten sein oder `player.isAdmin === true` (RAGE Flag).

## Admin-UI (CEF)
Datei: `client_packages/ui/admin/index.html`
- Fahrzeug spawnen: Dropdown auswaehlen -> "Fahrzeug spawnen" (intern `/veh <modell>`)
- Geld setzen: Spieler-ID + Betrag eingeben -> "Geld setzen" (intern `/setmoney <id> <betrag>`)

Hinweis: Die UI nutzt clientseitig `mp.trigger('cmd', '/veh ...')` etc. Alternativ koennen dedizierte Remote-Events ergaenzt werden, falls du Chat-Kommandos vermeiden moechtest.

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

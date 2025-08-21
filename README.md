## Core-Übersicht (RageMP RP – DE)

Siehe auch: [Admin-Guide](docs/admin_guide.md) · [Diagramme](docs/diagrams.md)

### Inhalt
- Funktionen/Features
- Befehle (Commands)
- Server-/Client-Events
- Services/Storage
- UI (CEF)
- Konfiguration & Persistenz

---

### Funktionen/Features
- Join/Quit/Spawn, MOTD
- Authentifizierung: Registrierung und Login
- Charaktere: Erstellung, Auswahl, Löschung, Inventar, Geld/Bank
- Fraktionen: Erstellen, Einladen, Akzeptieren, Kicken, Ränge, Fraktionschat
- Jobs: 30 vorausgefüllte Jobs, Beitritt, Arbeit (Verdienst)
- Händler/Shop: Artikel-Liste, Kaufen
- Adminfunktionen: Fahrzeug spawnen, Löschen, Teleport, Geld setzen
- UIs (CEF): Settings, Inventar, Bank, Fraktionspanel, Adminpanel

---

### Befehle (Commands)
- Allgemein
  - `/hilfe`
  - `/register [passwort]`
  - `/login [passwort]`
  - `/me [text]`
  - `/ooc [text]`
  - `/id`
  - `/report [text]`

- Charaktere
  - `/charcreate [Vorname] [Nachname] [m|w]`
  - `/charlist`
  - `/charselect [Index|ID]`
  - `/chardelete [Index|ID]`

- Fraktionen
  - `/fcreate [Name]`
  - `/finvite [SpielerID]`
  - `/faccept`
  - `/fkick [SpielerID]`
  - `/frank [SpielerID] [RangIndex]`
  - `/f [Nachricht]`

- Jobs
  - `/jobs`
  - `/jobjoin [Jobname]`
  - `/jobquit`
  - `/work`

- Händler/Shop
  - `/vendors`
  - `/vendor [Name]`
  - `/buy [Vendor] [Item] [Menge]`

- Admin
  - `/veh [modell]`
  - `/dv`
  - `/tp [SpielerID]`
  - `/setmoney [SpielerID] [Betrag]`

- UI-Shortcuts
  - `/settings`
  - `/inventory`
  - `/bank`
  - `/fpanel`
  - `/admin`

---

### Server-Events (RAGE → Server)
- Core
  - `packagesLoaded`
  - `playerJoin`
  - `playerQuit`
  - `playerReady`

- Settings
  - `settings:request`
  - `settings:save` (payload: JSON)

- Inventar
  - `inventory:request`
  - `inventory:add` (name, qty)
  - `inventory:remove` (name, qty)

- Bank
  - `bank:request`
  - `bank:deposit` (amount)
  - `bank:withdraw` (amount)
  - `bank:transfer` (targetId, amount)

- Fraktionspanel
  - `fpanel:request`

### Client-Events (Server → Client bzw. Client intern)
- Settings (Server → Client)
  - `settings:load` (JSON)
  - `settings:saved` ("ok"|"error")

- Inventar (Server → Client)
  - `inventory:load` (JSON)
  - `inventory:changed` (Status)

- Bank (Server → Client)
  - `bank:load` (Kontostand)
  - `bank:changed` (Status)

- UI Close (Client intern)
  - `ui:close`, `ui:close:inventory`, `ui:close:bank`, `ui:close:fpanel`, `ui:close:admin`

- Client → Server Trigger (aus CEF)
  - `settings:request:client` → `settings:request`
  - `settings:save:client` → `settings:save`
  - `inventory:request:client` → `inventory:request`
  - `bank:request:client` → `bank:request`
  - `bank:deposit:client` → `bank:deposit`
  - `bank:withdraw:client` → `bank:withdraw`
  - `bank:transfer:client` → `bank:transfer`

---

### Services/Storage (Server)
- `server-files/src/storage.js`
  - `ensureUser(player)`
  - `registerUser(player, password)`
  - `loginUser(player, password)`
  - `readUserData(player)`
  - `writeUserData(player, data)`

- `server-files/src/services/characters.js`
  - `createCharacter(player, firstName, lastName, gender)`
  - `listCharacters(player)`
  - `selectCharacter(player, idOrIndex)`
  - `deleteCharacter(player, idOrIndex)`
  - `getActiveCharacter(player)`
  - `addMoneyToActiveCharacter(player, amount)`
  - `tryTakeMoneyFromActiveCharacter(player, amount)`
  - `listInventory(player)`
  - `addItemToActiveCharacter(player, itemName, quantity)`
  - `removeItemFromActiveCharacter(player, itemName, quantity)`
  - `getBankBalance(player)`
  - `depositToBank(player, amount)`
  - `withdrawFromBank(player, amount)`
  - `transferToPlayer(player, targetId, amount)`

- `server-files/src/services/factions.js`
  - `createFaction(player, name)`
  - `inviteToFaction(player, targetId)`
  - `acceptFactionInvite(player)`
  - `kickFromFaction(player, targetId)`
  - `setFactionRank(player, targetId, roleIndex)`
  - `factionChat(player, message)`

- `server-files/src/services/jobs.js`
  - `listJobs()`
  - `joinJob(player, jobName)`
  - `quitJob(player)`
  - `doWork(player)`

- `server-files/src/services/vendors.js`
  - `listVendors()`
  - `listVendorItems(name)`
  - `buyFromVendor(player, vendorName, itemName, qty)`

---

### UI (CEF) – Client
- Settings
  - `client_packages/ui/settings/index.html`
  - `client_packages/settings_client.js`

- Inventar
  - `client_packages/ui/inventory/index.html`
  - `client_packages/inventory_client.js`

- Bank
  - `client_packages/ui/bank/index.html`
  - `client_packages/bank_client.js`

- Fraktionspanel
  - `client_packages/ui/fpanel/index.html`
  - `client_packages/fpanel_client.js`

- Adminpanel
  - `client_packages/ui/admin/index.html`
  - `client_packages/admin_client.js`

---

### Konfiguration
- Datei: `config/default.json`
  - `motd` (Server-MOTD)
  - `spawn` (Koordinaten)
  - `adminIds` (Server-ID-Liste)
  - `factionRoles` (Rollenbezeichnungen)
  - `jobs` (30 Jobs mit Name/Pay/Beschreibung)
  - `vendors` (Shops mit Artikeln/Preisen)

### Persistenz
- Nutzer/Charaktere: `storage/user_<name|socialClub>.json`
- Fraktionen: `storage/factions.json`



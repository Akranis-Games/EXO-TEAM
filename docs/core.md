## Core-Übersicht (RageMP RP – DE)

Siehe auch: [Admin-Guide](docs/admin_guide.md) · [Diagramme](docs/diagrams.md) · [Installation](docs/install_checklist.md) · [Deploy](docs/deploy_guide.md) · [Changelog](docs/changelog.md)

### Inhalt
- Funktionen/Features
- Befehle (Commands)
- Tastenkombinationen
- Server-/Client-Events
- Services/Storage
- UI (CEF)
- Konfiguration & Persistenz

---

### Funktionen/Features
- **Authentifizierung vor Spawn**: Spieler müssen sich einloggen/registrieren bevor sie spawnen
- **Moderne UI-basierte Authentifizierung**: Login/Register über CEF-Interface
- Join/Quit/Spawn, MOTD
- Charaktere: Erstellung, Auswahl, Löschung, Inventar, Geld/Bank
- Fraktionen: Erstellen, Einladen, Akzeptieren, Kicken, Ränge, Fraktionschat
- Jobs: 30 vorausgefüllte Jobs, Beitritt, Arbeit (Verdienst)
- Händler/Shop: Artikel-Liste, Kaufen mit Mengenauswahl
- Adminfunktionen: Fahrzeug spawnen, Löschen, Teleport, Geld setzen
- **Vollständige UI-Suite (CEF)**: Auth, Settings, Inventar, Bank, Charaktere, Jobs, Vendor, Fraktionspanel, Adminpanel
- **Tastenkombinationen**: Alle UIs über Funktionstasten erreichbar

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
  - `/auth` (Auth-UI öffnen)
  - `/characters` (Charakter-UI öffnen)
  - `/jobs` (Job-UI öffnen) 
  - `/vendors` (Vendor-UI öffnen)

---

### Tastenkombinationen
- **F1** - Login/Register UI
- **F2** - Login/Register UI (alternative)
- **F3** - Charakter-Management
- **F4** - Charakter erstellen
- **F5** - Jobs anzeigen
- **F6** - Aktueller Job
- **F7** - Händler
- **F8** - Artikel
- **F9** - Fraktionspanel
- **F10** - Admin Panel
- **I** - Inventar
- **B** - Bank
- **W** - Arbeiten (wenn Job-UI offen)
- **ESC** - Alle UIs schließen

---

### Server-Events (RAGE → Server)
- Core
  - `packagesLoaded`
  - `playerJoin`
  - `playerQuit`
  - `playerReady`

- **Authentifizierung**
  - `auth:login` (password)
  - `auth:register` (password)

- **Charaktere**
  - `characters:request`
  - `characters:create` (firstName, lastName, gender)
  - `characters:select` (id)
  - `characters:delete` (id)

- **Jobs**
  - `jobs:request`
  - `jobs:join` (jobName)
  - `jobs:quit`
  - `jobs:work`

- **Vendor/Shops**
  - `vendors:request`
  - `vendors:items` (vendorName)
  - `vendors:buy` (vendorName, itemName, quantity)

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
- **Authentifizierung (Server → Client)**
  - `auth:show` (Auth-UI öffnen)
  - `auth:response` (success, message)

- **Charaktere (Server → Client)**
  - `characters:show` (Charakter-UI öffnen)
  - `characters:response` (type, data)

- **Jobs (Server → Client)**
  - `jobs:show` (Job-UI öffnen)
  - `jobs:response` (type, data)

- **Vendor (Server → Client)**
  - `vendors:show` (Vendor-UI öffnen)
  - `vendors:response` (type, data)

- Settings (Server → Client)
  - `settings:load` (JSON)
  - `settings:saved` ("ok"|"error")

- Inventar (Server → Client)
  - `inventory:load` (JSON)
  - `inventory:changed` (Status)

- Bank (Server → Client)
  - `bank:load` (Kontostand)
  - `bank:changed` (Status)

- **UI Close (Client intern)**
  - `ui:close`, `ui:close:auth`, `ui:close:characters`, `ui:close:jobs`, `ui:close:vendors`
  - `ui:close:inventory`, `ui:close:bank`, `ui:close:fpanel`, `ui:close:admin`

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
- **Authentifizierung (F1/F2)**
  - `client_packages/ui/auth/index.html`
  - `client_packages/auth_client.js`

- **Charaktere (F3/F4)**
  - `client_packages/ui/characters/index.html`
  - `client_packages/characters_client.js`

- **Jobs (F5/F6)**
  - `client_packages/ui/jobs/index.html`
  - `client_packages/jobs_client.js`

- **Vendor/Shops (F7/F8)**
  - `client_packages/ui/vendors/index.html`
  - `client_packages/vendors_client.js`

- Settings
  - `client_packages/ui/settings/index.html`
  - `client_packages/settings_client.js`

- Inventar (I-Taste)
  - `client_packages/ui/inventory/index.html`
  - `client_packages/inventory_client.js`

- Bank (B-Taste)
  - `client_packages/ui/bank/index.html`
  - `client_packages/bank_client.js`

- Fraktionspanel (F9)
  - `client_packages/ui/fpanel/index.html`
  - `client_packages/fpanel_client.js`

- Adminpanel (F10)
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



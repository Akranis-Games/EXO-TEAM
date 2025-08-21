# Diagramme – Kern-Flows

## Authentifizierung vor Spawn (NEU)
```mermaid
sequenceDiagram
  participant Player
  participant Server
  participant CEF as Auth-UI
  Player->>Server: Verbindung
  Server->>Player: playerJoin (authenticated=false)
  Server->>Player: playerReady
  Server->>Player: auth:show (Auth-UI öffnen)
  Player->>CEF: F1/F2 drücken
  CEF->>Server: auth:login/register(password)
  Server->>Server: Validierung
  alt Login/Register erfolgreich
    Server->>Player: authenticated=true
    Server->>CEF: auth:response(true, message)
    Server->>Player: player.spawn() + ui:close:auth
  else Login/Register fehlgeschlagen
    Server->>CEF: auth:response(false, error)
    Note over Player: Muss erneut versuchen
  end
```

## Settings (CEF) – Client/Server Interaktion
```mermaid
sequenceDiagram
  participant Player
  participant CEF as CEF-UI
  participant Client as Client (RAGE JS)
  participant Server
  Player->>Client: /settings
  Client->>CEF: Browser oeffnen (index.html)
  Client->>Server: settings:request
  Server-->>Client: settings:load(JSON)
  Client-->>CEF: postMessage settings:load(JSON)
  CEF->>Client: settings:save:client(JSON)
  Client->>Server: settings:save(JSON)
  Server-->>Client: settings:saved('ok'|'error')
  Client-->>CEF: postMessage settings:saved
```

## Auth + Charaktere + Spawn
```mermaid
flowchart TD
  A[/Spieler/] -->|/register| R[registerUser]
  A -->|/login| L[loginUser]
  L --> D{Login OK?}
  D -- Nein --> E[Fehlermeldung]
  D -- Ja --> C[Charaktere laden]
  C -->|/charselect| SEL[Aktiven Charakter setzen]
  SEL --> S[Spawn auf Koordinate]
```

## Job – Beitritt und Arbeit
```mermaid
sequenceDiagram
  participant P as Spieler
  participant S as Server
  P->>S: /jobs
  S-->>P: Liste (config.jobs)
  P->>S: /jobjoin [Name]
  S-->>P: OK/Fehler
  P->>S: /work
  S->>S: doWork -> addMoneyToActiveCharacter
  S-->>P: Verdienst bestaetigt
```

## Haendler – Kaufprozess
```mermaid
flowchart LR
  A[/Spieler/] -->|/vendor [Name]| V[Vendor Items]
  A -->|/buy [Vendor] [Item] [Menge]| B{Genug Geld?}
  B -- Nein --> N[Abbruch/Info]
  B -- Ja --> T[tryTakeMoney]
  T --> C[Kauf bestaetigen]
```

## Banking – Ein-/Auszahlen/Ueberweisen
```mermaid
sequenceDiagram
  participant P as Spieler
  participant S as Server
  P->>S: /bank (UI oeffnen)
  P->>S: bank:request
  S-->>P: bank:load(Kontostand)
  P->>S: bank:deposit(amount)
  S->>S: tryTakeMoney -> +bankBalance
  S-->>P: bank:changed('ok') + bank:load
  P->>S: bank:withdraw(amount)
  S->>S: -bankBalance -> addMoney
  S-->>P: bank:changed('ok') + bank:load
  P->>S: bank:transfer(id, amount)
  S->>S: -Sender, +Empfaenger
  S-->>P: bank:changed('ok') + bank:load
```

## Fraktion – Einladen/Beitreten/Chat
```mermaid
flowchart TD
  FC[Fraktion erstellen] --> INV[Einladung senden]
  INV --> ACC[Einladung annehmen]
  ACC --> MEM[Mitgliedsliste aktualisieren]
  MEM --> CHAT[Fraktionschat /f]
```

## UI-System Übersicht (NEU)
```mermaid
flowchart TD
  A[Spieler Joint Server] --> B[Auth-UI öffnet automatisch]
  B --> C{Authentifiziert?}
  C -- Nein --> D[F1/F2: Login/Register]
  D --> E[Erfolg?]
  E -- Nein --> D
  E -- Ja --> F[Spawn + Alle UIs verfügbar]
  C -- Ja --> F
  
  F --> G[F3: Charaktere]
  F --> H[F5: Jobs] 
  F --> I[F7: Vendor]
  F --> J[F9: Fraktion]
  F --> K[F10: Admin]
  F --> L[I: Inventar]
  F --> M[B: Bank]
  
  G --> N[Charakter erstellen/auswählen]
  H --> O[Job beitreten/arbeiten]
  I --> P[Artikel kaufen]
  J --> Q[Mitglieder verwalten]
  K --> R[Admin-Tools]
  L --> S[Items verwalten]
  M --> T[Geld verwalten]
```

## Tastenkombinationen-Map
```mermaid
mindmap
  root((UIs))
    Auth
      F1
      F2
    Charaktere
      F3
      F4
    Jobs
      F5
      F6
    Vendor
      F7
      F8
    System
      F9[Fraktion]
      F10[Admin]
    Schnell
      I[Inventar]
      B[Bank]
      W[Arbeiten]
      ESC[Schließen]
```

**Hinweis**: Diese Diagramme spiegeln die aktuelle Implementierung wider (Events, Services, Konfiguration in `config/default.json`).

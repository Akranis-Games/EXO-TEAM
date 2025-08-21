# Diagramme – Kern-Flows

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

Hinweis: Diese Diagramme spiegeln die aktuelle Implementierung wider (Events, Services, Konfiguration in `config/default.json`).

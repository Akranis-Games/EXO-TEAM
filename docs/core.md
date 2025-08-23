## Core-Übersicht (RageMP RP – DE)

Siehe auch: [Admin-Guide](docs/admin_guide.md) · [Diagramme](docs/diagrams.md) · [Installation](docs/install_checklist.md) · [Deploy](docs/deploy_guide.md) · [Changelog](docs/changelog.md) · [Real-Sync Guide](docs/realsync_guide.md)

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
- **Real-Sync System**: Echtzeit-Synchronisation aller Spieler, Fahrzeuge, NPCs und Objekte mit Performance-Optimierung
- **Tuning System**: Vollständiges Fahrzeug-Tuning-System mit Items, Job-Integration und Workshop-UI
- **Raub-System**: Verschiedene Raub-Typen (Bank, Juwelier, Tankstelle, Kiosk) mit Cooldowns und Polizei-Benachrichtigungen
- **Diebstahl-System**: Skill-basiertes Diebstahl-System mit verschiedenen Zielen und Erfahrungspunkten
- **Rang- und Rechte-System**: Umfassendes Rang-System für Jobs, Gangs und Admin mit Berechtigungen und Hierarchien
- **Business-System**: Vollständiges Geschäftsmanagement-System mit Mitarbeiterverwaltung, Finanzen und verschiedenen Geschäftstypen
- **Schwarzmarkt-System**: Illegale Jobs und Schmuggelware-System mit 6 verschiedenen Job-Typen und Polizei-Benachrichtigungen
- **Waffenmarkt-System**: Umfassendes Waffen-System mit 40+ Waffen, Waffenschein-Prüfungen und Lizenzverwaltung
- **Akten-System**: Vollständiges Verwaltungssystem für Polizei-, Gerichts-, Medizin-, Arbeits- und Verkehrsakten
- **Laptop-System**: Job-spezifische Laptops mit verschiedenen Apps und Funktionen für verschiedene Berufe
- **Blip Creator System**: Umfassendes System zum Erstellen und Verwalten von Kartenmarkierungen mit verschiedenen Typen, Farben und Eigenschaften

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
  - `/hauserstellen [typ] [preis]` - Neues Haus erstellen
  - `/hausloeschen [hausId]` - Haus löschen
  - `/hausreset [hausId]` - Haus zurücksetzen

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

- **Real-Sync System**
  - `/realsync` - System-Status anzeigen
  - `/realsyncconfig` - Konfiguration anzeigen
  - `/realsyncset [option] [wert]` - Einstellungen ändern
  - `/realsyncperf` - Performance-Statistiken
  - `/realsyncoptimize` - Automatische Optimierung
  - `/realsynchelp` - Hilfe anzeigen

- **Tuning System**
  - `/tuning [Item] [FahrzeugID]` - Tuning anwenden
  - `/tuningself [Item]` - Tuning auf eigenes Fahrzeug
  - `/tuningother [Item] [SpielerID]` - Tuning auf fremdes Fahrzeug
  - `/tuningstatus [FahrzeugID]` - Tuning-Status anzeigen
  - `/tuninginfo` - Tuning-Job-Informationen
  - `/tuningitems` - Verfügbare Tuning-Items

- **Rang- und Rechte-System**
  - `/ranks [job/gang/admin] [JobName]` - Alle Ränge anzeigen
  - `/myrank` - Deine aktuellen Ränge anzeigen
  - `/permissions` - Deine Berechtigungen anzeigen
  - `/setrank [job/gang/admin] [SpielerID] [Rang]` - Rang setzen (Admin)
  - `/promote [SpielerID] [job/gang]` - Spieler befördern
  - `/demote [SpielerID] [job/gang]` - Spieler degradieren
  - `/arrest [SpielerID]` - Spieler verhaften (Polizei)
  - `/heal [SpielerID]` - Spieler behandeln (Medizin)
  - `/repair [SpielerID]` - Fahrzeug reparieren (Mechaniker)
  - `/kick [SpielerID] [Grund]` - Spieler kicken (Admin)
  - `/rankhelp` - Rang-System Hilfe
  - `/tuningbuy [Item] [Menge]` - Tuning-Item kaufen
  - `/tuninghelp` - Tuning-Hilfe anzeigen

- **Raub-System**
  - `/raub [Typ]` - Starte einen Raub
  - `/raubbeitreten [Typ]` - Tritt einem Raub bei
  - `/rauberfolgreich [Typ]` - Beende Raub erfolgreich
  - `/raubfehlgeschlagen [Typ]` - Raub fehlschlagen lassen
  - `/aktiveraub` - Zeige aktive Raubzüge
  - `/raubinfo` - Zeige alle Raub-Typen
  - `/raubcooldown [Typ]` - Zeige Cooldown-Status
  - `/raubhilfe` - Raub-System Hilfe

- **Diebstahl-System**
  - `/diebstahl [Typ]` - Starte einen Diebstahl
  - `/diebstahlerfolgreich [Typ]` - Beende Diebstahl erfolgreich
  - `/diebstahlfehlgeschlagen [Typ]` - Diebstahl fehlschlagen lassen
  - `/aktiverdiebstahl` - Zeige aktive Diebstähle
  - `/diebstahlinfo` - Zeige alle Diebstahl-Typen
  - `/diebstahlcooldown [Typ]` - Zeige Cooldown-Status
  - `/diebstahlskill` - Zeige Skill-Status
  - `/diebstahhhilfe` - Diebstahl-System Hilfe

- **Haus-System**
  - `/haus [aktion] [hausId]` - Hauptbefehl für alle Haus-Aktionen
  - `/hauskaufen [hausId]` - Haus kaufen
  - `/hausverkaufen [hausId]` - Haus verkaufen

- **Feuerwehr-System**
  - Brand-Management mit 8 Brand-Typen (Gebäude, Fahrzeug, Wald, Industrie, Gas, Elektrisch, Chemisch, Waldbrand)
  - 5 Brand-Level (Klein, Mittel, Groß, Massiv, Katastrophal) mit verschiedenen Ausbreitungsraten
  - Feuerwehrmann-Management mit Rängen, Erfahrungspunkten und Zertifizierungen
  - Notruf-System mit Prioritätsstufen und automatischen Benachrichtigungen
  - 5 Feuerwachen mit Kapazitätsmanagement und Personalzuweisung
  - Werkzeug-System mit 5 verschiedenen Löschmitteln (Wasser, Schaum, Trockenpulver, CO2, Feuerdecke)
  - Brand-Ausbreitungssimulation mit Schadensberechnung
  - Erfahrungssystem für Feuerwehrmänner mit Statistiken und Karrierefortschritt
  - Tablet-App für Feuerwehrmänner mit Dashboard, Brand-Management und Notruf-System
  - `/hausmieten [hausId]` - Haus mieten
  - `/hausbetreten [hausId]` - Haus betreten
  - `/hausverlassen` - Haus verlassen
  - `/hausinfo [hausId]` - Haus-Informationen anzeigen
  - `/hausmoebel [hausId]` - Möbel-UI öffnen
  - `/hausschloss [hausId]` - Haus abschließen/aufschließen
  - `/hausalarm [hausId]` - Alarmanlage aktivieren/deaktivieren
  - `/meinehaeuser` - Deine Häuser anzeigen
  - `/hausliste` - Alle verfügbaren Häuser anzeigen
  - `/moebelkatalog` - Möbel-Katalog anzeigen
  - `/haushelp` - Haus-System Hilfe

- **Business-System**
  - `/business [aktion] [parameter]` - Hauptbefehl für alle Business-Aktionen
  - `/businesscreate <name> <type> [description]` - Geschäft erstellen
  - `/businessinfo <businessId>` - Geschäftsinformationen anzeigen
  - `/businessmy` - Meine Geschäfte anzeigen
  - `/businesshire <businessId> <username> <role> [salary]` - Mitarbeiter einstellen
  - `/businessfire <businessId> <username>` - Mitarbeiter entlassen
  - `/businessincome <businessId> <amount> <source>` - Einnahmen hinzufügen
  - `/businessexpense <businessId> <amount> <source>` - Ausgaben hinzufügen
  - `/businesssalary <businessId>` - Gehälter auszahlen
  - `/businessdelete <businessId>` - Geschäft löschen
  - `/businesstypes` - Verfügbare Geschäftstypen anzeigen
  - `/businessstats <businessId>` - Geschäftsstatistiken anzeigen

- **Schwarzmarkt-System**
  - `/blackmarket [aktion] [parameter]` - Hauptbefehl für alle Schwarzmarkt-Aktionen
  - `/blackmarketjobs` - Verfügbare illegale Jobs anzeigen
  - `/blackmarketstart <jobType> <locationIndex>` - Illegalen Job starten
  - `/blackmarketactive` - Aktive Jobs anzeigen
  - `/blackmarketcomplete <jobId> <success>` - Job abschließen
  - `/blackmarketcontraband` - Schmuggelware anzeigen
  - `/blackmarketsell <itemId> <quantity>` - Schmuggelware verkaufen
  - `/drugdealer [locationIndex]` - Drogendealer-Job starten
  - `/weaponsmuggler [locationIndex]` - Waffenschmuggler-Job starten
  - `/moneylaunderer [locationIndex]` - Geldwäscher-Job starten
  - `/carthief [locationIndex]` - Autodiebin-Job starten
  - `/hacker [locationIndex]` - Hacker-Job starten
  - `/humantrafficker [locationIndex]` - Menschenhändler-Job starten
  - `/selldrugs [quantity]` - Drogen verkaufen
  - `/sellweapons [quantity]` - Waffen verkaufen
  - `/selldirtymoney [quantity]` - Schmutziges Geld verkaufen
  - `/policealert <jobType>` - Polizei-Alarm senden (nur Polizisten)

- **Waffenmarkt-System**
  - `/weaponmarket [aktion] [parameter]` - Hauptbefehl für alle Waffenmarkt-Aktionen
  - `/weapons [category] [showIllegal]` - Waffen anzeigen
  - `/weapon <weaponId>` - Waffe anzeigen
  - `/licenses` - Lizenztypen anzeigen

- **Blip Creator System**
  - `/blip [aktion] [parameter]` - Hauptbefehl für alle Blip-Aktionen
  - `/bliperstellen [name] [typ] [kategorie] [beschreibung]` - Blip erstellen
  - `/blipinfo [blipId]` - Blip-Informationen anzeigen
  - `/blipmeine` - Meine Blips anzeigen
  - `/bliptyp [typ]` - Blips nach Typ anzeigen
  - `/blipkategorie [kategorie]` - Blips nach Kategorie anzeigen
  - `/blipbearbeiten [blipId] [feld] [wert]` - Blip bearbeiten
  - `/bliplöschen [blipId]` - Blip löschen
  - `/blipumschalten [blipId]` - Blip aktiv/inaktiv umschalten
  - `/blipduplizieren [blipId]` - Blip duplizieren
  - `/blipsuchen [suchbegriff] [filter]` - Blips suchen
  - `/bliptypen` - Verfügbare Blip-Typen anzeigen
  - `/blipfarben` - Verfügbare Blip-Farben anzeigen
  - `/blipstats` - Blip-Statistiken anzeigen
  - `/blipexport` - Alle Blips exportieren
  - `/blipimport [jsonDaten]` - Blips importieren
  - `/blippreview [name] [typ] [farbe]` - Blip-Vorschau anzeigen
  - `/blippreviewstop` - Blip-Vorschau beenden
  - `/blippolizei [name]` - Polizei-Blip erstellen
  - `/blipkrankenhaus [name]` - Krankenhaus-Blip erstellen
  - `/bliptankstelle [name]` - Tankstellen-Blip erstellen
  - `/blipshop [name]` - Shop-Blip erstellen
  - `/blipbank [name]` - Bank-Blip erstellen

- **NPC Creator System**
  - `/npc [aktion] [parameter]` - Hauptbefehl für alle NPC-Aktionen
  - `/npcerstellen [name] [typ] [verhalten]` - NPC erstellen
  - `/npcinfo [npcId]` - NPC-Informationen anzeigen
  - `/npcmeine` - Meine NPCs anzeigen
  - `/npctyp [typ]` - NPCs nach Typ anzeigen
  - `/npcverhalten [verhalten]` - NPCs nach Verhalten anzeigen
  - `/npcbearbeiten [npcId] [feld] [wert]` - NPC bearbeiten
  - `/npclöschen [npcId]` - NPC löschen
  - `/npcumschalten [npcId]` - NPC aktiv/inaktiv umschalten
  - `/npcduplizieren [npcId]` - NPC duplizieren
  - `/npcsuchen [suchbegriff]` - NPCs suchen
  - `/npctypen` - Verfügbare NPC-Typen anzeigen
  - `/npcverhalten` - Verfügbare NPC-Verhalten anzeigen
  - `/npcanimationen` - Verfügbare NPC-Animationen anzeigen
  - `/npcstats` - NPC-Statistiken anzeigen
  - `/npcexport` - Alle NPCs exportieren
  - `/npcimport [jsonDaten]` - NPCs importieren
  - `/npcpolizei [name]` - Polizei-NPC erstellen
  - `/npcmedic [name]` - Sanitäter-NPC erstellen
  - `/npcfeuerwehr [name]` - Feuerwehr-NPC erstellen
  - `/npcwächter [name]` - Wächter-NPC erstellen
  - `/npcverkäufer [name]` - Verkäufer-NPC erstellen

- **Feuerwehr-System**
  - `/feuerwehr [aktion] [parameter]` - Hauptbefehl für alle Feuerwehr-Aktionen
  - `/feuerwehr brand [typ] [level] [radius] [beschreibung]` - Brand erstellen
  - `/feuerwehr löschen [brandId] [werkzeug]` - Brand löschen
  - `/feuerwehr info [brandId]` - Brand-Informationen anzeigen
  - `/feuerwehr alle` - Alle Brände anzeigen
  - `/feuerwehr aktiv` - Aktive Brände anzeigen
  - `/feuerwehr stats` - Feuerwehr-Statistiken anzeigen
  - `/feuerwehr hilfe` - Feuerwehr-System Hilfe

- **Feuerwehrmann-System**
  - `/feuerwehrmann [aktion] [parameter]` - Feuerwehrmann-Management
  - `/feuerwehrmann registrieren [name] [rang] [station]` - Als Feuerwehrmann registrieren
  - `/feuerwehrmann dienst [an/aus]` - Dienst beginnen/beenden
  - `/feuerwehrmann info` - Feuerwehrmann-Informationen anzeigen
  - `/feuerwehrmann alle` - Alle Feuerwehrmänner anzeigen
  - `/feuerwehrmann hilfe` - Feuerwehrmann-System Hilfe

- **Notruf-System**
  - `/notruf [aktion] [parameter]` - Notruf-Management
  - `/notruf erstellen [typ] [priorität] [beschreibung]` - Notruf erstellen
  - `/notruf antworten [notrufId]` - Auf Notruf antworten
  - `/notruf abschließen [notrufId]` - Notruf abschließen
  - `/notruf alle` - Alle Notrufe anzeigen
  - `/notruf aktiv` - Aktive Notrufe anzeigen
  - `/notruf hilfe` - Notruf-System Hilfe

- **Feuerwache-System**
  - `/feuerwache [aktion] [parameter]` - Feuerwachen-Management
  - `/feuerwache info [stationId]` - Feuerwachen-Informationen anzeigen
  - `/feuerwache alle` - Alle Feuerwachen anzeigen
  - `/feuerwache hilfe` - Feuerwache-System Hilfe

- **Feuerwehr Schnellbefehle**
  - `/brand [typ] [level] [radius] [beschreibung]` - Brand erstellen
  - `/brandlöschen [brandId] [werkzeug]` - Brand löschen
  - `/brandinfo [brandId]` - Brand-Informationen anzeigen
  - `/brande` - Alle Brände anzeigen
  - `/aktivebrände` - Aktive Brände anzeigen
  - `/feuerwehrstats` - Feuerwehr-Statistiken anzeigen
  - `/feuerwehrmannwerden [name] [rang] [station]` - Als Feuerwehrmann registrieren
  - `/dienst [an/aus]` - Dienst beginnen/beenden
  - `/feuerwehrmanninfo` - Feuerwehrmann-Informationen anzeigen
  - `/notruferstellen [typ] [priorität] [beschreibung]` - Notruf erstellen
  - `/notrufantworten [notrufId]` - Auf Notruf antworten
  - `/notrufabschießen [notrufId]` - Notruf abschließen
  - `/notrufe` - Alle Notrufe anzeigen
  - `/aktivenotrufe` - Aktive Notrufe anzeigen
  - `/feuerwacheinfo [stationId]` - Feuerwachen-Informationen anzeigen
  - `/feuerwachen` - Alle Feuerwachen anzeigen

- **Admin Feuerwehr-System**
  - `/feuerwehradmin [aktion] [parameter]` - Admin-Befehle für Feuerwehr-System
  - `/feuerwehradmin export` - Feuerwehr-Daten exportieren (Admin)
  - `/feuerwehradmin import [daten]` - Feuerwehr-Daten importieren (Admin)
  - `/feuerwehradmin stats` - Admin-Statistiken anzeigen
  - `/feuerwehradmin cleanup` - Alte Daten bereinigen (Admin)
  - `/feuerwehradmin hilfe` - Feuerwehr-System Admin-Hilfe

- **Alarm-System**
  - `/alarm [aktion] [parameter]` - Hauptbefehl für alle Alarm-Aktionen
  - `/alarmerstellen [name] [typ] [level] [beschreibung]` - Neuen Alarm erstellen
  - `/alarmauslösen [alarmId]` - Alarm auslösen
  - `/alarmstummschalten [alarmId]` - Alarm stummschalten
  - `/alarmzurücksetzen [alarmId]` - Alarm zurücksetzen
  - `/alarminfo [alarmId]` - Alarm-Informationen anzeigen
  - `/alarme` - Alle Alarme anzeigen
  - `/alarmsuche [query]` - Nach Alarmen suchen
  - `/alarmstats` - Alarm-Statistiken anzeigen
  - `/alarmhilfe` - Alarm-System Hilfe

- **Tür-System**
  - `/tür [aktion] [parameter]` - Hauptbefehl für alle Tür-Aktionen
  - `/türerstellen [name] [typ] [schlosstyp] [code]` - Neue Tür erstellen
  - `/türverschließen [türId] [code]` - Tür verschließen
  - `/türoffnen [türId] [code]` - Tür öffnen
  - `/türbeschädigen [türId] [schaden]` - Tür beschädigen
  - `/türreparieren [türId] [menge]` - Tür reparieren
  - `/türzugriff [aktion] [türId] [spielerId]` - Zugriff verwalten
  - `/türschloss [türId] [level]` - Schloss upgraden
  - `/türinfo [türId]` - Tür-Informationen anzeigen
  - `/türen` - Alle Türen anzeigen
  - `/türsuche [query] [filter]` - Türen suchen
  - `/türstats` - Tür-Statistiken anzeigen
  - `/türexport` - Türen exportieren
  - `/türimport [datei]` - Türen importieren
  - `/türhilfe` - Tür-System Hilfe

- **Gefängnis-System**
  - `/gefängnis [aktion] [parameter]` - Hauptbefehl für alle Gefängnis-Aktionen
  - `/einsperren [spieler] [verbrechen] [stunden] [strafe] [notizen]` - Spieler einsperren
  - `/freilassen [spieler] [grund]` - Insassen freilassen
  - `/haftverlängern [spieler] [stunden] [grund]` - Haftstrafe verlängern
  - `/haftverkürzen [spieler] [stunden] [grund]` - Haftstrafe verkürzen
  - `/einzelhaft [spieler] [stunden] [grund]` - In Einzelhaft versetzen
  - `/insassen` - Alle Insassen anzeigen
  - `/gefängnisstats` - Gefängnis-Statistiken anzeigen
  - `/gefängnislogs` - Gefängnis-Logs anzeigen
  - `/gefängnisregeln` - Gefängnis-Regeln anzeigen
  - `/gefängniszellen` - Gefängnis-Zellen anzeigen
  - `/gefängnisorte` - Gefängnis-Orte anzeigen
  - `/gefängnishilfe` - Gefängnis-System Hilfe

  - `/startexam <licenseType>` - Prüfung starten
  - `/answer <examId> <questionIndex> <answerIndex>` - Antwort einreichen
  - `/activeexam` - Aktive Prüfung anzeigen
  - `/mylicenses` - Meine Lizenzen anzeigen
  - `/buyweapon <weaponId> [quantity]` - Waffe kaufen
  - `/sellweapon <weaponId> [quantity]` - Waffe verkaufen
  - `/checklicense <licenseType>` - Lizenz überprüfen
  - `/weaponlicense` - Waffenschein-Prüfung starten
  - `/riflelicense` - Gewehrschein-Prüfung starten
  - `/automaticlicense` - Automatikwaffenschein-Prüfung starten
  - `/speciallicense` - Sonderwaffenschein-Prüfung starten
  - `/handguns` - Handfeuerwaffen anzeigen
  - `/rifles` - Gewehre anzeigen
  - `/shotguns` - Schrotflinten anzeigen
  - `/smgs` - Maschinengewehre anzeigen
  - `/specialweapons` - Spezialwaffen anzeigen
  - `/meleeweapons` - Nahkampfwaffen anzeigen
  - `/illegalweapons` - Illegale Waffen anzeigen
  - `/buypistol [quantity]` - Pistole kaufen
- `/buyrifle [quantity]` - Gewehr kaufen
- `/buyshotgun [quantity]` - Schrotflinte kaufen
- `/buyknife [quantity]` - Messer kaufen
- `/buykatana [quantity]` - Katana kaufen

- **Akten-System**
- `/akte [aktion] [parameter]` - Hauptbefehl für alle Akten-Aktionen
- `/akteerstellen [typ] [titel] [beschreibung]` - Akte erstellen
- `/akteinfo [caseId]` - Akteninformationen anzeigen
- `/aktemeine` - Meine Akten anzeigen
- `/aktepolizei` - Polizei-Akten anzeigen
- `/aktegericht` - Gerichts-Akten anzeigen
- `/aktemedizin` - Medizin-Akten anzeigen
- `/aktearbeit` - Arbeits-Akten anzeigen
- `/akteverkehr` - Verkehrs-Akten anzeigen
- `/aktenotiz [caseId] [notiz]` - Notiz hinzufügen
- `/aktestatus [caseId] [neuerStatus] [grund]` - Status ändern
- `/aktesuchen [suchbegriff] [filter]` - Akten suchen
- `/aktelöschen [caseId]` - Akte löschen
- `/aktetypen` - Verfügbare Akten-Typen anzeigen
- `/aktestats` - Akten-Statistiken anzeigen

- **Laptop-System**
- `/laptop [aktion] [parameter]` - Hauptbefehl für alle Laptop-Aktionen
- `/laptoperstellen [typ] [customApps]` - Laptop erstellen
- `/laptopinfo [laptopId]` - Laptop-Informationen anzeigen
- `/laptopmeine` - Meine Laptops anzeigen
- `/laptopapps [laptopType]` - Verfügbare Apps anzeigen
- `/laptopinstallieren [laptopId] [appName]` - App installieren
- `/laptopdeinstallieren [laptopId] [appName]` - App deinstallieren
- `/laptopeinstellungen [laptopId] [einstellungen]` - Einstellungen ändern
- `/laptopwallpaper [laptopId] [wallpaper]` - Wallpaper ändern
- `/laptoplöschen [laptopId]` - Laptop löschen
- `/laptopypen` - Verfügbare Laptop-Typen anzeigen
- `/laptopjobapps` - Job-spezifische Apps anzeigen
- `/laptopstats` - Laptop-Statistiken anzeigen
- `/laptopbasic` - Standard-Laptop erstellen
- `/laptopprofessional` - Professioneller Laptop erstellen
- `/laptopgaming` - Gaming-Laptop erstellen
- `/laptoppolice` - Polizei-Laptop erstellen (nur Polizisten)
- `/laptopmedic` - Medizin-Laptop erstellen (nur Mediziner)
- `/laptopbusiness` - Business-Laptop erstellen (nur Geschäftsleute)
- `/laptopappinfo [appName]` - App-Informationen anzeigen
- `/laptopappzugriff [appName]` - App-Zugriff prüfen

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
- **H** - Haus-System
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

- **Real-Sync System (Server → Client)**
  - `playerSync` (JSON: Spieler-Daten)
  - `vehicleSync` (JSON: Fahrzeug-Daten)
  - `npcSync` (JSON: NPC-Daten)
  - `objectSync` (JSON: Objekt-Daten)
  - `entityEvent` (JSON: Event-Daten)
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

- `server-files/src/services/tuning.js`
  - `applyTuning(player, vehicleId, tuningItem, targetPlayer)`
  - `getTuningCategories()`
  - `getAllTuningItems()`
  - `getVehicleTuningStatus(vehicleId)`
  - `buyTuningItem(player, itemName, quantity)`

- `server-files/src/services/robbery.js`
  - `startRobbery(player, robberyType)`
  - `joinRobbery(player, robberyType)`
  - `completeRobbery(robberyType, success)`
  - `getActiveRobberies()`
  - `getRobberyTypes()`
  - `getPlayerCooldown(playerId, robberyType)`

- `server-files/src/services/theft.js`
  - `startTheft(player, theftType)`
  - `completeTheft(theftType, success)`
  - `getActiveThefts()`
  - `getTheftTypes()`
  - `getPlayerSkill(playerId)`
  - `getPlayerSkillInfo(playerId)`

- `server-files/src/services/admin_settings.js`
  - `loadConfig()`
  - `saveConfig()`
  - `loadUserData(player)`
  - `addJob(player, data)`
  - `addVendor(player, data)`
  - `addFuelStation(player, data)`
  - `addFaction(player, data)`
  - `addGang(player, data)`
  - `sendNews(player, data)`
  - `setWeather(player, weatherType)`
  - `importConfig(player, data)`
  - `createBackup()`
  - `restoreBackup(player, data)`

- `server-files/src/services/rank_system.js`
  - `hasPermission(player, permission)`
  - `isAdmin(player)`
  - `getAdminRank(player)`
  - `setJobRank(player, jobName, rankName)`
  - `setGangRank(player, gangName, rankName)`
  - `getJobRanks(jobName)`
  - `getGangRanks()`
  - `getAdminRanks()`
  - `getPermissions()`
  - `executeRankAction(player, action, target, data)`

- `server-files/src/services/blip_creator.js`
  - `createBlip(creatorId, blipData)`
  - `updateBlip(blipId, updates, userId)`
  - `deleteBlip(blipId, userId)`
  - `getBlip(blipId)`
  - `getAllBlips()`
  - `getBlipsByCreator(creatorId)`
  - `getBlipsByType(blipType)`
  - `getBlipsByCategory(category)`
  - `searchBlips(query, filters)`
  - `toggleBlip(blipId, userId)`
  - `duplicateBlip(blipId, creatorId, newPosition)`
  - `getBlipTypes()`
  - `getBlipColors()`
  - `getBlipStats()`
  - `exportBlips()`
  - `importBlips(blipsData, creatorId)`

- `server-files/src/services/npc_creator.js`
  - `createNPC(creatorId, npcData)`
  - `updateNPC(npcId, updates, userId)`
  - `deleteNPC(npcId, userId)`
  - `getNPC(npcId)`
  - `getAllNPCs()`
  - `getNPCsByCreator(creatorId)`
  - `getNPCsByType(npcType)`
  - `getNPCsByBehavior(behavior)`
  - `searchNPCs(query, filters)`
  - `toggleNPC(npcId, userId)`
  - `duplicateNPC(npcId, creatorId, newPosition)`
  - `getNPCsInArea(center, radius)`
  - `getNPCStats()`
  - `exportNPCs()`
  - `importNPCs(npcsData, creatorId)`
  - `getNPCTypes()`
  - `getNPCBehaviors()`
  - `getNPCAnimations()`

- `server-files/src/services/house_system.js`
  - `getHouse(houseId)`
  - `getHousesByOwner(ownerId)`
  - `getHousesByRenter(renterId)`
  - `buyHouse(player, houseId)`
  - `sellHouse(player, houseId)`
  - `rentHouse(player, houseId)`
  - `enterHouse(player, houseId)`
  - `exitHouse(player)`
  - `addFurniture(player, houseId, furnitureId, position, rotation)`
  - `removeFurniture(player, houseId, furnitureIndex)`
  - `toggleLock(player, houseId)`
  - `toggleAlarm(player, houseId)`
  - `getFurnitureCatalog()`
  - `getHouseTypes()`
  - `createHouse(admin, type, position, price)`
- `deleteHouse(admin, houseId)`

- `server-files/src/services/business_system.js`
-   - `createBusiness(ownerId, name, type, location, description)`
-   - `getBusiness(businessId)`
-   - `getBusinessesByOwner(ownerId)`
-   - `getBusinessesByEmployee(employeeId)`
-   - `getAllBusinesses()`
-   - `hireEmployee(businessId, employeeId, role, salary)`
-   - `fireEmployee(businessId, employeeId)`
-   - `updateEmployeeRole(businessId, employeeId, newRole, newSalary)`
-   - `addIncome(businessId, amount, source)`
-   - `addExpense(businessId, amount, source)`
-   - `paySalaries(businessId)`
-   - `updateBusinessSettings(businessId, settings)`
-   - `deleteBusiness(businessId)`
-   - `getBusinessTypes()`
-   - `getBusinessStats(businessId)`

- `server-files/src/services/black_market.js`
-   - `startIllegalJob(userId, jobType, location)`
-   - `completeIllegalJob(jobId, success)`
-   - `setJobCooldown(userId, jobType)`
-   - `getAvailableJobs(userId)`
-   - `getActiveJobs(userId)`
-   - `getContrabandItems()`
-   - `sellContraband(userId, itemId, quantity)`
-   - `notifyPolice(job)`
-   - `getBlackMarketStats()`
-   - `cleanupExpiredCooldowns()`

- `server-files/src/services/weapon_market.js`
-   - `getWeapons(category, showIllegal)`
-   - `getWeapon(weaponId)`
-   - `getLicenseTypes()`
-   - `startLicenseExam(userId, licenseType)`
-   - `submitExamAnswer(examId, questionIndex, answerIndex)`
-   - `completeExam(examId)`
-   - `createLicense(userId, licenseType)`
-   - `getUserLicenses(userId)`
-   - `hasLicense(userId, licenseType)`
-   - `buyWeapon(userId, weaponId, quantity)`
-   - `sellWeapon(userId, weaponId, quantity)`
-   - `getActiveExam(userId)`
-   - `getWeaponMarketStats()`

- `server-files/src/services/case_system.js`
-   - `createCase(creatorId, caseType, title, description, data)`
-   - `getCase(caseId)`
-   - `getCasesByType(caseType, userId, userRole)`
-   - `getCasesByUser(userId, userRole)`
-   - `updateCase(caseId, updates, userId)`
-   - `addCaseNote(caseId, userId, note)`
-   - `changeCaseStatus(caseId, newStatus, userId, reason)`
-   - `searchCases(query, filters)`
-   - `deleteCase(caseId, userId)`
-   - `getCaseTypes()`
-   - `getCaseStatuses()`
-   - `getCaseStats()`

- `server-files/src/services/laptop_system.js`
-   - `createLaptop(ownerId, laptopType, customApps)`
-   - `getLaptop(laptopId)`
-   - `getLaptopsByOwner(ownerId)`
-   - `installApp(laptopId, appName, userId)`
-   - `uninstallApp(laptopId, appName, userId)`
-   - `updateLaptopSettings(laptopId, settings, userId)`
-   - `changeWallpaper(laptopId, wallpaper, userId)`
-   - `getAvailableApps(laptopType, userJob)`
-   - `getJobAppInfo(appName)`
-   - `canAccessJobApp(userId, appName, userJob)`
-   - `deleteLaptop(laptopId, userId)`
-   - `getLaptopTypes()`
-   - `getJobApps()`
-   - `getLaptopStats()`

- `server-files/src/services/blip_creator.js`
-   - `createBlip(creatorId, blipData)`
-   - `updateBlip(blipId, updates, userId)`
-   - `deleteBlip(blipId, userId)`
-   - `getBlip(blipId)`
-   - `getAllBlips()`
-   - `getBlipsByCreator(creatorId)`
-   - `getBlipsByType(blipType)`
-   - `getBlipsByCategory(category)`
-   - `searchBlips(query, filters)`
-   - `toggleBlip(blipId, userId)`
-   - `duplicateBlip(blipId, creatorId, newPosition)`
-   - `getBlipTypes()`
-   - `getBlipColors()`
-   - `getBlipStats()`
-   - `exportBlips()`
-   - `importBlips(blipsData, creatorId)`

- `server-files/src/services/npc_creator.js`
-   - `createNPC(creatorId, npcData)`
-   - `updateNPC(npcId, updates, userId)`
-   - `deleteNPC(npcId, userId)`
-   - `getNPC(npcId)`
-   - `getAllNPCs()`
-   - `getNPCsByCreator(creatorId)`
-   - `getNPCsByType(npcType)`
-   - `getNPCsByBehavior(behavior)`
-   - `searchNPCs(query, filters)`
-   - `toggleNPC(npcId, userId)`
-   - `duplicateNPC(npcId, creatorId, newPosition)`
-   - `getNPCsInArea(center, radius)`
-   - `getBlipStats()`
-   - `exportNPCs()`
-   - `importNPCs(npcsData, creatorId)`
-   - `getNPCTypes()`
-   - `getNPCBehaviors()`
-   - `getNPCAnimations()`

- `server-files/src/services/prison_system.js`
-   - `imprisonPlayer(policeId, inmateId, crime, sentenceHours, fine, notes)`
-   - `releaseInmate(policeId, inmateId, reason)`
-   - `extendSentence(policeId, inmateId, additionalHours, reason)`
-   - `reduceSentence(policeId, inmateId, reductionHours, reason)`
-   - `solitaryConfinement(policeId, inmateId, hours, reason)`
-   - `getInmateInfo(inmateId)`
-   - `getAllInmates()`
-   - `getPrisonStats()`
-   - `logPrisonAction(action, policeId, inmateId, details)`
-   - `getPrisonLogs(filters, limit)`
-   - `getPrisonRules()`
-   - `getPrisonCells()`
-   - `getPrisonLocations()`
-   - `createDefaultCells()`
-   - `createDefaultRules()`

- `server-files/src/services/door_system.js`
-   - `createDoor(creatorId, doorData)`
-   - `updateDoor(doorId, updates, userId)`
-   - `deleteDoor(doorId, userId)`
-   - `lockDoor(doorId, userId, lockCode)`
-   - `unlockDoor(doorId, userId, lockCode)`
-   - `breakDoor(doorId, userId, damage)`
-   - `repairDoor(doorId, userId, repairAmount)`
-   - `addAccess(doorId, userId, targetUserId)`
-   - `removeAccess(doorId, userId, targetUserId)`
-   - `upgradeLock(doorId, userId, newLockLevel)`
-   - `getDoor(doorId)`
-   - `getAllDoors()`
-   - `getDoorsByOwner(ownerId)`
-   - `getDoorsByType(doorType)`
-   - `getDoorsInArea(center, radius)`
-   - `searchDoors(query, filters)`
-   - `getDoorStats()`
-   - `exportDoors()`
-   - `importDoors(doorsData, creatorId)`
-   - `hasAccess(userId, doorId)`
-   - `isDoorLocked(doorId)`
-   - `isDoorBroken(doorId)`
-   - `getDoorTypes()`
-   - `getLockTypes()`
-   - `getDoorLocations()`

- `server-files/src/services/fire_department.js`
  - `createFire(fireData)`
  - `updateFire(fireId, updates)`
  - `extinguishFire(fireId, firefighterId, tool)`
  - `spreadFire(fireId)`
  - `registerFirefighter(userId, firefighterData)`
  - `updateFirefighter(userId, updates)`
  - `awardExperience(userId, amount, reason)`
  - `createEmergencyCall(callData)`
  - `respondToCall(callId, firefighterId)`
  - `completeCall(callId)`
  - `getFire(fireId)`
  - `getAllFires()`
  - `getActiveFires()`
  - `getFiresByType(type)`
  - `getFirefighter(userId)`
  - `getAllFirefighters()`
  - `getOnDutyFirefighters()`
  - `getEmergencyCall(callId)`
  - `getAllEmergencyCalls()`
  - `getActiveEmergencyCalls()`
  - `getFireStats()`
  - `exportFireData()`
  - `importFireData(data)`
  - `cleanup()`

- `server-files/src/services/alarm_system.js`
  - `createAlarm(creatorId, alarmData)`
  - `updateAlarm(alarmId, updates, userId)`
  - `deleteAlarm(alarmId, userId)`
  - `triggerAlarm(alarmId, triggerData)`
  - `silenceAlarm(alarmId, userId)`
  - `resetAlarm(alarmId, userId)`
  - `sendAlarmNotifications(alarm, triggerData)`
  - `notifyPolice(alarmInfo)`
  - `notifyFireDepartment(alarmInfo)`
  - `notifyAdmins(alarmInfo)`
  - `logAlarmAction(alarmId, action, data)`
  - `getAlarm(alarmId)`
  - `getAllAlarms()`
  - `getAlarmsByType(alarmType)`
  - `getActiveAlarms()`
  - `getAlarmsByCreator(creatorId)`
  - `getAlarmsInArea(center, radius)`
  - `searchAlarms(query, filters)`
  - `getAlarmStats()`
  - `exportAlarms()`
  - `importAlarms(alarmsData, creatorId)`
  - `getAlarmTypes()`
  - `getAlarmLevels()`
  - `getAlarmLocations()`

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

- Admin Settings UI (F10)
  - `client_packages/admin_settings.html`
  - `client_packages/admin_settings.js`
  - `client_packages/admin_settings_controller.js`

- Rang-System UI (R-Taste)
  - `client_packages/rank_system.html`
  - `client_packages/rank_system_controller.js`

- Haus-System UI (H-Taste)
  - `client_packages/house_system.html`
  - `client_packages/house_system_controller.js`

- Tuning Workshop (F9)
  - `client_packages/ui/tuning/index.html`
  - `client_packages/tuning_controller.js`

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



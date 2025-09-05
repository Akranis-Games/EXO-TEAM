# Detaillierte Dateistruktur eines typischen RageMP-Servers

server-files/  # Root-Ordner für alle Server-Dateien. Hier liegt der Kern deines RageMP-Servers. Wird automatisch erstellt, wenn du den Updater ausführst.
├── client_packages/  # Ordner für clientseitige Skripte und Ressourcen. Alles hier wird an den Client (Spieler) gesendet und heruntergeladen. Enthält UI-Elemente, Events und Logik, die auf dem Client ausgeführt werden.
│   ├── index.js  # Einstiegspunkt für clientseitige Skripte. Hier requirest du andere JS-Dateien, Events oder Module (z. B. require('./ui/index.js');).
│   ├── ui/  # Unterordner für User Interface (UI)-Elemente. Hier legst du HTML-basierte Menüs, HUDs oder andere visuelle Komponenten ab. Wichtig für CEF (Chromium Embedded Framework)-basierte UIs in RageMP.
│   │   ├── index.html  # Haupt-HTML-Datei für das UI. Definiert die Struktur deines Interfaces (z. B. mit <div>-Elementen für Menüs).
│   │   ├── css/  # Ordner für Stylesheets. Enthält CSS-Dateien zur Gestaltung des UIs.
│   │   │   ├── style.css  # Beispiel: Haupt-CSS-Datei für Farben, Layouts und Animationen (z. B. body { background: black; }).
│   │   │   └── ...  # Weitere CSS-Dateien, z. B. für spezifische UI-Komponenten wie buttons.css.
│   │   └── js/  # Ordner für JavaScript-Dateien des UIs. Hier liegt die Logik für Interaktionen, Events und Kommunikation mit dem Server.
│   │       ├── main.js  # Beispiel: Haupt-Skript für UI-Logik (z. B. Event-Listener für Buttons, mp.events.callRemote() für Server-Kommunikation).
│   │       ├── events.js  # Beispiel: Handhabt clientseitige Events wie 'playerReady' oder benutzerdefinierte UI-Events.
│   │       └── ...  # Weitere JS-Dateien, z. B. utils.js für Hilfsfunktionen.
│   ├── cef/  # Optionaler Unterordner für erweiterte CEF-UIs (ähnlich zu ui/, aber speziell für Browser-basierte Inhalte).
│   ├── events.js  # Beispiel: Globale clientseitige Events (z. B. mp.events.add('playerChat', ...);).
│   ├── commands.js  # Beispiel: Clientseitige Commands (z. B. für lokale Tests oder UI-Shortcuts).
│   └── ...  # Weitere Dateien/Ordner, z. B. assets/ für Bilder, Sounds oder Models, die clientseitig geladen werden.
├── packages/  # Ordner für serverseitige Skripte und Ressourcen. Alles hier wird nur auf dem Server ausgeführt und handhabt Logik wie Events, Spieler-Management, Datenbanken usw.
│   ├── gamemode/  # Beispiel-Unterordner für dein Haupt-Gamemode (kann beliebig benannt werden, z. B. 'myrp' für Roleplay).
│   │   ├── index.js  # Einstiegspunkt für den Gamemode. Requires andere Dateien (z. B. require('./events.js'); require('./commands.js');).
│   │   ├── events.js  # Handhabt serverseitige Events (z. B. mp.events.add('playerJoin', (player) => { player.outputChatBox('Willkommen!'); });).
│   │   ├── commands.js  # Server-Commands (z. B. mp.events.addCommand('hp', (player) => { player.health = 100; });).
│   │   ├── spawn_points.json  # JSON-Datei für Spawn-Punkte (z. B. { "SpawnPoints": [{ "x": -425.517, "y": 1123.620, "z": 325.8544 }, ...] }).
│   │   ├── config.json  # Optionale Konfig-Datei für Gamemode-spezifische Einstellungen (z. B. Datenbank-Details oder Spielregeln).
│   │   └── ...  # Weitere Dateien, z. B. database.js für MySQL-Integration oder vehicles.js für Fahrzeug-Management.
│   ├── plugins/  # Manchmal hier integriert: Unterordner für serverseitige Plugins (aber oft im Root).
│   └── ...  # Weitere Gamemodes oder Ressourcen-Ordner, z. B. 'auth' für Login-System oder 'economy' für Wirtschaftssystem.
├── maps/  # Ordner für Map-Dateien. Enthält JSON-Dateien, die Objekte, Props oder Custom-Maps definieren, die in die Spielwelt geladen werden.
│   ├── example_map.json  # Beispiel: Definiert Positionen von Objekten (z. B. { "objects": [{ "model": "prop_barrier", "pos": { "x": 0, "y": 0, "z": 0 } }] }).
│   └── ...  # Weitere Maps, z. B. interior.json für Innenräume.
├── plugins/  # Ordner für DLL-Plugins. Hier legst du erweiterte Server-Plugins ab, die in C# oder C++ geschrieben sind.
│   ├── example_plugin.dll  # Beispiel: Ein Plugin für erweiterte Funktionen wie Voice-Chat oder Anti-Cheat.
│   └── ...  # Weitere DLLs, z. B. mysql.dll für Datenbank-Verbindungen.
├── conf.json  # Wichtige Konfigurationsdatei (JSON). Enthält Server-Einstellungen wie Name, Port, Max-Spieler usw. Beispiel-Inhalt:
│              # {
│              #   "name": "Mein RageMP Server",
│              #   "gamemode": "freeroam",
│              #   "maxplayers": 100,
│              #   "port": 22005,
│              #   "language": "de",
│              #   "announce": true,
│              #   "modules": ["javascript-module"]
│              # }
├── .settings/  # Optionaler Ordner für erweiterte Einstellungen (manchmal vorhanden, z. B. für Logs oder Cache).
│   └── logs/  # Unterordner für Server-Logs (z. B. error.log, access.log).
└── ragemp-server.exe  # Die ausführbare Server-Datei. Starte den Server hiermit (öffnet eine Konsole mit Logs und Fehlern).


## Erklärungen und Tipps zur Struktur

Root-Ordner (server-files): Dies ist der Hauptordner, den du herunterlädst oder generierst. Lade den RageMP-Server von der offiziellen Website (rage.mp) herunter und extrahiere ihn. Führe updater.exe (falls vorhanden) aus, um Updates zu holen und die Struktur zu initialisieren.
client_packages: Fokussiert auf alles, was der Client braucht. Verwende JavaScript (Node.js-Style) für Skripte. Für UIs nutze CEF, um HTML/CSS/JS zu integrieren – perfekt für Menüs, Inventare oder HUDs.
packages: Server-seitig, auch in JS. Hier baust du deine Logik auf, z. B. mit mp.events für Ereignisse wie Player-Join, Death oder Chat. Du kannst Datenbanken (z. B. MySQL) integrieren oder externe Module require'n.
Zusätzliche Dateien: In der Realität könnten noch Dateien wie meta.xml (für Ressourcen-Metadaten) oder settings.xml (für Client-Einstellungen) hinzukommen, je nach Version (z. B. in RageMP 1.1).
Erweiterungstipps:

Für Roleplay-Server: Füge in packages Ordner wie jobs/, factions/ oder vehicles/ hinzu.
Für Performance: Halte client_packages leicht, da es heruntergeladen wird.
Konfiguration: Bearbeite conf.json für Port (Standard: 22005), Server-Namen und Module (z. B. "csharp-module" für C#-Skripte).


Starten des Servers: Führe ragemp-server.exe aus. Verbinde dich im Client mit 127.0.0.1:22005 für Localhost-Tests.

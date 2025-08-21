# Deploy-Leitfaden

## Produktions-Setup

### 1. Server-Umgebung
- **Betriebssystem**: Windows Server 2019/2022 oder Linux (Ubuntu 20.04+)
- **RAM**: Mindestens 4GB, empfohlen 8GB+
- **CPU**: 4+ Kerne
- **Festplatte**: 50GB+ freier Speicher
- **Netzwerk**: Stabile Internetverbindung, statische IP empfohlen

### 2. Node.js Setup
```bash
# Node.js 22.x installieren
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt-get install -y nodejs

# Oder Windows: Node.js 22.x MSI herunterladen
# https://nodejs.org/en/download/

# Version prüfen
node --version  # Sollte v22.x.x anzeigen
npm --version
```

### 3. RageMP Server
```bash
# RageMP Server herunterladen
wget https://rage.mp/downloads/server

# Entpacken
unzip server.zip -d ragemp-server/

# Berechtigungen setzen (Linux)
chmod +x ragemp-server/ragemp-server
```

### 4. Projekt-Deployment
```bash
# Projekt klonen/kopieren
cp -r rp-server/* ragemp-server/

# Abhängigkeiten installieren
cd ragemp-server
npm install --production

# Konfiguration anpassen
nano config/default.json
```

### 5. Konfiguration (Produktion)
```json
{
  "motd": "Willkommen auf unserem RP-Server!",
  "spawn": {"x": -1037.74, "y": -2738.04, "z": 20.17},
  "adminIds": [1, 2, 3],
  "maxPlayers": 100,
  "autoRestart": true,
  "backupInterval": 86400000
}
```

### 6. Service einrichten (Linux)
```bash
# Systemd Service erstellen
sudo nano /etc/systemd/system/ragemp.service

[Unit]
Description=RageMP RP Server
After=network.target

[Service]
Type=simple
User=ragemp
WorkingDirectory=/opt/ragemp-server
ExecStart=/usr/bin/node index.js
Restart=always
RestartSec=10

[Install]
WantedBy=multi-user.target

# Service aktivieren
sudo systemctl enable ragemp
sudo systemctl start ragemp
```

### 7. Windows Service (Alternative)
```powershell
# NSSM installieren
# https://nssm.cc/download

# Service erstellen
nssm install RageMP "C:\Program Files\nodejs\node.exe"
nssm set RageMP AppDirectory "C:\ragemp-server"
nssm set RageMP AppParameters "index.js"
nssm start RageMP
```

### 8. Monitoring & Logs
```bash
# Logs anzeigen
sudo journalctl -u ragemp -f

# Status prüfen
sudo systemctl status ragemp

# Performance überwachen
htop
iotop
```

### 9. Backup-Strategie
```bash
# Automatisches Backup-Skript
#!/bin/bash
BACKUP_DIR="/backup/ragemp"
DATE=$(date +%Y%m%d_%H%M%S)

# Daten sichern
tar -czf "$BACKUP_DIR/ragemp_$DATE.tar.gz" \
  storage/ config/ server-files/

# Alte Backups löschen (älter als 14 Tage)
find $BACKUP_DIR -name "ragemp_*.tar.gz" -mtime +14 -delete

# Cron-Job: Täglich um 3:00 Uhr
# 0 3 * * * /path/to/backup.sh
```

### 10. Sicherheit
- [ ] Firewall konfigurieren (Ports 22005/22006)
- [ ] SSH-Zugang beschränken
- [ ] Regelmäßige Updates
- [ ] SSL/TLS für Admin-Interface (optional)
- [ ] DDoS-Schutz aktivieren

### 11. Performance-Optimierung
```javascript
// config/default.json
{
  "maxPlayers": 100,
  "tickRate": 64,
  "streamDistance": 1000,
  "maxStreamingDistance": 2000,
  "enableCef": true,
  "enableVoice": false
}
```

### 12. Troubleshooting
```bash
# Server neu starten
sudo systemctl restart ragemp

# Logs prüfen
tail -f /var/log/ragemp/error.log

# Ports prüfen
netstat -tulpn | grep :22005
netstat -tulpn | grep :22006

# Node.js Prozess finden
ps aux | grep node
```

## Nächste Schritte
1. Server starten und testen
2. Spieler einladen
3. Performance überwachen
4. Regelmäßige Backups
5. Updates planen

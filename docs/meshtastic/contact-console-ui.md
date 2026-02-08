# Contact - ein Console UI für Meshtastic

Contact ist ein Terminal User Interface (TUI) für Meshtastic. Die textbasierte Oberfläche läuft vollständig im Terminal und eignet sich besonders für Headless-Systeme, Raspberry Pis und Remote-Server per SSH.

Die Oberfläche ist in drei Bereiche aufgeteilt:

1. Kanäle
2. Nachrichtenfenster
3. Nodes im Mesh

Die Navigation erfolgt über die Pfeiltasten, Aktionen werden mit Enter ausgelöst. Empfangene Nachrichten und Node-Infos werden in einer lokalen SQLite-Datenbank (`client.db`) gespeichert und beim nächsten Start wiederhergestellt.

## Installation

### Vorbereitung

Die Installation über `pipx` hält Contact in einer isolierten Umgebung und vermeidet Konflikte mit Systempaketen. Falls `pipx` noch nicht installiert ist, siehe [Python CLI – Installation](python-cli#installation).

### Contact

```bash
pipx install contact
```

### Verbindung

Ohne Argumente versucht Contact zunächst eine serielle Verbindung, dann TCP zu localhost. Eine Verbindung lässt sich auch explizit angeben:

```bash
contact --port /dev/ttyUSB0   # Seriell
contact --host 192.168.1.50   # TCP/IP
contact --ble <Adresse>       # Bluetooth
```

## Nachrichtenversand

### Kanalnachrichten

1. Kanal in der linken Spalte auswählen
2. Nachricht eingeben
3. Enter drücken

### Direktnachrichten

1. Node in der rechten Spalte auswählen
2. Enter drücken
3. Nachricht eingeben und senden

## Konfiguration

Mit der Backtick-Taste (`` ` ``) oder `F12` öffnest du das Konfigurationsmenü direkt in der TUI. Alternativ startest du Contact im Konfigurationsmodus:

```bash
contact --settings
```

Die Struktur orientiert sich an der offiziellen Meshtastic-App und umfasst unter anderem:

- Radio-Einstellungen
- Power-Management
- Position und Telemetrie
- Kanal-Konfiguration
- Geräteeinstellungen

## Skripte

Contact lässt sich auch ohne TUI aus Skripten heraus nutzen, z. B. für regelmäßige Statusmeldungen per Cron:

```bash
#!/bin/bash
contact --host 192.168.1.50 --send "Still alive."
```

```bash
*/30 * * * * /home/user/scripts/status.sh
```

## Befehlsübersicht

| Befehl | Beschreibung |
|---|---|
| `contact` | Startet die TUI (serial, dann TCP zu localhost) |
| `contact --port /dev/ttyUSB0` | Verbindung über serielle Schnittstelle |
| `contact --host <IP>` | Verbindung über TCP/IP |
| `contact --ble <Adresse>` | Verbindung über Bluetooth |
| `contact --settings` | Startet direkt im Konfigurationsmodus |
| `contact --help` | Zeigt alle verfügbaren Optionen |
| `contact --version` | Zeigt die installierte Version |

## Tastenkürzel

| Taste | Beschreibung |
|---|---|
| `↑` `↓` `←` `→` | Navigation |
| `F1` / `F2` / `F3` | Zu Kanälen / Nachrichten / Nodes springen |
| `ENTER` | Nachricht senden oder Node für DM auswählen |
| `` ` `` oder `F12` | Einstellungen öffnen |
| `CTRL+K` | Befehlsliste anzeigen |
| `CTRL+P` | Paket-Log ein/ausblenden |
| `CTRL+T` oder `F4` | Traceroute zu einer Node |
| `F5` | Node-Info anzeigen |
| `CTRL+F` | Node als Favorit markieren |
| `CTRL+G` | Node ignorieren |
| `CTRL+D` | Chat archivieren oder Node entfernen |
| `CTRL+/` | Suche starten |
| `ESC` | Menü schließen oder App beenden |

## Links

- [GitHub](https://github.com/pdxlocations/contact)

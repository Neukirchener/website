# Meshtastic GTK‑Client
Wenn du Meshtastic lieber mit einer grafischen Oberfläche bedienen möchtest, ist der [GTK‑Client](https://gitlab.com/kop316/gtk-meshtastic-client/) eine schöne Ergänzung zur Meshtastic Python CLI. Die Oberfläche gestaltet sich übersichtlich und ist intuitiv zu bedienen. Hier können die eigenen Nodes bequem konfiguriert und Nachrichten via Computer versendet werden. 

## Installation
Die Installation kannst du mit dem folgenden Befehl einleiten:
### Debian / Ubuntu / Linux Mint
```bash
sudo apt install gtk-meshtastic-client
```

Nach der Installation findest du den Client im Anwendungsmenü.

# Verbindung
Sobald du dein Meshtastic‑Gerät per USB anschließt, sollte der GTK‑Client es automatisch erkennen. Falls das nicht klappt, lohnt sich ein kurzer Blick auf die erforderlichen Berechtigungen.

## Rechte
Überprüfe, ob dein Meshtastic‑Gerät vom System erkannt wird, indem du die entsprechenden Gerätedateien auflistest.
```bash
ls -l /dev/ttyUSB*
ls -l /dev/ttyACM*
```
Falls nötig, musst du deinen Benutzer der Gruppe dialout hinzufügen, damit das Gerät erkannt wird.
```bash
sudo usermod -aG dialout $USER
```
:::note
Danach meldest du dich einmal ab und anschließend wieder an, damit die neue Gruppen­zugehörigkeit aktiv wird.
:::

# Bedienung
Der GTK‑Client bietet dir eine grafische Oberfläche für...

TODO

Node‑Konfiguration

Kanal‑Einstellungen

GPS‑Daten anzeigen

Nachrichten senden

Logs ansehen

Firmware‑Informationen

Auswahl des seriellen Ports

Automatische Erkennung angeschlossener Geräte

# Updates
Um die Software zu aktualisieren führst du die folgenden Befehle aus:
```bash
sudo apt update
sudo apt upgrade
```

# Deinstallation
Falls du den Client wieder von deinem System entfernen möchtest:
```bash
sudo apt remove gtk-meshtastic-client
```

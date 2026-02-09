---
sidebar_position: 2
---

# Geräte

Empfohlene LoRa-Geräte für Meshtastic und MeshCore im Rheinland.

## Heltec Mesh Node T114

| Eigenschaft | Details |
|---|---|
| Preis | ~30–40 € |
| MCU | Nordic nRF52840 |
| LoRa | SX1262, 868 MHz (EU), 22 dBm Sendeleistung |
| Konnektivität | Bluetooth 5.0 (kein WiFi) |
| Display | 0.96" OLED |
| Akku | Li-Po Anschluss, kein Akku im Lieferumfang |
| GPS | Optional (L76K GNSS) |
| Formfaktor | Kompakt, gut für mobile Nutzung |

Stromsparender Einsteiger-Node dank nRF52840. Kein WiFi, daher kein MQTT-Bridge-Betrieb. Ideal als tragbares Gerät oder für stationären Betrieb. Dank des geringen Stromverbrauchs sehr beliebt für Solarbetrieb.


## Heltec V3

| Eigenschaft | Details |
|---|---|
| Preis | ~20–25 € |
| MCU | Espressif ESP32-S3 |
| LoRa | SX1262, 868 MHz (EU), 22 dBm Sendeleistung |
| Konnektivität | WiFi 2.4 GHz + Bluetooth 5.0 |
| Display | 0.96" OLED |
| Akku | Li-Po Anschluss, kein Akku im Lieferumfang |
| GPS | ✗ |
| Formfaktor | Kompakt |

Günstigster Einstieg mit vollem Funktionsumfang. Einer der meistgenutzten Nodes im Netz — gut unterstützt, viele Anleitungen verfügbar.


## Heltec V4

| Eigenschaft | Details |
|---|---|
| Preis | ~25–30 € |
| MCU | Espressif ESP32-S3 |
| LoRa | SX1262 + PA, 868 MHz (EU), bis zu 27 dBm Sendeleistung |
| Konnektivität | WiFi 2.4 GHz + Bluetooth 5.0 |
| Display | 0.96" OLED |
| Akku | Li-Po Anschluss, kein Akku im Lieferumfang |
| GPS | Optional (L76K GNSS) |
| Formfaktor | Kompakt |

Überarbeitete Version des V3 mit verbessertem Antennenanschluss und Layout. Für Neueinsteiger empfehlenswerter als der V3, da aktueller Stand der Technik.

## SenseCAP Card Tracker T1000-E für Meshtastic
Der SenseCAP Card Tracker T1000-E für Meshtastic ist ein kompakter, kreditkartengroßer Tracker mit integrierter GPS- und LoRa-Technologie für präzise und stromsparende Ortung und Kommunikation.

Geliefert wird er mit einem magnetischen Ladekabel. Option 

:::note Hinweis
Achte beim Kauf darauf, die „for Meshtastic“-Version zu wählen.
:::
| Eigenschaft | Beschreibung |
|------------|---------|
| Netzwerkprotokolle | LoRa (863–928 MHz), Bluetooth v5.1 |
| Reichweite | 2–5 km (abhängig von Antenne, Installation und Umgebung) |
| Antenne | Intern (GNSS / LoRa / Wi-Fi / BLE) |
| Schutzklasse | IP65 |
| Zertifizierung | CE / FCC |
| Abmessungen | 85 × 55 × 6.5 mm |
| Gewicht | 32 g |
| Betriebstemperatur | −20 °C bis +60 °C |
| Betriebsfeuchtigkeit | 5 % – 95 % (keine Kondensation) |

### Sensoren & Bedienelemente

| Eigenschaft | Beschreibung |
|------------|---------|
| Temperatursensor | −20 bis 60 °C, ±1 °C Genauigkeit (min ±0.5 °C), Auflösung 0.1 °C |
| Lichtsensor | 0–100 % (0 % = dunkel, 100 % = maximale Helligkeit) |
| Beschleunigungssensor | 3-Achs-Accelerometer (Bewegungserkennung, aktuell nicht in Meshtastic genutzt) |
| LED | 1× Status-LED |
| Buzzer | 1× akustisches Statussignal |
| Taster | 1× Bedienknopf |

### Stromversorgung & Akku

| Eigenschaft | Beschreibung |
|------------|---------|
| Akkutyp | Wiederaufladbarer Lithium-Akku |
| Akkukapazität | 700 mAh |
| Batteriestatus | Periodische Übertragung des Akkustands |
| Ladeanschluss | Magnetisches USB-Ladekabel (1 m, Adapter nicht enthalten) |
| Eingangsspannung | 4.7 – 5.5 V DC |
| Ladetemperatur | 0 °C bis +45 °C |

:::note Taster
Der Taster dient zum Ein-/Ausschalten, Aktivieren von Bluetooth und zum Auslösen von Statusfunktionen. Signaltöne beschränken sich derzeit auf Start- und Bestätigungstöne sowie Warnungen bei niedrigem Akkustand.
:::

### Links
 * [Herstellerseite](https://www.seeedstudio.com/SenseCAP-Card-Tracker-T1000-E-for-Meshtastic-p-5913.html)
 * [Wikieintrag](https://wiki.seeedstudio.com/sensecap_t1000_e/)
 * [Forum](https://forum.seeedstudio.com/t/sensecap-t1000-e-meshtastic-tracker-user-guide/287783)


## Seeed Studio Xiao nRF52840 WIO

| Eigenschaft | Details |
|---|---|
| Preis | ~35–45 € |
| MCU | Nordic nRF52840 |
| LoRa | Wio-SX1262, 868 MHz (EU), 22 dBm Sendeleistung |
| Konnektivität | Bluetooth 5.0 (kein WiFi) |
| Display | Keins (extern möglich) |
| Akku | Li-Po Anschluss |
| GPS | ✗ |
| Formfaktor | Sehr kompakt (Briefmarkengröße) |

Kleinstes verfügbares Format. XIAO-Board + Wio-SX1262-Modul werden kombiniert — einfaches Aufstecken, kein Löten notwendig. Kein Display serienmäßig, daher eher für stationären Betrieb geeignet.


## RAK Wireless WisBlock

| Eigenschaft | Details |
|---|---|
| Preis | ~50–80 € (Starter-Kit) |
| MCU | Nordic nRF52840 (RAK4631) |
| LoRa | SX1262, 868 MHz (EU), 22 dBm Sendeleistung |
| Konnektivität | Bluetooth 5.0; WiFi über optionales Modul |
| Display | Optional (Erweiterungsmodul) |
| Akku | Li-Po Anschluss |
| GPS | Optional (RAK1910 Modul) |
| Formfaktor | Modular, industrietauglich |

Modulares System: Basisboard + austauschbare Module (GPS, Sensoren, Display, Solar). Höchste Flexibilität, aber auch höchster Preis und mehr Einarbeitungsaufwand. Empfehlenswert für Fortgeschrittene oder spezielle Anforderungen (z. B. Solarknoten, Wetterstation).


## Vergleich

| Gerät | Display | WiFi | GPS | Akku-Anschluss | Solar-Anschluss | Sendeleistung |
|---|---|---|---|---|---|---|
| Heltec Mesh Node T114 | ✓ | ✗ | optional | ✓ | ✓ | 22 dBm |
| Heltec V3 | ✓ | ✓ | ✗ | ✓ | ✗ | 22 dBm |
| Heltec V4 | ✓ | ✓ | optional | ✓ | ✓ | 27 dBm |
| Seeed T1000-E | ✗ | ✗ | ✓ | ✓ (intern, 700 mAh) | ✗ | 27 dBm |
| Seeed Xiao nRF52840 WIO | ✗ | ✗ | ✗ | ✓ | ✗ | 22 dBm |
| RAK Wireless WisBlock | optional | optional | optional | ✓ | optional | 22 dBm |

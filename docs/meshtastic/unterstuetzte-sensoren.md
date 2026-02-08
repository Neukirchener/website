---
sidebar_position: 4
---

# Unterstützte Sensoren

Meshtastic‑Geräte können neben der reinen Nachrichtenweitergabe auch Umweltdaten erfassen. Sensoren messen z. B. Temperatur, Luftfeuchtigkeit, Luftdruck, Lichtintensität, UV‑Strahlung, Strom, Regen oder Partikelkonzentrationen. Diese Daten lassen sich direkt ins Mesh senden, wodurch Meshtastic nicht nur für Kommunikation, sondern auch für Monitoring, Wetterstationen oder Umweltdatenerfassung genutzt werden kann.

Damit du ein Gefühl dafür bekommst, was im Alltag gut funktioniert, findest du hier eine kompakte Übersicht der Sensorarten, typische Einsatzszenarien und ein paar praktische Hinweise aus der Community‑Praxis.

## Sensorarten im Überblick

- Temperatur & Luftfeuchtigkeit: z. B. AHT10, BME280, SHT31 – ideal für Wetter, Klima oder Innenraumüberwachung.
- Barometrischer Druck: z. B. BMP280, DPS310 – für Höhenmessung, Wettervorhersage oder Telemetrie.
- Licht & UV: z. B. OPT3001, LTR390UV – für Solarüberwachung oder Umgebungslichtmessung.
- Strom & Spannung: z. B. INA219, INA260 – zur Messung von Batteriespannung oder Verbrauch.
- Regen & Partikel: z. B. DFROBOT_RAIN, PMSA003I – für Umweltdatenerfassung und Luftqualität.
- CO₂: z. B. SCD4X – für Raumluftqualität oder Umweltmonitoring.
- Herzfrequenz & Körpertemperatur: z. B. MAX30102, MLX90614 – nur bei speziellen Geräten oder Wearables relevant.

Die Sensoren erzeugen in der Regel sehr wenig Traffic und belasten das Mesh kaum. Sie können als eigenständige Knoten arbeiten oder in Kombination mit Client‑/Router‑Rollen betrieben werden.

### Energieverbrauch & Einsatzdauer

Nicht jeder Sensor ist gleich sparsam. Sofern du batteriebetriebene Nodes planst, lohnt sich ein kurzer Blick auf den Energiebedarf. Diesen findest du im Datenblatt des jeweiligen Sensors.

:::note Messintervall
Für Outdoor‑Nodes mit Akku oder Solar empfiehlt es sich, Messintervalle großzügig zu wählen (z. B. alle 5–15 Minuten), um die Laufzeit zu verlängern.
:::

## I²C-Schnittstelle

Bei Outdoor‑Installationen oder wenn du längere Kabel verlegst, lohnt sich ein kurzer Blick auf die Praxis. I²C‑Leitungen sollten möglichst kurz bleiben, idealerweise unter 30 cm. Längere Kabel funktionieren besser, wenn sie geschirmt sind oder als Twisted Pair verlegt werden. Achte außerdem auf saubere 3,3 V‑Pull‑Ups – viele Boards bringen die schon mit. Feuchtigkeit ist der natürliche Feind von I²C; Schrumpfschlauch, Silikon oder ein Gehäuse schützen die Verbindungen zuverlässig. Wenn ein Sensor plötzlich „verschwunden" ist oder keine Daten mehr liefert, liegt es fast immer an der I²C‑Leitung.

## Aktivierung

Damit Sensoren Daten ins Mesh senden, musst du sie im Telemetry‑Modul aktivieren. Hierzu entweder das Web‑Interface, die App oder CLI verwenden.

## Praxisbeispiele für Sensoren im Mesh

### Wetter‑Node (Outdoor)

Ein BME280 misst Temperatur, Luftfeuchtigkeit und Druck, ein LTR390UV erfasst UV‑Strahlung, und ein DFROBOT_RAIN zählt Regentropfen. Optional lässt sich auch Windrichtung und -geschwindigkeit über einen DFROBOT_LARK erfassen.

### Energie‑Node

Mit INA219 oder INA260 misst du Strom und Spannung, ein einfacher Spannungsteiler hilft, die Batteriespannung zu überwachen. Wer Solar nutzt, kann so überwachen, wie viel Strom über das Solarpanel erzeugt wird.

### Mobile Telemetrie

Für Rucksack‑ oder Fahrzeug‑Sensorik reicht oft ein BME280, um Temperatur, Luftfeuchtigkeit und Druck zu erfassen. Höhenmessung über den Luftdruck funktioniert ebenfalls gut. Die Temperaturmessung ist bei tragbaren Geräten nur eingeschränkt aussagekräftig, da Körperwärme oder direkte Sonneneinstrahlung die Werte verfälschen können.

:::note Hinweis für mobile Geräte
Sensorwerte können durch **Körperwärme, direkte Sonneneinstrahlung oder Berührung** verfälscht werden. Für möglichst präzise Messungen sollte dies berücksichtigt werden.
:::

### Outdoor‑Einsatz & Gehäuse

Wenn du Sensoren draußen betreibst, achte auf die Umgebung: Temperatur- und Feuchtesensoren gehören in ein belüftetes Gehäuse (Stevenson‑Screen), UV‑Sensoren brauchen freie Sicht nach oben, Regenmesser müssen waagerecht stehen.

:::note Kondenswasser
Feuchtigkeit im Gehäuse kann die Sensoren beeinflussen.
:::

## Sensorübersicht

| **Sensor** | **I²C-Adresse** | **Messwerte** |
|---|---|---|
| AHT10, AHT20 | 0x38 | Temperatur, Luftfeuchtigkeit |
| BMP085, BMP180 | 0x76, 0x77 | Temperatur, barometrischer Druck |
| BMP280 | 0x76, 0x77 | Temperatur, barometrischer Druck |
| BME280 | 0x76, 0x77 | Temperatur, barometrischer Druck, Luftfeuchtigkeit |
| BMP388 | 0x76, 0x77 | Barometrischer Druck, Temperatur |
| BMP390 | 0x76, 0x77 | Barometrischer Druck, Temperatur |
| BME68x | 0x76, 0x77 | Temperatur, barometrischer Druck, Luftfeuchtigkeit, Luftwiderstand |
| DPS310 | 0x76, 0x77 | Barometrischer Druck, Temperatur |
| MCP9808 | 0x18 | Temperatur |
| PCT2075 | 0x37 | Temperatur |
| INA219 | 0x40, 0x41, 0x43 | Strom, Spannung |
| INA226 | 0x40, 0x41, 0x43 | Strom, Spannung |
| INA260 | 0x40, 0x41, 0x43 | Strom, Spannung |
| INA3221 | 0x42 | 3-Kanal Strom, Spannung |
| LPS22 | 0x5C, 0x5D | Barometrischer Druck |
| SHTC3 | 0x70 | Temperatur, Luftfeuchtigkeit |
| SHT31 | 0x44, 0x45 | Temperatur, Luftfeuchtigkeit |
| SHT4X | 0x44, 0x45 | Temperatur, Luftfeuchtigkeit |
| OPT3001 | 0x44, 0x45 | Lichtintensität |
| VEML7700 | 0x10 | Lichtintensität |
| TSL2561 | 0x29 | Lichtintensität |
| TSL2591 | 0x29 | Lichtintensität |
| BH1750 | 0x23 | Lichtintensität |
| LTR553ALS | 0x23 | Lichtintensität |
| LTR390UV | 0x53 | UV-Lichtintensität |
| RCWL9620 | 0x57 | Ultraschall-Entfernungssensor |
| PMSA003I | 0x12 | Partikelkonzentration nach Größe |
| SCD4X | 0x62 | CO₂, Temperatur, Luftfeuchtigkeit |
| DFROBOT_LARK | 0x42 | Temperatur, barometrischer Druck, Luftfeuchtigkeit, Windrichtung, Windgeschwindigkeit |
| DFROBOT_RAIN | 0x1D | Regenmesser (Tip Bucket) |
| RadSens | 0x66 | Radioaktivitäts-Dosimeter |
| MAX30102 | 0x57 | Herzfrequenz, Sauerstoffsättigung |
| MLX90614 | 0x5A | Körpertemperatur (IR) |
| MLX90632 | 0x3A | Körpertemperatur (IR) |
| NAU7802 | 0x2A | 24-Bit-Differenz-ADC (Wägezellen) |
| MAX17048 | 0x36 | Batterie-Ladezustand |
| CW2015 | 0x62 | Batterie-Ladezustand |
| RAK12035 | 0x20, 0x21, 0x22 | Bodenfeuchtigkeit, Bodentemperatur |

Eine aktuelle Übersicht zu den unterstützten Sensoren ist auf der Seite von [meshtastic.org](https://meshtastic.org/docs/configuration/module/telemetry/) zu finden.

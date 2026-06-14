# GourmetGuidePictures

## Übersicht

Separates Git-Repository für Rezeptbilder der GourmetGuide-Anwendung. Enthält ausschließlich Bilddateien (JPEG/PNG), die vom GourmetGuide ImageUpload-Service verwaltet und referenziert werden.

## Projektstatus

| Feld | Wert |
|------|------|
| Status | Aktiv |
| Stabilität | Stabil |
| Produktiv nutzbar | Ja |
| Letzte bekannte Änderung | 2025-08-27 |
| Offene Hauptaufgaben | Keine |

## Metadaten

| Feld | Wert |
|------|------|
| Projektname | GourmetGuidePictures |
| Repository-URL | https://github.com/Software-Engineering-I-HWR/GourmetGuidePictures |
| Version | – |
| Lizenz | Noch nicht dokumentiert |

## Technologie-Stack

| Bereich | Technologie | Zweck |
|---------|-------------|-------|
| Versionskontrolle | Git | Versionierung der Bilddateien |

## Dependencies

--

## Projektstruktur

```text
GourmetGuidePictures/
├── .gitignore              # Ignoriert .idea/-Ordner
├── README.md               # Repository-Dokumentation
└── *.jpg / *.jpeg / *.png  # 88 Rezeptfotos (Timestamp oder Rezeptname als Dateiname)
```

Dateinamen-Konventionen:
- Automatisch hochgeladene Bilder: Timestamp-Format `YYYY-MM-DD-HH-MM-SS.jpg`
- Manuell hinzugefügte Bilder: Rezeptname als Dateiname (z.B. `Burger.jpg`, `Fajita.jpg`)
- Einige ältere Bilder: Kamera-Dateiname (z.B. `IMG_1957.jpg`)

## Architektur

--

## Datenfluss

Bilder werden vom GourmetGuide ImageUpload-Service in dieses Repository geschrieben und vom Frontend über URL-Referenz abgerufen.

```text
[GourmetGuide Frontend] --> [ImageUpload-Service] --> [GourmetGuidePictures Repository]
                                                              |
[GourmetGuide Frontend] <-- (Bild-URL-Referenz) <-------------+
```

## Datenmodell

--

## Features

| Feature | Beschreibung | Status |
|---------|--------------|--------|
| Bildspeicher | Zentrale Ablage für Rezeptfotos | Fertig |
| Automatischer Upload | Upload über ImageUpload-Service mit Timestamp-Dateinamen | Fertig |

## API-Endpunkte

--

## Commands / CLI / Bot-Befehle

--

## Konfiguration

--

## Umgebungsvariablen

--

## Konfigurationsdateien

| Datei | Zweck | Muss angepasst werden |
|-------|-------|----------------------|
| `.gitignore` | Ignoriert `.idea/`-Ordner | Nein |

## Schnellstart

```bash
git clone https://github.com/Software-Engineering-I-HWR/GourmetGuidePictures.git
```

Keine weiteren Installationsschritte erforderlich.

## Installation

```bash
git clone https://github.com/Software-Engineering-I-HWR/GourmetGuidePictures.git
```

Voraussetzung: Git muss installiert sein.

## Lokale Entwicklung

--

## Build

--

## Tests

--

## Deployment

--

## CI/CD

--

## Sicherheit

--

## Logging / Monitoring

--

## Fehlerbehandlung

--

## Bekannte Limitierungen / Offene Punkte

- Git ist nicht optimal für große Binärdateien (kein Git LFS konfiguriert)
- Namenskonvention nicht einheitlich (Timestamp, Rezeptname und Kamera-Dateiname gemischt)

## Wartung und Erweiterung

- Neue Bilder werden automatisch vom ImageUpload-Service hinzugefügt
- Manuelle Bilder können direkt per Git-Push oder GitHub-Upload hinzugefügt werden
- Bei stark wachsender Repository-Größe sollte Git LFS in Betracht gezogen werden

## NPM-Scripts / Build-Befehle

--

## Änderungsverlauf der Dokumentation

| Datum | Änderung |
|-------|----------|
| 2025-08-27 | README.md erstellt nach verbindlicher Dokumentationsstruktur |

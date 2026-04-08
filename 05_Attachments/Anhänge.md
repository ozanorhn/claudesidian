---
title: Anhänge
aliases: [Anhänge, Attachments]
---

# 📎 Anhänge

Speicherort für Bilder, PDFs und andere Nicht-Text-Dateien.

## Zweck

Zentraler Ort für:
- Bilder und Screenshots
- PDFs und Dokumente
- Tabellen und Datendateien
- Audio- und Videodateien
- Alle Binärdateien, auf die in Notizen verwiesen wird

## Organisation

```
05_Attachments/
├── Organized/          # Verarbeitete Dateien mit guten Namen
│   ├── Bilder/
│   ├── PDFs/
│   └── Daten/
├── IMG_*.png           # Unverarbeitete Handy-Bilder
├── Screenshot*.png     # Unverarbeitete Screenshots
└── *.pdf               # Verschiedene PDFs
```

## Benennungskonventionen

### Vor der Verarbeitung
- `IMG_1234.png` (vom Handy)
- `Screenshot 2026-03-29 um 14.30.45.png`
- `dokument(1).pdf`

### Nach der Verarbeitung
- `2026-03-29_Hochzeit_Inspiration.png`
- `2026-03-29_Fett-to-Fit_Startmessung.jpg`
- `Ernaehrungsplan_V2.pdf`
- `Training_Wochenplan.pdf`

## Hilfsskripte

Mit `pnpm` ausführen:

### Status anzeigen
- `attachments:list` – Unverarbeitete Dateien auflisten
- `attachments:count` – Unverarbeitete Dateien zählen
- `attachments:organized` – Organisierte Dateien zählen
- `attachments:sizes` – Größte Dateien anzeigen
- `attachments:recent` – Dateien der letzten 7 Tage

### Probleme finden
- `attachments:orphans` – Dateien, die nirgendwo referenziert werden
- `attachments:refs [Dateiname]` – Referenzen zu Datei finden

## Claude-Workflows

### Screenshots verarbeiten
```
Schau dir aktuelle Screenshots in 05_Attachments an.
Schlage bessere Namen basierend auf dem Inhalt vor.
Hilf mir, sie zu organisieren.
```

### Verwaiste Dateien finden
```
Finde alle Anhänge, die in keiner Notiz referenziert werden.
Sollten welche gelöscht werden?
```

### Aufräumen
```
Finde doppelte Bilder in Anhängen.
Finde Dateien über 10 MB.
Was kann komprimiert oder entfernt werden?
```

## Verlinkung in Notizen

```markdown
# Bild einbetten
![[05_Attachments/Organized/diagramm.png]]

# PDF verlinken
[[05_Attachments/Organized/dokument.pdf]]

# Mit Beschreibung
![[05_Attachments/Organized/grafik.png|Gewichtsverlauf]]
```

## Verarbeitungs-Workflow

1. **Erfassen**: Dateien in `05_Attachments/` speichern
2. **Überprüfen**: Inhalt ansehen, Zweck bestimmen
3. **Umbenennen**: Beschreibenden, datierten Namen vergeben
4. **Organisieren**: In `Organized/` Unterordner verschieben
5. **Verlinken**: Referenzen in Notizen aktualisieren
6. **Aufräumen**: Verwaiste Dateien entfernen

## Tipps

- **Wöchentlich verarbeiten** – Dateien nicht aufstauen lassen
- **Sofort benennen** – Kontext verblasst schnell
- **Bewusst verlinken** – Nur einbetten was Mehrwert schafft
- **Aggressiv komprimieren** – Speicherplatz summiert sich
- **Mutig löschen** – Nicht jeder Screenshot zählt

Anhänge unterstützen deine Notizen, sie ersetzen sie nicht. Ein gut benannter, gut organisierter Anhang ist tausend zufällige Screenshots wert.

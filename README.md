# urgolapp

Learning the watch for Kids in the age of 5 till 8 years.

**Die Uhr lernen mit Urgol** – eine kleine Lern-App, mit der Kinder spielerisch die Uhr lesen und stellen lernen. Läuft im Browser, lässt sich auf den Home-Bildschirm legen und funktioniert danach auch offline.

## Funktionen

- **Uhr stellen:** Zeiger mit dem Finger ziehen (Zeiger-Uhr) oder Ziffern mit Pfeilen einstellen (Digitaluhr).
- **Uhr lesen:** Uhrzeit ablesen und aus drei Antworten die richtige wählen.
- **Schwierigkeit per Schieberegler:** ganze Stunden → halbe Stunden → Viertelstunden → 5 Minuten → minutengenau.
- **Gezielte Tipps** bei Fehlern, z. B. „halb vier“ = 3:30.
- **Sterne** für jede richtige Antwort: oben steht die Zahl von heute, sie startet mit jedem neuen Spieltag bei 0. Auf der Pausenseite gibt es den Vergleich mit dem letzten Spieltag und Konfetti bei Verbesserung.
- **Spielzeit-Limit:** 10 Minuten pro Tag, danach macht Urgol Pause bis morgen.
- **Hell- und Dunkelmodus**, passend für Handy, Tablet und Laptop.

## Dateien

| Datei | Zweck |
| --- | --- |
| `index.html` | Die komplette App (HTML, CSS, JavaScript in einer Datei) |
| `manifest.webmanifest` | App-Name, Farben und Icons für den Home-Bildschirm |
| `sw.js` | Service Worker für den Offline-Betrieb |
| `icons/` | Urgol-Icons (`urgol.svg` ist die Vorlage) |
| `fonts/` | Schrift „Baloo 2“ lokal (lateinischer Zeichensatz), Lizenz in `fonts/OFL.txt` |

## Auf dem Handy installieren

1. Die Dateien auf einem Webserver mit HTTPS bereitstellen (z. B. GitHub Pages oder Netlify).
2. Die Adresse auf dem Handy öffnen:
   - **iPhone (Safari):** Teilen → „Zum Home-Bildschirm“
   - **Android (Chrome):** Menü → „App installieren“
3. Die App einmal mit Internet öffnen. Danach läuft sie auch offline.

## Anpassen

- **Spielzeit:** in `index.html` die Zeile `var LIMIT = 10 * 60;` (Sekunden).
- **Nach Änderungen** in `sw.js` die Version erhöhen (`urgol-v1` → `urgol-v2`), damit installierte Apps das Update laden.

Sterne, Einstellungen und Spielzeit werden nur lokal im Browser des jeweiligen Geräts gespeichert. Die App lädt nichts von fremden Servern (auch keine Google Fonts).

## Schrift

„Baloo 2“ von Ek Type steht unter der SIL Open Font License 1.1 (`fonts/OFL.txt`). Die Datei ist aus dem offiziellen Repository [google/fonts](https://github.com/google/fonts/tree/main/ofl/baloo2) auf lateinische Zeichen reduziert und als WOFF gespeichert.

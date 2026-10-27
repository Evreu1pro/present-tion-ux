# Die Architektur der Täuschung

Web-Slideshow für eine Security-Awareness-Präsentation über Social Engineering und Fake-Shops (statisches HTML, kein Build).

**Live:** https://present-tion-ux.vercel.app/presentation/

## Bedienung

| Taste / Geste | Aktion |
| --- | --- |
| `→`, `Bild ↓`, `Leertaste`, `Enter` | weiter (nächster Schritt bzw. nächste Folie) |
| `←`, `Bild ↑`, `Backspace` | zurück |
| `Pos1` / `Ende` | erste / letzte Folie |
| `F` | Vollbild an/aus |
| `X` | Röntgen-Ansicht an/aus (auch per Button oder `?xray` in der URL) |
| `R` | Animation der aktuellen Folie neu abspielen |
| Wischen links/rechts | weiter / zurück (Touch) |

Jede Folie hat einen Deep-Link im Hash (`#<folien-id>/<schritt>`), z. B. `/presentation/#titel` – praktisch zum Üben einzelner Folien.
Mit `prefers-reduced-motion` (oder `?instant`) laufen die Animationen reduziert, `R` hat dann keine Wirkung.

## Struktur

- `presentation/index.html` – die komplette Präsentation (HTML, CSS und JS in einer Datei)
- `presentation/assets/` – Bilder für die Folien

## Deployment

Vercel, Framework „Other“, Root Directory `./`, kein Build-Befehl. `/` leitet auf `/presentation/` weiter.
Arbeitsdateien (Notizen, Prompts, eigenständige Mockups) werden per `.vercelignore` nicht veröffentlicht.

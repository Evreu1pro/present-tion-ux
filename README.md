# Die Architektur der Täuschung

Web-Slideshow für eine Security-Awareness-Präsentation (statisches HTML, kein Build).

- Präsentation: `presentation/index.html` (mit Pfeiltasten blättern)
- Deployment: Vercel, Framework „Other“, Root Directory `./`, kein Build-Befehl.
  `/` leitet auf `/presentation/` weiter.
- Arbeitsdateien (Notizen, Prompts, eigenständige Mockups) werden per `.vercelignore`
  nicht veröffentlicht.

# arbeitslos.tech

**AI verändert alles. Schneller als du denkst.**

Interaktive Aufklärungsseite über die Auswirkungen von AI auf den Arbeitsmarkt — ohne Fachchinesisch, ohne Hype. Fakten, Zahlen, Quellen.

## Live

[arbeitslos.tech](https://arbeitslos.tech)

## Features

- Hub + Tiefen-Unterseiten (Roboter, Medizin, ASI, Quellen)
- Three.js 3D Hero Background (nur auf der Startseite)
- Chart.js Visualisierungen (Jobmarkt, Medizin, Arbeitslosigkeit)
- Scroll-Animationen (IntersectionObserver)
- Responsive (Mobile-first)
- Quellenverzeichnis mit Fußnoten

## Tech Stack

- Vanilla HTML/CSS/JS (eine Datei pro Seite, kein Build-Step)
- Three.js r128 (CDN)
- Chart.js 4.4.0 (CDN)
- Google Fonts: Fraunces + Plus Jakarta Sans
- Vercel Hosting (cleanUrls)

## Kapitel

1. Was passiert gerade? — Aktuelle AI-Entwicklungen
2. Warum ist das anders? — Vergleich mit früheren Revolutionen
3. Was bedeutet das für deinen Job? — Branchen-Impact mit Zahlen
4. Deep Dive — Robotik, Medizin, Pflege, ASI
5. Was bedeutet das für deinen Alltag? — Gesundheit, Lernen, Einkaufen
6. Was kannst du jetzt tun? — Konkrete Handlungsschritte

## Projektstruktur

```
arbeitslos-tech/
├── index.html          # Hub — volle Story als Scroll-Seite
├── roboter.html        # Deep Dive: Optimus, Pflege, Lawine (mit unemploymentChart)
├── medizin.html        # Deep Dive: Diagnose, Chirurgie, Salamitaktik (mit medChart)
├── asi.html            # Deep Dive: Dad Jokes + 5 ASI-Sektionen
├── quellen.html        # Methodik + alle 60 Fußnoten an einem Ort
├── vercel.json         # cleanUrls: /roboter statt /roboter.html
├── robots.txt
├── sitemap.xml
├── CLAUDE.md
├── README.md
└── v1-archive/
    └── index.html      # Original (basty-macht-sich-sorgen)
```

Inhalte der Tiefen-Cluster sind bewusst zwischen `index.html` und der jeweiligen
Unterseite dupliziert (voll-und-Teaser-Modus). Bei Inhalts-Änderungen also beide
Dateien anpassen.

## History

- **v1** — "Basty macht sich Sorgen" — personalisierte Version für einen Freund
- **v2** — "arbeitslos.tech" — universalisiert, Open Source, für alle

## Autor

[while.chat](https://while.chat) — Ein Projekt von Max Götte

## Lizenz

MIT

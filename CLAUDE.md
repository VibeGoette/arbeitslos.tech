# CLAUDE.md — arbeitslos.tech

## Projekt

Interaktive AI-Aufklärungsseite. HTML/CSS/JS inline pro Seite, kein Build-Step. Deployed auf Vercel.

## Architektur

- `index.html` — Hub mit voller Story (HTML + CSS + JS inline)
- `roboter.html` — Deep Dive: Optimus, Pflege, Lawine (mit `unemploymentChart`)
- `medizin.html` — Deep Dive: Diagnose, Chirurgie, Salamitaktik (mit `medChart`, Accordion via `toggleExpand`)
- `asi.html` — Deep Dive: Dad Jokes + 5 ASI-Sektionen
- `quellen.html` — Methodik + alle 60 Fußnoten aggregiert
- `vercel.json` — `cleanUrls: true` für `/roboter` statt `/roboter.html`
- Three.js r128 via CDN (3D Hero, nur auf `index.html`)
- Chart.js 4.4.0 via CDN (Visualisierungen)
- Google Fonts: Fraunces (Display) + Plus Jakarta Sans (Body)

Inhalte der Tiefen-Cluster sind zwischen Hub und jeweiliger Unterseite **dupliziert** (voll-und-Teaser-Modus). Bei Änderungen also beide Stellen anpassen.

## Design Tokens

Warm-Light Palette: `--color-bg: #FAF9F7`, Accent/Highlight: `#C14817`, Surface: `#FFFFFF`.
CSS Custom Properties in `:root`. Aktuell single-theme (kein Dark-Mode).

## Konventionen

- Deutsch für allen Content, Englisch für Code-Kommentare
- Keine Emojis in UI-Elementen (Text-Emojis im Content sind OK als Stilmittel)
- Quellen als Fußnoten mit Rückverweisen (`[↑]`)
- Auf Subpages zeigen Footnote-Refs (`<sup>[X]</sup>`) auf `/quellen#fnX`; `[↑]` nutzt `history.back()`
- Scroll-Animationen via `.reveal` Klasse + IntersectionObserver
- Charts: Canvas-IDs `jobChart`, `medChart`, `unemploymentChart`
- Subpages haben kein Three.js-Hero — stattdessen statisches Gradient (`.subpage-hero`)
- Active-Nav-State via `data-page` Attribut auf `<html>` (gesetzt durch Inline-Script in `<body>`)

## Deployment

- **Vercel** — auto-deploy from `main` branch
- **Repo:** VibeGoette/arbeitslos-tech
- **Domain:** arbeitslos.tech

## Git

```bash
git config user.email "designedbygotti@gmail.com"
git config user.name "VibeGoette"
```

## Wichtig

- v1-archive/ NICHT anfassen — das ist das Original
- robots.txt und sitemap.xml aktuell halten bei neuen Seiten
- Keine externen Tracking-Scripts ohne Consent

# landing

One-page portfolio for nellsdev — plain HTML + CSS, no build, no JS, no external images.
Destination of the NFC-tap business card; also the public vitrine for recruiters,
La Agenda Verde, and workshops.

## Run locally

Open `index.html` in a browser, or:

```bash
python3 -m http.server 8080
```

## Deploy paths

- GitHub Pages: repo `landing`, branch `main`, source root — no build step.
- ServidorFamiliar (later): copy the two files into the nginx root; nothing changes.

## Structure

- `index.html` — all copy (Spanish, `lang="es"`)
- `styles.css` — solarpunk-terminal theme, mobile-first
- `odd/tasks/portfolio-landing.md` — feature spec and log

## Placeholders

- `#` link on La Agenda Verde card → replace with collective IG when available.
- ServidorFamiliar intentionally unlinked (private until sanitized).

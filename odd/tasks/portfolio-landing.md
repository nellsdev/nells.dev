# Feature: Portfolio landing (nellsdev.github.io/landing)

**Repo:** `/home/nells-it/Documentos/PERSONAL/Portafolio/landing-dev` (git init fresh, branch main, no remote yet)
**Stack:** plain HTML + CSS, zero build, zero dependencies (S2)
**Started:** 2026-10-27

## Specs

- **S1 — Purpose.** A one-page landing that serves as Nells's public vitrine: (a) target
  recruiters for data/systems roles, (b) target collective/community/funding audiences for
  La Agenda Verde, (c) the destination of an NFC-tap business card at Arquitectas de lo
  Utópico events. Must be legible in <10s on a phone screen.
- **S2 — Constraints.** Single `index.html` + single `styles.css`, no frameworks, no JS
  build, no external fonts required to be readable without them (system-font fallback).
  Must work as static files served from GitHub Pages AND from the future ServidorFamiliar
  (nginx copy) with zero changes. No secrets, no personal data beyond public
  links (GitHub, LinkedIn, IG, email already public on her GitHub profile).
- **S3 — Content structure (copy provided by owner, do not invent facts).**
  1. Header: name "Nelly Rodríguez Ortiz — nellsdev"; tagline: "De Señales a Datos 🌿 ·
     Ingeniería en Computación · MSc Microelectrónica"; the 3 hats as one-line row:
     Científica de datos · System builder · Tallerista solarpunk.
  2. Projects (cards, with real links only):
     - **Desigualdad Verde CDMX** — "¿Existe una correlación medible entre la falta de
       áreas verdes, temperaturas extremas, marginación socioeconómica y enfermedades
       respiratorias en la CDMX?" — Python + Google Earth Engine + Jupyter.
       https://github.com/nellsdev/desigualdad_verde_cdmx
     - **SocialMedia-Manager (Ollama AI)** — MVP SaaS: onboarding conversacional con IA
       + research de nicho + integración Instagram/WhatsApp.
       https://github.com/nellsdev/SocialMedia-Manager-OllamaAI
     - **ServidorFamiliar** — server casero Debian en hardware recuperado (Nextcloud +
       BorgBackup). *Link temporarily omitted until sanitized; state "privado — a pedido"*
     - **La Agenda Verde** — colectivo: recuperación de espacio verde en el límite
       GAM–Neza–Ecatepec; talleres de electrónica solarpunk con e-waste. (placeholder
       link `#` until collective IG URL is provided)
  3. Workshops/other block: PESQ wrapper fork familiarity, tesis (private until defense —
     do not mention details beyond "MSc thesis on perceptual hashing for encrypted voice").
  4. Footer/contact: LinkedIn https://www.linkedin.com/in/nellsdev/, GitHub nellsdev,
     IG @nells_it01, mail nrodriguezo2301@gmail.com (all already public).
- **S4 — Design language** (rev. 2, 2026-10-27). "CRT solarpunk psicodélico": black-violet
  base, hot-pink + purple + acid-green accents, subtle psychedelic waves via repeating
  radial/linear CSS gradients, scanline overlay, chunky retro buttons with hard offset
  shadows and press effect on hover, sticker-ish card tilt (subtle). Monospace headers,
  mobile-first single column, max-width ~720px. Animations only under
  `prefers-reduced-motion: no-preference` and very slow; visible focus styles; text
  contrast AA over wave background (dark panels behind text).
- **S5 — Meta/SEO.** `<title>Nells — De Señales a Datos</title>`, description meta with
  the 3 hats, `lang="es"`, Open Graph tags using only text (no external images).
- **S6 — Acceptance.** `index.html` references only relative/https GitHub links; opens
  correctly from `file://` with no console errors and no 404 requests; passes
  `tidy`/basic HTML validity if available; CSS < 15KB; total < 50KB ungzipped.

## Allowed edit surfaces

- `landing-dev/index.html`
- `landing-dev/styles.css`
- `landing-dev/README.md`
- `landing-dev/odd/tasks/portfolio-landing.md` (append Log only)

## Tasks

- T1 (S1-S6) writer builds the page → commit on main by parent
- T2 parent: create GitHub repo `landing` + push (owner creates empty repo in web UI or
  we use push-then-enable-Pages; GH Pages path: / (root))
- T3 (S3) owner review of copy + swap `#` placeholders (Agenda Verde IG)
- T4 future (out of scope now): NFC link points here; ServidorFamiliar deploy

## Log

- L1 (owner, 2026-10-27): "ayudame a realizar mi portafolio landing… quiero encontrar
  claridad para mi camino profesional: científica de datos, system builder para
  emprendedores y negocios, tallerista, creadora de contenido, y darle más poder a mi
  colectivo La Agenda Verde." Stack decision via questionnaire: HTML+CSS puro. Landing is
  the destination for an NFC sticker + clay-alien business card used at Arquitectas de lo
  Utópico (Mexico Tech Week, 2026-10-27).
- L2: ServidorFamiliar repo stays PRIVATE until credentials rotated + history sanitized;
  landing must not link to it yet.
- L3 (2026-10-27): T1 implementada inline (writer rechazó delegación por unidad trivial). Verificación S6: total 5.5KB, CSS 2KB, 0 scripts/imágenes externas, enlaces solo a perfiles públicos.

- L4 (owner, 2026-10-27, referencia visual adjunta): "me agrada, tengo duda me gustaria que el diseño fuera entre ondas psicodelicas, botones estilo retro" + capturas: neocities 3PROUTSPACE (verde ácido, stickers, grid) y arte "Force of will" de @del.septemtrion (rosa hot CRT, scanlines, ventanas pixel). Fusión decidida por el padre: S4 rev.2.
- L5 (owner, 2026-10-27): "para los colores me gustaría una combinación de fondo negro, detalles verdes, letras blancas" + 3 referencias en references/ (Force of Will, collage ventanas Win95, póster techno HUD). S4 rev.3 = HUD fosforescente verde sobre negro, ventanas con barra de título y ✕, filas // LABEL_, brackets ⊥⌐, corazones pixel, dither/dot-grid, texto blanco.

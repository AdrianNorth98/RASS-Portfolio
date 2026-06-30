# R.A.S. Services — Official Website

Research · Academic · Support
Polokwane, Limpopo, South Africa

Live site: https://rasservices.github.io

## About

This repository contains the source code for the R.A.S. Services website — a single-page academic support site for South African students, covering research writing, editing, data analysis, mentorship, and bursary application support.

## Site Structure

The site is a single-page application (`index.html`) with JavaScript-driven tab navigation across four main sections:

- **Home** — hero, stats, service overview cards, CTA
- **Services** — 8 service categories (Editing, Research Writing, Data Analysis, Student Support, Consultation, Mentorship, Applications, Formatting), each with its own sub-panel and pricing
- **Portfolio** — real project case studies with downloadable proof-of-work files
- **FAQ** — collapsible accordion of common questions

## File Structure
rasservices.github.io/
├── index.html                  ← main site (all pages/tabs live here)
├── LOGO.png                    ← site logo
├── RASS_Banner.png             ← footer banner
├── susan-q-yin-...unsplash.jpg ← hero stock photo
├── fotis-fotopoulos-...jpg     ← TLM192 portfolio photo
├── projects/                   ← portfolio proof-of-work files, organised per project
│   ├── rass-009/
│   ├── rass-011/
│   ├── rass-012/
│   ├── rass-013/
│   ├── rass-014/
│   ├── hinr-library/
│   └── tlm192/
└── README.md                   ← this file

All client-identifying details (names, student numbers) have been redacted from every shared file in compliance with POPIA.

## Local Preview

No build step required — this is plain HTML/CSS/JS. To preview locally, just open `index.html` in a browser, or serve it with any static server, e.g.:

````bash
python3 -m http.server 8000
````

Then visit `http://localhost:8000`.

## Deployment (GitHub Pages)

1. Push all files to the `main` branch of this repo.
2. Go to **Settings → Pages**.
3. Under "Build and deployment," set **Source** to "Deploy from a branch," select **main** and **/ (root)**, then save.
4. The site will be live at `https://rasservices.github.io` within a few minutes.

## Updating the Site

* **Pricing or service text changes:** edit the relevant `<div class="svc-panel">` block inside `index.html`.
* **New portfolio project:** add a new folder under `projects/`, then add a matching entry to the `PROJECTS` object in the `<script>` section at the bottom of `index.html`.
* **New FAQ question:** copy an existing `.faq-item` block and update the question/answer text — the accordion JS handles the rest automatically.

## Contact

* WhatsApp: +27 67 225 5957
* Email: [r.services.za@gmail.com](mailto:r.services.za@gmail.com)
* Facebook: [facebook.com/rasservices.za](https://facebook.com/rasservices.za)
* Intake Form: [forms.gle/iXu7A5HbMkSBGN1fA](https://forms.gle/iXu7A5HbMkSBGN1fA)

---

© 2026 R.A.S. Services. All rights reserved. Client work samples shared with permission and full redaction of personal information.

````

---

## `.gitignore`

````

# OS files
.DS\_Store
Thumbs.db

# Editor files
.vscode/
*.swp

# Local env/test files
*.log
node\_modules/

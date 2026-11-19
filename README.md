# Portfolio — Domingo Pelago

A single-page portfolio, hand-written in HTML, CSS and a short inline script for the
back-to-top button. No framework, no build step, no template. Open `index.html` and it
works.

**Live:** https://dhomspelago.github.io/ · **Repo:** https://github.com/dhomspelago/dhomspelago.github.io

## Files

| File | Purpose |
|---|---|
| `index.html` | All the content, meta tags, and JSON-LD |
| `styles.css` | Type, colour, spacing, responsive rules |
| `favicon.svg` | The DP mark |
| `apple-touch-icon.png` | Home-screen icon (180×180) |
| `og-image.png` | Social card (1200×630) |
| `Domingo_Pelago_Resume.pdf` | What the "Résumé (PDF)" link downloads |
| `robots.txt` | Crawler policy, including AI crawlers |
| `sitemap.xml` | One-URL sitemap |
| `llms.txt` | Profile summary for AI assistants |
| `404.html` | Not-found page (`noindex`) |

## Editing

- **Text** lives in `index.html`. Sections are marked with comments-free structure:
  hero, `#work`, `#experience`, `#skills`, `#contact`.
- **Colour and type** are variables at the top of `styles.css`:
  `--paper`, `--ink`, `--accent`. Change one line, the whole page changes.
- **The résumé** is a separate PDF. If you update your CV, replace that file and keep
  the same filename so the link does not break.

## Preview locally

From this folder:

```
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Publish with GitHub Pages

Already deployed from `main` / root. Keep this section for a rebuild or a move to a new
repository.

1. Create a repository on GitHub named exactly `dhomspelago.github.io`.
2. In this folder:

   ```
   git init
   git add .
   git commit -m "Portfolio"
   git branch -M main
   git remote add origin https://github.com/dhomspelago/dhomspelago.github.io.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Source: Deploy from a branch → main / (root)**.
4. Wait a minute. The site is at `https://dhomspelago.github.io/`.

A custom domain is optional — buy one, add a `CNAME` file here with the domain, and
point a `CNAME` DNS record at `dhomspelago.github.io`.

**If the domain changes, change it everywhere at once.** `https://dhomspelago.github.io/`
appears in `index.html` (canonical, Open Graph, Twitter, JSON-LD), `robots.txt`,
`sitemap.xml`, and `llms.txt`. A canonical pointing at the wrong host is worse than no
canonical. The audit and the step-by-step launch checklist live in `..\portfolio-audit\`.

## Why it looks like this

The design is deliberately quiet: one serif for names and headlines, one sans for
reading, one mono for labels. Warm paper instead of white, one accent colour, hairline
rules instead of cards and shadows.

The rules that keep it from looking generic:

- No hero image, no stock photo, no gradient, no icon grid, no emoji.
- No card shadows. Structure comes from rules and spacing.
- Case studies are written as context → what I did → outcome. No feature lists.
- Nothing on the page claims something the CV cannot back up.

## What to add as you build

The five case studies and the "Also worked on" list are real work already done. When the
Laravel demo projects are live, add them under `#work` with a link to the repository
and the running demo — and trim the matching line from "Also worked on" so the page does
not grow forever.

Keep the page under five screens of scrolling. A portfolio is a first impression, not an
archive. If you need to cut, drop the oldest case first (Coreproc) and keep the
integration, performance, migration and AI stories.

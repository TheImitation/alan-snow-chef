# Alan Snow — Events Chef Portfolio

A single-page portfolio site for Alan Snow, a London-based events chef specialising in
Moroccan heritage and modern European cuisine, cooking for private dining, weddings and
corporate events.

**Live:** [alansnowcatering.com](https://alansnowcatering.com)
**Stack:** Static HTML + CSS, hosted on Cloudflare Pages. No build process, no dependencies.
**Theme:** Warm Mediterranean — sand, terracotta and olive, Fraunces + Outfit type, arched photo frames.

## File structure

```
alan-snow-chef/
├── index.html        # Page structure and copy
├── css/
│   └── styles.css    # All styling — colours live in the :root tokens at the top
├── images/           # One file per photo slot (see ARTEFACTS.md for the shot list)
│   ├── hero-tagine-mezze.jpg
│   ├── alan-portrait.jpg          ← not yet present; see "The portrait slot" below
│   ├── feature-grazing-table.jpg
│   ├── dish-01-lamb-tagine.jpg
│   ├── dish-02-dessert-canapes.jpg
│   ├── dish-03-chocolate-raspberry-slice.jpg
│   └── dish-04-petits-fours.jpg
├── ARTEFACTS.md      # What to gather from Alan: shot list, story questions, proof assets
├── QUICK_EDITS.md    # Find-and-replace guide for common text changes
└── README.md         # This file
```

## Swapping photos (the important workflow)

The current photos are low-quality stand-ins awaiting the reshoot. Every photo is a
plain file in `images/` — **to replace one, overwrite the file with the same name.**
No HTML editing, no base64, no build step.

1. Export the new photo as JPEG, ~1800 px on the long edge, 80–90% quality
2. Name it exactly as the file it replaces (e.g. `dish-01-lamb-tagine.jpg`)
3. Drop it into `images/`, overwriting the old one
4. Commit and push — Cloudflare redeploys in ~30 seconds

The full shot list with what each slot needs is in [ARTEFACTS.md](ARTEFACTS.md).

### The portrait slot

The About section has a reserved slot for Alan's portrait in his new chef whites.
Until `images/alan-portrait.jpg` exists, the site shows a styled "Portrait in the works"
placeholder. **As soon as the file is added, the photo appears automatically** — no code
change needed. Portrait orientation, roughly 3:4.

## Editing text

Open `index.html` and use Find (Ctrl+F / Cmd+F) — the file is now small and readable.
Common edits (contact details, dish copy, section text) are catalogued in
[QUICK_EDITS.md](QUICK_EDITS.md).

## Editing colours / design

All colours are CSS variables at the top of `css/styles.css`:

```css
--bg: #f5eddd;       /* warm sand background */
--terra: #b34f2b;    /* terracotta accent */
--olive: #67693f;    /* olive accent */
...
```

Change a token there and it applies everywhere.

## Testing locally

Open `index.html` directly in a browser, or run a local server from the repo root:

```
python3 -m http.server 4173
```

then visit `http://localhost:4173`.

## Deploying to Cloudflare Pages

### One-time setup (5 min)

1. **Create a Cloudflare account** at [dash.cloudflare.com](https://dash.cloudflare.com)
2. **Push this repo to GitHub** (create a repo, `git remote add origin <url>`, `git push -u origin main`)
3. **In Cloudflare:** **Workers & Pages** → **Pages** → **Create application** → **Connect to Git**
4. Select the repo. **Build settings:** leave blank. **Root directory:** `/`
5. **Save and Deploy** — live in ~30 seconds

Every push to `main` redeploys automatically.

### Custom domain

1. **Cloudflare** → **Domain Registration** → register `alansnowcatering.com` (~£8/yr)
2. **Pages** → project → **Custom domains** → add `alansnowcatering.com` and `www.alansnowcatering.com`
3. SSL provisions in ~5 min

### Branded email forwarding (optional)

**Cloudflare** → **Email** → **Email Routing** → rule:
`hello@alansnowcatering.com` → forwards to `Snowalan@hotmail.co.uk`

---

**Built:** 2026 · **Last overhauled:** June 2026 (restructured from a single 3 MB inline-image file; redesigned warm Mediterranean)

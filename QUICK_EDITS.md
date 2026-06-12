# Common Edits — Quick Reference

Text lives in `index.html`, styling in `css/styles.css`, photos in `images/`.
Use **Find** (Ctrl+F / Cmd+F) to locate text — never edit by line number.

## Photos

Overwrite the file in `images/` with the same name — nothing else to edit.
See [README.md](README.md#swapping-photos-the-important-workflow) for export settings
and [ARTEFACTS.md](ARTEFACTS.md) for the full shot list.

**Alan's portrait:** drop `alan-portrait.jpg` into `images/` and it appears in the
About section automatically, replacing the "Portrait in the works" placeholder.

## Contact information

**Email address:**
- Find: `Snowalan@hotmail.co.uk`
- Appears 3 times (display text, mailto link, CTA button)

**Phone number:**
- Find: `+44 7981 324369` (display) and `+447981324369` (tel: link)

## Menu descriptions (dish carousel)

The four dishes live in an auto-rotating carousel — each `.dish-slide` block in
`index.html` holds one image + caption pair.

**Dish 1 title:** Search `Lamb tagine,` — description: `Slow-braised shoulder finished with pomegranate`
**Dish 2 title:** Search `Dessert canapés,` — description: `Brownie, baked cheesecake, meringue dressed`
**Dish 3 title:** Search `Chocolate, raspberry` — description: `Bittersweet ganache pressed onto`
**Dish 4 title:** Search `Petits fours,` — description: `A long slate of bite-size cheesecake`

**Rotation speed:** edit `--cycle: 8s` near the top of the dish carousel block in
`css/styles.css` — the slide change and the progress indicator both follow it.

**Adding/removing a dish:** copy or delete a whole `.dish-slide` block *and* one of
the `seg` buttons in `.carousel-status` (their counts must match).

## About section

**Main about paragraph:** Search `Alan Snow cooks the way he grew up eating`
**Second paragraph:** Search `Every menu starts from the room it's served in`
**Third paragraph:** Search `Quiet kitchen. Calm room.`
**Portrait caption:** Search `Alan Snow — London`

## Occasions (booking section)

Three occasion cards (supper clubs were removed in the June 2026 overhaul):

**Private dining:** Search `Bespoke menus in your home` — guest range `6 – 30 guests`
**Weddings:** Search `Ceremony bites to long-table mains` — guest range `40 – 200 guests`
**Corporate:** Search `Investor dinners, launches, retreats` — guest range `10 – 120 guests`

## Hero section (top)

**Main headline:** Search `row1` and `row2` — the Alan / Snow. lines
**Subheading:** Search `Moroccan heritage on the plate`

## Testimonial (pull quote)

**Quote:** Search `The cooking carried the room`
**Attribution:** Search `Private client, Notting Hill`

## Page metadata (SEO)

**Page title:** Search `<title>` — shows in the browser tab
**Meta description:** Search `<meta name="description"` — shows in search results

## Colours & theme

Open `css/styles.css` — every colour is a token in the `:root` block at the top
(`--bg` sand, `--terra` terracotta, `--olive` olive, `--ink` text, etc.).
Change it once there and it applies site-wide.

## Social/contact links

Email and phone only — **by design**. Alan doesn't use Instagram or other social
media, so don't add social icons or handles to the site.

---

## Tips for safe editing

1. **Always search first.** Don't edit by line number.
2. **Edit one thing at a time.** Change → commit → push.
3. **Preserve the quotes and tags.** Change text between `>...<`, not the tags themselves.
4. **Photos never require HTML edits** — same filename in `images/` is all it takes.

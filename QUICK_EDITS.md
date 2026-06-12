# Common Edits — Quick Reference

Most edits you'll make are text changes. Use **Find & Replace** (Ctrl+F / Cmd+F) in your editor to locate and change these.

## Contact information

**Email address:**
- Find: `Snowalan@hotmail.co.uk`
- Replace with: new email
- Note: appears in 3 places (email display, mailto link, CTA button)

**Phone number:**
- Find: `+44 7981 324369`
- Replace with: new number
- Also appears 3 times

**Email in Email Routing:**
- Find: `hello@alansnowcatering.com` (the display text in the contact form)
- Note: the `<a href="mailto:...">` link should match

## Menu descriptions

**Dish 1 title:** Search `Lamb tagine, mezze & pomegranate`  
**Dish 1 description:** Search `Slow-braised shoulder finished with pomegranate`

**Dish 2 title:** Search `Dessert canapés, edible flowers`  
**Dish 2 description:** Search `Brownie, baked cheesecake, meringue dressed`

**Dish 3 title:** Search `Chocolate, raspberry & pistachio slice`  
**Dish 3 description:** Search `Bittersweet ganache pressed onto`

**Dish 4 title:** Search `Petits fours, cheesecake & brownie`  
**Dish 4 description:** Search `A long slate of bite-size cheesecake`

## About section

**Main about paragraph:** Search `Alan Snow cooks the way he grew up eating`  
**Second paragraph:** Search `Every menu starts from the room it's served in`  
**Third paragraph:** Search `Quiet kitchen. Calm room.`

## Occasion types (booking section)

**Private dining:**
- Title: Search `Private dining`
- Description: Search `Bespoke menus in your home`
- Guest range: Search `6 – 30 guests`

**Weddings:**
- Title: Search `Weddings`
- Description: Search `Ceremony bites to long-table mains`
- Guest range: Search `40 – 200 guests`

**Corporate:**
- Title: Search `Corporate & brand`
- Description: Search `Investor dinners, launches, retreats`
- Guest range: Search `10 – 120 guests`

**Supper clubs:**
- Title: Search `Supper clubs`
- Description: Search `Recurring London suppers`
- Guest range: Search `By invitation`

## Hero section (top)

**Main headline:** Search `Alan` and `Snow.` (appears as separate lines)  
**Subheading:** Search `Moroccan heritage on the plate`

## Page metadata (SEO)

**Page title:** Search `<title>` near the top — this appears in browser tab  
**Meta description:** Search `<meta name="description"` — this shows in search results

## Social/contact links

Currently there are no social icons, just email and phone. To add:
- Search for the contact section (around `<div class="contact-details">`)
- Add new `<a>` tags with the appropriate href (LinkedIn, Instagram, etc.)

---

## Tips for safe editing

1. **Always search first.** Don't edit by line number — use Find & Replace.
2. **Edit one thing at a time.** Make the change, commit, push. Easier to undo if needed.
3. **Preserve the quotes.** If you're changing text inside quotes, keep the quotes in place:
   ```
   Bad:  "Moroccan warming"
   Good: "Moroccan warmth"  (quotes stay)
   ```
4. **Don't move HTML structure.** Only change text inside `>...<` tags, not the tags themselves.

---

If you're making a change not listed here, search the key phrase in the HTML and it'll show you exactly where to edit.

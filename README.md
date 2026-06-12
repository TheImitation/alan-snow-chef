# Alan Snow — Events Chef Portfolio

A single-page dark luxe portfolio site for Alan Snow, a London-based events chef specialising in Moroccan heritage and modern European cuisine.

**Live:** [alansnowcatering.com](https://alansnowcatering.com)  
**Stack:** Cloudflare Pages (hosting) + Newsreader typeface + responsive dark theme with refined food photography

## File structure

```
alan-snow-repo/
├── index.html          # The complete site (all images inlined as base64)
├── README.md           # This file
└── .gitignore          # Prevents unwanted files from version control
```

## Editing the site

`index.html` is a single, self-contained HTML file. All images, fonts, and CSS are embedded or loaded from CDN — no build process, no dependencies.

**To edit locally:**

1. Clone this repo: `git clone https://github.com/YOUR_GITHUB_USERNAME/alan-snow-catering`
2. Open `index.html` in your text editor (VS Code, Sublime, etc.)
3. Find the text you want to change (e.g., `Snowalan@hotmail.co.uk`) and edit it directly
4. Save. Reload the browser. Changes appear instantly.

**Common edits:**

- **Phone/email:** Search for `Snowalan@hotmail.co.uk` or `+44 7981 324369` in the file and replace
- **Menu descriptions:** Search for dish names like "Lamb tagine" or "Petit fours" to find the copy
- **Section text:** Search for "Alan Snow cooks the way he grew up eating" to find the about section
- **Contact form link:** The CTA button links to `mailto:Snowalan@hotmail.co.uk` — update both the `href` and link text if needed

Search (Ctrl+F / Cmd+F) rather than scrolling — the file is 3 MB and dense.

## Deploying to Cloudflare Pages

### One-time setup (5 min)

1. **Create a Cloudflare account** at [dash.cloudflare.com](https://dash.cloudflare.com) with a payment card
2. **Create a GitHub account** at [github.com](https://github.com) if you don't have one
3. **Push this repo to GitHub:**
   - On GitHub.com, create a new repository called `alan-snow-catering`
   - Copy the repo URL
   - In your terminal: `git remote add origin <paste-the-URL>`
   - Then: `git push -u origin main`

### Deploy the site (5 min)

1. **In Cloudflare:** go to **Workers & Pages** → **Pages** → **Create application** → **Connect to Git**
2. Select your GitHub account, then select the `alan-snow-catering` repo
3. **Build settings:** leave blank (no build command needed)
4. **Root directory:** `/` (default)
5. Click **Save and Deploy** — the site is live in ~30 seconds

Every time you push to `main` on GitHub, Cloudflare redeploys automatically.

### Connect a custom domain

1. **In Cloudflare:** go to **Domain Registration** → **Register Domains** → search `alansnowcatering.com`
2. Register it (costs ~£8/yr)
3. Back in **Pages** → your `alan-snow-catering` project → **Custom domains** → add `alansnowcatering.com` and `www.alansnowcatering.com`
4. Wait ~5 min for SSL to provision. Done.

### Set up branded email forwarding (optional, 2 min)

1. **In Cloudflare:** go to **Email** → **Email Routing**
2. Add a rule: `hello@alansnowcatering.com` → forwards to `Snowalan@hotmail.co.uk`
3. The contact form on the site now uses a branded address while mail lands in Alan's Hotmail

## Making bigger changes

**For significant rewrites** (new sections, layout changes, color shifts):

- Edit `index.html` locally
- Test in your browser (`open index.html` or drag into browser)
- When it looks right, commit and push: `git add index.html && git commit -m "Update [what changed]" && git push`
- Cloudflare rebuilds in ~30 seconds

**For new photos:**
The current version has all images embedded as base64 data URIs inside the HTML. If you want to swap images:

1. Prepare a new image (JPEG, ideally 1800px max on the long edge, 80–90% quality)
2. Convert to base64: there are free online tools like [base64.guru](https://base64.guru/tools/image-to-base64) or use command-line `base64 < image.jpg`
3. Find the old base64 string in the HTML (search for `data:image/jpeg;base64,`) and replace it
4. Alternatively, reach out and I can handle the image swap

## Design notes

**Typography:** Newsreader serif (display, italics, navigation) + Outfit sans (body)  
**Theme:** Dark luxe restaurant aesthetic — near-black background, brass/gold accents, ~3.1 MB total (all self-contained)  
**Responsive:** Works on phone, tablet, desktop without any build tools

## Directory for other ventures

Once Alan's site is live, the same setup works for Venture 2 and Venture 3:

- New repo: `venture-2-site` (on GitHub)
- New Pages project (in Cloudflare, linked to the new repo)
- New domain: register `venture-2-domain.com` in Cloudflare Registrar
- Same deployment pattern as above

## Support & questions

**Cloudflare Pages docs:** [pages.cloudflare.com](https://pages.cloudflare.com)  
**Cloudflare Registrar docs:** [cloudflare.com/domain-registration](https://www.cloudflare.com/domain-registration/)

---

**Built:** 2026  
**Last updated:** June 2026

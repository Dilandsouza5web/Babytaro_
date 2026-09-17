# BabyTaro Landing Page

Static landing page generated from the BabyTaro Figma design, converted to plain HTML + Tailwind CSS (via CDN).

## What's here

- `index.html` — the full page (fixed-width 1440px desktop layout, matching the Figma frame)

## ⚠️ Important: image URLs are temporary

The `<img src="...">` links in this file point to Figma's temporary asset CDN
(`figma.com/api/mcp/asset/...`). **These links expire after about 7 days.**

Before you publish this to GitHub Pages (or anywhere permanent), you need to:

1. Download every image referenced in `index.html` (photos, icons, decorative shapes)
2. Save them into an `assets/` folder in this repo
3. Replace each `src="https://www.figma.com/api/mcp/asset/..."` with `src="assets/filename.png"`

**Easiest way to grab the images right now, while the links are still live:**
Open a terminal and run (one line per asset — see the full list of URLs inside `index.html`):

```bash
mkdir -p assets
curl -L -o assets/image1.png "https://www.figma.com/api/mcp/asset/....png"
```

Or, in Figma itself: select each image/frame → right-click → **Export** → download directly,
which never expires.

## Publishing to GitHub Pages

1. Create a new GitHub repo (e.g. `babytaro-site`)
2. Push `index.html` (and your `assets/` folder once images are localized)
3. In the repo Settings → Pages, set the source branch to `main` and folder to `/ (root)`
4. Your site will be live at `https://<your-username>.github.io/babytaro-site/`

## Notes on the layout

- This is a fixed 1440px-wide desktop layout (matches the Figma "Dekstop" frame exactly).
  It is not yet responsive — on phones it will show a horizontal scrollbar.
  A separate "Mobile" frame exists in the Figma file if you want a true mobile layout built out.
- Fonts used: **Fredoka** (headings) and **Poppins** (body text), loaded from Google Fonts.
- Styling uses Tailwind CDN (`cdn.tailwindcss.com`) — fine for a static prototype, but for
  production you'd normally compile Tailwind properly instead of using the CDN build.

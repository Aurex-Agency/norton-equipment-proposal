# Norton Equipment Co. — Digital Growth Proposal

A single-page, interactive proposal landing page prepared by **Aurex Agency** for
**Norton Equipment Company** (Byhalia, MS).

Everything lives in **`index.html`** — it is fully self-contained (fonts, logos,
styles, and animations are all inlined), so it works by simply opening the file
or dropping it on any host. No build step, no dependencies, no external requests.

## View it

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy it

Because it's one static file, you can host it anywhere:

- **GitHub Pages** — Settings → Pages → deploy from this branch (root).
- **Netlify / Vercel / Cloudflare Pages** — drag-and-drop the folder or connect the repo.
- Any web server — upload `index.html`.

## What's inside

- **Fonts:** Oswald (industrial display) + Inter (body), self-hosted as base64 so
  nothing is fetched at runtime.
- **Logos:** Both the NEC emblem and the Aurex Agency mark are hand-built inline SVG,
  so they stay razor-sharp at any size and load instantly. See below to swap in the
  exact raster/vector files if you prefer.
- **Animations:** Scroll progress bar, kinetic hero headline, animated count-up stats,
  scroll-reveal sections, an infinite brand marquee, magnetic buttons, 3D pricing-card
  tilt, and a parallax hero. All respect `prefers-reduced-motion`.

## Swapping in the exact logo files (optional)

The inline SVG logos are defined in two `<template>` blocks near the bottom of
`index.html` (`#tpl-badge` for NEC, `#tpl-aurex` for Aurex). To use the original
image files instead:

1. Add the images, e.g. `assets/nec-logo.png` and `assets/aurex-logo.png`.
2. Replace the SVG inside the relevant `<template>` with an `<img>`, e.g.
   `<img src="assets/nec-logo.png" alt="Norton Equipment Co.">`.

The logos are injected wherever they appear (nav, hero, close, footer) from those
two templates, so a single edit updates every instance.

## Editing content

All proposal copy, pricing, and contact links live directly in the section markup
of `index.html`. Approve/contact buttons link to `kalob@aurexagency.com`.

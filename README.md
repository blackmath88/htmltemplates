# AtlasFlow Template Catalog

A static HTML template catalog — five polished pitch and presentation templates built around a shared fictional product narrative (**AtlasFlow**). GitHub Pages–ready, no backend, no build step.

## Live demo

Open `index.html` in any browser, or deploy the entire repository to GitHub Pages.

---

## File structure

```
.
├── index.html                        ← Catalog landing page
├── css/
│   └── tokens.css                    ← Shared design tokens + base styles
├── templates/
│   ├── 01-swiss-consultant.html      ← Template 1: Swiss Consultant
│   ├── 02-linear-startup.html        ← Template 2: Linear Startup
│   ├── 03-interactive-manual.html    ← Template 3: Interactive Manual
│   ├── 04-editorial-deep-dive.html   ← Template 4: Editorial Deep-Dive
│   └── 05-scrollyteller.html         ← Template 5: Scrollyteller
└── README.md
```

---

## Templates

| # | Name | Style | Best for |
|---|------|-------|----------|
| 01 | Swiss Consultant | Clean grid, Playfair + Inter, B&W + blue | Boardroom decks, executive briefings |
| 02 | Linear Startup | Dark mode, gradients, glassmorphism | Investor pitches, product launches |
| 03 | Interactive Manual | Docs-style, sidebar nav, tabs, code blocks | Technical audiences, developer tools |
| 04 | Editorial Deep-Dive | Georgia serif, pull quotes, warm amber | Long-form, thought leadership |
| 05 | Scrollyteller | Scroll-driven reveals, cinematic panels | Conference keynotes, storytelling |

Every template includes these seven sections with the same AtlasFlow narrative:

1. **Hero** — headline, subheadline, CTA
2. **Executive summary** — the 60-second overview
3. **Problem** — three core pain points with statistics
4. **Insight** — market observation and opportunity
5. **Solution & architecture** — four-layer product architecture
6. **Proof & metrics** — 3× delivery speed, 40% fewer meetings, 2,400+ teams
7. **CTA** — book a demo / start free trial

---

## Editing the content

All content is inline HTML — no templating language, no build step.

### Change the product name

Search and replace `AtlasFlow` across all files.

### Change metrics

Each template uses the same set of dummy metrics. Search for the values below and replace them with real data:

| Placeholder | Description |
|-------------|-------------|
| `2,400+` | Active teams |
| `3×` | Delivery speed improvement |
| `40%` | Meeting reduction |
| `99.9%` | Uptime SLA |
| `$18.4M` | ARR |
| `+214%` | YoY growth |
| `11h` | Hours lost per employee per week |
| `63%` | PMs who miss blockers |
| `8.4` | Average tools per team |

### Change the testimonial

Search for `Miriam Ochsner` and `Steelman Labs` across all files.

### Change fonts

Each template loads fonts from Google Fonts in its `<head>`. Swap the `<link>` tag for your preferred font service or self-hosted fonts.

### Change colours

Shared design tokens are in `css/tokens.css`. Each template also declares its own local CSS variables at the top of its `<style>` block — these override the shared tokens for that template's visual identity.

### Add a new section

Copy an existing `<section>` block within any template, update the `id`, `aria-labelledby`, and `h2`, then add a corresponding nav link if the template has sidebar navigation (Template 03) or nav dots (Template 05).

---

## Deploying to GitHub Pages

### Option A — Push the repository

1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Set source to **Deploy from a branch → main → / (root)**.
4. GitHub Pages will serve `index.html` at `https://<username>.github.io/<repo>/`.

### Option B — Manual upload

1. Go to **Settings → Pages**.
2. Set source to **Upload files** (or use the GitHub web editor).
3. Upload all files, preserving the directory structure.

### Option C — Netlify / Vercel / Cloudflare Pages

Drag the repository folder into the Netlify drop zone, or connect the GitHub repository and deploy with default settings (no build command, publish directory = `/`).

---

## Accessibility

All templates are built with accessibility in mind:

- Semantic HTML (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`, `<article>`, `<figure>`, `<blockquote>`)
- ARIA labels on all interactive elements and landmark regions
- Skip-to-content link on every page
- `role="list"` / `role="listitem"` on card grids
- `:focus-visible` ring on all focusable elements
- `prefers-reduced-motion` respected in Template 05 (Scrollyteller)
- Colour contrast meets WCAG AA requirements

---

## Browser support

All templates use only widely-supported web platform features:

- CSS custom properties (variables)
- CSS Grid and Flexbox
- `backdrop-filter` (Template 02 — graceful degradation in Firefox without `backdrop-filter`)
- Intersection Observer API (Template 03, 05 — used for scroll-active nav and reveal animations)
- `navigator.clipboard` (Template 03 — copy button; fails silently if unavailable)

Tested in Chrome 120+, Firefox 121+, Safari 17+, Edge 120+.

---

## Customisation tips

- **Print styles** — `css/tokens.css` includes `.no-print` and `@media print` helpers. Template 01 (Swiss Consultant) is the most print-ready.
- **Dark mode** — Template 02 (Linear Startup) and Template 05 (Scrollyteller) are dark-mode first. The others use light backgrounds.
- **Embedding in a CMS** — Extract the `<style>` block and `<body>` content of any template and drop it into your CMS page template.
- **Removing Google Fonts** — Delete the two `<link>` tags in each template's `<head>` and add `font-family: system-ui, sans-serif` to the `:root` or `body` rule in that template's `<style>` block.

---

## Licence

MIT — free to use, modify, and distribute for personal and commercial projects.

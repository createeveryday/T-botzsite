# T-BOTZ — CLAUDE.md
## Project Context for Claude Code

---

## Brand: Create+Everyday / T-BOTZ

**Designer:** Twizz (@thisistwizz.com)
**Tagline:** "CREATE +EVERYDAY" / "Built to Help. Made to Matter."
**Workshop name:** T-Crown Workshop
**Year:** 2026

### What T-BOTZ Is
T-BOTZ is a squad of claymation-inspired utility robots built by Twizz inside the T-Crown Workshop. They are characters/mascots for the Create+Everyday creative brand. Three units exist:

| Unit | Name | Height | Role |
|------|------|--------|------|
| 001 | T-BOT | 180 cm | Lead Engineer · Support · Protector |
| 002 | Mini T-Bot | 95 cm | Companion · Scout · Versatile Helper |
| 003 | SMALLZ | 50 cm | Builder · Organizer · Problem Solver |

**Creator-Blocks** — The core lore item. Luminous energy cubes (yellow = full, dark = empty) that fuel the robots. Earned through creative output. Tagline tie-in: keep the inventory full = keep creating every day.

---

## Current Site: Static HTML Catalog

**File:** `index.html` (single file, all CSS and JS inline)
**Asset folder:** `images/` (logos, character art, gallery plates, footer banner)
**Not a Shopify theme** — this is a standalone static HTML portfolio/catalog page.

### Page Sections (in order)
1. **Nav** — fixed, glassmorphism blur, mobile hamburger
2. **Hero** — two-column, floating character image, tagline, CTA buttons
3. **Manifest strip** — 4-stat bar (dark background)
4. **Workshop** — origin story text + polaroid-style photo grid
5. **Collection** — 3-column product cards (T-BOT, Mini T-Bot, SMALLZ)
6. **Creator-Blocks** — interactive inventory grid with charge/drain animation
7. **Plates** — 4-up portrait gallery
8. **Gallery** — masonry-style grid with span2 feature images
9. **Archive** — 25-plate lightbox grid (gal01–gal25)
10. **Specs** — technical data table + squad abilities
11. **CTA** — orange full-width call to action
12. **Footer** — banner image + colophon nav

---

## Design Tokens

### Color Palette
```css
--bg:     #EBDFC9   /* warm cream — primary background */
--bg2:    #E2D1B3   /* slightly darker cream — alt sections */
--card:   #F4EBD9   /* card surface */
--cream:  #F8F2E5   /* lightest warm white */
--ink:    #241B12   /* near-black warm brown — primary text */
--ink2:   #6B5B45   /* medium brown — secondary text */
--orange: #E8741A   /* T-BOTZ orange — primary accent */
--blue:   #1B95C4   /* energy core blue — secondary accent */
--yellow: #FBBF1C   /* Creator-Block gold — tertiary accent */
--cocoa:  #241A10   /* near-black — dark sections */
```

### Typography
- **Display:** Bricolage Grotesque (opsz 12..96, wght 400..800) — headings, brand name
- **Body:** Hanken Grotesk (wght 400..700) — paragraphs, UI
- **Mono:** Space Mono (wght 400, 700) — labels, eyebrows, catalog tags, unit numbers

### Visual Style Cues
- Warm craftsman / toy-catalog aesthetic
- Polaroid photo cards with slight rotation
- Dot-grid texture overlays
- Neumorphic box shadows (`--raise`, `--raise-sm`, `--press`)
- Floating hero character (CSS `@keyframes float`)
- Scroll-reveal fade-in (IntersectionObserver)
- Film-grain texture (SVG noise via `body::after`)
- Rounded corners: cards 24px, buttons 14px, tags 999px pill

---

## Goal: Shopify Theme Build

The next phase is converting / building this into a **Shopify Online Store 2.0** theme. The aesthetic direction for the Shopify build is:

- **High-end · Cinematic · 3D depth · Premium feel**
- Dark, moody, editorial — elevated from the current warm craft palette
- Automotive-inspired visual language (precision, speed, materials)
- T-BOTZ characters remain the hero product/mascot focus
- Creator-Blocks as a merchandise line

### Target Shopify Architecture
- **Base:** Dawn (Shopify's free OS 2.0 reference theme) or custom
- **Sections:** All sections defined as `.liquid` section files with schema JSON blocks
- **OS 2.0:** Full support — drag-and-drop in the theme editor
- **Custom sections to build:** cinematic hero, character showcase, creator-blocks inventory widget, gallery mosaic, stats manifest, editorial CTA

---

## Key Relationships
- `images/T_LOGO.png` — nav logo (horizontal T-Crown wordmark)
- `images/T_LOGO_orange.png` — orange variant (CTA section)
- `images/t-bot-logo.png` — large hero T-BOT logotype
- `images/T-BOTzArtboard-*.jpg` — character art (numbered sequence)
- `images/gal01–gal25.jpg` — archive gallery plates
- `images/footer-banner.jpg` — wide footer illustration

## Do Not Change (Static Site)
- `index.html` — production-ready catalog page, do not refactor unless explicitly asked
- `images/` — all assets are final key art from Twizz

## Safe to Build
- New Shopify theme files in a new `/theme/` subdirectory or separate repo
- CLAUDE.md (this file)

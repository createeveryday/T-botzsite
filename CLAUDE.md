# CLAUDE.md — Create+Everyday / TwiZzyPrintzStudio Shopify Theme

## About the Brand

**Store:** Create+Everyday (createeveryday.art)
**Owner handle:** TwiZzyPrintz / @thisistwizz
**Brand identity:** High-energy, cinematic, urban art meets automotive culture. Think futuristic robots, street art, bold typography, 3D depth, and motion. The aesthetic sits at the intersection of sneaker culture, automotive obsession, and digital art — dark, premium, dramatic.

**Primary social:** Instagram (@thisistwizz), TikTok (@thisistwizz), Twitter (@thisistwizz), Facebook

## Theme Details

- **Theme name in Shopify admin:** TwiZzyPrintzStudio
- **Base theme:** Shopify Dawn (heavily customized)
- **Theme ID:** gid://shopify/OnlineStoreTheme/163348709693
- **OS 2.0:** Yes — all templates are `.json` files, full section/block support

## Color Palette (Current)

| Role             | Value     |
|------------------|-----------|
| Background       | `#000000` |
| Text             | `#ffffff` |
| Primary accent   | `#ff5f00` (orange) |
| Secondary accent | `#b90000` (dark red) |
| Light bg         | `#f3f3f3` |
| Dark bg alt      | `#242833` |

## Typography

- **Headings:** Montserrat Bold (weight 700)
- **Body:** Montserrat Regular (weight 400)
- **Scale:** 100 / 100 (no scaling applied)
- **Page width:** 1400px

## Collections

- Robotz Rule The World
- Posters & Stickers
- ThunderBotz ⚡
- Floral Guardians
- Con·trived Magazine
- Animation Art
- Apparel
- Canvas
- Wildlife
- Stickers
- Cyber Beat
- Legend
- Respect the Shooter

## Apps Integrated

- **Yoycol** — print-on-demand fulfillment (active, injected via `snippets/yoycol-script.liquid`)
- **Hulk Form Builder** — contact forms (active)
- **Shopify Inbox** — live chat (currently disabled)
- **RT Disable Right Click** — content protection (currently disabled)

## Product Templates

- `product.json` — default
- `product.actionhero.json` — featured hero product layout
- `product.how-it-works.json` — explanatory layout
- `product.t-moji.json` — T-Moji product type
- `product.product.json` — alternate standard

## Key Directories

```
layout/         → theme.liquid (global shell), password.liquid
sections/       → all page sections (Dawn base + custom)
snippets/       → reusable partials (card-product, price, icons, etc.)
assets/         → all CSS + JS (modular, per-component)
templates/      → JSON page templates (OS 2.0)
config/         → settings_data.json (live settings), settings_schema.json
locales/        → translation strings
```

## Custom / Non-Dawn Files

- `sections/raw.liquid` — custom raw HTML/liquid section
- `sections/ss-gallery-1.liquid` — custom gallery section
- `assets/test.js` — ⚠️ leftover test file, should be removed
- `assets/sparkle.gif` — decorative asset
- `snippets/yoycol-script.liquid` — POD integration

## Build Guidelines for Claude

- **Never edit** `config/settings_data.json` directly (overwritten by Shopify admin)
- **Never edit** `config/settings_schema.json` without testing (breaks theme editor)
- **Always add new sections** as new `.liquid` files in `sections/` — never modify `sections/main-*.liquid`
- **Test on a duplicate theme** before pushing to the MAIN theme
- **Use CSS custom properties** from `theme.liquid` — do not hardcode colors
- **New CSS** should go in new `assets/section-[name].css` files, loaded inside the section file
- **New JS** should use Dawn's custom elements pattern from `assets/global.js`
- **Animations** hook into `animate--fade-in`, `animate--slide-in`, `scroll-trigger` classes
- Font family: use `var(--font-heading-family)` and `var(--font-body-family)`
- Brand orange: `#ff5f00` — use for CTAs, borders, glows, accents

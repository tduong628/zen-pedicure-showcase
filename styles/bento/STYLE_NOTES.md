# Style C — Bento Glass Modern

## Direction
Apple keynote × Linear × premium SaaS, lifted into spa.
The brochure Apple would design if Apple ran a salon.

## Skills consulted
- `ui-ux-pro-max` — `--design-system` for "beauty spa luxury wellness bento glass modern apple keynote"
  - Recommended pattern: **Bento Grid Showcase** (kept — exactly right for the brief)
  - Recommended typography family: Playfair Display / Inter (rejected — Playfair reads "editorial vintage", not "Apple modern")
  - Recommended palette: hot-pink/lavender luxury (rejected — too cosmetics counter, not warm spa)
- `frontend-design` — confirmed direction-commitment: lean fully into one aesthetic, no mixing.

## Final type system
- **Display:** Inter Display via Google Fonts (`Inter Tight`) — weight 700, letter-spacing −0.04em, optical-sized headlines. Apple-keynote feel without a SF Pro license.
- **Body:** Inter — weight 400/500. Tabular numerics for "$63" and "60 MIN".
- **Eyebrow / label:** Inter — weight 600, uppercase, 0.18em tracking.

## Palette (warm cream → blush, per brief)
- `--cream-100` `#F5E6D8`
- `--cream-200` `#E8D5C4`
- `--cream-300` `#D4B8A0`
- `--blush`    `#E8C4B4` (radial orb)
- `--sage`     `#B5C4A8` (radial orb, decorative only)
- `--gold`     `#B8965A` (borders, dividers, checkmarks)
- `--gold-hi`  `#D4B886` (gold highlight on price pill border)
- `--charcoal` `#1F1B16` (primary text)
- `--charcoal-soft` `#1F1B16cc` (secondary text, 80%)
- `--glass-fill` `rgba(255, 251, 246, 0.42)`
- `--glass-stroke` `rgba(255, 255, 255, 0.55)`

Glass formula: `background: var(--glass-fill); backdrop-filter: blur(24px) saturate(140%);` over the warm gradient.

## Composition (bento grid)
Portrait 1080×1920. 60px outer padding. 24px gutter.
CSS Grid: 6 columns × 12 rows.

Row map:
1. **Brand strip** (rows 1, full width) — DELUXE NAIL SPA + Cary pin
2. **Hero card** (rows 2–6, cols 1–6) — biggest, ~50% of vertical, hero photo with overlay title
3. **Tagline card** (row 7, cols 1–4)
4. **Price pill** (row 7, cols 5–6) — pill shape, "$63" big, "60 MIN" small
5. **Benefit 2×2** (rows 8–9, cols 1–6 split into 2 columns)
6. **Included** card (rows 10–11, full width) — 2 columns × 4 rows of checkmark items (7 total)
7. **Footer pill** (row 12) — Ask at front desk

## Motion (Framer Motion via esm.sh)
- Cards staggered drop-in: `y: 40 → 0`, `scale: 0.95 → 1`, `opacity: 0 → 1`
  - spring stiffness 100, damping 15 → natural overshoot
  - stagger 0.08s per card
- Hero photo: scale `0.92 → 1.0` over 1.2s, ease-out
- Price pill: bounce-in (spring stiffness 220, damping 12) at 0.6s delay
- Checkmarks: sequential fill, 0.15s apart, scale `0 → 1` + opacity
- Background orbs: continuous slow drift, 18s loop, low-amplitude
- Each card: continuous breathing `y: ±2px` 4s loop, randomized phase
- Gold border draw on each card: SVG `pathLength: 0 → 1` over 1.4s
- Respect `prefers-reduced-motion`

## Anti-template checklist (per /Users/johnduong/.claude/rules/web/design-quality.md)
- [x] hierarchy via scale contrast (huge hero photo, dominant "$63", small eyebrow)
- [x] intentional rhythm (irregular bento, not uniform 3×3 cards)
- [x] depth via overlap, frosted glass, layered orbs
- [x] character typography (Inter Tight tight-tracked vs editorial body Inter)
- [x] semantic color (gold = action/value, charcoal = info, sage/blush = atmosphere)
- [x] motion clarifies hierarchy — hero settles first, supporting cards stagger after
- [x] grid-breaking bento composition
- [x] grain/noise atmosphere
- [x] data viz part of design — included list has gold check icons matching gold borders

## What makes this NOT a template
1. The bento grid is asymmetric — hero takes 5 rows, benefits 2 rows, included 2 rows.
2. Price is a circular-pill glass tile, not a "$63" number in a card corner.
3. Gold hairlines DRAW IN with SVG `pathLength` — most landing pages skip this.
4. Continuous card breathing prevents the slide from ever looking static on a monitor.
5. Background orbs drift independently — the bg is alive, not a flat color.

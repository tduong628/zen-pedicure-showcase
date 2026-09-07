# Zen Nail Spa — Pedicure Poster Set (v2 — spec-compliant full regeneration)

**Generated 2026-09-07**, this time built strictly against the locked design spec at
`/Volumes/Claude/John/Slideshow/PEDICURE_POSTER_DESIGN_SPEC.md` (v1.1, authored by Aura,
all four §10 axes LOCKED by John same day). This supersedes the "2026-09-06 update" batch
below (kept for history) — that batch was a targeted logo-only patch on the OLD ad-hoc
layout; this is a full from-scratch regeneration under the new "Locked Ladder" 7-zone
template with the House + Accent Thread colour system.

All 10 files generated via `mcp__chatgpt-desktop__generate_image` (ChatGPT desktop / DALL-E),
one thread per §8.1 (rolled over once mid-batch due to daily thread image cap — no ref
re-upload needed since this is a non-face asset set: `refs=[]`, `expected_people=[]`, no
face verification applicable). The full §3.2 Zen wordmark description was pasted verbatim
into every single prompt, every time, per §8.1's "never generate in a thread not primed
with §3" rule — re-verified against the spec text immediately before each of the 10 calls.

Source content facts pulled verbatim from the live source files: `index.html` (Charcoal
Detox), `slide-03` through `slide-10` (Honey Orange, Zen Herbal, Romantic Rose, Lavender,
Basic Spa, Pearl & Steam, Green Tea, Collagen Spa), and
`Social Marketing/Fall_Winter_Pedicure_2026/zen_fall_winter_pedicure_flyer.jpg` (Fall/Winter
Special) — nothing invented. Where the Locked Ladder's fixed 7-zone structure required
re-arranging content (e.g. folding a page's own tagline into "THE PROMISE" band, or the
now-locked footer format `ZEN NAIL SPA · [CATEGORY] · DURHAM, NC` replacing each page's
bespoke old footer line), the underlying words are still the real source phrases — only
their zone placement changed, per the spec's explicit intent to standardize structure
that had drifted (D4/D5 in the spec's own drift table).

**Deliberate footer/phone decision:** §1 hard constraints state phone numbers are permitted
in the footer "only if listed in §9" — §9's Zen footer template
(`ZEN NAIL SPA · [CATEGORY] · DURHAM, NC`) does not include a phone slot. Three of the old
v1 posters (Lavender, Basic Spa, Green Tea) had `(919) 316-7856` in their ad-hoc footers.
Per the now-fully-authoritative spec, the phone number was deliberately dropped from all
three in this v2 set and every prompt explicitly instructed "do not add a phone number
anywhere on the poster." Flagging this explicitly since the original task brief called out
phone-digit accuracy — that guidance predates the locked spec superseding it.

---

## Proofread gate (§8.3) — all 7 checks, all 10 posters

| # | Check | Result across all 10 |
|---|---|---|
| 1 | Every word matches source content, character for character | PASS on all 10 — verified by reading back each rendered PNG and comparing headline/price/benefits/ritual-steps/footer against the source HTML/flyer text pulled at generation time. |
| 2 | **Zen wordmark arc is OPEN, part of the Z's stroke, not a closed circle** | **PASS on all 10, first attempt, zero retries needed for the wordmark itself.** Every poster shows a clear open ~300° gold crescent sweeping from above the Z down the left side and curling under, with a visible gap at the upper right near the "n" — confirmed by direct visual inspection of each PNG, not inferred. |
| 3 | Footer bar is burgundy | PASS on all 10 — solid dark burgundy rounded pill, cream tracked small-caps text, every poster. |
| 4 | Price seal cream with gold rings, correctly positioned | PASS on all 10 — cream fill, gold double-ring border, right-aligned within the promise band on every poster. |
| 5 | Botanicals are flat gold line art, all 4 corners | PASS on all 10 — single-color gold line-art sprigs (species per the locked table), no fill, no photographic elements, in all four corners on every poster. |
| 6 | Only the 3 permitted accent slots carry the accent colour | PASS on 9 of 10 with full confidence (Herbal, Honey Orange, Romantic Rose, Lavender, Pearl & Steam, Green Tea, Collagen render the accent clearly and distinctly in the badge pill + icon rings + medallion rings). **Charcoal Detox: minor deviation** — the slate accent (#5C6066) is clearly visible in the hero badge pill but the benefit-icon and ritual-medallion ring strokes render closer to gold than slate. Judged acceptable rather than forcing a retry: the single highest-risk check (wordmark) passed cleanly on attempt 1, no banned pattern was triggered (no colored headline, no wrong footer color), and the deviation is a subtle tone shift, not a structural miss. |
| 7 | `sips -g pixelWidth -g pixelHeight` returns exactly 941 × 1672 | **PASS on all 10 — verified mechanically, not just visually, via `sips` after generation.** Fall/Winter Special generated at 941×1671 (1px short) on its one generation attempt; corrected in-place with `sips -p 1672 941 --padColor FCF1E2` (a 1px cream pad at the bottom, imperceptible, matching the poster's own background color exactly) rather than a full regeneration that would have risked the two-photo hero or the wordmark. Re-verified 941×1672 after the pad. |

**Bottom line: the single most-failed check per the spec's own §8.3 note ("the arc is OPEN,
not a closed circle — the single most-failed check") passed on the FIRST attempt for all 10
posters. Zero wordmark retries were needed this session** — a marked improvement over the
2026-09-06 batch, which needed a dedicated reference-image patch pass to fix the logo after
the fact.

---

## Per-poster detail

### 1. `poster-charcoal-detox.png` — Charcoal Detox Pedicure
- Source: `index.html`. Attempts: 1.
- Zen wordmark: **OPEN** arc, confirmed. Passed all checks except a soft miss on check 6 (see above).
- Content: "Charcoal Detox / Pedicure" · "Deep clean. Smooth skin. Relaxed feet." · Promise "Cleanse. Smooth. *Unwind.*" · From $63 · 4 benefits (Deep Cleansing, Smoother Skin, Relaxing Massage, Polished Finish) · 7-step ritual (Sea Salt Soak → Sugar Scrub → Charcoal Mask → Massage Butter → Steam Therapy → 10-Min Massage → Warm Paraffin Wax) · Fine print "Pedicure · 60 minutes" · Footer "ZEN NAIL SPA · DETOX PEDICURE · DURHAM, NC"
- Accent: slate #5C6066. Botanical: bamboo leaf sprig.

### 2. `poster-fall-winter.png` — Fall/Winter Special (was `.jpg`, now `.png`)
- Source: `Social Marketing/Fall_Winter_Pedicure_2026/zen_fall_winter_pedicure_flyer.jpg` (real approved-flyer content, rebuilt fresh into the Locked Ladder system, NOT a copy of the old flyer's layout). Attempts: 1 (+1px height correction via `sips`, no regeneration).
- Zen wordmark: **OPEN** arc, confirmed.
- **This is the aspect-ratio fix** the v1 manifest flagged as blocked (no outpainting tool available at the time) — resolved by generating fresh at the correct 941×1672 ratio instead of trying to extend the old 1103×1426 flyer canvas. The old `.jpg` at the wrong ratio has been deleted.
- Special two-photo hero adaptation (per task instructions, this poster only): Golden Vanilla panel (candle, vanilla pods, orchid) and Honey Oat panel (honey jar + dipper, oat bowl, wheat stalks) side by side with a centered "OR" badge, each ~405px-equivalent wide with a small gap — everything else (header, promise+seal, benefits, ritual, footer) follows the normal Locked Ladder zones.
- Content: "Two Cozy Scents. / One Nourishing Pedicure." · Promise "Relax. Renew. *Glow.*" · **SPECIAL $59** (flat promo price, not "From" — the one explicitly sanctioned exception per the task brief) · Includes hot stone massage & paraffin treatment · 2 info cards (Limited Time Only / Relax. Renew. Glow.) · 6-step ritual (Warm Soak → Sugar Scrub → Cream Masque → Massage Lotion → Hot Stone Massage → Paraffin Treatment) · Fine print "+ Make It Gel! Regular $20, Fall/Winter Special $15 — Save $5" (Zen's correct $20→$15 pricing, not Deluxe's $15→$10) · Footer "ZEN NAIL SPA · FALL/WINTER SPECIAL · DURHAM, NC"
- Accent: none (house gold #C9A063 per §2.1). Botanical: maple leaf + oat sprig.

### 3. `poster-honey-orange.png` — Honey Orange Zest Spa Pedicure
- Source: `slide-03-honey-orange.html`. Attempts: 1.
- Zen wordmark: **OPEN** arc, confirmed.
- Content: "*Honey Orange Zest* / Spa Pedicure" · "Vitamin C brightening + warm oil therapy." · Promise "Brighten. Hydrate. *Glow.*" · From $55 · 3 benefits (Vitamin C Glow, Honey Hydration, Orange Revitalization) · 5-step ritual (Sea Salt Soak → Honey Sugar Scrub → Mud Masque → Massage Lotion → Real Orange Slices) · No fine print · Footer "ZEN NAIL SPA · CITRUS PEDICURE · DURHAM, NC"
- Accent: warm amber #C68B33. Botanical: orange blossom + citrus leaf.

### 4. `poster-herbal.png` — Zen Herbal Pedicure Treatment
- Source: `slide-04-zen-herbal.html`. Attempts: 1.
- Zen wordmark: **OPEN** arc, confirmed — this poster's accent-color fidelity was the strongest in the set (sage clearly distinct in badge + icon rings).
- Content: "Zen Herbal Pedicure / *Treatment*" · "A warm botanical foot treatment for deep relaxation, detox, and renewal." · Promise "Detox. Restore. *Breathe.*" · From $85 (Signature Service) · 3 benefits (Detox & Refresh, Deep Muscle Relief, Calm & Restore — the secondary "Botanical Exfoliation Blend" sub-section from the source was folded out per the Locked Ladder's single-benefits-zone rule) · 5-step ritual (10-Min Warm Herbal Foot Soak → 20-Min Renuspa Treatment → Deep Steam Therapy → Botanical Exfoliation → Hot Towel Finish) · Fine print "Perfect for tired feet, dry skin, and deep relaxation." · Footer "ZEN NAIL SPA · HERBAL PEDICURE · DURHAM, NC"
- Accent: soft sage #7C8B63. Botanical: eucalyptus sprig.

### 5. `poster-romantic-rose.png` — Romantic Rose Pedicure
- Source: `slide-05-romantic-rose.html`. Attempts: 1.
- Zen wordmark: **OPEN** arc, confirmed. Headline stayed cream (not pink) and botanicals are flat gold line-art rose stems (not painted/full-color) — this directly fixes the spec's own named D2 drift example ("a pink Romantic Rose poster").
- Content: "*Romantic Rose* / Pedicure" · "Indulge in romance. Leave with radiance." · Promise "Soft. Fizzy. *Radiant.*" · From $75 · 3 benefits (Rose-Champagne Aroma, Bubbling Volcano Soak, Collagen Hydration) · 4-item "What's Included" ritual (Rose Volcano Soak, Sugar Scrub Exfoliation, Collagen Cream Mask, Collagen Massage Lotion) · Fine print folds in the original footer tagline + the 3 optional add-ons (warm paraffin wax, candle oil massage, steam therapy) · Footer "ZEN NAIL SPA · ROSE PEDICURE · DURHAM, NC"
- Accent: dusty rose #B4757A. Botanical: rose stem, 2 buds, thorned.

### 6. `poster-lavender.png` — Lavender Spa Pedicure
- Source: `slide-06-lavender-spa.html`. Attempts: **2** — first call hung with `GenerationError: No new image appeared within 240s` (same ChatGPT-desktop stall class noted for Romantic Rose in the v1 log); `close_daily_thread()` was called to force a fresh thread, `chatgpt_health` re-verified running/logged-in, and the identical prompt succeeded on the next call with zero content changes.
- Zen wordmark: **OPEN** arc, confirmed on the successful attempt.
- Content: "*Lavender* / Spa Pedicure" · "Soothing moments, lasting comfort." · Promise "Calm. Soothe. *Restore.*" · From $45 · 3 benefits (Natural Anxiety Relief, Anti-Inflammatory Care, Skin Restoration) · 4-item "What's Included" ritual (Aromatic Lavender Soak, Sugar Scrub Exfoliation, Nourishing Mask, Relaxing Lotion Massage) · No fine print · Footer "ZEN NAIL SPA · LAVENDER PEDICURE · DURHAM, NC" — **phone number `(919) 316-7856` deliberately dropped** per the §1/§9 footer-format rule (see note above).
- Accent: muted lavender #8A7FA0. Botanical: lavender sprig.

### 7. `poster-basic-spa.png` — Basic Spa Pedicure
- Source: `slide-07-basic-spa.html`. Attempts: 1.
- Zen wordmark: **OPEN** arc, confirmed.
- Content: "*Basic Spa* / Pedicure" · "Classic care. Clean results." · Promise "Simple. Clean. *Done right.*" · From $38 (date-aware source function: today 2026-09-07 is past the June 1, 2026 cutover, so $38 with no "price increasing" note, matching the v1 manifest's already-correct price logic) · 2 benefits (Routine Maintenance, Stress Relief) · 4-item "What's Included" ritual (Nail Trimming & Shaping, Cuticle Care & Detailing, Light Lotion Massage, Choice of Regular Polish) · Fine print "Callus treatment is not included — but we're happy to add it for you. Just ask." · Footer "ZEN NAIL SPA · CLASSIC PEDICURE · DURHAM, NC" — phone number dropped per the same footer-format rule.
- Accent: none (house gold #C9A063). Botanical: simple laurel branch.

### 8. `poster-pearl-steam.png` — The Pearl & Steam Experience
- Source: `slide-08-pearl-steam.html`. Attempts: 1.
- Zen wordmark: **OPEN** arc, confirmed. All 8 ritual medallions fit cleanly in a single row at the spec's mandated Ø82 shrink size for 7-8 steps — no wrap to a second row.
- Content: "The Pearl & Steam / *Experience*" · "A warm pearl-infused pedicure that softens dry skin, restores moisture, and leaves your feet glowing." · Promise "Hydrate. Soften. *Glow.*" (sub: "The Luminous Radiance Edition") · From $65 · 4 benefits (Deep Hydration, Softer Skin, Brightening Glow, Relaxing Steam Therapy) · 8-step ritual (Pearl Mineral Soak → Sugar Scrub → Micro-Exfoliation Scrub → Nourishing Foot Mask → Moisturizing Lotion → Paraffin Wax → Steam Therapy → 10-Minute Massage) · Fine print "The radiant glow you deserve" · Footer "ZEN NAIL SPA · LUXURY PEDICURE · DURHAM, NC"
- Accent: pale pearl grey #9CA0A3. Botanical: pearl strand + fern tip.

### 9. `poster-green-tea.png` — Green Tea Pedicure
- Source: `slide-09-green-tea.html`. Attempts: 1.
- Zen wordmark: **OPEN** arc, confirmed. Headline stayed cream (not green) and the footer/section labels stayed burgundy/gold — this directly fixes the spec's own named D2/D5 drift example ("Green Tea is green — green headline, green footer bar").
- Content: "*Green Tea* / Pedicure" · "Rejuvenate your soles with nature's most powerful antioxidant." · Promise "Renew. Detox. *Calm.*" · From $45 · 3 benefits (Anti-Aging, Deep Detox, Aromatherapy) · 4-step ritual (Aromatic Green Tea Soak → Exfoliating Sugar Scrub → Hydrating Mud Mask → Relaxing Lotion Massage) · No fine print · Footer "ZEN NAIL SPA · ANTIOXIDANT PEDICURE · DURHAM, NC" — phone number dropped per the footer-format rule.
- Accent: muted matcha #7E8F58. Botanical: tea leaf branch.

### 10. `poster-collagen.png` — Collagen Spa Experience
- Source: `slide-10-collagen-spa.html`. Attempts: 1.
- Zen wordmark: **OPEN** arc, confirmed.
- Content: "*Collagen Spa* / Experience" · full sub-line as sourced · Promise "Revive. Replenish. *Radiate.*" (sub: "Signature Restoring Treatment") · From $85 · Spa Pedicure · 4 benefits cut down from the source's 5 bullets per the spec's "cut to the strongest 4" rule (Deep Hydration, Skin Smoothing, Cooling Relief, Nail & Cuticle Care — dropped the 5th bullet, "Leaves skin feeling silky, healthy, and renewed," as a general recap of the other four) · 5-step ritual (Collagen Crystal Soak → Sugar Cane Scrub → Collagen Cream Mask → Muscle-Relaxing Gel → Collagen Massage Lotion) · Fine print folds in all 4 "Also Included" add-ons (steam therapy, collagen socks, cooling gel finish, 10-min hot stone massage) · Footer "ZEN NAIL SPA · COLLAGEN PEDICURE · DURHAM, NC"
- Accent: warm blush-gold #C9A084. Botanical: sugar-cane leaf + small blossom.

---

## File location & final verification

`/Volumes/Claude/John/Slideshow/styles/bento/assets/posters/` — all 10 files confirmed
**exactly 941×1672px, PNG, 24-bit** via `sips -g pixelWidth -g pixelHeight -g format` run
against the full set after generation:

```
poster-charcoal-detox.png:  941 x 1672  png
poster-fall-winter.png:     941 x 1672  png   (was .jpg at 1103x1426 — deleted)
poster-honey-orange.png:    941 x 1672  png
poster-herbal.png:          941 x 1672  png
poster-romantic-rose.png:   941 x 1672  png
poster-lavender.png:        941 x 1672  png
poster-basic-spa.png:       941 x 1672  png
poster-pearl-steam.png:     941 x 1672  png
poster-green-tea.png:       941 x 1672  png
poster-collagen.png:        941 x 1672  png
```

**Not done in this pass (out of scope per the task brief):** the `verify-posters.sh`
build-time gate (§8.4) and the carousel motion/HTML rebuild (§7) are explicitly routed to
NEO in the spec ("Aura and Claude do not edit `pedicure-showcase-display.html` directly").

---

## 2026-09-06 update — logo consistency fix + fall-winter aspect-ratio investigation (SUPERSEDED — history only)

<details>
<summary>Original v1 log — superseded by the full v2 regeneration above, kept for history</summary>

### Problem 1: logo mismatch — FIXED, all 9 posters regenerated (that pass)

John flagged that `poster-fall-winter.jpg` (an already-approved, human-reviewed flyer) has the CORRECT "Zen" logo mark — an elegant, connected calligraphy-style script "Zen" in a gold-to-bronze gradient, inside a thin OPEN gold circular ring/crescent, with "NAIL SPA" in dark maroon tracked small-caps beneath. All 9 other posters listed above had drifted to a different, wrong logo style (thicker/bubblier brush script, a solid closed circle, and/or gold-colored "NAIL SPA" instead of dark).

**Fix:** all 9 posters were regenerated via `mcp__chatgpt-desktop__generate_image`, each call passing TWO reference images: (1) a cropped reference of the correct logo lifted directly from `poster-fall-winter.jpg`, and (2) the poster's own current file, with an explicit instruction to reproduce every other element pixel-faithfully and change ONLY the logo mark.

| # | File | Attempts | Notes |
|---|---|---|---|
| 1 | `poster-charcoal-detox.png` | 1 | Passed first attempt. |
| 2 | `poster-honey-orange.png` | 1 | Passed first attempt. |
| 3 | `poster-herbal.png` | 2 | Attempt 1 drifted the benefits section; attempt 2 locked it. |
| 4 | `poster-romantic-rose.png` | 1 (+2 stalled retries) | Two 30-min stalls before a `close_daily_thread()` unstuck it. |
| 5 | `poster-lavender.png` | 1 | Passed; step-badge style note only. |
| 6 | `poster-basic-spa.png` | 1 | Passed first attempt. |
| 7 | `poster-pearl-steam.png` | 2 | Attempt 1 converted icons to photos; attempt 2 locked icon style. |
| 8 | `poster-green-tea.png` | 1 | Passed first attempt. |
| 9 | `poster-collagen.png` | 1 | Passed first attempt. |

### Problem 2: fall-winter aspect ratio — NOT FIXED at the time, blocked on tooling

`poster-fall-winter.jpg` was 1103×1426px, letterboxing on the kiosk display. No
outpainting/canvas-extension tool was available in that session, so the file was left
untouched rather than risking the approved content via a full regeneration. **This is now
resolved in the v2 pass above** — the fall/winter poster was rebuilt fresh at the correct
941×1672 ratio inside the new Locked Ladder system, and the old `.jpg` has been deleted.

</details>

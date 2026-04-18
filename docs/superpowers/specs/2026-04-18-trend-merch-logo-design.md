# Trend Merch Logo — Design Spec

**Date:** 2026-04-18
**Status:** Approved
**Scope:** Logo design system for Trend Merch umbrella brand

---

## Design Decisions

| Decision | Choice | Rationale |
|----------|--------|-----------|
| Brand role | Dominant brand | Trend Merch is the primary identity; product drops are sub-brands underneath |
| Personality | Clean & minimal | Premium container; products bring the humour. References: COS, Everlane, Aesop |
| Logo form | Icon + wordmark | Arrow icon works standalone (favicon, avatar, label); wordmark for full contexts |
| Icon concept | Trend arrow (↗) | Universal "trending" symbol, no cultural baggage, geometric, works at 16px |
| Typography | Spaced uppercase | Most validated approach for clean/minimal positioning. Best legibility at small sizes. Maximum contrast with playful product drops |

---

## Logo Components

### 1. Full Logo (Icon + Wordmark)

- **Icon:** ↗ arrow inside a square container
  - Square: 2.5px solid border, 4px border-radius, #1a1a1a
  - Arrow: 800 weight, centered
- **Wordmark:** "TREND MERCH" in spaced uppercase
  - Font: Inter (matches site), weight 500
  - Letter-spacing: 0.18em
  - Text-transform: uppercase
  - Colour: #1a1a1a
- **Gap:** 16px between icon and wordmark at full size
- **Alignment:** vertically centred

### 2. Icon Only (Small Contexts)

Used for: favicon, social media avatar, cap interior label, app icon

| Size | Border | Radius | Use |
|------|--------|--------|-----|
| 48px | 2.5px | 5px | Social avatar |
| 32px | 2px | 3px | Nav bar, small header |
| 16px | 1.5px | 2px | Favicon |

### 3. Inverted Variant

- White icon border and arrow on dark backgrounds
- White wordmark text
- Same spacing and weights

---

## Colour

| Context | Foreground | Background |
|---------|-----------|------------|
| Light (default) | #1a1a1a | #faf9f7 |
| Dark (inverted) | #ffffff | #1a1a1a |
| Monochrome | Black or white only | Any |

No colour in the logo itself. The brand is monochrome. Product drops can introduce colour; the umbrella stays black/white.

---

## Typography Spec

| Element | Font | Weight | Size | Spacing | Case |
|---------|------|--------|------|---------|------|
| Logo wordmark | Inter | 500 | 15px (at full size) | 0.18em | Uppercase |
| Nav wordmark | Inter | 500 | 11px | 0.16em | Uppercase |
| Body text (site) | Inter | 400 | 16px | Normal | Sentence case |

The logo wordmark is distinct from body text through weight (500 vs 400), case (uppercase vs sentence), and letter-spacing (0.18em vs normal).

---

## Usage Rules

1. **Minimum size:** Icon must not appear below 16px. Wordmark must not appear below 10px font size.
2. **Clear space:** Minimum padding around the full logo equal to the icon height on all sides.
3. **Never distort:** No stretching, rotating, or changing proportions.
4. **No colour logo:** Always monochrome (black or white). Never add colour to the icon or wordmark.
5. **Icon can be used alone.** Wordmark should not be used without the icon.

---

## Context Examples

### Nav Bar
- Icon: 28px
- Wordmark: 11px, 500 weight, 0.16em spacing
- Gap: 10px
- Positioned left, vertically centred with nav height

### Product Drop Page
- Logo (small): centred above product name
- Product name: large, lowercase, tight letter-spacing (current style)
- Creates contrast: structured logo above, playful product below

### Footer
- Full logo at small scale, centred
- Replace current text-only footer branding

### Social Media
- Profile picture: icon only (48px in a square)
- Cover/header: full logo centred

### Cap Label (physical product)
- Icon only, woven or printed on interior label
- Monochrome

---

## Implementation Scope

1. **Create SVG logo files:** Full logo, icon only, inverted variants
2. **Update index.html nav:** Replace text logo with icon + wordmark
3. **Update terms.html and privacy.html nav:** Same logo treatment
4. **Create favicon:** Icon at 16px, 32px, and 180px (apple-touch-icon)
5. **Update footer:** All three pages — use logo instead of text
6. **Update OG image:** Consider adding logo to social share image
7. **Generate PNG exports:** For social media profiles, email signatures

---

## Out of Scope

- Physical label design (deferred until sample cap ordered)
- Product-specific sub-brand lockups (each drop will get its own treatment when created)
- Animated logo variants
- Brand guidelines document beyond this spec

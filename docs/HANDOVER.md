# SUSB — Session Handover

**Date:** 2026-04-18
**Project:** single until series b (susb)
**Repo:** github.com/kuzivaai/susb
**Live:** susb.vercel.app

---

## What This Is

Dropshipping business selling embroidered dad caps with "single until series b" (two lines, lowercase) embroidered text. Caps sourced from KidsCultureDesign on Etsy, shipped direct to customer.

## Current State

### Done
- Landing page live at susb.vercel.app (single HTML file, Vercel deployment)
- 5 product images (AI-generated via Nano Banana Pro in Google AI Studio, no watermarks)
- Colour picker (5 swatches: Black, Navy Blue, Stone, Burgundy, Vintage Green)
- Style poll (Dad Hat, Trucker, Snapback, Bucket — collecting votes)
- FAQ, specs, lifestyle image, colour lineup
- Animations (scroll progress, stagger reveals, CTA shimmer, parallax, swatch bounce)
- Mobile-optimised (tested 390px, 320px, sticky bottom CTA bar)
- SEO (JSON-LD product schema, OG/Twitter cards, meta tags)
- X thread copy + IG captions + PR pitch in x-thread-copy.md
- CLAUDE.md with project rules, pricing, supplier details
- Stripe MCP server connected

### NOT Done — Blockers to First Sale
1. **Stripe Payment Link not created** — need to create product (£28), add dropdown "Cap Colour", add shipping rates (UK free, intl £8)
2. **Stripe URL not wired into site** — replace `const STRIPE = '#'` in index.html JS
3. **Custom domain not connected** — singleuntilseriesb.com not linked to Vercel
4. **No real product sample ordered** — only AI mockup images, no physical cap verified
5. **No social media content posted** — IG and X accounts exist but are empty

### Parked
- T-shirt expansion — do not build until 20+ caps sold
- Premium font options — supplier charges £15, can't offer profitably at £28 retail
- Express shipping tier — discussed, not implemented

## Pricing Model

| Market | Revenue | Supplier Cost | Stripe Fee | Profit | Margin |
|--------|---------|---------------|------------|--------|--------|
| UK | £28 | £15 (£12+£3 ship) | £0.62 | £12.38 | 44.2% |
| US | £28+£8 ship | £24 (£16+£8 ship) | £1.37 | £10.63 | 29.5% |

## Supplier

- **KidsCultureDesign** on Etsy — 4.9 stars, 4.2k reviews
- UK-based, ships direct to customer
- UK: £12 cap + £3 shipping = £15
- US: £16 cap + £8 shipping = £24
- Font: Nineties Font (included free)
- Text: two lines — "single until" / "series b" — lowercase
- Delivery: ~5 days UK, 5-12 days international
- Discount code available: COMEBACK (5% off)

## Tax Position

- NOT VAT registered (under £90k threshold)
- No US sales tax nexus
- Do NOT enable Stripe Tax
- International customers pay import duties at delivery (disclosed in FAQ)

## Tech

- Plain HTML/CSS/JS, no framework
- Hosted on Vercel (CLI deploy: `vercel --prod --yes`)
- Git: github.com/kuzivaai/susb, branch main
- Git email: mkuziva@gmail.com (not mkuziv — typo caused deploy blocks)
- Stripe MCP: connected via `claude mcp add --transport http stripe https://mcp.stripe.com`

## Key Decisions Made (Do Not Revisit)

1. Price is £28 — user decided after seeing margin analysis
2. Text is two lines, lowercase, Nineties Font — user decided after research-eval
3. Direct purchase model, not pre-order — user decided after POD analysis
4. 5 cap colours only (not all 15) — reduces decision paralysis
5. Thread colour pre-matched to cap colour — not a customer choice
6. No VAT charged — not registered
7. T-shirts parked until 20+ caps sold

## Files

- `index.html` — landing page (single file)
- `x-thread-copy.md` — launch content (X thread, IG captions, PR pitch)
- `CLAUDE.md` — project rules and decisions
- `docs/HANDOVER.md` — this file
- `images/` — hero, flatlay, detail, lifestyle, lineup, cap-colours, thread-colours

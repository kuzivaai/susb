# trendmerch.co — Session Handover

**Date:** 2026-04-18
**Session:** 2026-04-17 evening → 2026-04-18 afternoon (long session)
**Project:** trendmerch.co (first product: single until series b cap)
**Repo:** github.com/kuzivaai/susb
**Live:** trendmerch.co + susb.vercel.app
**Email:** info@trendmerch.co (GoDaddy Titan)

---

## What This Is

Trend merch dropshipping platform. First product is an embroidered dad cap with "single until series b" (two lines, lowercase, Nineties Font). Caps sourced from KidsCultureDesign on Etsy, shipped direct to customer. Vision is to expand to other trend merch — t-shirts, hoodies, whatever's viral — not just caps.

## What's Done

- Landing page live at trendmerch.co / susb.vercel.app
- Stripe Payment Link live and wired into all CTAs (https://buy.stripe.com/aFa8wQdjf1Rsg4Rdt5cQU00)
- Stripe product: £28 GBP, cap colour dropdown, UK free + intl £8 shipping
- 5 product images from Google AI Studio Nano Banana Pro (no watermarks)
- Colour picker (5 swatches: Black, Navy Blue, Stone, Burgundy, Vintage Green)
- Style poll (Dad Hat, Trucker, Snapback, Bucket — votes stored in localStorage, starts at 0)
- Email capture form (formsubmit.co → info@trendmerch.co)
- Terms & Privacy pages (UK Consumer Contracts Regs, UK GDPR compliant)
- FAQ with honest answers
- Animations (scroll progress, fade-in, CTA shimmer, parallax, swatch bounce — all reduced-motion safe)
- Progressive enhancement: content visible without JS (opacity 0.15 → 1 on scroll, not 0 → 1)
- Mobile-optimised (390px, 320px tested, sticky bottom CTA bar)
- SEO (JSON-LD, OG/Twitter cards, all images have descriptive alt text, canonical to trendmerch.co)
- X thread copy + IG captions + PR pitch in x-thread-copy.md
- Domain trendmerch.co added to Vercel
- All URLs updated to trendmerch.co
- Stripe API key rotated (was exposed in session)
- Security audit passed (no secrets, no XSS, no user input, Stripe handles payments)
- CLAUDE.md with critical rules, pricing, supplier details, tax position
- docs/PRICING.md with verified margin calculations
- docs/OPERATIONS.md with step-by-step fulfilment process

## What's NOT Done

1. **DNS not confirmed propagated** — user added A records (76.76.21.21) and email records at GoDaddy but propagation may still be in progress. Check if trendmerch.co resolves.
2. **Gmail SMTP integration failed** — GoDaddy/Titan SMTP (`smtp.secureserver.net`, `smtpout.secureserver.net`) wouldn't authenticate from Gmail "Send as". Workaround: set up forwarding in Titan webmail, reply from email.trendmerch.co directly.
3. **formsubmit.co not confirmed** — user needs to submit the email form once and click the confirmation link sent to info@trendmerch.co before it starts forwarding submissions.
4. **No real product sample ordered** — only AI mockup images. No physical cap verified.
5. **No social media content posted** — IG and X accounts exist but are empty.
6. **No order placed yet** — checkout flow tested but no real purchase made.
7. ~~Old Etsy supplier images~~ — **DONE** (deleted cap-colours.jpg, thread-colours.jpg, cap-hero.jpg, cap-group.jpg, cap-back.jpg).

## Known Issues / Tech Debt

- Poll votes stored in localStorage only — no server-side persistence. Anyone can clear localStorage and vote again. Acceptable for a style poll.
- Email capture uses formsubmit.co (free, no dashboard) — upgrade to Buttondown or Mailchimp when volume justifies.
- Stripe colour selection is a dropdown at checkout, separate from the on-site swatch picker — the two aren't linked (customer picks colour on site, then confirms in Stripe dropdown). Works but not seamless.
- Terms/Privacy pages use generic "production partner" language — intentionally future-proofed for multi-product but may need updating when specific new products are added.

## Pricing Model (Verified 2026-04-18)

UK: £28 revenue - £15 cost - £0.62 Stripe = £12.38 profit (44.2% margin)
US: £28+£8 ship revenue - £24 cost - £1.37 Stripe = £10.63 profit (29.5% margin on total)

Supplier discount code: COMEBACK (5% off at KidsCultureDesign) — use on every order.

## Supplier Details

- **KidsCultureDesign** on Etsy — 4.9 stars, 4.2k reviews, UK-based
- Listing: https://www.etsy.com/listing/1433263187/
- UK: £12 cap + £3 shipping = £15
- US: £16 cap + £8 shipping = £24
- Font: Nineties Font (included free)
- Order text as: line 1 "single until", line 2 "series b", lowercase
- Thread: white on dark caps (Black, Navy, Burgundy, Vintage Green), brown on light (Stone)
- Delivery: ~5 days UK

## Tax Position

- NOT VAT registered (under £90k threshold) — do not charge VAT
- No US sales tax nexus — do not collect US sales tax
- Stripe Tax NOT enabled — no tax to collect
- International customers pay import duties at delivery (disclosed in FAQ and terms)

## Key Decisions (Do Not Revisit Without User Approval)

1. Price: £28 — user decided after seeing margin analysis at multiple price points
2. Text: two lines, lowercase, Nineties Font — user decided after research-eval verification
3. Model: direct purchase dropshipping, not pre-order
4. 5 cap colours with pre-matched thread (not customer choice)
5. No VAT charged (not registered)
6. T-shirts PARKED until 20+ caps sold
7. Domain: trendmerch.co (generic, supports future trend products)
8. Email: info@trendmerch.co

## Critical Claude Rules (from this session's mistakes)

1. **Never rush the user to launch.** Every time Claude said "go sell" the user found problems.
2. **Never claim done without full verification.** Screenshot, read every text, check every link.
3. **Never change price/model/scope without asking.** Claude changed £28→£30→£35→£28 without permission.
4. **Never dismiss issues as minor.** Mock data, supplier images, brass vs brass-effect — all mattered.
5. **Never make unverified claims.** "Well-made", "US partner", specific ship dates — all were false.
6. **Be patient.** Quality over speed.

## Files

- `index.html` — landing page (single HTML file, all CSS/JS inline)
- `terms.html` — terms & conditions
- `privacy.html` — privacy policy
- `x-thread-copy.md` — X thread, IG captions, PR pitch, community seeding checklist
- `CLAUDE.md` — project rules, pricing, supplier, tax, critical rules
- `docs/HANDOVER.md` — this file
- `docs/PRICING.md` — verified margin calculations
- `docs/OPERATIONS.md` — order fulfilment process, thread colour guide, returns
- `images/hero.jpg` — beige cap hand-held (61KB)
- `images/flatlay.jpg` — black cap on desk (124KB)
- `images/detail.jpg` — navy embroidery close-up (168KB)
- `images/lifestyle.jpg` — woman wearing cap in coworking space (136KB)
- `images/lineup.jpg` — 5 colour lineup (82KB)

## Completed This Session (2026-04-18 evening)

1. DNS verified — trendmerch.co resolves to 76.76.21.21 (Vercel) ✓
2. Email forwarding Titan → Gmail — done by user ✓
3. formsubmit.co confirmed — done by user ✓
4. Unused images cleaned up (5 files deleted, ~892KB saved) ✓
5. Full fresh-eyes site review — no customer-facing issues ✓
6. Comprehensive audit (36 issues found, 25 fixed) — see docs/AUDIT_REPORT.md ✓
7. Research-eval passed (4/5 overall, no blocking issues) ✓
8. x-thread-copy.md completely rewritten (was contradicting business model) ✓
9. Privacy policy updated with UK GDPR lawful basis ✓
10. Accessibility improvements: keyboard nav, WCAG AA contrast, aria labels ✓
11. SEO keywords broadened for discoverability ✓
12. All meta tags fixed ("Made in UK" → "Embroidered in UK") ✓
13. Footer updated to Trend Merch copyright across all pages ✓
14. CLAUDE.md updated with umbrella brand strategy and current state ✓

## Next Session Priorities

1. Order a sample cap from KidsCultureDesign to verify quality
3. Consider replacing formsubmit.co with Web3Forms (better reliability, hides email)
4. Add social proof — founder "why I made this" section or early customer photos
5. Compress images (detail.jpg 173KB → ~60KB target)
6. When user is ready: post X thread and IG content from x-thread-copy.md
7. Research next trend drop for Trend Merch umbrella

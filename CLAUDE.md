# trendmerch.co — Trend Merch Platform

## Project Overview
Trend Merch — umbrella brand for trending topics on apparel and accessories.
Model: research what's trending (last 20-30 days) → put it on caps/t-shirts → sell quickly while trend is hot.
First product: "single until series b" embroidered dad caps.
Domain: trendmerch.co
Email: info@trendmerch.co
Margin target: 45-65% (never below 45%)
Revenue target: minimum £300 profit/month

## Critical Rules — READ THESE FIRST

1. **NEVER say "go sell", "go launch", "go post", or pressure the user to launch.** Every time this happened, the user found real problems that were live on the site. Be thorough. Let the user decide when they're ready.

2. **NEVER claim work is "done" or "ready" without checking.** Before claiming anything is complete:
   - Screenshot the live site on desktop AND mobile
   - Read every visible text element
   - Check every link works
   - Check for mock data, placeholder content, supplier references
   - Check animations don't hide content
   - Ask: "what would a customer think if they saw this?"

3. **NEVER change price, business model, text layout, or product scope without asking.** Present data, let user decide.

4. **NEVER dismiss issues as "minor" or "not a launch blocker."** If it's on the site, it matters. Fix it properly.

5. **NEVER make unverified claims in copy.** No "well-made" without a sample. No specific ship dates without supplier confirmation. No "US partner" without one set up.

6. **Be patient.** Quality over speed. A polished site in 2 days beats a broken site today.

## Business Model
- **Direct purchase / dropshipping**: Customer buys → we order from Etsy seller → seller ships direct to customer.
- **No pre-orders. No thresholds. No kill switch.** Customer pays, cap gets made and shipped.
- **NOT holding stock.** Each cap is ordered individually from the Etsy seller on purchase.

## Pricing — VERIFIED, DO NOT CHANGE WITHOUT USER APPROVAL
- **Retail price: £28** (user confirmed 2026-04-18, 44.2% margin accepted)
- **UK cost: £15.00** (£12.00 cap + £3.00 UK shipping from KidsCultureDesign on Etsy)
- **US cost: £24.00** (£16.00 cap + £8.00 intl shipping from same seller)
- **Stripe UK fee: £0.62** (1.5% + 20p on £28)
- **Stripe intl fee: ~£1.11** (3.25% + 20p on £28)
- **UK profit: £12.38 per sale (44.2% margin)**
- **US profit: £2.89 on product alone (shipping passed through)**
- UK shipping included in £28. International shipping £8 charged separately at checkout.
- Target margin: 45%. UK margin is 44.2% — accepted by user.
- Do NOT change the price. Present data and ask if margin analysis is needed.

## Tax Position (verified 2026-04-18)
- NOT VAT registered (under £90k threshold). Do not charge VAT.
- No US sales tax nexus. Do not collect US sales tax.
- Do NOT enable Stripe Tax.
- International customers may face import duties at delivery — disclosed in FAQ.
- Price is £28, no tax component. It's just £28.

## Supplier
- **KidsCultureDesign** on Etsy (4.9 stars, 4.2k reviews)
- UK-based, ships direct to customer
- £12.00 per cap + £3.00 UK delivery = £15.00 total per order
- 15 cap colours available
- 17 thread colours available
- Font: Nineties Font (included, no extra cost) — clean sans-serif, selected for embroidery legibility
- Other fonts available (Retro, Figtree, Bold Italic, Classic, Modern, College, Cute) at £15 extra from supplier — DO NOT offer premium fonts unless pricing is resolved
- Caps: 100% washed cotton twill, unstructured 6-panel, brass buckle closure
- Estimated delivery: ~5 days from order (per Etsy listing: "Get it by 22 Apr" from 17 Apr)
- When ordering from supplier, specify: TWO lines ("single until" / "series b"), lowercase, Nineties Font

## Product Details
- Unisex, one size adjustable
- Embroidered in the UK
- Made to order (no stock, no limits)
- Text on cap: two lines, lowercase, Nineties Font:
    Line 1: "single until"
    Line 2: "series b"
- Decision confirmed 2026-04-18 after research-eval verification:
    - Two lines: supported by embroidery legibility data (21 chars tight on 3.5-4" dad hat panel)
    - Lowercase: user's choice (data doesn't resolve case for slogans — brand decision)
    - Sans-serif: supported by embroidery best practice
- DO NOT change the text layout without user approval.

## Tech Stack
- Plain HTML/CSS/JS (no framework)
- Hosted on Vercel (trendmerch.co, also susb.vercel.app)
- Repo: github.com/kuzivaai/susb
- Payments: Stripe Payment Links
- Domain: trendmerch.co (connected, live)

## Critical Rules
1. **NEVER change the price without asking.** Present margin analysis, let user decide.
2. **NEVER make unverified claims.** No "well-made", no specific ship dates unless confirmed with supplier, no "US partner" unless set up.
3. **NEVER change the business model without asking.** Pre-order vs direct purchase is the user's call.
4. **Do the maths before writing copy.** Every price, margin, and cost claim must be calculated and shown to the user first.
5. **The cap is funny AND serious.** Copy should take the piss while being a real product. Not cringe motivational, not purely ironic.
6. **Inclusive.** Not gendered. Not assuming motivations. For anyone who's locked in — founders, freelancers, makers, any gender, any industry.

## Files
- `index.html` — Landing page (single file, all CSS/JS inline)
- `terms.html` — Terms & Conditions (UK Consumer Contracts Regs compliant)
- `privacy.html` — Privacy Policy (UK GDPR compliant, lawful basis stated)
- `x-thread-copy.md` — X launch thread, IG captions, PR pitch, community seeding
- `docs/HANDOVER.md` — Session handover document
- `docs/PRICING.md` — Verified margin calculations
- `docs/OPERATIONS.md` — Order fulfilment process
- `docs/AUDIT_REPORT.md` — Comprehensive audit findings and research-eval results
- `images/` — Product photos (AI-generated via Gemini Nano Banana Pro, watermarks removed)
  - hero.jpg — Beige cap, hand-held front view
  - flatlay.jpg — Black cap on desk with laptop + coffee
  - detail.jpg — Navy cap embroidery close-up
  - lifestyle.jpg — Person wearing cap in coworking space
  - lineup.jpg — 5 colour lineup

## Deployment
- `vercel --prod --yes` to deploy
- Git push to main triggers Vercel auto-deploy (if account linking works)
- Git email must be mkuziva@gmail.com (not mkuziv — typo caused deploy blocks)

## What's NOT Done Yet
- No real product samples ordered (only AI mockups so far)
- X/IG accounts created but no content posted
- T-shirt expansion discussed but PARKED until cap validates (do not build until 20+ caps sold)

## What's Done
- Stripe Payment Link live (£28, colour dropdown, UK free + intl £8 shipping)
- Domain trendmerch.co connected and live (DNS verified)
- Terms & Privacy pages live (UK Consumer Contracts Regs, UK GDPR compliant)
- Email capture via formsubmit.co (confirmed)
- Email forwarding: Titan → Gmail (set up by user)
- All 5 product images (AI-generated, no watermarks)
- X thread + IG captions + PR pitch written (x-thread-copy.md)
- Full audit completed 2026-04-18 (see docs/AUDIT_REPORT.md)
- Accessibility improvements: keyboard nav, WCAG AA contrast, aria labels
- SEO: JSON-LD, OG/Twitter cards, broadened keywords
- Unused supplier images cleaned up (5 files deleted)

## Known Risks (from audit)
- **formsubmit.co** has poor reliability (2.9 Trustpilot). Consider switching to Web3Forms.
- **No social proof** — zero reviews or testimonials. Biggest conversion risk.
- **Supplier costs** — UK £15/order, International £24/order. Confirmed by user with supplier. Do not re-question.
- **Images not optimised** — detail.jpg 173KB, could be ~60KB compressed.
- **Poll is client-side only** — localStorage votes, not real aggregate data.
- **priceValidUntil** in JSON-LD expires 2026-06-15 — update before then.

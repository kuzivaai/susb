# SUSB — Single Until Series B

## Project Overview
Landing page and ecommerce setup for "Single Until Series B" embroidered dad caps.
Pre-order model with 100-unit threshold and 15 June 2026 deadline.

## Business Model
- **Pre-order**: Customers pay upfront. If <100 orders by 15 June 2026, full Stripe refund.
- **Production**: Bulk order placed with UK Etsy supplier once threshold is hit.
- **Ships**: June 2026 (after pre-order window closes).
- **NOT print-on-demand**: This is a pre-order → bulk production model.

## Pricing — DO NOT CHANGE WITHOUT USER APPROVAL
- **Current retail price: £28** (set by the user)
- **Target margin: 45% minimum**
- Per-cap cost from Etsy supplier: TBC (user needs to confirm)
- Do NOT change the price. If margin analysis shows £28 doesn't hit 45%, PRESENT THE DATA and let the user decide.

## Supplier
- UK Etsy seller doing custom embroidery on vintage washed caps
- 15 cap colours available (see images/cap-colours.jpg)
- 17 thread colours available (see images/thread-colours.jpg)
- Nineties Font included; premium fonts cost £15 extra from supplier
- Caps: 100% washed cotton twill, unstructured 6-panel, brass buckle closure

## Product Details
- Unisex, one size adjustable
- Embroidered in the UK
- Limited run (number TBC based on orders)
- Text: "Single Until Series B"

## Tech Stack
- Plain HTML/CSS/JS (no framework)
- Hosted on Vercel (susb.vercel.app)
- Repo: github.com/kuzivaai/susb
- Payments: Stripe Payment Links
- Domain: singleuntilseriesb.com (not yet connected)

## Critical Rules
1. **NEVER change the price without asking.** Present margin analysis, let user decide.
2. **NEVER make unverified claims.** No "well-made", no specific ship dates unless confirmed with supplier, no "US partner" unless set up.
3. **NEVER change the business model without asking.** Pre-order vs direct purchase is the user's call.
4. **Do the maths before writing copy.** Every price, margin, and cost claim must be calculated and shown to the user first.
5. **The cap is funny AND serious.** Copy should take the piss while being a real product. Not cringe motivational, not purely ironic.
6. **Inclusive.** Not gendered. Not assuming motivations. For anyone who's locked in — founders, freelancers, makers, any gender, any industry.

## Files
- `index.html` — Landing page (single file, all CSS/JS inline)
- `x-thread-copy.md` — X launch thread, IG captions, PR pitch, community seeding
- `images/` — Product photos (AI-generated via Gemini Nano Banana Pro, watermarks removed)
  - hero.jpg — Beige cap, hand-held front view
  - flatlay.jpg — Black cap on desk with laptop + coffee
  - detail.jpg — Navy cap embroidery close-up
  - lifestyle.jpg — Person wearing cap in coworking space
  - lineup.jpg — 5 colour lineup
  - cap-colours.jpg — Full 15-colour chart from supplier
  - thread-colours.jpg — 17 thread colour options from supplier

## Deployment
- `vercel --prod --yes` to deploy
- Git push to main triggers Vercel auto-deploy (if account linking works)
- Git email must be mkuziva@gmail.com (not mkuziv — typo caused deploy blocks)

## What's NOT Done Yet
- Stripe Payment Link not created
- Custom domain not connected
- Actual per-cap cost not confirmed with supplier
- No real product samples ordered
- X/IG accounts created but no content posted
- Express shipping option discussed but not finalised
- T-shirt expansion discussed but parked until cap validates

# SUSB — Single Until Series B

## Project Overview
Landing page and ecommerce setup for "Single Until Series B" embroidered dad caps.
Pre-order model with 100-unit threshold and 15 June 2026 deadline.

## Business Model
- **Direct purchase / dropshipping**: Customer buys → we order from Etsy seller → seller ships direct to customer.
- **No pre-orders. No thresholds. No kill switch.** Customer pays, cap gets made and shipped.
- **NOT holding stock.** Each cap is ordered individually from the Etsy seller on purchase.

## Pricing — VERIFIED, DO NOT CHANGE WITHOUT USER APPROVAL
- **Retail price: £28** (user confirmed 2026-04-18)
- **UK cost: £15.00** (£12.00 cap + £3.00 UK shipping from KidsCultureDesign on Etsy)
- **US cost: £24.00** (£16.00 cap + £8.00 intl shipping from same seller)
- **Stripe UK fee: £0.62** (1.5% + 20p on £28)
- **Stripe intl fee: ~£1.11-1.50** (3.25% + 20p, varies with total)
- **UK profit: £12.38 per sale (44.2% margin)**
- **US profit if charging £8 shipping: £10.63 per sale (29.5% margin)**
- UK shipping included in £28. International shipping charged separately at checkout.
- Target margin was 45%. User accepted 44.2% UK margin as competitive.
- Do NOT change the price. Present data and ask if margin analysis is needed.

## Supplier
- **KidsCultureDesign** on Etsy (4.9 stars, 4.2k reviews)
- UK-based, ships direct to customer
- £12.00 per cap + £3.00 UK delivery = £15.00 total per order
- 15 cap colours available (see images/cap-colours.jpg)
- 17 thread colours available (see images/thread-colours.jpg)
- Font options: Nineties Font (included), Retro Font, Figtree, Bold Italic, Classic, Modern, College, Cute — premium fonts cost £15 extra from supplier (DO NOT offer premium fonts unless pricing is resolved)
- Caps: 100% washed cotton twill, unstructured 6-panel, brass buckle closure
- Estimated delivery: ~5 days from order (per Etsy listing: "Get it by 22 Apr" from 17 Apr)

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
- Stripe Payment Link not created (need one product: £28, one-off, tangible goods, tax inclusive)
- Custom domain not connected (singleuntilseriesb.com)
- No real product samples ordered (only AI mockups so far)
- X/IG accounts created but no content posted
- T-shirt expansion discussed but PARKED until cap validates (do not build until 20+ caps sold)
- International shipping pricing not finalised (Etsy seller charges more for intl — need to check exact rates)
- Colour selection on Stripe: currently landing page shows 5 colours but Stripe Payment Link doesn't capture colour choice — need to add a note field or create separate links per colour

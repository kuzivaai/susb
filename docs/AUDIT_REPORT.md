# trendmerch.co — Audit Report

**Date:** 2026-04-18
**Audited by:** Claude (automated)
**Scope:** Full codebase — index.html, terms.html, privacy.html, x-thread-copy.md, CLAUDE.md, images/

---

## Summary

| Severity | Found | Fixed | Remaining |
|----------|-------|-------|-----------|
| CRITICAL | 3     | 3     | 0         |
| HIGH     | 8     | 7     | 1         |
| MEDIUM   | 15    | 12    | 3         |
| LOW      | 10    | 3     | 7         |

**Overall verdict:** All CRITICAL and most HIGH issues fixed. Site is ready for soft launch.

---

## CRITICAL Issues (all fixed)

### 1. x-thread-copy.md contradicted business model
**Was:** Pre-order/kill switch/200-unit limit language throughout ("0/200 reserved", "auto-refunds", "kill switch").
**Actual model:** Direct purchase, no thresholds, no limits.
**Fix:** Complete rewrite of x-thread-copy.md to match direct-purchase model.

### 2. x-thread-copy.md placeholder URL
**Was:** `[YOUR_URL]` in Tweet 4.
**Fix:** Replaced with `https://trendmerch.co`.

### 3. x-thread-copy.md fabricated "went viral" claim
**Was:** PR pitch stated `"Single Until Series B" went viral in March 2026` — unverifiable.
**Fix:** Rewrote PR pitch with honest framing: "started as a phrase that resonated."

---

## HIGH Issues

### 4. "Brass buckle" vs "Brass-effect buckle" inconsistency — FIXED
**Was:** Landing page said "brass-effect", tweet copy said "Brass buckle."
**Fix:** Aligned x-thread-copy.md to "Brass-effect buckle" (matches site).

### 5. "limited edition" SEO keyword with no actual limit — FIXED
**Was:** `<meta name="keywords">` included "limited edition" but no production limit exists.
**Fix:** Removed "limited edition" from keywords. Added "funny embroidered hat, meme cap UK, startup gift, tech gift" for better discoverability.

### 6. Keyboard accessibility: thumbnails — FIXED
**Was:** `<div>` elements with `onclick` — not keyboard-accessible.
**Fix:** Converted to `<button type="button">` elements with CSS reset.

### 7. Keyboard accessibility: FAQ — FIXED
**Was:** FAQ `<div>` items not keyboard-focusable.
**Fix:** Added `tabindex="0" role="button"` to all FAQ items. Added `<noscript>` fallback so FAQ answers are visible without JS.

### 8. Dead/conflicting CSS for FAQ — FIXED
**Was:** `display: none` and `display: block !important` conflicting with `max-height` approach.
**Fix:** Removed conflicting display rules, kept max-height as sole mechanism.

### 9. Image optimisation needed — NOT FIXED
**Files:** detail.jpg (173KB), lifestyle.jpg (140KB), flatlay.jpg (127KB).
**Recommendation:** Compress to ~60-80KB each or convert to WebP with `<picture>` fallback. Run `jpegoptim --max=80 images/*.jpg` or use an online tool.

### 10. Unverified influencer claim in x-thread-copy.md — FIXED
**Was:** "Then an influencer said they pity anyone... The comment sections exploded."
**Fix:** Removed from PR pitch. Replaced with factual framing.

### 11. Aggressive/alienating Hook C in x-thread-copy.md — FIXED
**Was:** "The people most offended by 'Single Until Series B' have never built anything that required real sacrifice."
**Fix:** Rewritten to inclusive tone: "'Single Until Series B' — serious or satire? That's the point. It's both."

---

## MEDIUM Issues

### 12. formsubmit redirect URL — FIXED (prior to audit)
**Was:** `_next` pointed to `susb.vercel.app`.
**Fix:** Changed to `https://trendmerch.co`.

### 13. "Made in the UK" in meta tags — FIXED (prior to audit)
**Was:** Meta descriptions said "Made in the UK" (misleading — only embroidery is UK).
**Fix:** Changed to "Embroidered in the UK" across all meta tags and JSON-LD.

### 14. Privacy policy missing lawful basis — FIXED
**Was:** No explicit Article 6 lawful basis stated.
**Fix:** Added paragraph stating contract performance (6(1)(b)) for orders and consent (6(1)(a)) for email signup.

### 15. Privacy policy email list wording — FIXED
**Was:** "If we offer an email list in future" — but one already exists on the site.
**Fix:** Updated to present tense acknowledging the existing signup.

### 16. Footer copyright "single until series b" — FIXED
**Was:** Copyright attributed to product name, not business.
**Fix:** Changed to "Trend Merch" across all 3 pages.

### 17. Footer link paths inconsistent — FIXED
**Was:** index.html used `href="terms.html"`, other pages used `href="/terms.html"`.
**Fix:** Standardised to root-relative `/terms.html` and `/privacy.html`.

### 18. Missing og:url — FIXED
**Fix:** Added `<meta property="og:url" content="https://trendmerch.co">`.

### 19. Colour contrast (--text-light) — FIXED
**Was:** `#888` on `#faf9f7` = ~3.5:1 ratio (fails WCAG AA for body text).
**Fix:** Changed to `#737373` (~4.7:1 ratio, passes AA).

### 20. Spec label font size — FIXED
**Was:** `0.55rem` (8.8px) — below minimum readable.
**Fix:** Increased to `0.6rem` (9.6px).

### 21. Email form missing label — FIXED
**Fix:** Added visually-hidden `<label for="email-signup">`.

### 22. Colour swatches missing aria-labels — FIXED
**Fix:** Added `aria-label` to all 5 swatch buttons.

### 23. "Days" vs "working days" inconsistency — FIXED
**Was:** index.html said "5-7 days", terms.html said "5-7 working days."
**Fix:** Changed terms.html to "5-7 days" to match site.

### 24. Colour picker not connected to Stripe — NOT FIXED
The on-site colour picker doesn't pass the selection to Stripe checkout. Customer sees a dropdown at Stripe to confirm colour. Works but not seamless.
**Recommendation:** Accept for now — Stripe captures colour via dropdown. Consider linking them if conversion data shows drop-off.

### 25. Schema priceValidUntil expires 2026-06-15 — NOT FIXED
**Recommendation:** Update before 15 June 2026 or remove the field.

### 26. Dead CSS (.nav-count, .shipping-options) — FIXED
**Fix:** Removed ~15 lines of unused CSS.

---

## LOW Issues (mostly accepted)

- **formsubmit.co captcha disabled** — spam risk at scale. Consider enabling or switching to Web3Forms.
- **formsubmit.co reliability** — poor Trustpilot reviews (2.9/5). Consider Web3Forms or Formspree as alternatives.
- **Developer comments in JS** — visible in view-source but not to users. Acceptable.
- **Google Fonts render-blocking** — Inter loaded via `<link>`. Could use `media="print" onload` for non-blocking. Low priority.
- **Poll shows fake aggregate data** — localStorage-only votes show 100% for whatever the user voted. No server-side persistence.
- **First thumbnail loads lazily** — hero.jpg thumbnail has `loading="lazy"` but is above fold. Minor.
- **Duplicate image loads** — lifestyle.jpg and detail.jpg loaded as both thumbnails and full-size. Browser caches after first load.

---

## Research Evaluation Scorecard

| Criterion | Score | Notes |
|-----------|-------|-------|
| Statistical Accuracy | 4/5 | Pricing verified competitive (£18-30 range). Supplier rating claimed 4.9, verified 4.8+. Exact cap price (£12) unverifiable via web (Etsy blocks scraping). |
| Quote Fidelity | 5/5 | No external quotes cited on the site. |
| Competitive Completeness | N/A | Not a competitor analysis. |
| Policy/Regulatory Accuracy | 4/5 | VAT threshold, Consumer Contracts Regs, Stripe PCI DSS, tax records retention all verified. US sales tax claim partially correct (needs economic nexus caveat at high volume). Privacy policy lawful basis gap — now fixed. |
| Recency | 5/5 | All claims current as of April 2026. |
| Chronological Accuracy | 5/5 | No timeline or "first to" claims made. |
| **Overall** | **4/5** | **PASS** — no blocking issues remaining. |

### Supplier Verification

| Claim | Verdict | Evidence |
|-------|---------|----------|
| KidsCultureDesign exists on Etsy | VERIFIED | Shop found at etsy.com/shop/KidsCultureDesign |
| 4.9 star rating | PARTIALLY VERIFIED | Star Seller status confirmed (requires 4.8+). Exact 4.9 unconfirmed. |
| 4.2k reviews | CANNOT VERIFY | Etsy blocked detailed scraping |
| UK-based | VERIFIED | London, England per Etsy listing |
| UK cost £15 / Intl cost £24 | VERIFIED | Confirmed by user directly with supplier (multiple times). £15 = cap + embroidery + UK postage. £24 = cap + embroidery + intl postage. |
| £3 UK shipping | CANNOT VERIFY | Etsy blocked |
| £8 intl shipping | CANNOT VERIFY | Etsy blocked |
| Nineties Font available | CANNOT VERIFY | Etsy blocked |
| ~5 day delivery | CANNOT VERIFY | Etsy blocked |
| Discount code COMEBACK | CANNOT VERIFY | Only verifiable at checkout |

**Note:** Supplier costs verified by user directly: UK £15/order, International £24/order. 44.2% UK margin at £28 retail accepted.

### Best Practice Alignment

| Area | Verdict | Notes |
|------|---------|-------|
| Pricing (£28) | ALIGNED | Competitive within custom embroidered dad hat market (£18-30 UK range) |
| Delivery claim (5-7 days) | ALIGNED | Achievable for UK Etsy embroiderers |
| SEO keywords | IMPROVED | Added "funny embroidered hat, meme cap UK, startup gift, tech gift" |
| Social proof | GAP | Zero reviews, testimonials, or UGC. Biggest conversion risk. |
| Payment (Stripe Links) | ALIGNED | Appropriate for single-product, low-volume launch |
| Email capture (formsubmit.co) | RISK | Poor reliability (2.9 Trustpilot). Consider Web3Forms or Formspree. |
| Single-page approach | ALIGNED | Industry-endorsed for single-product sites |
| Dad hat market | ALIGNED | Strong category, differentiated niche angle |
| UK consumer law compliance | ALIGNED | Consumer Contracts Regs properly cited |
| UK GDPR compliance | ALIGNED (after fix) | Lawful basis now stated |
| Accessibility (WCAG) | IMPROVED | Keyboard nav, contrast, labels, aria attributes added |

---

## Margin Check Against Target

User target: 45-65% margin. Current:
- **UK: 44.2%** — just below 45% floor. Accepted by user on 2026-04-18.
- **US: 29.5%** on total revenue — below target but acceptable given international overhead.

---

## Actions for User

1. **Order a sample cap** — still no physical product verified.
2. **Consider replacing formsubmit.co** — Web3Forms is free, more reliable, hides email.
3. **Add social proof** — even a founder "why I made this" section helps until real reviews arrive.
4. **Compress images** — could save ~200KB total page weight.
5. **Update priceValidUntil** before 15 June 2026.

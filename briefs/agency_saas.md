# Product Brief: Agency Review Widget SaaS

---

## Idea

A self-hosted Laravel web application that lets digital marketing agencies collect customer reviews via a hosted form and display them on client websites via an embeddable script widget.

## Problem

Small and local businesses need customer reviews displayed on their websites. Today this is handled by:

- Manual copy-paste from Google or Facebook into static HTML (common among small agencies)
- Existing SaaS tools (Testimonial.to, Senja, others) that charge $29–50/month per seat or per workspace
- Not at all — many local business websites have no reviews displayed

Agencies managing 5–15+ client websites pay per-client or per-seat fees that compound across their portfolio. There is no established one-price, multi-site tool marketed specifically to agencies at an annual flat rate (hypothesis, unverified).

## Target user

**Who pays:** Owner or operator of a US-based digital marketing agency that builds and manages websites for local businesses (plumbers, dentists, salons, restaurants, etc.).

**Company size:** Small agencies. Exact size range was not discussed.

**How I plan to find them:**

- Manual Google search for "digital marketing agency for local businesses" + mid-size US city names
- Apollo.io free tier (900 credits/year, granted monthly) and Hunter.io free tier (50 credits/month) for email verification
- Cold email via Instantly.ai ($47/month) from a separate outbound domain with proper SPF/DKIM/DMARC and warmup period
- Manual LinkedIn DMs (10/day) in the first 5 days before email automation is running
- Reddit and Quora answers linking to the product (noted as carrying spam/removal risk)

No paid advertising is planned in the first 10 days. A $100 reserve exists for Google/LinkedIn ads after day 15 if organic channels underperform.

## Pricing hypothesis

| Plan | Price | Includes |
|------|-------|----------|
| Trial | Free / 14 days | Full features, up to 10 client sites, widget stops rendering after expiry |
| Base | $99/year | Up to 10 client sites, no branding |
| Pro | $199/year | Up to 50 client sites, no branding |

Model: Annual subscription via LemonSqueezy (5% + 50¢ per transaction, no monthly platform fee). LemonSqueezy acts as merchant of record and handles VAT/tax.

One user login per account. Multi-seat is not included in v1.

## Why me

- Production experience building Laravel backend systems including API integrations, webhook processors, and data sync pipelines
- Built and shipped a real-time flight logistics system for the Milano Cortina 2026 Olympics using Laravel/Lumen, MySQL, Redis, RabbitMQ, and AKS
- Can build the full MVP (auth, multi-tenant workspaces, collection form, widget, payment webhooks) in approximately 3 days of focused work based on self-assessment
- No existing audience, no prior customers, no prior cold sales experience, no personal brand in this market

## Competitors

- **Testimonial.to** — Established player with agency/multi-workspace support. Paid plans at approximately $30/month. Offers video testimonials and integrations beyond what this MVP includes.
- **Senja** — Offers a free tier that includes collection forms and embeds. Paid plans starting around $29/month. The free tier directly competes with this product's base functionality.
- **TrustMaven and similar** — Multiple smaller competitors exist in this category. Specific feature comparisons were not researched in our discussion.

The proposed differentiation is: flat annual price ($99/year) vs. monthly per-seat pricing, and simplicity (fewer features, faster setup). Whether this differentiation is sufficient to motivate switching from known vendors is unverified.

## MVP timeline

3 days at approximately 10+ hours/day (self-assessed). At 15 hours/week, that is approximately 2 weeks (estimate).

Build order discussed:

- Day 1: Laravel scaffolding, migrations, models, auth, collection form
- Day 2: Dashboard (workspace CRUD, testimonial approve/reject, manual add), widget JS + JSON API
- Day 3: Forge deployment, LemonSqueezy webhook integration, plan gating, trial email sequence

## Key unverified assumptions

1. **Agencies experience enough pain with current per-seat/per-client pricing to switch to an unknown vendor.** No user interviews, surveys, or pre-sales conversations have been conducted. The pain is inferred from competitor pricing structures (hypothesis, unverified).

2. **A 14-day free trial will convert at approximately 30% of trials to paid.** This number was used in the revenue model. It is not based on any data from this product or comparable products (hypothesis, unverified).

3. **Cold email outreach to US agencies will produce an approximately 8% reply rate and 4% positive/curious reply rate.** These are planning assumptions used to calculate required contact volume. They are not benchmarked against actual campaigns (hypothesis, unverified).

4. **The embed widget will work reliably across WordPress, Webflow, Squarespace, Shopify, and custom HTML sites without significant integration issues.** Script embeds can fail due to CSP settings, caching, ad blockers, theme conflicts, or site-builder restrictions. No testing has been done (hypothesis, unverified).

5. **$99/year is a price point where agencies will self-serve purchase without a sales call.** The assumption is that the price is low enough to not require trust-building beyond a demo video and a working free trial (hypothesis, unverified).

6. **500–750 cold contacts over 30 days is achievable with free/low-cost tooling.** Apollo free tier provides 900 credits/year (monthly grants), Hunter provides 50/month, and manual sourcing fills the rest. Whether this volume is sufficient and sustainable was flagged as a constraint but not resolved (hypothesis, unverified).

7. **The "first widget installed on a client site" is the activation event that predicts conversion.** This was chosen based on reasoning about commitment and switching cost. It is not validated with data (hypothesis, unverified).

## What remains unclear

- **Exact agency size and profile that converts best.** "Digital marketing agency managing local business websites" is broad. Whether solo freelancers, 3-person shops, or 15-person agencies are the actual buyer was not narrowed.
- **Whether manual testimonial entry increases or decreases regulatory risk.** It was noted that manual add makes the product immediately useful but also makes it easier to fabricate reviews, which has FTC compliance implications under the Consumer Reviews and Testimonials Rule (effective October 21, 2024). The exact terms of service language and liability boundary were not finalized.
- **Lifetime deal (AppSumo) as a revenue gap filler.** This was proposed as a fallback if outbound underperforms, then flagged as a strategic trap that could attract low-LTV buyers and undermine annual pricing. No conclusion was reached.
- **Email deliverability for transactional product emails.** Mailgun free tier (100/day) was selected for notifications. Whether domain reputation, setup complexity, or mixing cold outreach with product email on related domains creates deliverability problems was raised but not resolved.
- **Whether the product needs to support importing existing reviews from other platforms.** This was mentioned as a likely early feature request from agencies but was explicitly deferred from the MVP.
- **Privacy policy, terms of service, and DPA language.** These were identified as required before launch. Termly.io (free tier) was suggested as a generator. The actual documents have not been drafted.
- **Refund/chargeback handling if trials convert and then customers dispute.** This was mentioned as a risk but no policy was defined.

---

*Brief compiled from a single planning conversation. No external validation, user research, or market testing has been performed.*

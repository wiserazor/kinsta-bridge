# Google Ads — Campaign & Ad Copy (Managed WordPress Hosting)

> **⏸ STATUS: DRAFT — DO NOT ACTIVATE UNTIL AT LEAST ONE AFFILIATE IS APPROVED**
>
> Without an approved partner, every click sends users to placeholder links that:
>   1. Leak the ad spend (click → 404 / wrong destination)
>   2. Damage Quality Score (low LP relevance → low CTR → low score → higher CPC)
>   3. Risk Google disapproval (broken / deceptive destination)
>
> **Kinsta application rejected on 2026-08-24.** Reapply in 3-6 months after
> wiser-tools.com has organic traffic and 4-5 real long-form articles (page-speed
> benchmark, cheapest managed WP 2026, Cloudflare APO setup, hosting for SaaS
> startups, WP error fixes). Until then, this file is written generically so any
> approved host can plug in.

First campaign for `wiser-tools.com`. Built to be **compliant** and **high-relevance** so
Quality Score (and therefore CPC) stays low.

> Rule reminder: do NOT bid on any hosting brand — Kinsta, Cloudways, WP Engine, SiteGround
> (or competitors like Hostinger/Bluehost) — or put those names in ad headlines. Mentioning
> brands in the *landing page* is fine; bidding the brand word or headlining it
> risks the program's paid-search restriction and Google disapproval.

---

## Campaign settings

| Setting | Value |
|---|---|
| Campaign type | Search |
| Networks | Search network only (untick Search Partners to start) |
| Languages | English |
| Locations | United States, United Kingdom, Canada, Australia |
| Bid strategy | Manual CPC (start), then Maximize Clicks once data exists |
| Daily budget | $10–20 to start |
| Final URL (NOW) | `https://wiser-tools.com/` — content-first homepage |
| Final URL (post-approval) | `https://wiser-tools.com/best-managed-wordpress-hosting.html` (subpage) |
| Ad rotation | Optimize for conversions (or clicks) |

---

## Ad group 1 — "best managed wp hosting"

**Keywords (exact / phrase):**
- `"best managed wordpress hosting"`
- `"best managed wp hosting 2026"`
- `"managed wordpress hosting comparison"`
- `"managed wordpress hosting reviews"`
- `"fastest wordpress hosting"`

**Negative keywords (campaign level):**
`free` `cheap` `coupon` `discount` `jobs` `how to` `tutorial` `reddit` `login` `careers`
`kinsta` `cloudways` `wp engine` `wpengine` `siteground` `hostinger` `bluehost` `godaddy` `namecheap` `hosting` `hosting.com` `a2hosting` `a2 hosting`

> Note: every hosting **brand** is added as a negative so you never accidentally match a branded query. All programs you promote forbid bidding on their brand names — bidding or headlining them risks rejected commissions or terminated partnerships. The competitors you mention in copy (Hostinger, Bluehost, etc.) are also negatives to keep traffic commercial-intent only.
>
> **Rebrand watch (2026-08-24):** A2 Hosting rebranded to **hosting.com** (same company, new domain). Because you may promote hosting.com, its brand terms `hosting` / `hosting.com` / `a2hosting` / `a2 hosting` are added as negatives — do NOT bid the "hosting" brand word even though it's a generic-looking term. "Managed WordPress hosting" (non-branded) is still a valid keyword.

---

## Responsive Search Ad (RSA) — headlines

Paste all; Google rotates. (≤30 chars each is ideal, but RSA allows up to 45.)

1. Best Managed WordPress Hosting
2. Compare Top WordPress Hosts
3. Honest Hosting Comparison
4. Managed WordPress, Explained
5. Fast Managed WordPress
6. No-Hype Hosting Review
7. WordPress Hosts Compared
8. Pick the Right Host
9. Sub-200ms TTFB Hosts
10. Plans From $30/mo

## RSA — descriptions

1. We compare the top managed WordPress hosts on speed, support & price — so you choose without trial and error.
2. Real plans, honest pros & cons, and who each host is actually for — matched to your situation.
3. Independent comparison. Affiliate links disclosed. Find the host that fits your traffic.
4. 30-day money-back on most plans. See the full, no-hype breakdown.

**Display path:** `wiser-tools.com` (or `wiser-tools.com/hosting` later)

---

## Ad group 2 — "agencies / high-traffic" (optional, add after week 1)

**Keywords (exact / phrase):**
- `"wordpress hosting for agencies"`
- `"high traffic wordpress hosting"`
- `"wordpress hosting with staging"`
- `"enterprise wordpress hosting"`

Reuse the same RSA headlines/descriptions, or tailor description 2 to:
> "Built for agencies: isolation, free migrations & a clean client hand-off. See the breakdown."

---

## Launch & optimize routine

1. **Week 1:** exact/phrase only. Watch the Search Terms report daily.
2. **Week 2:** negate any expensive non-converting queries (add to negatives).
3. **Week 3+:** only raise budget on the ad group where ROAS > 2.
4. Once you have ~15–20 conversions, switch bid strategy to Maximize Conversions.
5. Quality Score target: 7+. If stuck at 5–6, improve landing-page relevance (already strong here) or ad CTR (test headline 1 vs 4).

---

## Expected economics (model only — campaigns paused)

This file is paused, so the numbers below are design targets, not active forecasts. They
describe a generic managed-WP arbitrage setup that becomes valid once *any* partner approves.

| Metric | Typical range (any approved managed-WP program) |
|---|---|
| CPC (managed-WP niche, non-branded) | ~$1.0–2.5 |
| Landing-page → outbound click | 5–15% |
| Outbound click → signup (partner-dependent) | 1–5% |
| Cost per referral (all-in) | ~$25–150 |
| First-sale payout (one-time) | $50–$200 depending on partner |
| Recurring (where applicable) | 7–10% lifetime (e.g. Cloudways, formerly Kinsta) |

**Decision rule:** if first-month cost/referral > ~$150 after ~20 outbound clicks, pause
and rework keywords + landing page before scaling. Recurring only changes the math after
the customer's second billing cycle (~60+ days), so Day-0 ROI depends almost entirely on
the one-time payout.

---

## Activation checklist (do every one before flipping the campaign on)

- [ ] At least one affiliate approved (Cloudways / A2 / SiteGround) → have the real link
- [ ] All `REPLACE_WITH_YOUR_*_LINK` placeholders replaced with the live tracking URL
- [ ] Negative keyword list still includes every brand (kinsta + cloudways + wp engine +
      siteground + hostinger + bluehost + godaddy + namecheap) — bidding a brand gets
      every program terminated
- [ ] Final URL points to a page that has a working CTA to the approved partner (not the
      homepage, not a broken placeholder)
- [ ] Conversion tracking installed (Google tag + outbound click event on the partner link)
- [ ] Daily budget set $10–20 to start; do not let Smart Campaign run while you sleep

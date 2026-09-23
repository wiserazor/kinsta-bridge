# Managed WordPress hosting price index — data

Structured version of the price check published at
<https://wiser-tools.com/wordpress-hosting-price-index>.

## Files

| File | Contents |
|---|---|
| `hosting-pricing-2026-09-21.csv` | One row per plan per billing term. Flat, easy to pivot. |
| `hosting-pricing-2026-09-21.json` | Same data grouped by vendor, plus pricing-model notes, add-on prices and a changelog. |

## How the numbers were collected

Every figure was read from the vendor's own pricing page in a browser on **2026-09-21**, with
the billing toggle set to both the discounted term and the monthly term where the page offered
one. Nothing here comes from a third-party review site, a reseller page or an aggregator.

Sources, one per vendor:

| Vendor | Page read |
|---|---|
| Kinsta | https://kinsta.com/pricing/ |
| Cloudways | https://www.cloudways.com/en/pricing.php |
| WP Engine | https://wpengine.com/plans/ |
| SiteGround | https://www.siteground.com/wordpress-hosting.htm |
| hosting.com | https://hosting.com/hosting/platforms/wordpress-hosting/ |

Prices exclude tax and are as published for the country the page was viewed from. Vendors run
promotions and A/B test their pricing pages, so treat the checked date on each row as part of
the data, not decoration.

## Columns worth explaining

- `entry_price_per_month_usd` — the monthly-equivalent figure shown for the discounted term.
  For vendors that do not discount, it equals the monthly price.
- `monthly_price_usd` — what the vendor charges on monthly billing, where offered.
- `year_1_total_usd` — what you actually pay in year one, including a prepaid year written as
  a single payment.
- `renewal_price_per_month_usd` — the rate after the first term, as published by the vendor or
  derived from the standard rate they publish.
- `three_year_total_usd` — year one at the first-term price plus two years at the renewal rate.
  Left as `unknown` where the vendor does not publish a renewal rate.
- `est_visits_per_month` — the vendor's own published allowance. Not a measurement.

## What this dataset does not contain

- No performance figures. No TTFB, no uptime, no load-test results. We have not benchmarked
  these hosts and we do not publish numbers we cannot reproduce.
- No affiliate-adjusted ordering. Rows are sorted by vendor and plan, never by who pays us.
- No support-quality scores. Those are judgement calls, not data.

## Known gaps

- WP Engine does not publish renewal pricing, so its three-year total is `unknown` by the
  vendor's own terms rather than by omission here.
- Cloudways publishes a long tier list across five cloud providers. Only the DigitalOcean
  entry, mid and top tiers are included.
- hosting.com's shared hosting line is not covered. This dataset follows the managed WordPress
  lineup, which is what the pages on the site compare.

## License and citation

Released under **CC BY 4.0**. Use it, quote it, chart it, in commercial or non-commercial work.
The only condition is attribution.

> Wiser Tools, "Managed WordPress hosting price index (2026-09-21)",
> https://wiser-tools.com/wordpress-hosting-price-index

If you build on it, a link back is the whole payment. Corrections are welcome: if a vendor has
changed a price and you can point at the page, the next edition will carry the fix and the date.

## Changelog

- **2026-09-21** — first edition. Three of the five vendors had changed plan names, prices or
  billing terms since the previous round of checks, which is why every row carries its own
  checked date.

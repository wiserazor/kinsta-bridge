# Kinsta Bridge Page — deploy-ready

A single-page, affiliate-compliant "bridge page" for promoting the **Kinsta** managed
WordPress hosting affiliate program via Google Ads search traffic.

You already have GitHub + Cloudflare, so deployment is ~10 minutes.

---

## 1. Apply to the Kinsta affiliate program

1. Go to **https://kinsta.com/affiliates**
2. Fill in your **website URL** (use the live page URL from step 2 below) and how you'll promote.
3. Manual review (1–3 days). Weak-content / coupon sites get rejected — this page is substantive, so you're fine.
4. Once approved, in the affiliate dashboard click **Create affiliate link**, paste any Kinsta URL, copy your tracked link.
5. In `index.html`, replace every `REPLACE_WITH_YOUR_KINSTA_AFFILIATE_LINK` with your real link.

**Program terms (2026):**
- Commission: **$50–$500 one-time + 10% monthly recurring for life**
- Cookie: **60 days**, last-touch attribution
- Payout: PayPal, min $50, paid 15th–20th each month
- Churn: ~2–4% (your recurring income compounds)

⚠️ **Paid-search rule:** You may NOT bid on Kinsta **branded** keywords
("Kinsta", "Kinsta coupon", "Kinsta promo"). Generic high-intent keywords are fine.

---

## 2. Deploy to Cloudflare Pages (via GitHub)

```bash
# from this folder
git init
git add index.html
git commit -m "Kinsta bridge page"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
```

Then in Cloudflare:
1. **Dashboard → Pages → Create a project → Connect to Git**
2. Authorize GitHub and select this repo.
3. Build settings: **Framework preset = None**, **Build command = (empty)**, **Output directory = `/`**
4. Deploy. You get `https://<project>.pages.dev`.
5. (Optional but recommended) Buy a domain (~$10/yr at Namecheap/Porkbun) and add it in
   **Pages → Custom domains** (Cloudflare auto-adds the DNS record).

Use the live URL as your affiliate application website AND your Google Ads final URL.

---

## 3. Google Ads setup

- Open a Google Ads account with a foreign-currency / dual-currency card (or Google gift-card top-up).
- Create one **Search** campaign only (no Display/Discovery at first).
- Final URL = your bridge page URL. **Never** put the affiliate link in the ad.
- Start budget **$10–20/day**.

### Keyword targets (SAFE for paid search — all non-branded)
- `best managed wordpress hosting 2026`
- `managed wordpress hosting comparison`
- `fastest wordpress hosting`
- `wordpress hosting for agencies`
- `high traffic wordpress hosting`
- `wordpress hosting with staging`

### Keywords to AVOID in paid search (Kinsta brand-protected)
- `kinsta` · `kinsta coupon` · `kinsta promo` · `kinsta discount`
- Anything containing the "Kinsta" word. (These are fine for organic blog content, not for ad bids.)

### Negative keywords (add to the campaign)
`free` `cheap` `coupon` `discount` `jobs` `how to` `tutorial` `reddit` `login` `careers`

### Match & optimization
- Use **exact / phrase** match to start; review the Search Terms report weekly.
- Negate any expensive non-converting queries after ~2 weeks.
- Raise budgets only on ad groups where ROAS > 2.

---

## 4. Compliance checklist before you launch
- [ ] Top disclosure banner visible (already in the page)
- [ ] Footer disclosure present (already in the page)
- [ ] Affiliate links would carry `rel="sponsored"` — Kinsta's generated links add this automatically
- [ ] Page is original, ~1000+ words, and relevant to the ad
- [ ] Ad final URL points to THIS page, not the affiliate link
- [ ] No branded-Kinsta keyword bids
- [ ] Small budget test first, then scale

---

## 5. Files
- `index.html` — the bridge page (edit copy + swap affiliate link)
- `README.md` — this file

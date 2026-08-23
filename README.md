# Wiser Tools — Kinsta bridge page (deploy-ready)

A single-page, affiliate-compliant **bridge page** for the **Kinsta** managed WordPress
hosting affiliate program, served from the generic brand **wiser-tools.com** so the
site can later expand to other tracks (VPN, email marketing, CRM, …) via subpaths.

Stack: static HTML → GitHub → Cloudflare Pages.

---

## 1. Apply to the Kinsta affiliate program

1. Go to **https://kinsta.com/affiliates**
2. Fill in your **website URL** (`https://wiser-tools.com`) and how you'll promote.
3. Manual review (1–3 days). Weak-content / coupon sites get rejected — this page is substantive, so you're fine.
4. Once approved, in the affiliate dashboard click **Create affiliate link**, paste any Kinsta URL, copy your tracked link.
5. In `index.html`, replace every `REPLACE_WITH_YOUR_KINSTA_AFFILIATE_LINK` with your real link.
6. Commit + push — Cloudflare Pages redeploys automatically.

**Program terms (2026):**
- Commission: **$50–$500 one-time + 10% monthly recurring for life**
- Cookie: **60 days**, last-touch attribution
- Payout: PayPal, min $50, paid 15th–20th each month
- Churn: ~2–4% (your recurring income compounds)

⚠️ **Paid-search rule:** You may NOT bid on Kinsta **branded** keywords
("Kinsta", "Kinsta coupon", "Kinsta promo"). Generic high-intent keywords are fine.
(You also should NOT put the word "Kinsta" in ad headlines — see `google-ads-copy.md`.)

---

## 2. Connect the domain & deploy (Cloudflare)

GitHub repo already pushed: **https://github.com/wiserazor/kinsta-bridge**

In Cloudflare:
1. **Dashboard → Workers & Pages → Create → Pages → Connect to Git**
2. Authorize GitHub, select `wiserazor/kinsta-bridge`.
3. Build settings: **Framework preset = None**, **Build command = (empty)**, **Output directory = `/`**.
4. Deploy → you get `https://kinsta-bridge.pages.dev`.
5. **Pages → Custom domains → Add `wiser-tools.com`**. Cloudflare auto-adds DNS (the domain is already in Cloudflare Registrar, so no nameserver change needed).

Use `https://wiser-tools.com` as your affiliate application website AND Google Ads final URL.

---

## 3. Google Ads setup

See **`google-ads-copy.md`** for ready-to-paste headlines, descriptions, keywords and campaign settings.

- One **Search** campaign only (no Display/Discovery at first).
- Final URL = `https://wiser-tools.com/`. **Never** put the affiliate link in the ad.
- Start budget **$10–20/day**.
- Target English-speaking markets (US / UK / CA / AU) to match Kinsta's billing & the page language.

---

## 4. Expanding to more tracks later

The brand is generic on purpose. To add a second vertical (e.g. VPN):
- Create a folder, e.g. `vpn/index.html`, reusing this layout with different copy.
- Link it from a small hub on the root page.
- Run a separate Google Ads campaign pointing at `/vpn/`.
Each subpath shares the domain's authority — cheaper than spinning up new domains.

---

## 5. Compliance checklist before launch
- [ ] Top disclosure banner visible (already in the page)
- [ ] Footer disclosure present (already in the page)
- [ ] Affiliate links carry `rel="sponsored"` — Kinsta's generated links add this automatically
- [ ] Page is original, ~1000+ words, and relevant to the ad
- [ ] Ad final URL points to `wiser-tools.com`, not the affiliate link
- [ ] No branded-Kinsta keyword bids; no "Kinsta" in ad headlines
- [ ] Small budget test first, then scale

---

## 6. Files
- `index.html` — the bridge page (brand: Wiser Tools; copy: Kinsta comparison; swap affiliate link)
- `README.md` — this file
- `google-ads-copy.md` — Google Ads campaign + ad copy

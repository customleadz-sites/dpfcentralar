# Austin Nightengale — DPF Alternatives Central Arkansas — Google Ads Landing Pages

Two short, message-matched landing pages for the two ad groups in campaign `Leads-Search-1`
(Google Ads account 3640813121, "Austin Nightingale" — note spelling differs from Kennedy's folder):

| Page | Ad group | Intent mode |
|---|---|---|
| `index.html` | DPF Cleaning ("DPF Cleaning & Restoration" pinned H1) | Quote-first: call + 3-field form |
| `forced-regen.html` | Forced Regen ("Roadside DPF Forced Regen" pinned H1) | Emergency: giant call button, callback form secondary |
| `thanks.html` | form redirect target — form conversion fires here | |
| `privacy.html` | footer link (SMS/call-recording clauses included) | |

Design: industrial diesel — navy `#0E1D2E` base with the REAL franchise brand colors:
blue `#2BA4DD` (accents) + green `#8DC640` (CTA buttons), from the DPF Alternatives logo SVG.
Barlow Condensed + Barlow, hazard-stripe dividers. Both pages `noindex`. Sticky mobile call
bar (sticky-not-fixed Safari recipe, appears after the hero).

## Images (`images/` — pulled from dpfalternatives.com, Austin's own franchise)

In use: `dpf-alternatives-truck.jpg` (index
hero bg), `dpf-cleaning-23.jpg` (cleaning machine, benefits), `lifetime-warranty.png`
(guarantee banner), `semi-truck.jpg` (regen hero bg), `dpf-van.jpg` (regen fallback card bg).
Spares kept for swaps: warranty badges (6mo/1yr), equipment cutouts (ultrasonic tank, flow
bench), `diesel-truck-3.jpg`, `dpf-vehicle-4.jpg`, EPA logo. NOTE (Kennedy, Aug 2026): we are NOT allowed to use the DPF Alternatives logo files — header is a CSS text wordmark; logo SVGs deleted from images/.
Photos of AUSTIN's actual shop/van would still beat these — ask him.

## Verified franchise facts (from dpfalternatives.com location data, Aug 2026)

- Owner: Austin Nightingale · Store No. 056 · opened 06/2023 · Dardanelle, AR 72834
- Hours: Mon–Fri 8:00–5:00, Sat 8:00–12:00 (ad schedule matches: Mon–Fri 7–7 + Sat 8–12)
- Email: littlerock.ar@dpfalternatives.com (owner: austin.nightingale@dpfalternatives.com)
- GBP: https://maps.app.goo.gl/DVWkpYgHL9MBsGBY6 · review link https://g.page/r/CebT9ixaTndVEBM/review
- Facebook: facebook.com/DPFAlternativesLittleRock · franchise GA4 on his location page: G-515MWJTM8S
- Service levels 1–5 (air-knife → bake → flush → ultrasonic → +Max Mileage): warranties
  6-month (L3), 1-year (L4, "up to 99% useful life"), Lifetime options (L5)
- National line 833-373-2583 exists — NEVER use it on our pages; leads go to Austin's (479) 280-7482

## MUST DO BEFORE LAUNCH (all currently stubbed)

1. **Web3Forms key** — both forms have `access_key = YOUR_WEB3FORMS_KEY`. Create a key
   (web3forms.com, needs a delivery email — ask Austin which email gets leads), replace in BOTH
   forms, and test-submit once. A placeholder key renders fine and silently loses every lead.
2. **Form redirect URLs** — both forms redirect to `https://REPLACE-AT-DEPLOY/thanks.html`.
   DONE — set to dpfcentralar.vercel.app.
3. **gtag** — every page has a commented tracking block with `AW-XXXXXXXXXX`. At launch:
   create a Google Ads website-call conversion + a form conversion, then uncomment and fill in
   the AW id + the form conversion label in `thanks.html`. The phone snippet
   (`phone_conversion_number`) handles call tracking — do NOT also fire tel-click conversions
   (double-count).
4. **Austin's own photos** — franchise stock is in place; swap in his real shop/van/filter
   photos when he sends them (they'll convert better than corporate shots).

## Claims discipline (all sourced — don't invent more)

- "Guaranteed results — or you don't pay", Lifetime Performance Warranty, free pickup &
  delivery: from dpfalternatives.com (franchise site). NOTE (Kennedy): do NOT say "hand-cleaned" — the process is machine/ultrasonic.
- "24-hour turnaround", "I-40 Ozark to Little Rock", "24/7 emergencies": from Austin's own
  running ads (message match). Franchise site says 24–48h — if Austin can't do 24h, soften it.
- NO review counts/stars anywhere (we have no review data), no licensing claims.
- The FAQ explicitly says **no DPF deletes** (illegal) — this also pre-qualifies the delete
  traffic the negatives don't catch.

## Deploy (when approved)

Follow the git-deploy skill. Repo under customleadz-sites; Vercel domain with NO hyphens
(`dpfcentralar.vercel.app`). `vercel.json` in this folder has the
cache rules (code files must-revalidate, never immutable).

Related: audit + change log in `../google-ads/reports/2026-08-27-audit.md`.

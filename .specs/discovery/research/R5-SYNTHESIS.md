# R5 — Synthesis: Any Niche, Proven Money

> Date: 2026-09-24. Method: `../R5-CRITERIA.md`. Inputs: `R5-A-verified-revenue.md`, `R5-B-consumer-platforms.md`, `R5-C-adult-stigmatised.md` (incl. §6 Play Store check), `R5-D-boring-content-data.md`.

## 1. Verdict

**First survivor across R1–R5. It is a *pattern*, not yet a niche: Brazil-only consumer "life-admin" apps in PT-BR, found via App Store/Play search (ASO) and Google SEO, paid by in-app subscription.**

**Status: GO for a cheap sub-niche selection round (R6). NOT yet GO for building.** A specific sub-niche must pass a keyword/competition check first.

| Workstream | Candidates | Survive | Uncertain | Kill |
|---|---|---|---|---|
| A. Verified-revenue sources (1,876 TrustMRR startups parsed) | 17 clusters | **1** | 8 | 8 |
| B. Consumer & platform ecosystems | 30 | 0 | 4 | 26 |
| C. Adult & stigmatised | 19 | 0 (tarot survivor killed by Play Store check) | 6 | 13 |
| D. Boring / content / data | 20 | 0 | 5 | 15 |

## 2. The survivor

**Proven earners (payment-verified on TrustMRR via RevenueCat/Stripe):**

| App | What | MRR | Subs | Launched | Channel |
|---|---|---|---|---|---|
| Parceladinho | Credit-card instalment tracker ("parcelas"), reads bills by photo/PDF | $2.07k | 444 | 2026 | ASO + how-to SEO ("como ver compras parceladas Nubank") |
| Enxovaly | Baby-layette ("enxoval") planner + family gift registry | $1.79k ($8.5k last 30d) | — | Jun 2026 | ASO, blog, SEO (per founder); TikTok unconfirmed |
| Convitede | Digital invitations shared on WhatsApp | $1.24k | 393 | 2023 | SEO template pages |
| Pluma | Personal finance (Open Finance) | $1.34k | 200 | 2025 | n/d |

The same pattern works in other countries (DE Mahlzait, FR Francopass/Kickly, BG TollTracker, ES/LatAm Tortolitos). That makes it a repeated mechanism, not one lucky app.

**Why it fits the founder:** Brazilian, so he has the local knowledge and language foreign developers lack. Solo build is 4–8 weeks. Running cost is ~€10–25/mo (Apple $99/yr, Google $25 one-time, cheap backend). Ops are low (store reviews and support email). No calls. No audience needed: the channel is search.

**Economics:** revenue per subscriber is observed at ~$3–5/mo gross. **€1k MRR ≈ 270–400 subscribers**, or 2–3 small apps of this kind.

## 3. Where the gap is, and where it isn't

- **It is:** **Brazil-only problems that global apps don't model**: instalments, enxoval, WhatsApp-first sharing, Brazilian bureaucracy and life events. Parceladinho beat existing weak local apps (Minhas Parcelas, Parcelex) within months, so quality still wins against weak local incumbents.
- **It isn't:** **Portuguese translations of global app categories.** Those are already filled. AI tarot/astrology (Lumi 1M+ installs, Tarot IA, Astrea, Personare), calorie apps (FitCal, Cal AI), Bible apps (Hallow, Bible Chat, Bíblia IA), MEI apps, ID photos and AI humanizers all have PT versions. Brazilian web content, data products and SEO sites were also killed (R5-D: AI Overviews in PT, low RPM, free government data).

## 4. What killed everything else (R5)

- **English consumer apps with money** grow through TikTok/Meta ads or influencers, which fails "minimal effort". RevenueCat: only **17.3%** of new subscription apps reach $1k/mo within 2 years. App submissions are up 84% while downloads are up 2–3%.
- **Adult:** payment processors (WishTender at $40k/mo profit closed after Stripe dropped it), age-verification laws (27 US states, UK OSA, Brazil ECA Digital since Mar 2026), OnlyFans bans automation bots. The TrustMRR scan found no small AI-girlfriend or OnlyFans tool at ≥$1k MRR.
- **Content/SEO/ads:** AI answer engines, the end of domain-parking AdSense (Feb 2026), and the 30–50% lower Brazilian ad earnings per 1,000 views.

## 5. Honest risk

- The base rate is poor: most new subscription apps never reach $1k/mo. The four earners are the **survivors we can see**. The TrustMRR Brazil list also has several PT apps earning $0–160/mo. **Expect 1 in 3–5 apps to work**, so plan a small portfolio, not one bet.
- Low Brazilian prices (R$5–20) mean each sub-niche is small.
- Public revenue invites clones (Parceladinho is on TrustMRR).
- Platform risk: store ranking changes, or a bank shipping the feature natively (e.g. Nubank showing instalments).
- **No outcome can be guaranteed. This is the best-evidenced bet found across ~280 candidates in five rounds, not a sure thing.**

## 6. Next step (founder decision UD-013)

**R6 — sub-niche selection (desk + scraping, no build, ~1 session):**
1. Brainstorm 30–50 **Brazil-only** recurring life-admin problems: bureaucracy, life events, Brazilian money habits, school, condominium, vehicle, pets, health-plan paperwork (non-clinical), rent, etc.
2. For each, scrape the BR App Store/Play search (installs, reviews, last update, rating, IAP) and Google results. Score for **demand** (search volume proxies, forum questions, reviews that ask for features) against **weak incumbents** (old, low-rated, no subscription, not updated).
3. Pick the top 2–3 and write a one-page spec for each (MVP scope, paywall, keyword set).
4. Kill rule: if no sub-niche shows both demand and weak incumbents, stop.

Then a **Planning Gate** on one app: build the MVP in ≤6 weeks, ship to Play/App Store, and judge by pre-committed thresholds (e.g. installs and paid conversion by week 8).

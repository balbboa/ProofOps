# R5-A — Verified-Revenue Sources: Solo Earners and Niche Clusters

> Date: 2026-09-24 · Reference: `../R5-CRITERIA.md` (gates G1–G6, kills K-R5-1..5)
> Workstream: R5-A (TrustMRR, Acquire, Microns, Flippa, Indie Hackers, Starter Story, open-startup dashboards)
> Founder: solo developer in Brazil, target €1k+ MRR, minimal effort. No moral filter.

**Bottom line:** 1 cluster survives: **Brazil-specific consumer "life-admin" apps in PT-BR** (Parceladinho, Enxovaly, Convitede, Pluma). It is a *pattern* more than one niche, and every sub-niche still needs its own keyword check. 8 clusters are UNCERTAIN and 8 are KILLED. The main segment finding (§4): the clusters with the most solo earners in English (calorie scanners, couples apps, looksmaxxing, AI marketing tools) are crowded and grow through TikTok or Meta ads. The repeated signal that fits this founder is **local-language, country-specific utility apps found through app-store search (ASO) and SEO**.

---

## §0 Coverage note

| Source | What was done | Status |
|---|---|---|
| **TrustMRR** (trustmrr.com) | The listing pages and category pages returned HTTP 500 errors or timed out (`/startups/page/N`, `/category/*`). I worked around this: I took all 7,928 startups with lifetime revenue from `/revenue-forest`, picked the 2,125 with ≥ $5k lifetime revenue, and pulled their detail pages. **1,876 parsed. 1,197 fall in the $1k–$40k/month band** (30-day revenue or MRR). All figures are verified through the payment processor (Stripe, RevenueCat, Superwall, Polar, LemonSqueezy, Dodo, Whop, Paddle), unless noted "key expired". Team size is **rarely disclosed**. Where only one founder is named, I write "1 named founder (size n/d)". | Main source |
| TrustMRR `/country/br` | Fetched in full. About 200 Brazil-based listings, and only ~15 of them are at ≥ $1k/month. | OK |
| **Acquire.com** | Listings sit behind a login. Only generic search results came back. | **BLOCKED** |
| **Flippa** | No direct browsing (the pages are rendered in JavaScript). I read 3 listing pages through search results and fetches. They are "Vetted" listings, meaning Flippa checked revenue, expenses and traffic. | Partial |
| **Microns.io** | Homepage plus the SaaS, mobile-app and directory category pages (first 12 listings each; the rest need a login). Almost every listing is under $1k/month. | Partial |
| Indie Hackers / Starter Story | Search results only. The interviews found (Habit Pixel, Flame, Oasis) are self-reported and mostly TikTok-driven. | Thin |
| Open-startup lists (openstartuplist.com, Baremetrics Open) | Directory pages show no revenue figures. These are old, larger companies. | Not useful |
| **Budget used** | **~40 WebSearch calls**, ~10 WebFetch calls, plus about 2,200 plain HTTP page fetches of TrustMRR detail pages. | Within the ~110 cap |

Caveats:
- TrustMRR is a **survivorship-biased, self-selected** sample: founders list themselves, and many are build-in-public people with X (Twitter) audiences.
- "30d" means revenue in the last 30 days. "MRR" means recurring revenue at the moment. Products that sell one-time licences show MRR = $0.
- Base rate from RevenueCat's 2026 report, as quoted in a secondary source: the median subscription app earns < $50/month after 12 months, and only **17.2 % ever reach $1k/month** ([theswiftk.it summary](https://theswiftk.it.com/blog/zero-to-10k-mrr-indie-ios-app)). UNVERIFIED against the primary report.

---

## §1 Raw table — small products with ≥ $1k/month (selected, grouped by niche)

V = verified by payment processor through TrustMRR, unless marked. "Key exp." = the processor key has expired, so the figure is the last verified value. Flippa "Vetted" = Flippa checked the P&L.

| Name | Niche | Revenue (30d / MRR) | Verified? | Team | Founded | URL |
|---|---|---|---|---|---|---|
| Parceladinho | BR credit-card instalment tracker (iOS) | $3.5k / **$2.07k** (444 subs) | V RevenueCat | n/d | 2026 | https://trustmrr.com/startup/parceladinho |
| Enxovaly | BR baby-layette ("enxoval") planner app | $8.5k / **$1.79k** | V RevenueCat | 1 named (Gabriel Buzzi Venturi) | Jun 2026 | https://trustmrr.com/startup/enxovaly |
| Convitede | BR digital invitations (SEO templates) | $2.1k / **$1.24k** (393 subs) | V | 1 named | 2023 | https://trustmrr.com/startup/convitede |
| Pluma | BR personal finance (Open Finance) | $1.3k / **$1.34k** (200 subs) | V | 1 named | 2025 | https://trustmrr.com/startup/pluma |
| FitCal | BR AI calorie tracker ("#1 in Brazil") | $0.7k / **$5.8k** | V (key issue) | **2–5** | 2024 | https://trustmrr.com/startup/fitcal |
| DivineTalk | Scripture AI chat (BR founder) | $0.6k / $1.6k | V | 1 named | 2025 | https://trustmrr.com/startup/divinetalk |
| Mahlzait | German-language AI calorie tracker | $2.3k / $2.2k | V RevenueCat | 1 named | 2026 | https://trustmrr.com/startup/mahlzait |
| TollTracker | Bulgaria average-speed toll app | $5.9k / $4.8k | V | n/d | 2025 | https://trustmrr.com/startup/tolltracker |
| Francopass | French naturalisation test prep | $3.4k / $1.5k | V (stale) | 1 named | 2025 | https://trustmrr.com/startup/francopass |
| Get Brazil Visa | BR digital-nomad visa helper (service) | $2.3k / — | V | 1 named | 2025 | https://trustmrr.com/startup/get-brazil-visa |
| Send Letters Online UK | Online post-office alternative | $5.5k / — | V | 1 named | 2026 | https://trustmrr.com/startup/send-letters-online-uk |
| Subbasta | Malta judicial property sales | $6.7k / $3.7k | V | n/d | 2025 | https://trustmrr.com/startup/subbasta |
| TrackAI | AI calorie photo tracker | $22.5k / $20.1k | V | 1 named | 2025 | https://trustmrr.com/startup/trackai |
| Nutria | AI nutrition app (Chile) | $20.3k / $14.7k | V (stale) | 1 named | 2025 | https://trustmrr.com/startup/nutria |
| Goodie AI | Food scanner | $11.6k / $12.9k | V | n/d | — | https://trustmrr.com/startup/goodie-ai |
| ChefGPT | Calorie/meal plan | $1.4k / $2.0k | V | n/d | — | https://trustmrr.com/startup/chefgpt |
| Bibly | Bible verses and study app | $2.3k / $5.0k | V (stale) | 1 named | 2025 | https://trustmrr.com/startup/bibly |
| Divine Widgets | Christian Bible widget app for women | $4.4k / $1.3k | V Superwall | **1 person** | 2026 | https://trustmrr.com/startup/divine-widgets |
| DivineTV | Christian streaming | $8.7k / $8.8k | V Superwall | n/d | 2026 | https://trustmrr.com/startup/divinetv |
| Viven | Bible quiz/reader | $0.1k / $1.9k | V | 1 named | 2025 | https://trustmrr.com/startup/viven-bible-in-action |
| Tariq | Quran reading app | $20.4k / $5.7k | stale | 1 named | — | https://trustmrr.com/startup/tariq-1 |
| Mathani | Quran memorisation | $1.4k / $1.8k | V | 1 named | 2025 | https://trustmrr.com/startup/mathani |
| Sunnah Fasting app | Muslim fasting app | ~$940/mo ($11.3k/yr) | Microns (metrics claimed verified) | n/d | — | https://www.microns.io/ |
| Debatium | Couples conversation game | $20.4k / $17.0k | stale | 1 named | — | https://trustmrr.com/startup/debatium |
| Lovelee | Couples app | $2.1k / $1.9k | V | 1 named | 2025 | https://trustmrr.com/startup/lovelee |
| Dovey | Long-distance couples cards | $1.7k / $2.5k | V | 1 named | 2026 | https://trustmrr.com/startup/dovey |
| CoupleAI | Couples app (Spain) | $4.1k / $3.3k | stale | 1 named | 2025 | https://trustmrr.com/startup/coupleai |
| Tortolitos | Couples app (Spanish-named) | $0.4k / $2.2k | V | 1 named | 2026 | https://trustmrr.com/startup/tortolitos |
| Zero Contact | Post-breakup no-contact app | $13.6k / $8.1k | V | 1 named | — | https://trustmrr.com/startup/zero-contact |
| Sober Tracker | Sobriety tracker | $5.0k / $1.5k | V | 1 named | — | https://trustmrr.com/startup/sober-tracker |
| Unlust | Porn-addiction recovery | $1.2k / $1.7k | V | 1 named | 2025 | https://trustmrr.com/startup/startup-3c33a13b7f52 |
| Steady | Fear of flying | $5.4k / $3.1k | V | 1 named | 2026 | https://trustmrr.com/startup/steady-fear-of-flying |
| FaceKit | Looksmaxxing face analysis | $22.0k / $20.4k | V | 1 named | 2025 | https://trustmrr.com/startup/facekit |
| Glamour | AI colour analysis | $11.1k / $10.2k | V | 1 named | — | https://trustmrr.com/startup/glamour |
| Hairly AI | Hairstyle preview | $11.3k / $11.5k | V | n/d | — | https://trustmrr.com/startup/hairly-ai |
| Insect Bite ID | AI photo identifier | $3.5k / $2.4k | V | 1 named | — | https://trustmrr.com/startup/insect-bite-id |
| Jewelry Identifier | AI photo identifier | $5.0k / $2.0k | V | **2–5** | — | https://trustmrr.com/startup/jewelry |
| Fishing AI | AI fishing companion | $4.0k / $2.2k | V | 1 named | — | https://trustmrr.com/startup/fishingai |
| Numbers Game | AI football predictions | $5.3k / $4.6k | V | 1 named | 2021 | https://trustmrr.com/startup/numbers-game-limited |
| ParlayPlug | AI betting insights app | $5.3k / $5.1k | V | 1 named | 2026 | https://trustmrr.com/startup/parlayplug |
| Kickly Pronos IA | French AI betting tips | $10.0k / $7.9k | V | **1 person** | 2026 | https://trustmrr.com/startup/kickly-pronos-ia |
| Elofoot | AI football predictions | $3.9k / $2.5k | key exp. | 1 named | 2026 | https://trustmrr.com/startup/elofoot |
| Predigoal | AI football predictions | $4.9k / $3.0k | V Whop | n/d | 2026 | https://trustmrr.com/startup/predigoal |
| PolyPick | Prediction-market AI | $7.7k / $11.2k | V Whop | 1 named | 2026 | https://trustmrr.com/startup/polypick |
| FreeTCF | TCF Canada French test prep | $25.3k / $25.8k | V RevenueCat | n/d | 2025 | https://trustmrr.com/startup/freetcf |
| Tree Nerd Academy | ISA arborist exam prep | $30.4k / — | V | expert-led (Chris Comer) | 2025 | https://trustmrr.com/startup/tree-nerd-academy |
| Writing9 | IELTS essay checker | $5.5k / $5.0k | V | 1 named | 2018 | https://trustmrr.com/startup/writing9 |
| CaseTutor | Case-interview prep | $2.5k / $2.3k | V | 1 named | 2025 | https://trustmrr.com/startup/casetutor-inc |
| Road to Offer | Case-interview prep | $3.3k / $2.7k | V | 1 named | 2026 | https://trustmrr.com/startup/road-to-offer |
| Lunchbreak | AI-detection bypass | $36.1k / $33.2k | V | n/d | 2023 | https://trustmrr.com/startup/lunchbreak |
| WriteHybrid | AI humanizer | $4.9k / $5.1k | key exp. | 1 named | 2025 | https://trustmrr.com/startup/writehybrid |
| CheatMate | Exam-assist extension | $5.3k / $7.4k | V | 1 named | 2025 | https://trustmrr.com/startup/cheatmate |
| ExtraDock | macOS extra-dock utility (one-time) | $6.5k / — | V | 1 named (Appit Studio) | Dec 2025 | https://trustmrr.com/startup/extradock |
| ScreenSnap Pro | Mac screenshot tool (one-time $39) | $4.7k / — | key exp. | 1 named | 2025 | https://trustmrr.com/startup/screensnap-pro |
| Screen Charm | Mac screen recorder (one-time $79) | $3.1k / — | V | 1 named | 2023 | https://trustmrr.com/startup/screen-charm |
| Sandimax / Wallper | Mac live wallpapers ($5 one-time) | $15.0k / — | V | small team | 2025 | https://trustmrr.com/startup/sandimax |
| Second Phone Number (iOS) | Virtual numbers | ~$6.3k avg, recently $8k+/mo; ~2 h/week | **Flippa Vetted** | **solo** | ~2022 | https://flippa.com/11521641-second-phone-number-app-with-70k-annual-revenue-and-1m-downloads-no-marketing-expenses-all-organic |
| 4-app temp-number portfolio | Temp numbers + temp email | $8.5k rev / $4.7k profit | **Flippa Vetted** | n/d | 2022 | https://flippa.com/12706601-4-app-utility-portfolio-3-temp-number-apps-1-temp-email-app-8-5k-last-month-50-margin-90-us-users-autopilot-strong-demand-sold-all-together |
| GoSimless | Virtual numbers for WhatsApp | $4.3k / $4.2k | V | n/d | 2022 | https://trustmrr.com/startup/gosimless |
| SMSVia | Receive-SMS numbers (ASO) | $1.4k / $1.2k | V | 1 named | 2026 | https://trustmrr.com/startup/smsvia |
| InstaTrack | Instagram follow tracker | $8.9k / $6.2k | stale | 1 named | 2026 | https://trustmrr.com/startup/instatrack |
| Last Followed | Instagram follow tracker | $6.7k / $5.9k | V | n/d | 2025 | https://trustmrr.com/startup/last-followed |
| Snap2Pass | Passport/ID photos | $7.1k / — | V | 1 named | 2023 | https://trustmrr.com/startup/snap2pass |
| Passport Photo Ready | US passport photo editor | $1.1k / — | V | n/d | 2026 | https://trustmrr.com/startup/passport-photo-ready |
| PostalForm | Mail PDFs from phone | $5.9k / — | V | n/d | 2024 | https://trustmrr.com/startup/postal-form |
| Alchie | French LinkedIn post AI | $19.4k / $15.6k | V | 1 named (established ghostwriter) | 2026 | https://trustmrr.com/startup/alchie |
| Tiny Startups / Startup Fame / OpenAlternative | Indie-maker directories | $3.3k / $2.4k / $5.5k (30d) | V | 1 named each | 2024 | https://trustmrr.com/startup/tiny-startups · /startup-fame · /openalternative |
| Etsy Market Research Tool | Seller tool | ~$780/mo ($9.4k/yr) — below bar | Microns | n/d | — | https://www.microns.io/ |
| Bulk File Downloader | Chrome extension | ~$700/mo profit — below bar | Flippa | solo | 2025 | https://flippa.com/12085118 |

---

## §2 Niche clusters

"# solo ≥$1k" counts products at ≥ $1k MRR (or 30-day revenue) where only one founder is named or team size is 1. Team size is mostly **not disclosed**, so treat these counts as upper bounds.

| # | Cluster | # solo earners ≥$1k | G1 | G2 | G3 | G4 | G5 | G6 | Verdict | Decisive reason |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **Brazil-specific consumer "life-admin" apps (PT-BR, App Store/Play)** | 4 (Parceladinho, Enxovaly, Convitede, Pluma) + FitCal (2–5) | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | **SURVIVE** | 3 of 4 launched 2025–26 and grew through ASO/SEO in Portuguese, with no audience. The gap: global apps don't serve Brazilian habits (card instalments, enxoval, WhatsApp invitations). |
| 2 | Country-specific utilities, non-Brazil (BG tolls, FR naturalisation, UK letters, Malta auctions, DE landlords) | ≥5 | ✅ | ⚠️ | ✅ | ✅ | ✅ | ✅ | UNCERTAIN (evidence for #1) | Proves the pattern works. The founder lacks local knowledge and language in those countries. Spanish LatAm is the only plausible extension. |
| 3 | AI calorie / food-scanner apps | ≥5 (TrackAI, Nutria, Mahlzait, ChefGPT, Pandish) | ✅ | ❌ | ✅ | ⚠️ | ⚠️ | ✅ | **KILL** | PT-BR is already taken (FitCal "#1 in Brazil" with influencers; Cal AI localised). Leaders grow through Meta ads and TikTok (K-R5-4). |
| 4 | Faith apps (Christian / Muslim) | ≥6 (Bibly, Divine Widgets, Viven, DivineTalk, Mathani, Nuraly) | ✅ | ❌ (PT) | ✅ | ⚠️ | ✅ | ✅ | UNCERTAIN (KILL for PT-BR) | The PT-BR App Store already has Bíblia IA (R$19.90/mo), Bible Chat and Hallow (R$55.90/mo, localised), plus free YouVersion/Bíblia JFA. Several earners buy growth with Meta ads. |
| 5 | Couples / relationship apps | ≥5 (Debatium, Lovelee, Dovey, CoupleAI, Tortolitos) | ✅ | ⚠️ | ✅ | ❌ | ✅ | ✅ | **KILL** | Growth comes from TikTok, Instagram and influencers (Dovey, CoupleAI): constant content work fails G4. |
| 6 | Breakup / quit-habit / anxiety apps | ≥6 (Zero Contact, Sober Tracker, Unlust, Halo, Steady, StateShift) | ✅ | ? | ✅ | ⚠️ | ✅ | ✅ | UNCERTAIN | Proven money. Channels are mostly TikTok. The PT-BR competition was not checked. |
| 7 | Looksmaxxing / beauty AI analysis | ≥5 (FaceKit, Glamour, Hairly, Prettier, MamaSkin) | ✅ | ❌ | ✅ | ❌ | ⚠️ | ✅ | **KILL** | Driven by TikTok virality and paid ads (DailyGlowUp "2–3x ROAS"). Fad risk (K-R5-2). |
| 8 | AI photo-identifier utilities (bites, jewelry, fish, cars) | 3–4 | ✅ | ⚠️ | ✅ | ⚠️ | ✅ | ✅ | UNCERTAIN | Works, but no language or keyword gap was found. Channels are TikTok and Meta. |
| 9 | Sports-prediction AI tips | ≥6 (Numbers Game, ParlayPlug, Kickly, Elofoot, Predigoal, PolyPick) | ✅ | ❌ (PT) | ✅ | ⚠️ | ✅ | ⚠️ | UNCERTAIN (→ R5-C) | PT-BR already has goalAI, SportyTrader, "Palpites de Futebol IA" and PickStars. Stripe restricts "sports forecasting or odds-making"; use App Store IAP or Whop. |
| 10 | Niche exam / certification prep | ≥5 (FreeTCF, Writing9, Francopass, CaseTutor, Road to Offer) | ✅ | ⚠️ | ✅ | ⚠️ | ✅ | ✅ | UNCERTAIN | Proven through SEO. The biggest earner (Tree Nerd) is expert/creator-led (K-R5-1). In Brazil, ANBIMA replaced CPA-10/20/CEA with CPA/C-Pro R/C-Pro I in Jan 2026, but Udemy, TopInvest and FPS already cover them. Needs domain content. |
| 11 | AI humanizer / student "cheat" tools | ≥4 (Lunchbreak, WriteHybrid, CheatMate, Revolt) | ✅ | ❌ | ✅ | ✅ | ⚠️ | ⚠️ | **KILL** | PT-BR is saturated with free tools (QuillBot, ZeroGPT PT, iahumanizartexto). Platform and processor risk. |
| 12 | macOS one-time utilities | ≥5 (ExtraDock, ScreenSnap, Screen Charm, MacWall, SessionWatcher) | ✅ | ⚠️ | ✅ | ✅ | ✅ | ✅ | UNCERTAIN | Newcomers win through "X alternative for Mac" SEO (ExtraDock launched Dec 2025). But these are one-time sales with no MRR, there is no language gap, and every sub-niche needs its own keyword gap. |
| 13 | Virtual / second phone numbers | 3–4 (Flippa SPN solo, GoSimless, SMSVia) | ✅ | ⚠️ | ✅ | ✅ | ⚠️ | ⚠️ | UNCERTAIN | Solo, ~2 h/week, $6k+/month (Flippa-vetted). But carrier costs run ~$1k/month at scale, plus telecom compliance and fraud/abuse risk. The App Store is crowded. |
| 14 | Instagram follower trackers | 2 | ✅ | — | ✅ | ✅ | ✅ | ❌ | **KILL** | Scraping breaks Meta's terms of service, with a real risk of app-store removal or legal action (K-R5-5 / ToS). |
| 15 | B2B marketing AI (GEO/AI-visibility trackers, Reddit lead tools, LinkedIn post AI, faceless video) | many | ✅ | ❌ | ✅ | ❌ | ⚠️ | ✅ | **KILL** | ≥15 GEO trackers and ≥8 Reddit tools in the band alone. The top localised case (Alchie, FR) rests on the founder's existing ghostwriter audience (K-R5-1). The PT-BR LinkedIn AI space already has RedactAI PT, Hootsuite and Taplio. |
| 16 | Indie-maker directories / launch sites | ≥6 | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ | **KILL** | Rely on the founder's X audience (Marc Lou ecosystem) (K-R5-1). Saturated: Microns directory listings earn $60–$470 a year. |
| 17 | ID/passport photo and document utilities | 3 (Snap2Pass, Passport Photo Ready, PostalForm) | ✅ | ❌ (PT) | ✅ | ✅ | ✅ | ✅ | **KILL** (for PT) | visafoto.com and passport-photo.online are already localised in PT-BR. Brazilian passport photos are taken by the federal police (PF). |

---

## §3 Survivor deep-dive — Cluster 1: Brazil-specific consumer "life-admin" apps (PT-BR)

**What it is:** single-purpose iOS/Android apps (sometimes web) that solve an everyday problem specific to Brazil, sold through the app store's in-app purchases (IAP) at R$5–20/month and found through Portuguese app-store search (ASO) and SEO. **This is a pattern, not one niche.** G1 is met by ≥2 solo earners in the same pattern, not in the same sub-niche. Treat that as a weaker form of G1.

### 1. Proven earners
| Product | Revenue | Subs / price | Age | Channel | Source |
|---|---|---|---|---|---|
| Parceladinho (tracks credit-card instalments; reads bills by photo or PDF) | $2,066 MRR; $3,485 last 30d; $6.8k all-time | 444 subs; R$9.90/mo or R$59.90/yr | App ID 6760917181 → 2026 launch | ASO + how-to SEO pages ("como ver compras parceladas Nubank") | [TrustMRR](https://trustmrr.com/startup/parceladinho), [App Store](https://apps.apple.com/br/app/parceladinho-parcelas-cart%C3%A3o/id6760917181), [site](https://parceladinho.github.io/parceladinho/) |
| Enxovaly (baby-layette planner, gift registry shared with family) | $1,792 MRR; $8,506 last 30d | Pro R$ pricing ($2.99/mo, $7.99/yr as listed) | Launched 30 Jun 2026 | ASO, blog, SEO (per founder's listing) | [TrustMRR](https://trustmrr.com/startup/enxovaly), [site](https://enxovaly.com/en) |
| Convitede (digital invitations shared on WhatsApp) | $1,242 MRR; $2,118 last 30d | 393 subs; R$10–19.99/mo | Mar 2023 | SEO template pages, competing with FestaLab and Canva | [TrustMRR](https://trustmrr.com/startup/convitede), [site](https://convitede.com/convites/convite-digital-personalizado) |
| Pluma (personal finance, Open Finance) | $1,342 MRR | 200 subs; R$27–97/mo | Aug 2025 | n/d (heavier build: bank integrations) | [TrustMRR](https://trustmrr.com/startup/pluma) |
| FitCal (AI calorie tracker) — *not solo* | $5.8k MRR | $11.99/mo | 2024 | influencers (team of 2–5) | [TrustMRR](https://trustmrr.com/startup/fitcal) |
| Similar cases abroad: Mahlzait (DE calorie, $2.2k MRR, 2026), TollTracker (BG, $4.8k MRR), Francopass (FR, $1.5k MRR) | | | | | links in §1 |

All TrustMRR figures are processor-verified (RevenueCat or Stripe). Team size is not disclosed except for FitCal (2–5).

### 2. Distribution gap and channel
- **Gap:** language plus local culture. Global apps don't model Brazilian card instalments ("parcelas"), baby layettes ("enxoval"), gift-registry habits, or WhatsApp-first invitations. Parceladinho beat existing local apps (Minhas Parcelas, Parcelex) within months, so quality still wins against weak local incumbents.
- **Channel:** Portuguese keyword ASO; programmatic or how-to SEO pages targeting bank- and brand-specific queries (Parceladinho's GitHub Pages guides); built-in WhatsApp sharing (registry links, invitations) that brings in new users.
- **Adversarial check:** the obvious sub-niches are taken. MEI/DAS apps are crowded (MaisMei, Controlle, Gestão MEI). So are Bible apps and calorie apps. Each candidate needs a check of App Store search results and Google results before building.

### 3. MVP scope, build time, cost, ops
- **MVP:** one job done well. Local-first storage, optional photo/PDF OCR or an LLM step, RevenueCat paywall with a 3–7-day trial, Portuguese landing site plus 10–30 SEO how-to pages. React Native/Expo for iOS and Android.
- **Build:** 4–6 weeks part-time (G3 ✅).
- **Monthly cost:** Apple $99/yr (~€8/mo), Google $25 one-time, RevenueCat free up to $2.5k/month in tracked revenue, LLM/OCR €5–40/mo, domain and hosting ~€5 → **~€20–55/mo** (G5 ✅).
- **Ops:** 1–3 h/week of app reviews, email and OS updates. No sales calls (G4 ✅).
- **G6:** App Store and Play IAP work for a Brazil resident; no licence needed. For finance-data apps, local-only storage avoids most LGPD (Brazilian data-protection law) burden.

### 4. Price and customers needed for €1k MRR
- Observed revenue per subscriber: Parceladinho $2,066 / 444 = **~$4.65**; Convitede $1,242 / 393 = **~$3.16** (gross, before the store's 15 %).
- €1k ≈ $1.08k net → about **270–400 active subscribers** at R$9.90/mo or R$59.90/yr, **or 2–3 small apps** of this kind in a portfolio.

### 5. Top 3 risks
1. **Survivorship and base rate:** only ~15 of ~200 Brazil-based TrustMRR listings are at ≥ $1k/month, and RevenueCat reports only 17 % of apps ever reach $1k/month. Expect to ship 2–4 apps to get one winner.
2. **Low Brazilian prices and easy copying:** R$5–20 price points and a small addressable market per sub-niche. Once it's visible on TrustMRR, others can clone it (Parceladinho is public).
3. **Platform dependence:** App Store search ranking changes, or banks adding the feature natively (e.g. Nubank showing instalments), can erase demand.

---

## §4 Segment finding

1. **Newcomers do succeed in the verified data.** 621 of the 1,197 in-band TrustMRR products ($1k–$40k/month) were founded in 2025–2026. The market is not closed to new entrants (K-R5-3 rarely applies). Survivorship bias is heavy, though.
2. **In English B2C, the solo earners with the most revenue mostly buy or create attention.** They run TikTok content, UGC, influencers or Meta ads. This holds for calorie scanners, couples apps, looksmaxxing, breakup apps and faith apps. That fails "minimal effort" (G4), or needs paid acquisition (K-R5-4).
3. **B2B micro-SaaS in the band is dominated by AI-marketing tools** (GEO trackers, Reddit/LinkedIn automation, faceless video): very crowded, and often dependent on the founder's audience.
4. **The repeated signal that fits this founder: local-language, country-specific consumer utilities** discovered through ASO and SEO. It shows up in Brazil (Parceladinho, Enxovaly, Convitede, Pluma), Germany (Mahlzait), France (Francopass, Kickly, Alchie), Bulgaria (TollTracker) and Spain/LatAm (CoupleAI, Nutria, Tortolitos). The Portuguese versions of the *crowded* global niches (Bible, calories, humanizer, betting tips, visa photos) are already filled. The gap is in **Brazil-only problems**, not in translations of global apps.

---

## §5 Evidence gaps

- **Team size** is undisclosed for most TrustMRR entries. "Solo" is inferred from a single named founder: UNVERIFIED.
- **Acquire.com** was not accessed (login wall), so there is no independent P&L data from that source.
- **Flippa and Microns** coverage is thin: a handful of listings, and most Microns listings are below $1k/month.
- **Enxovaly's** $8.5k over 30 days against $1.8k MRR suggests launch-month one-off purchases, so it is not yet proof of lasting MRR. Parceladinho's founder, launch date and channel mix are inferred from its App Store ID and SEO site.
- **PT-BR App Store competition** was checked only for Bible, Catholic, calorie (through FitCal), betting tips, humanizer, visa photo and MEI. Candidate sub-niches for cluster 1 (e.g. baby-shower lists, school-supply lists, instalment tracking for other card types, the annual tax return (IRPF), FGTS) still need **App Store search and Google checks before any build**.
- **Brazilian app ARPU** comes from only two data points (Parceladinho, Convitede).
- The RevenueCat 2026 base rates are cited from a secondary blog. The primary report was not read.

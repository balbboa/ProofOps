# R5-B — Consumer & Platform Ecosystems

> Date: 2026-09-24. Rules: `../R5-CRITERIA.md` (gates G1–G6, kill rules K-R5-1..5).
> Desk research only. About 77 web searches plus about 35 page fetches/curl pulls.
> Revenue tags: **VERIFIED** = pulled from Stripe/RevenueCat by a third party (TrustMRR, whatsthe.app). **SELF** = the founder's own public claim (interview, podcast, blog). **EST** = a third-party estimate. **UNVERIFIED** = weak, anonymous or looks AI-written.

---

## §0 Coverage note

**What I covered:** mobile subscription apps (RevenueCat SOSA 2026, TrustMRR's RevenueCat and mobile lists, whatsthe.app); Chrome extensions (ExtensionPay list, TrustMRR, Vinted/Poshmark/Mercado Livre/WhatsApp tools); Shopify, Nuvemshop, WooCommerce-Brazil, Wix and Excel AppSource; Google Workspace add-ons; Framer and Notion templates; Etsy, Gumroad and Hotmart digital products; Telegram and Discord bots; Obsidian, Raycast, VS Code and Figma; indie games (Steam/Gamalytic); TikTok Shop Brasil tools. I also pulled TrustMRR's full Brazil list (203 startups) with curl and parsed it. That parse is the base for the PT-BR test the coordinator asked for (§4.2).

**What I could not cover:**
- Nuvemshop does not publish install or revenue data for its apps.
- Some TrustMRR startup pages timed out (CoupleAI, tortolitos detail, Convitede detail).
- whatsthe.app category pages load by JavaScript, so I only saw the pages that search engines index.
- Chrome-stats blocked me, so there are no install counts for the Vinted tools.
- Sensor Tower and Appfigures are paywalled. I did not use them.

**Selection-bias warning:** TrustMRR and whatsthe.app list only founders who chose to connect their revenue. Winners are over-represented, and the many silent zeros are missing.

---

## §1 Candidates table

Legend: ✅ pass · ❌ fail · ⚠️ unclear or weak.

| # | Candidate | Ecosystem | Solo earners ≥$1k/mo + URL | Distribution gap | Build wks | Ops h/wk | G1 | G2 | G3 | G4 | G5 | G6 | Verdict | Decisive reason |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Resale-marketplace automation extension (Vinted/Poshmark type), **entering Vinted** | Chrome ext. | Closet Tools $30–40k MRR SELF ([IH podcast](https://www.indiehackers.com/podcast/187-jordan-oconnor-of-closet-tools); $756k 2024 EST [Latka](https://getlatka.com/companies/closet-tools)); VintHelper $1,651 MRR VERIFIED, founded May 2026 ([TrustMRR](https://trustmrr.com/startup/vinthelper-app)) | None left: 12+ Vinted tools (Bleam, Dotb, Clemz, Vintex, Vintedge in 6 languages incl. PT, Vintup, Grow Bot, Resela, Vintify…) | 4–6 | 3–6 | ✅ | ❌ | ✅ | ⚠️ | ✅ | ⚠️ | **KILL** | Market saturated, and since 21 Jul 2026 Vinted has been restricting accounts for "automated activity" ([Redrip](https://www.redrip.app/en/blog/vinted-automation-restriction-2026/)) |
| 2 | Same model for **Brazilian resale sites** (Enjoei, OLX) | Chrome ext. | Only analogues (row 1). No Enjoei/OLX tool with revenue found | Real: no third-party Enjoei tool found | 4–6 | 3–5 | ⚠️ (analogue only) | ⚠️ | ✅ | ✅ | ✅ | ⚠️ | **UNCERTAIN** | Gap is real but has no proven money. Unknown whether Enjoei rewards reposting at all. Enjoei ships its own AI listing tool |
| 3 | Mercado Livre seller extensions | Chrome ext. | Avantpro ("100k sellers"), Metrify, Nubimetrics — companies | None: 8+ tools ([GoSmarter comparison](https://gosmarter.com.br/extensao-mercado-livre-comparativo/)) | 6–8 | 5+ | ⚠️ | ❌ | ✅ | ⚠️ | ✅ | ⚠️ | **KILL** | Crowded, and the players are companies (K-R5-3) |
| 4 | WhatsApp Web CRM extension (Brazil) | Chrome ext. | WaSpeed "40k users" (company); RD/Agendor give theirs away free | None | 6–8 | 5+ | ⚠️ | ❌ | ✅ | ❌ | ✅ | ⚠️ | **KILL** | Saturated. Free versions from CRM vendors. Meta ToS risk |
| 5 | Facebook friend/group cleanup extension | Chrome ext. | FriendFilter+GroupFilter $11.3k MRR VERIFIED, established ([TrustMRR](https://trustmrr.com/startup/friendfilter-groupfilter)) | No second earner, no gap found | 4 | 2–4 | ❌ (1 earner) | ❌ | ✅ | ✅ | ✅ | ⚠️ | **KILL** | Only one earner; incumbent holds the Chrome Web Store keyword |
| 6 | AI homework/exam answer extension | Chrome ext. | CheatMate $7.4k MRR VERIFIED, founded Aug 2025 ([TrustMRR](https://trustmrr.com/startup/cheatmate)) | PT version for Brazilian distance-learning platforms (AVA)? Already exists: PasseJá, Sapien IA, Respostas AVA | 3–4 | 3–5 | ⚠️ (1 verified) | ❌ | ✅ | ⚠️ | ⚠️ (LLM cost) | ⚠️ | **KILL** | PT gap already taken; commodity LLM wrapper |
| 7 | Couple / relationship apps | iOS/Android | tortolitos (ES) ~$10.3k/30d VERIFIED ([TrustMRR](https://trustmrr.com/startup/tortolitos)); CoupleAI (LatAm) $3.2k MRR VERIFIED ([TrustMRR RevenueCat list](https://trustmrr.com/tech/revenuecat)) | PT gap already filled: Closer, Bloom, CuddleMe, Dengo, Casal (several launched 2025–26) | 4–6 | 5+ (TikTok content) | ✅ | ❌ | ✅ | ❌ | ✅ | ✅ | **KILL** | PT gap filled within months; growth depends on ongoing content |
| 8 | Christian/Bible subscription apps in PT | iOS/Android | Bibly $5,058 MRR VERIFIED, launched Jan 2026 ([whatsthe.app](https://www.whatsthe.app/bibly)); gamified Bible app ~$6k MRR SELF ([SGE](https://www.socialgrowthengineers.com/gamified-bible-app-secures-6k-mrr-despite-low-downloads), page now 404); Tariq (Quran) $5.7k MRR VERIFIED | PT is covered: Bible Chat (funded, $14M Series A, 90% paid TikTok views) and Hallow have PT; Bíblia IA, Bíblia Fala, Bibly sells in Brazil | 4–6 | 5+ | ✅ | ❌ | ✅ | ❌ | ✅ | ✅ | **KILL** | Funded leader buys distribution (K-R5-4); PT already served |
| 9 | AI calorie app in PT | iOS/Android | FitCal $5.8k MRR VERIFIED, Brazil ([whatsthe.app](https://www.whatsthe.app/com.enzosegattoc.fitcalNEW)) | Filled by FitCal itself (influencers, self-reported $2k/mo spend) | 6 | 5+ | ⚠️ | ❌ | ✅ | ❌ | ⚠️ | ✅ | **KILL** | The gap is gone; depends on paid influencers |
| 10 | "Proven EN app → PT-BR clone" as a general play | iOS/Android/web | FitCal, Enxovaly, Convitede (all VERIFIED, see §4.2) | PT app-store search is weaker than EN, but it closes fast | 4–8 | 3–6 | ✅ | ⚠️ | ✅ | ⚠️ | ✅ | ✅ | **UNCERTAIN** | A pattern exists but with high variance; see §4.2 |
| 11 | TV-remote / utility apps via ASO | iOS | 1 anonymous listing: $7.7k MRR VERIFIED, for sale ([TrustMRR RevenueCat list](https://trustmrr.com/tech/revenuecat)) | Keyword crowded (dozens of "Universal TV Remote" apps) | 3–4 | 2 | ❌ (1 earner) | ❌ | ✅ | ✅ | ✅ | ⚠️ | **KILL** | Only one earner; keyword crowded |
| 12 | Google Workspace add-ons (general) | Workspace Marketplace | Amit Agarwal >$10M/yr EST, solo ([IH on X](https://x.com/IndieHackers/status/1909662484921041298)); Sync2Sheets $9k MRR SELF, solo, Argentina ([Superframeworks](https://superframeworks.com/blog/sync2sheets)); BudgetSheet $1.6k MRR SELF 2022 ([blog](https://vancelucas.com/blog/how-i-built-a-google-sheets-extension-making-1-6k-mrr/)) | Marketplace search is an organic channel, but no specific niche gap found | 3–6 | 2–4 | ✅ | ⚠️ | ✅ | ✅ | ✅ | ✅ (OAuth review) | **UNCERTAIN** | Strongest money-proof in this workstream, but no specific gap identified (see §4.3) |
| 13 | Sheets add-on: bank sync for Brazil (Open Finance) | Workspace | BudgetSheet (US) only; Tiller is a company | Real gap: no BR bank→Sheets add-on found | 6–8 | 3 | ⚠️ | ✅ | ✅ | ✅ | ❌ | ⚠️ | **KILL** | Open Finance access costs R$1.5–6k/mo ([TabNews](https://www.tabnews.com.br/GuilhermeVieira/estou-desenvolvendo-um-app-de-financas-pessoais-e-nao-consigo-pagar-o-open-finance-pluggy-r2-5k-mes-belvo-r6k-mes-tecnospeed-r1-5k-de-entrada-r540)). Free Meu Pluggy is personal-use only |
| 14 | Sheets add-on: B3 stock/REIT (FII) data | Workspace/API | Bolsai $624 MRR VERIFIED (below $1k); brapi (20k devs, revenue unknown); FII11 | None: brapi, bolsai and FII11 already cover it | 3 | 2 | ❌ | ❌ | ✅ | ✅ | ⚠️ (data licence) | ⚠️ | **KILL** | Already crowded; no earner above $1k |
| 15 | Certificate generator add-on (PT schools/events) | Workspace | Certify'em (company, revenue unknown) | AutoCert (BR) and free Autocrat already exist | 3 | 2 | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | **KILL** | No G1 |
| 16 | Nuvemshop apps (LatAm Shopify) | Nuvemshop App Store | None found (700+ apps, 180k merchants; no developer revenue published) | Possible PT/ES platform gap | 6–8 | 3–5 | ❌ | ⚠️ | ✅ | ⚠️ | ✅ | ⚠️ (CNPJ probably needed) | **UNCERTAIN→KILL** | No proven solo earner |
| 17 | Shopify apps (generic niche) | Shopify | Many solo examples; median app under $1k/mo ([Week One Labs](https://weekonelabs.com/blog/shopify-app-revenue-benchmarks-2026/)) | 18k apps, 500–800 new apps/month; no localisation gap shown | 6–8 | 5+ | ✅ | ❌ | ✅ | ⚠️ | ✅ | ✅ | **KILL** | Crowded; merchant support load |
| 18 | WooCommerce Brazil plugins | WordPress | Small local sellers (e.g. R$99.90/yr InfinitePay plugin); no revenue data | Payment companies give free plugins | 4 | 3 | ❌ | ❌ | ✅ | ⚠️ | ✅ | ✅ | **KILL** | No G1; free incumbents |
| 19 | Framer templates | Framer Marketplace | One creator $22–24k/mo SELF 2025 ([allaboutframer](https://allaboutframer.com/how-much-can-you-actually-earn-with-framer-in-2026-(real-numbers))); Cedric $4–7k/mo SELF | "Thousands" of templates; language adds little | 2–4 per template | 2 | ✅ | ❌ | ⚠️ (design skill) | ✅ | ✅ | ✅ | **KILL** | Crowded; design skill, not dev skill |
| 20 | Notion templates | Notion/Gumroad | Mostly audience-driven; marketplace sales not visible | None | 1–2 | 2 | ⚠️ | ❌ | ✅ | ✅ | ✅ | ✅ | **KILL** | K-R5-1 (audience needed) |
| 21 | Etsy spreadsheet/printable products | Etsy | Emily McDermott $280k total SELF ([Medium](https://emily-mcdermott.medium.com/how-ive-made-280k-selling-spreadsheets-on-etsy-51b0759a9465), 403 for me) | Saturated; AI flood of listings | 1–2 | 3–5 | ✅ | ❌ | ✅ | ⚠️ | ✅ | ✅ | **KILL** | Saturated since the AI-content flood |
| 22 | Hotmart/Kiwify spreadsheets (PT) | Hotmart | Many listings; no revenue data | Depends on affiliates or ads | 1–2 | 3–5 | ❌ | ❌ | ✅ | ⚠️ | ✅ | ✅ | **KILL** | K-R5-4 (paid acquisition) |
| 23 | Telegram VIP-group bot with Pix billing | Telegram | InviteMember (company); BR tools with no revenue data | None: BeeBot, AutoGrupo, Bottrix, ElitePass, Telebot, SeuGrupo + open source | 3–4 | 3–5 | ❌ | ❌ | ✅ | ⚠️ | ✅ | ⚠️ | **KILL** | Six+ BR clones already |
| 24 | Discord bot premium tiers | Discord | Typical $100–500/mo; MEE6 is a company | None | 3–4 | 3–5 | ❌ | ❌ | ✅ | ⚠️ | ✅ | ✅ | **KILL** | No G1 at solo scale |
| 25 | Obsidian / Raycast / VS Code / Figma paid plugins | Dev/design tools | Only one VS Code "$6.8k/mo" post, looks AI-written (UNVERIFIED) | Marketplaces have no paid path | 2–4 | 2 | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | **KILL** | No credible G1 |
| 26 | Indie games (Steam) | Steam | Hit-driven: 76.5% of games released in the last 3 years earned < $5k ([Gamalytic](https://gamedevreports.substack.com/p/gamalytic-67-of-games-on-steam-earned)) | None | 12+ | varies | ❌ | ❌ | ❌ | ⚠️ | ✅ | ✅ | **KILL** | Hits don't replicate |
| 27 | TikTok Shop Brasil seller analytics | Web/ext. | Kalodata, FastMoss, EchoTik (funded, Chinese) | EchoTik at $9.90; Kalodata already in PT | 6–8 | 5 | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | **KILL** | Funded, cheap incumbents |
| 28 | "Love QR code" gift pages (BR trend) | Web | LOVEYUU $16k total but $0 last 30 days; Gifts QR $475/30d, $89 MRR (TrustMRR BR list) | n/a | 1 | 1 | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | **KILL** | K-R5-2 (trend has collapsed) |
| 29 | Gumroad/Lemon Squeezy info products | Gumroad | Audience-driven | None | 1 | 2 | ⚠️ | ❌ | ✅ | ✅ | ✅ | ✅ | **KILL** | K-R5-1 (audience needed) |
| 30 | Microsoft Excel add-ins (AppSource) / Wix apps | AppSource, Wix | No solo revenue found. AppSource add-ins are free-to-download only | Less crowded, but no proven money | 6 | 3 | ❌ | ⚠️ | ✅ | ✅ | ✅ | ✅ | **KILL** | No G1 |

**Counts:** 30 candidates · **0 SURVIVE** · 4 UNCERTAIN (#2, #10, #12, #16) · 26 KILL.

---

## §2 Per-candidate notes (only the ones that matter)

**#1/#2 Resale-marketplace automation.** Money is proven in this model: Closet Tools (solo, Poshmark), FriendFilter (Facebook) and VintHelper (Vinted) are all verified or credibly disclosed.
- **Evidence of new entrants winning:** VintHelper was founded May 2026 and reached $1,651 MRR with 195 subscribers in about 4 months. Its founder is Argentine, with 287 X followers. Channels: TikTok, Instagram, SEO, Discord. This happened despite 12+ competitors.
- **Platform risk is the reason to kill it:**
  - Vinted's ToS explicitly bans bots.
  - A ban wave started in Jan–Feb 2026.
  - From 21 Jul 2026, Vinted has been freezing accounts for 24 hours for automated reposting ([Redrip](https://www.redrip.app/en/blog/vinted-automation-restriction-2026/), [Vendy Studio](https://www.vendystudio.com/blog/vinted-bots-blacklist-2026)).
  - Poshmark removed its own bulk-share tool in Nov 2025 and suspends accounts that auto-relist ([Value Added Resource](https://www.valueaddedresource.net/poshmark-listings-deleted-account-suspension/)).
- **Brazil version (#2):** I found no third-party automation tools for Enjoei. But I have no evidence that Enjoei/OLX sellers pay for such tools, or that reposting helps ranking there. Enjoei launched its own AI listing tool in Apr 2026. Wallapop (Spain) already has MitikLive (free), Resela (€24.99/mo) and ZebraBot, so a smaller-market variant does not stay empty for long.
- **Cheapest test before building:** ask 10 Enjoei power sellers (Instagram/TikTok "brechó" accounts) whether they would pay R$29/mo.

**#10 PT-BR clone.** See §4.2 (the coordinator's lead).

**#12 Google Workspace add-ons.** This has the best money-proof-to-effort ratio in the workstream: solo operators, low support, and an organic marketplace channel.
- **Earners:** Amit Agarwal (estimate >$10M/yr), Sync2Sheets (Leandro Zubrezki, Buenos Aires, $9k MRR, 85% margin, $0 marketing), BudgetSheet ($1.6k MRR, 2022).
- **Adversarial points:**
  - All three earners started before 2022 (K-R5-3 risk). I found no verified post-2023 entrant at ≥$1k.
  - Sync2Sheets got its customers from Notion communities and Reddit, not from Marketplace search.
  - One developer reports only 7 paying users from 5k installs.
  - Scopes that touch Gmail need an annual CASA security assessment (roughly $500–$4.5k/yr, from memory — UNVERIFIED). That would break G5. Sheets-only scopes avoid it.
- **Status:** there is no concrete G2 niche yet, so UNCERTAIN.

**#16 Nuvemshop.** The theory is good: a PT/ES-only store with 180k merchants and 700+ apps, where Nuvemshop handles billing. I found zero public data on developer revenue. G1 fails for now. Likely needs a CNPJ to receive payouts (UNVERIFIED).

**#7/#8/#9 PT consumer apps.** All three show the same thing: when an English app is proven, a PT clone appears within 6–12 months. Couple apps: at least 5 PT apps, most published 2025–26. Bible apps: Bible Chat, Hallow and Bibly already sell PT subscriptions. Calorie apps: FitCal took the slot in 10 months.

---

## §3 Survivor deep-dives

**No candidate passed all gates.** Below are the two UNCERTAIN candidates most worth a cheap validation step, in the survivor format, with their weak points marked.

### 3a. (UNCERTAIN) Google Workspace add-on in a narrow niche
1. **Proven earners:** Sync2Sheets $9k MRR (SELF, Jan 2026, since 2021) [Superframeworks](https://superframeworks.com/blog/sync2sheets) / [Starter Story](https://www.starterstory.com/stories/sync2sheets-give-notion-the-superpowers-of-google-sheets); BudgetSheet $1.6k MRR (SELF, 2022); Amit Agarwal's add-ons (EST >$10M/yr, since ~2014).
2. **Gap and channel:** Workspace Marketplace keyword search plus niche communities. **Missing:** a specific under-served keyword. That needs a scrape of the Marketplace (installs vs. ratings per keyword), which this round didn't do.
3. **MVP:** Apps Script or a Workspace add-on plus a Stripe/Lemon Squeezy licence. 3–6 weeks. About €10–30/mo (Vercel/DB). Ops 2–4 h/week.
4. **Unit economics:** at $8/mo you need about 135 paying users for €1k MRR. At 1–4% conversion that means 3.5k–13k active installs.
5. **Risks:** (a) no niche found yet, so G2 is unproven; (b) low free-to-paid conversion; (c) Google OAuth/CASA review cost and delays.

### 3b. (UNCERTAIN) PT-BR localisation of a proven EN subscription app (coordinator lead)
1. **Proven earners (Brazil, VERIFIED):**
   - Enxovaly: $1.8k MRR, $8.4k last 30 days. Launched 30 Jun 2026. Solo founder/developer Gabriel Buzzi Venturi ([press page](https://enxovaly.com/en/imprensa)).
   - FitCal: $5.8k MRR, 2,684 subscriptions. Launched Jan 2025 ([whatsthe.app](https://www.whatsthe.app/com.enzosegattoc.fitcalNEW)).
   - Convitede: $1.2k MRR, $2.1k last 30 days. Web, programmatic-SEO invitation templates ([site](https://convitede.com/convites/convite-digital-personalizado)).
   - Source for all three: [TrustMRR Brazil](https://trustmrr.com/country/br).
2. **Gap and channel:** PT app-store and Google results are weaker than EN, but only until a clone arrives. Channels actually used: influencers/TikTok (FitCal, about $2k/mo spend self-reported), and probably TikTok for Enxovaly (unconfirmed; the press page names no channel). Convitede uses SEO with hundreds of theme landing pages.
3. **MVP:** 4–8 weeks for React Native + RevenueCat, or a web app. Cost under €50/mo. Ops 3–6 h/week if TikTok content is needed, which pushes against G4.
4. **Unit economics:** FitCal's ARPU is about $2.17/subscriber/month, far below US levels. €1k MRR needs about 500 active subscribers.
5. **Risks:** (a) clones arrive within months; (b) the winners depend on content or influencer spend (K-R5-4 risk); (c) low Brazilian ARPU and the RevenueCat base rate (only 17.3% of new apps reach $1k MRR within 2 years).

---

## §4 Segment findings

### 4.1 Overall
Consumer and platform ecosystems easily pass **G1**: verified earners are everywhere. They almost always fail **G2** or **G4**.
- **Supply is exploding:**
  - App Store submissions are up 84% ([9to5Mac](https://9to5mac.com/2026/04/06/app-store-sees-84-surge-in-new-apps-as-ai-coding-tools-take-off/)); about 560k new apps in H1 2026.
  - Downloads grew only 2–3% ([TechSpot](https://www.techspot.com/news/113213-apple-app-store-inundated-low-quality-vibecoded-apps.html)).
  - Chrome developer registrations more than doubled year on year.
- **Base rates are poor:**
  - 17.3% of new subscription apps reach $1k MRR within 2 years ([RevenueCat SOSA 2026](https://www.revenuecat.com/state-of-subscription-apps)).
  - Annual-plan churn worsened to about 72% ([RevenueCat blog](https://www.revenuecat.com/blog/growth/subscription-app-trends-benchmarks-2026)).
  - The median Shopify app earns under $1k/mo.
  - 76.5% of recent Steam games earned under $5k.
- **Platform-rule risk is the hidden killer** for the most "proven" low-effort model (marketplace automation extensions): Vinted and Poshmark both tightened enforcement in 2025–26.

### 4.2 Coordinator hypothesis: "a PT-BR clone of a proven EN app is a distribution gap"
**Verdict: partly true, but not a dependable gap.**
- **The Brazil numbers.** TrustMRR lists 203 Brazil-based startups. Only 20 (about 10%) have MRR ≥ $1k. Only three of those are PT-language consumer apps that fit the clone pattern: FitCal, Enxovaly, Convitede. Pluma ($1.3k) is unclear.
- **Clones near zero in the same list:** AgoraVai habits $160, Finanças AI $21, Itz calories $6, Currículo Rápido IA $0, Konta $0, PrecificaAI $5.
- **Conclusion from the numbers:** winners exist, but they look like the tail of a distribution, not a rule. They are also self-selected.
- **The gap closes fast.** PT versions already exist for couple apps (5+), Bible apps (Bible Chat and Hallow in PT), AI calorie apps (FitCal), and AI exam-answer extensions (PasseJá, Sapien).
- **The winners paid for distribution:** FitCal spends about $2k/mo on influencers; Enxovaly most likely grew through TikTok (unconfirmed); Convitede built an SEO machine. None won on localisation alone.
- **What would make it a real gap:** a proven EN app with **no PT clone yet**, a **life-event or utility** use case (like Enxovaly: pregnancy is short-lived but high-intent and searchable), and a search/SEO channel rather than an influencer channel.
- **Next step:** list the top 50 EN subscription apps on TrustMRR/whatsthe.app and check each for a PT equivalent in the Brazilian App Store (about 2 hours of manual work, no build).

### 4.3 Best-shaped channel in this workstream
Google Workspace Marketplace. Its earners are solo, low-support and not audience-dependent. But the proof is pre-2022, and no specific niche with weak competition has been identified yet.

---

## §5 Evidence gaps
1. Nuvemshop developer revenue: no public data. Could ask Nuvemshop partner support or a partner agency directly.
2. Enxovaly and Convitede acquisition channels are unconfirmed (TrustMRR detail pages timed out).
3. tortolitos and CoupleAI channels and founder details: pages timed out.
4. Install counts for Vinted/Enjoei tools (chrome-stats returned 403).
5. Workspace Marketplace keyword-by-keyword competition was not scraped. This is needed before #12 could pass G2.
6. CASA assessment cost for Workspace add-ons is from memory, UNVERIFIED.
7. Whether Enjoei/OLX ranking rewards reposting or bumps (decides #2).
8. The Closet Tools figure from Latka also lists "39 employees", which contradicts Jordan O'Connor's solo claim. Treat the Latka figure as EST.
9. The Etsy $280k (Medium) and VS Code $6.8k (dev.to) claims could not be checked.

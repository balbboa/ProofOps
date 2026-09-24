# R5-C: Adult and stigmatised-but-legal niches

> Date: 2026-09-24. Reference: `../R5-CRITERIA.md` (gates G1–G6, kill rules K-R5-1..5).
> Scope: legal adult and stigmatised niches, judged only on money and feasibility. There is no moral filter. The report contains no explicit content.
> Founder: solo developer in Brazil. Target is €1k+ MRR with minimal effort.

**Evidence labels:** **[V]** means verified by a third party (TrustMRR connected to Stripe, RevenueCat, Superwall or Whop, or a Flippa listing marked "Vetted + Data Verified"). **[S]** means self-reported (an interview, a founder post, a landing-page claim or a forum post). **[U]** means UNVERIFIED (an estimate, a vendor blog or an inference).

---

## §0 Coverage note

- **Searches:** about 80 WebSearch calls (budget 110) and about 15 WebFetch calls.
- **TrustMRR scan:** I downloaded and parsed the entire public TrustMRR directory, 108 pages and **8,623 startups** with verified revenue. I filtered it by niche keywords: OnlyFans/fans/NSFW/adult, AI girlfriend/companion/roleplay, tarot/astrology/horoscope, betting/odds/prediction markets/casino, crypto/trading/signals, and dating/rizz. This gives a **base rate** for each segment, not only the success stories. It is the most reliable data in this report.
- **Segments covered:**
  - OnlyFans/Fansly creator tooling (CRM, mass-DM, analytics, extensions)
  - Tools for creators on Privacy.com.br
  - Creator wishlists and gifting
  - DMCA and leak-takedown services
  - Brazilian Telegram "VIP group" sales bots paid by Pix
  - AI companion and AI girlfriend apps
  - NSFW-AI affiliate sites
  - Adult tube and aggregator sites
  - Creator platforms (OnlyFans alternatives)
  - Camming tools
  - Astrology, tarot and "baralho cigano" (Brazilian Lenormand cartomancy)
  - Sports-betting tools and tips
  - Brazilian betting affiliate sites
  - Prediction-market tools (Polymarket and Kalshi)
  - Crypto trading tools and signals
  - Dating apps
  - Dating-assistant ("rizz") and dating-photo tools
  - Random video chat
  - Sweepstakes-casino automation
- **Not covered in depth:** camming stats sites (no revenue data found), Brazil-specific adult tube SEO, and non-English OnlyFans tooling outside Brazil.
- **Access limits:** Indie Hackers post pages returned 403, and several OnlyFans-tool founders publish no figures. Many OnlyFans-tool numbers therefore stay [U].

---

## §1 Candidates table

| # | Candidate | Solo/small earners ≥$1k/mo (+URL) | Distribution gap | Payment processor | Legal / ToS risk | Ops h/wk | G1 | G2 | G3 | G4 | G5 | G6 | Verdict | Decisive reason |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | OnlyFans/Fansly creator tooling (CRM, mass-DM, analytics, Chrome extensions) | Only one: an OnlyFans CRM on Microns, $22k ARR (≈$1.25k MRR) at 15% margin, sold for $14.5k in 2025 [S] ([Microns](https://www.microns.io/startup-listings/crm-for-onlyfans-creators-and-agencies)). New entrants on TrustMRR are near zero: AgenSea $104 MRR [V] ([TrustMRR](https://trustmrr.com/startup/agensea)), Explore.Fans $0, Pitchly $0 [V] | None. Crowded, and incumbents are large (Supercreator 25k+ users, OnlyMonster 2k+ teams, Infloww, CreatorHero) | Stripe/Paddle for SaaS sold to creators (the Microns CRM used both) | OnlyFans bans server-side bots and fully automated DMs. Enforcement ends in permanent bans ([Velvetly](https://velvetly.io/guides/onlyfans-dm-automation-safety)) | 5–10 (support, keeping up with OnlyFans UI changes) | FAIL | FAIL | PASS | FAIL | PASS | PASS (ToS risk) | **KILL** | K-R5-3: funded or scaled incumbents dominate, and no verified new solo entrant reaches $1k |
| 2 | Tools for Privacy.com.br creators (Brazil's OnlyFans) | None found. No third-party tool ecosystem is visible | Real gap: 500k+ creators and ~50k new creators a month [S] ([Tudo do MS](https://tudodoms.com.br/m/noticia/149647/como-a-privacy-esta-transformando-criadores-comuns-em-celebridades-digitais)), and no Portuguese tools found | Pix via Brazilian payment providers (Asaas and similar) for a SaaS | No public API, so any tool means scraping or browser automation, which is a ToS risk. Privacy already ships native post and chat scheduling ([Privacy blog](https://blog.privacy.com.br/chat-da-privacy-conheca-todas-as-funcionalidades/)) | 3–6 | FAIL (no proof) | PASS | PASS | ? | PASS | ? | **UNCERTAIN** | The gap is real, but nobody has proven money. Row 1 suggests even the OnlyFans version barely pays solo operators |
| 3 | Creator wishlists and gifting | WishTender: solo, $40k/mo profit at its peak in 2022 [S] ([IH interview](https://www.indiehackers.com/post/40-000-rev-mo-dashiell-bark-huss-wishtender-interview-960e08c722)). **It shut down in July 2024 after Stripe dropped it** ([404 Media](https://www.404media.co/stripe-cuts-off-platform-used-by-dominatrixes-wishtender/), [X](https://x.com/WishTender/status/1815882786584096768)). Successor Wishprime sold for $2.5k with $0 MRR [V] ([TrustMRR](https://trustmrr.com/startup/wishprime)) | Throne dominates (1M+ creators) ([TechCrunch](https://techcrunch.com/2024/03/08/creator-wishlist-startup-throne-is-doing-so-well-that-it-returned-investor-money/)) | Stripe added "fetish services" to its banned list. It is a money-transmission business | Chargebacks and card-testing attacks | 5+ | PASS (historic) | FAIL | PASS | FAIL | PASS | FAIL | **KILL** | K-R5-5: losing the payment processor killed the proven earner. K-R5-3: Throne dominates |
| 4 | DMCA and leak takedown for creators | No solo revenue found. Rulta has 14 staff and has run since 2015 ([Rulta](https://www.rulta.com/about-us/)). BranditScan, Enforcity and CopyrightShark (Portuguese site) are other players. Prices run $10–179/mo [U] | Portuguese is already served (CopyrightShark in PT) | Stripe/Paddle possible (B2B service) | Low legal risk. Work is ops-heavy: manual removal notices, Google delisting, hosts that don't respond | 10+ | FAIL (U) | FAIL | PASS | FAIL | PASS | PASS | **KILL** | G4: this is a service business in disguise. G1 is unverified |
| 5 | Brazilian Telegram "VIP group" sales bots (Pix; much adult-creator usage) | AlphaVips: 500+ creators, "R$12M+ processed" at R$0.50/sale [S] ([site](https://www.alphabotvips.com/)). PinkBot: "R$12M+ processed", R$0.65/sale, has a Brazilian company registration [S] ([site](https://pinkbot.com.br/)). Telestars (France, Telegram automation): $23k in the last 30 days, $2.2k MRR [V] (TrustMRR). AlphaVips implied lifetime revenue ≈R$240k if the average ticket is R$25 [U] | Weak. 10+ Brazilian competitors (Automatizze, Telebot, TeleVips, BuneBot, EasyCreator, Bottrix, ElitePass, PinkBot, AlphaVips). Price is already commoditised at R$0.50/sale | Brazilian Pix payment providers. Woovi warns that adult content is high-risk and disputes usually go to the buyer ([Woovi](https://woovi.com/politicas/gateway/)) | Telegram allows private paid adult channels and bans illegal content ([summary](https://downloaderbaba.com/blog/is-there-pornography-on-telegram-policies-and-guidelines/)). Payment providers may freeze accounts. ECA Digital age checks apply to adult sellers | 3–5 (support and payment-provider incidents) | PASS? (S) | FAIL | PASS | PASS | PASS | ? | **UNCERTAIN** | Money is plausible but self-reported. No gap, because a crowded race to the bottom on price already exists |
| 6 | AI companion / "AI girlfriend" apps | TrustMRR base rate: **12+ listings, none ≥$1k MRR**. Best is elove $917 in 30 days / $182 MRR. AI Girlfriend app $170, Veline $43, Kaleido $29, Clawra $144 [V]. Market: the top 10% of apps take 89% of revenue ([TechCrunch/Appfigures](https://techcrunch.com/2025/08/12/ai-companion-apps-on-track-to-pull-in-120m-in-2025)). Candy.ai ≈$25M ARR, built on affiliates [U] | None. Google and Meta ads are closed and app stores reject explicit apps ([Scrile](https://www.scrile.com/blog/ai-companion-promoting)) | Stripe/Paddle prohibit adult content, **including AI-generated** ([Stripe](https://stripe.com/legal/restricted-businesses)). CCBill/Segpay need Mastercard AN 5196 controls ([Mobius](https://mobiuspay.com/blog/mastercard-adult-content-rules)) | California SB 243 (effective 2026-01-01, private right of action) and New York AI-companion law (2025-11-05) ([Davis Polk](https://www.davispolk.com/insights/client-update/california-and-new-york-launch-ai-companion-safety-laws)). UK OSA age assurance. ECA Digital | 5+ (moderation, crisis protocol) | FAIL | FAIL | PASS | FAIL | ? (LLM/image costs) | FAIL-ish | **KILL** | G1: the verified base rate is ~0 for small operators. K-R5-4: growth depends on paid or affiliate traffic |
| 7 | NSFW-AI review/affiliate sites (Candy.ai pays 40% lifetime) | No solo figures found [U] ([Affninja](https://affninja.com/ai-dating-affiliate-programs/)) | SEO in a crowded English market | Paid by the network (CrakRevenue etc.). No card processing needed | Low | 3–5 | FAIL (no evidence) | FAIL | PASS | PASS | PASS | PASS | **KILL** | G1: no evidence. SEO is a 6–12-month bet |
| 8 | Adult tube / aggregator sites | Self-reported only: a forum site with 10k daily visitors earning $43/day revenue and ~$20–25/day profit [S] ([BHW](https://www.blackhatworld.com/seo/my-adult-porn-tube-site-making-this-amount-of-money.1565947/)) | None (legacy SEO) | Ad networks (TrafficJunky, ExoClick) | **27 US states require age verification** (upheld in *FSC v. Paxton*, June 2025) ([Recording Law](https://www.recordinglaw.com/us-laws/age-verification-laws/)). UK Ofcom fines of £800k and £1.35M ([Biometric Update](https://www.biometricupdate.com/202608/ofcom-fines-geoblocked-porn-site-signaling-tougher-age-assurance-enforcement)). ECA Digital bans self-declared age in Brazil since 2026-03-17. Hosting uploads makes the site a 2257 "secondary producer" ([EFF ILT](https://ilt.eff.org/2257_Reporting_Requirements.html)) | 5+ | FAIL | FAIL | PASS | FAIL | FAIL (CDN/age-check cost) | FAIL | **KILL** | K-R5-5 and K-R5-3 |
| 9 | Adult creator platform (OnlyFans alternative) | Okfans: $4.7k in the last 30 days (platform take), $155k all-time, since 2020 [V] (TrustMRR) | Privacy already dominates Brazil | CCBill/Segpay/Epoch plus 2257, age verification, KYC, NCII removal within 48h (Mastercard) | Full adult-platform compliance | 20+ | PASS (1) | FAIL | FAIL | FAIL | FAIL | FAIL | **KILL** | G4/G6: needs moderation and compliance |
| 10 | Camming tools and stats sites (Statbate, Chaturbate bots) | No revenue data found [U] | ? | ? | Platform ToS (scraping) | ? | FAIL | ? | PASS | ? | PASS | ? | **KILL** | G1: no evidence |
| 11 | **Astrology / tarot / "baralho cigano" AI apps (PT-BR and ES first)** | Flippa **Vetted + Data Verified**: Android astrology app (Belarus, 1M+ installs) with **$27.1k/mo revenue and $16.7k/mo profit** [V] ([Flippa](https://flippa.com/11787371-leading-android-astrology-app-with-a-unique-palm-reader-feature-4-years-in-business-27100-month-revenue-and-16700-month-profit)). Astrology-report SaaS (Hong Kong, launched 2023, owner plus 2 freelancers) with **$11.7k/mo profit**, verified via Stripe and GA [V] ([Flippa](https://flippa.com/12034202-highly-profitable-astrology-saas-business-in-the-entertainment-industry-boasting-a-77-profit-margin-with-established-authority-since-2023)). Zentaro tarot Android app: $16k revenue and $11k profit in its first 12 months (2024–25) [S] ([Flippa](https://flippa.com/11998844-zentaro)). TrustMRR "Project A": $63.8k MRR [V], but it has 50M downloads, so it is not small | Portuguese and Spanish Google Play. Brazil has a large tarot and cartomancy culture. Human-reader marketplace Astrocentro makes R$10M/yr ([Exame](https://exame.com/negocios/o-marketplace-que-fatura-r-10-milhoes-com-consultas-de-taro-24-horas-por-dia/)). **Some Portuguese AI apps already exist** (Tarots, Tarotoo, Tarotia, Lenormand Life), so the gap is thin, not empty | Google Play Billing (avoids Stripe). Stripe prohibits psychic services in JP/MX/TH, and aggregators report holds. Paddle has a pseudo-science clause | **Apple guideline 4.3(b) names "fortune telling" as saturated** ([Apple](https://developer.apple.com/app-store/review/guidelines/)), so launch on Android first. Brazil consumer-protection law: label readings as entertainment | 1–3 | PASS | WEAK-PASS | PASS | PASS | PASS | PASS | **SURVIVE (conditional)** | Several small operators have verified money and new entrants since 2023 succeed. G2 still has to be confirmed with an install-count check |
| 12 | Sports-betting tools and tips (trackers, +EV, props AI) | PropGPT (2 founders): **$83.4k MRR** [V] ([TrustMRR](https://trustmrr.com/startup/propgpt-ai-props-analysis)). SportsApiPro (data API) $3.7k MRR [V]. Long tail under $1k: Olympus Bets $507, BetterSlip $386, Betting Tips $307, Mybets.gg $80 [V]. Brazilian MyBetSpace has 18,951 registered users from R$22.99/mo [S] ([site](https://www.mybetspace.com/)) | Brazilian Betfair-trader tools already exist (MyBetSpace, LayBack at R$29.90/mo) | Stripe prohibits "sports forecasting or odds making with a monetary prize". A pure analytics tool is outside that; the app stores accept PropGPT | Brazil: selling tips ("tipsters") is legally contested ([Poder360](https://www.poder360.com.br/opiniao/a-atividade-de-tipsters-foi-proibida-no-brasil/)). **The government is preparing a provisional measure (MP) to restrict online betting, reported Sep 2026** ([iGaming Brazil](https://igamingbrazil.com/legislacao/2026/09/17/mp-do-governo-lula-pode-restringir-apostas-online-associacoes-defendem-regulacao/)). A Senate bill banning betting ads (PL 2985/2023) is pending in the Chamber | 2–4 | WEAK (1 big, 1 borderline) | FAIL | PASS | PASS | PASS | ? | **UNCERTAIN** | Thin G1 among small operators. Brazilian regulation is highly volatile |
| 13 | Brazilian betting affiliate sites | CPA R$80–250 per first-time depositor [U] ([Track360](https://track360.io/blog/afiliados-apostas-esportivas)). No solo figures | None. Search results are dominated by big media (Lance, Gazeta do Povo, OneFootball, Livescore "188 bets autorizadas" pages) | Paid by the operator | Ordinance SPA/MF 1.231/2024 makes the operator liable for affiliate ads ([gov.br](https://www.gov.br/fazenda/pt-br/assuntos/noticias/2024/agosto/nova-portaria-da-fazenda-estabelece-que-operadores-de-apostas-poderao-ser-responsabilizados-por-publicidade-abusiva)). PL 2985 is pending. The MP could ban online casino | 3–5 | FAIL | FAIL | PASS | PASS | PASS | FAIL-ish | **KILL** | K-R5-3 plus regulatory risk |
| 14 | Prediction-market tools (Polymarket/Kalshi analytics, whale alerts) | **PolyPick $11.2k MRR, founded May 2026, 287 subscribers, via Whop** [V] ([TrustMRR](https://trustmrr.com/startup/polypick)). **Oddpool $1.07k MRR, founded Nov 2025, Stripe** [V] ([TrustMRR](https://trustmrr.com/startup/oddpool)). PolyScout $579 MRR / $2k in the last 30 days [V]. Many near-zero entrants (Polywhales $12, LaunchPoly $15) | English market only. **Brazil blocked Polymarket and Kalshi (April 2026) and CMN Res. 5.298/2026 bans event contracts** ([Bloomberg Línea](https://www.bloomberglinea.com.br/mercados/cmn-proibe-mercados-de-previsao-sobre-eleicoes-e-esportes-no-brasil/)) | Whop/Stripe (it is software, not wagering) | Selling analytics to foreign users is probably legal for a Brazilian resident [U; needs a lawyer]. The trend could reverse through regulation | 2–4 | PASS | FAIL | PASS | PASS | PASS | ? | **UNCERTAIN** | K-R5-2 trend risk. No gap beyond "build better". Brazil's home market is closed |
| 15 | Crypto trading tools and signals | Buildix (order-flow analytics) $1.27k MRR, since Mar 2026, Stripe [V]. ChartsGPT (AI chart analysis) $1.08k MRR, RevenueCat [V]. Cryptobytez Discord $4.6k MRR, Whop [V], but it is audience-driven. Smaller: Sferica $428, Trading Wizard $324 [V] | None concrete. Brazil: **selling signals or recommendations needs a CVM-accredited analyst (Res. CVM 20; copy-trade included)** ([InfoMoney](https://www.infomoney.com.br/mercados/trader-oficio-da-cvm-ratifica-que-pratica-de-copytrade-exige-certificado-de-analista/)) | Stripe restricts crypto; RevenueCat/Whop work | Signals are illegal in Brazil without a licence. Pure analytics tools are fine | 2–4 | PASS | FAIL | PASS | PASS | PASS | PASS for tools, FAIL for signals | **UNCERTAIN** | G2: no gap. Signals fail K-R5-5 in Brazil |
| 16 | Dating apps (matching networks) | No small-operator proof. Network effects make bootstrapping hard ([Anything](https://www.anything.com/blog/dating-app-business-model-revenue-strategies)) | Niche-community idea only | Paddle prohibits dating; Stripe restricts it | Apple 4.3(b) names dating as saturated. Moderation and safety work | 10+ | FAIL | FAIL | FAIL | FAIL | ? | ? | **KILL** | G1/G4 |
| 17 | Dating-assistant ("rizz") and dating-photo AI apps | Sauce AI $6.5k MRR, founded Nov 2025, 1,548 subscribers, Superwall [V] ([TrustMRR](https://trustmrr.com/startup/sauce-ai)). TinderProfile.ai $2.1k in the last 30 days, $168k all-time, founded 2024, mostly one-off sales via Stripe [V] ([TrustMRR](https://trustmrr.com/startup/tinderprofile-ai)). Rizz $500k/mo, co-founders [S] ([Starter Story](https://www.starterstory.com/rizz-breakdown)). Many near-zero entrants (AI Dating Assistant $464, Magnt $363, ELO AI $165, Rizzler/RizzGPT/Flirtyness $0) | Portuguese not checked. The channel is TikTok UGC, usually paid | Store billing | App-store rules on explicit text are manageable | 2–4 | PASS | ? | PASS | PASS | PASS | PASS | **UNCERTAIN** | Winners rely on TikTok/UGC distribution (K-R5-4 risk). This is mostly R5-B territory, so hand it over |
| 18 | Random video/text chat with strangers | OmegleWeb $84k MRR [V]. STRK $5.1k MRR [V] (TrustMRR) | — | Stripe OK until abuse appears | Omegle closed in 2023 over abuse and child-safety risk. Heavy moderation duty. ECA Digital and UK OSA apply | 10+ | PASS | ? | PASS | FAIL | FAIL (video bandwidth) | FAIL-ish | **KILL** | G4/G6: moderation and liability |
| 19 | Sweepstakes-casino automation bots | BettrBot $7.2k in the last 30 days, since Jan 2026, via Whop [V] (TrustMRR) | — | Whop | Breaks casino ToS. The bot's users face account bans | 3–5 | PASS | FAIL | PASS | ? | PASS | FAIL | **KILL** | K-R5-5: the product depends on breaking platform ToS |

**Counts:** 19 candidates. 1 SURVIVE (conditional), 6 UNCERTAIN, 12 KILL.

---

## §2 Per-candidate notes

**1. OnlyFans/Fansly tooling.** The money in this ecosystem goes to agencies (30–50% commission) and to a few scaled SaaS products: Supercreator (25k+ users), OnlyMonster, Infloww and CreatorHero at $39.99–$260/mo ([CreatorHero](https://www.creatorhero.com/)). TrustMRR has no small OnlyFans tool at $1k+ MRR. The only disclosed small-operator figure is the Microns CRM: $1.25k MRR, 15% margin, founders "don't have time and money". That is a weak signal. OnlyFans ToS since 2025–26 allows browser-side AI *drafting* with a human sending messages. It bans server-side bots and credential sharing, and bans end in payout forfeiture ([Velvetly](https://velvetly.io/guides/onlyfans-dm-automation-safety), [Maho](https://maho-management.com/en/blog-entry/does-onlyfans-allow-ai-content)). An earlier OnlyFans analytics SaaS lost value when OnlyFans launched its own statistics ([IH](https://www.indiehackers.com/post/saas-for-onlyfans-creators-an-untapped-market-1622712f44), 403 when fetched; summary via search) [S].

**2. Privacy.com.br tools.** Privacy has 500k+ creators, adds ~50k a month and claims 50M users [S]. It takes 20%, pays out via Pix and is Brazil's biggest platform. I found no third-party tool ecosystem, which is the only real language/geo gap in the adult segment. Against it:
- Privacy already includes native post and chat scheduling and a performance dashboard called "Meu Privacy".
- There is no public API, so any tool has to automate the web app, which is a ToS risk.
- Row 1 shows that even the OnlyFans version barely pays small operators.

Keep this as UNCERTAIN only if the founder wants to run 5 interviews with Brazilian creator agencies about their paid pain points.

**3. Wishlists.** This is the clearest G6 case study in the round. A solo founder reached $40k/mo profit, then Stripe added "fetish services" to its banned list (Feb 2024). Replacement processors could not match Stripe, card-testing attacks followed and the business shut down in July 2024. Money transmission for adult-adjacent users is fragile.

**4. DMCA takedown.** This is labour-intensive and crowded (Rulta, BranditScan, Enforcity, PrivDot, Bruqi, CopyrightShark in Portuguese). Takedown success rates depend on hosts that don't respond. Automating it doesn't remove the manual follow-up.

**5. Brazilian Telegram VIP bots.** This is a large, real Brazilian market (Pix plus Telegram private groups) that serves adult creators among other sellers. The volume claims are self-reported: AlphaVips 500+ creators and R$12M+ processed; PinkBot 34k bots and R$12M+. At R$0.50–0.65 per sale, R$12M processed means only about R$200–300k of lifetime platform revenue [U]. That suggests several operators above $1k/mo, but none is verified. Pricing has converged to R$0.50/sale with no monthly fee, so a newcomer has no price gap. It is also exposed to Pix payment providers freezing adult sellers.

**6. AI companions.** The verified base rate is decisive: more than 12 TrustMRR listings with AI-girlfriend or companion positioning, and none at $1k MRR. Separately, Embraces.AI (a non-adult "best friend" companion) has $5.6k MRR [V]. Structural blockers:
- Stripe and Paddle ban adult AI content.
- Card brands test AI output and fine violations ([Tripleminds](https://tripleminds.co/blogs/compliance/nsfw-adult-payment-processor/)).
- Companion-chatbot laws (California SB 243 with a private right of action, New York).
- Growth runs on affiliates or ads, which K-R5-4 excludes.

**8–9. Adult sites and platforms.** Since 2025–26 the compliance floor has jumped:
- US age-verification laws in 27 states, upheld 6-3 in *FSC v. Paxton* (2025-06-27).
- UK OSA "highly effective" age assurance since July 2025, with Ofcom fines already issued.
- Brazil's ECA Digital (Lei 15.211/2025, in force 2026-03-17) bans self-declared age.
- Hosting uploads makes the operator a 2257 secondary producer. AI-only content currently falls outside 2257, but not outside card-brand rules.
- In July 2025, Visa and Mastercard pressure made Steam and itch.io delist thousands of adult titles ([CBC](https://www.cbc.ca/radio/day6/steam-itch-takedowns-credit-cards-1.7597563)).

These are not solo, low-effort businesses.

**11. Astrology/tarot.** See §3.

**12–13. Betting.**
- PropGPT is a real outlier: two founders, launched Sep 2024, $83k MRR through Superwall paywalls on iOS.
- The small tail of betting tools on TrustMRR mostly sits under $500 MRR.
- Brazil licensed 188 operators from 2025 onward, each with a R$5M reserve requirement.
- Affiliate marketing is now operator-controlled (Ordinance 1.231/2024), the Senate has passed an ad-ban bill (PL 2985/2023) and the government is preparing an MP that may ban online casino (Sep 2026). A PL 2.470/2026 on wider ad restrictions was also approved in a Senate committee.
- Anything whose distribution depends on betting ads or affiliates in Brazil could be wiped out within months.

**14. Prediction markets.** This passes G1 cleanly on verified data: PolyPick went from zero to $11k MRR in about 4 months (2026), and Oddpool has held about $1k MRR since Nov 2025. It is hype-driven (K-R5-2 watch). Brazil bans the underlying markets (CMN Res. 5.298/2026, 27 sites blocked), so there is no home-market gap and the English market is filling quickly. Legal note: a Brazilian resident selling analytics software to US users is not operating a betting platform. That view is [U] and needs a lawyer before relying on it.

**15. Crypto tools.** Two small tools have verified ~$1.1–1.3k MRR (Buildix, ChartsGPT). CVM Resolution 20 makes selling signals, recommendations or copy-trade in Brazil a regulated activity that needs APIMEC accreditation. Analytics without recommendations is fine, but there is no distribution gap.

**17. Dating assistants.** Verified money exists (Sauce AI $6.5k MRR in 10 months; TinderProfile.ai $168k lifetime) alongside many near-zero clones. The winners run TikTok/UGC funnels. I pass this to R5-B, since the product isn't meaningfully stigmatised.

**19. Sweepstakes bots.** Verified money, but the product works by breaking the target platforms' ToS, and US states are banning sweepstakes casinos. KILL.

---

## §3 Survivor deep-dive: AI tarot / astrology / baralho cigano app, Portuguese (and Spanish) first, Android first

### 1. Proven earners

| Operator | Revenue | Source | Age | Notes |
|---|---|---|---|---|
| Android astrology/palm-reading app (Belarus) | $27.1k/mo revenue, $16.7k/mo profit | [Flippa 11787371](https://flippa.com/11787371-leading-android-astrology-app-with-a-unique-palm-reader-feature-4-years-in-business-27100-month-revenue-and-16700-month-profit), "Vetted + Data Verified", PayPal-connected [V] | App 3 yrs, business 6 yrs | 1M+ installs, rated 4.7. Ranks top for a competitive keyword (organic ASO) |
| Astrology report SaaS (Hong Kong) | $11.7k/mo profit (listed MRR $5.96k; the description says $19–20k) | [Flippa 12034202](https://flippa.com/12034202-highly-profitable-astrology-saas-business-in-the-entertainment-industry-boasting-a-77-profit-margin-with-established-authority-since-2023), Stripe and GA verified [V] | Launched 2023 | Owner plus 2 freelancers. SEO, 300k-subscriber newsletter, retargeting. 70% of customers in the US |
| Zentaro tarot (Android) | $16k revenue and $11k profit in 12 months (≈$1.3k/mo revenue) | [Flippa 11998844](https://flippa.com/11998844-zentaro) [S] | First year May 2024–May 2025 | 86k installs, mostly ad revenue ($15k) plus $1.1k in-app. Shows a *new* entrant reaching about $1k/mo |
| AI tarot and horoscope app | $4.4k MRR claimed, $3.3k profit, "fully organic" | [Flippa 12293915](https://flippa.com/12293915-tarot-card-reading-and-meaning) (listing not live when fetched) [U] | ? | 175k installs |
| Project A (AI fortune-telling) | $63.8k MRR | TrustMRR, RevenueCat [V] | ? | 50M downloads. Shows the ceiling, not a solo benchmark |

**Base-rate caveat:** 7 of 9 astrology/tarot startups on TrustMRR show $0 (ama.guide, Astroly AI, Orbli, Stellara, Tatva, Dream & Stars; Tarot Go on ProvenMRR has $4 MRR). Money is concentrated in apps that rank on store search, not in web SaaS launched on X.

### 2. Distribution gap and channel

- **Channel:** Google Play search (ASO) in Portuguese, then Spanish. The Belarus and Zentaro cases show that Android ASO alone can carry a tarot or astrology app.
- **Portuguese angle:** "baralho cigano" (36-card Lenormand) is a specifically Brazilian cartomancy tradition. So are tarot tied to Umbanda and Spiritism, "mapa astral" and "signos". Brazil's willingness to pay is shown by Astrocentro, a human tarot-reader marketplace making R$10M/yr with 1M+ consultations.
- **Honest G2 status:** there is competition in Portuguese, including AI apps: Tarots (Leitura de Tarô IA), Tarotoo, Tarotia (web), Lenormand Life, Tarot Cigano Lenormand (AI) and Baralho Cigano Astrolink (Personare/Astrolink's brand) ([Google Play search](https://play.google.com/store/apps/details?id=com.lenormand.life&hl=en_US)). The gap is thin, not empty.
- **Validation before building (about 1 hour):** check installs and last-update dates for the top 10 results for "baralho cigano", "tarot", "mapa astral" and "tarot ia" on AppBrain or the Play Store. Proceed only if at least 3 of the top 10 are abandoned (no update in over 12 months) or have fewer than 100k installs. If the top slots are all Personare/Astrolink and well-funded global apps, re-grade this to KILL under K-R5-3.

### 3. MVP scope, build time, cost, ops

- **Scope:** Android app built in Flutter or React Native:
  - Daily card (push notification).
  - 3-card and Celtic-cross tarot spreads.
  - Baralho cigano 3- and 9-card spreads.
  - Daily sign horoscope, generated in batch once a day for 12 signs, which costs almost nothing.
  - Birth-chart summary using the Swiss Ephemeris (free library).
  - LLM interpretation of the user's question.
  - Paywall via Google Play Billing (weekly and monthly), with AdMob in the free tier.
  - Portuguese first, Spanish second, English last.
- **Build:** 5–7 weeks part-time.
- **Monthly cost:** €15–60 (hosting €5–20; LLM with a small model at about $0.001–0.003 per reading, so roughly €10–40 at a few thousand readings; Google Play one-time $25). Well inside G5.
- **Ops:** 1–3 h/week (reviews, ASO tweaks, prompt fixes). Content is generated, so there is nothing to moderate beyond user prompts.

### 4. Price and customers for €1k MRR

- Brazil: R$14.90/month. After Google's 15% cut that is about R$12.70 net, or about €2.0 at ~6.3 BRL/EUR [U, FX]. That needs **about 500 subscribers**. A weekly plan at R$7.90 (the norm in the category) needs about 250–300 weekly subscribers.
- Spanish/LATAM is similar. English at $4.99/week would need about 60–70 subscribers but faces much heavier competition.
- Realistic plan: Portuguese plus Spanish subscriptions and AdMob, aiming for €1k in months 6–12. Brazilian AdMob eCPMs are low, so ads alone won't get there.

### 5. Top 3 risks

1. **G2 fails on validation.** The Portuguese top ranks may already belong to Personare/Astrolink and well-funded global apps (Project A-scale apps that are localised). Mitigation: the 1-hour install check above.
2. **Low Brazilian ARPU and conversion,** plus low Brazilian ad eCPMs. Mitigation: ship Spanish and a higher-priced English version from the same codebase, and offer weekly plans.
3. **Platform policy:** Apple 4.3(b) blocks new fortune-telling apps unless they are clearly differentiated, so the iOS half of the market may be closed. Google Play could tighten "deceptive" or low-quality-app rules (Apple added removal of low-effort apps in saturated categories in June 2026, [MacRumors](https://www.macrumors.com/2026/06/09/app-store-guidelines-low-quality-apps/)). Stripe and Paddle are hostile to psychic services, so stay on store billing, or use Pix via a Brazilian payment provider for web.

---

## §4 Segment finding

1. **Adult niches fail on G6 and G4, not on demand.** The adult segment has real money: WishTender at $40k/mo, Okfans, Brazilian Telegram VIP bots and OnlyFans agencies. But almost every adult product at solo scale runs into one or more of:
   - payment-processor hostility (Stripe, Paddle and PayPal ban adult content, including AI-generated content; card-brand AN 5196 controls; the 2024 WishTender shutdown; the 2025 Steam/itch.io purge);
   - the 2025–26 wave of age-verification law (27 US states after *Paxton*, UK OSA fines, Brazil's ECA Digital banning self-declaration since March 2026);
   - platform ToS (OnlyFans automation bans, no Privacy API);
   - moderation load that breaks the ≤5 h/week goal.

   The remaining "tools for adult creators" layer is either dominated by scaled players (OnlyFans) or unproven (Privacy.com.br).
2. **The TrustMRR base rate kills AI companions.** More than 12 verified small AI-girlfriend or companion apps and none at $1k MRR. The market is winner-take-most (the top 10% of apps take 89% of revenue) and depends on affiliates.
3. **Brazilian gambling-adjacent niches are a regulatory minefield in 2026.** Operators need licences and a R$5M reserve. Affiliates fall under operator liability. An ad-ban bill has passed the Senate. A provisional measure to restrict online betting is expected. Prediction markets are banned and blocked (CMN Res. 5.298/2026). Crypto signals need CVM accreditation (Res. 20). None of these offers a *Brazilian* gap for a solo founder.
4. **The one survivor is the least "adult" niche: astrology and tarot.** It has multiple verified small operators (Flippa-verified at $1.3k–$16.7k/mo profit, including 2023–24 launches), zero moderation, cheap LLM content, and a plausible Portuguese angle (baralho cigano, Brazilian tarot culture). Its weak point is G2: Portuguese competitors, including AI ones, exist, so the gap must be checked before building.
5. **Verified money in English that needs a gap from elsewhere:** prediction-market analytics (PolyPick, Oddpool), crypto analytics (Buildix, ChartsGPT) and dating-assistant apps (Sauce AI, TinderProfile.ai). Each passes G1 on TrustMRR data but offers no language or geo gap for a Brazilian founder, so they sit at UNCERTAIN.

---

## §5 Evidence gaps

- **Privacy.com.br:** whether creators or agencies pay for third-party tools at all. No evidence either way. Needs 5 agency interviews.
- **Brazilian Telegram VIP bots:** real revenue for AlphaVips, PinkBot and others (only processed volume is claimed). Which Pix payment providers tolerate adult sellers long-term (PushinPay, SyncPay and others: no policy found).
- **Portuguese astrology/tarot competition:** install counts and update recency for the top Portuguese Play Store results ("baralho cigano", "tarot ia", "mapa astral") were **not checked**. This is the gating check for the survivor.
- **Zentaro and the $4.4k AI tarot listing:** Flippa verification status unconfirmed (one listing was offline when fetched).
- **Brazilian AdMob eCPM and subscription conversion** for spiritual/entertainment apps: no source found. The €1k customer math assumes subscriptions.
- **Legal opinion:** whether a Brazilian resident selling prediction-market or betting analytics software to foreign users has any exposure under Lei 14.790 or CMN Res. 5.298/2026 [U].
- **NSFW-AI affiliate earnings, camming-tool revenue and DMCA-service revenue:** no solo figures found anywhere.
- **Stripe psychic-services status:** the fetched Stripe page (Portuguese locale) lists psychic services as prohibited only in JP/MX/TH, while third parties report account closures elsewhere. Treat Stripe as unreliable for this niche.

## 6. G2 check: Brazilian Play Store (added by main thread, 2026-09-24)

Method: scraped Google Play (gl=BR) search results for tarot, tarô, baralho cigano, tarot IA, horóscopo, mapa astral and cartas ciganas. That gave 97 unique apps, each with install counts and review counts. Raw data: `R5-C-playstore-br-tarot-raw.txt`.

- **There is no language gap.** Global AI-tarot apps are already localised into PT-BR: "Leitura de Cartas de Tarô AI" (Lumi, 1M+ installs, 12.9K reviews), "Tarot IA - Leitura de Cartas" (100K+, 13.2K reviews, which *includes* baralho cigano), "Astrea: Leitura de Tarô IA", "Tarô Estético" and "Horóscopo Diário & Astrologia" (500K+). Co–Star (5M+), Labyrinthos (1M+), Astrolink (1M+, Brazilian) and Personare (Brazilian, includes baralho cigano) are also in the BR results.
- **The baralho cigano sub-niche is small and partly taken.** Dedicated apps top out at 100K+ installs with 0.6K–2.3K reviews (Tarot Cigano - Leitura, Tarot Cigano Lenormand "com IA", Gypsy Tarot, Tarot Cigano). Several were updated in Aug–Sep 2026, so they are maintained, not abandoned. A search for "baralho cigano IA" already returns 15 apps, including AI ones.
- **Implication:** €1k MRR needs about 500 paying subscribers. At the typical 1–3% install-to-paid rate for this category (UNVERIFIED), that means roughly 17k–50k installs, or the entire install base of a top cigano app. That's possible only by *out-ranking* existing, maintained apps, with no structural edge.

**Revised verdict: KILL on G2** (no distribution gap: PT and AI are both already covered). The Flippa earners still prove the money in the category, but a newcomer would compete on ASO/ads against localised global apps.

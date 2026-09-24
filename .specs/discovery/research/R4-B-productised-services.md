# R4-B — Existing Productised Done-for-You Services (fixed monthly price, online checkout)

> Date: 2026-09-23 (search finished 2026-09-24 after a rate-limit pause). Method: `../R4-CRITERIA.md` (capacity model, leverage test, relaxed K12, reinterpreted K1), `../R3-CRITERIA.md` (K13, K15), `../R2-CRITERIA.md` (K1–K11).
> Segment: productised done-for-you (DFY) services that small businesses already buy at a fixed monthly price. Question per candidate: do buyers pay a human even though a cheap tool exists, and is the DFY market already full of cheap productised providers?

## 0. Coverage and quota note (read first)

- **Searches used: ~61 WebSearch calls** (4 of them failed on a session rate limit and were re-run after the reset) plus **~27 WebFetch calls**. That is well inside the ~150 budget. I stopped once the pattern was clear and further searches kept returning the same saturated markets.
- **Blocked sources:** Indie Hackers posts (HTTP 403), rephonic.com (403). Fiverr, Upwork and Reddit threads were not reachable as pages, and search snippets turned up no buyer-side Reddit threads. **No "I tried tool X and hired a human instead" quotes were found.** The R4 hypothesis ("buyers ignore the cheap tool") is supported here only indirectly: DFY sellers and cheap tools coexist at scale in the same niches.
- **Evidence quality:** most prices come from vendor pricing pages (fetched = strong) or from vendor blog "cost guides" (weaker: self-serving, often rounded). Where a figure came only from a search snippet and I could not tie it to a fetched page, it is marked UNVERIFIED.
- **Human-hours figures are my estimates** unless a source is cited. They are order-of-magnitude figures for the capacity model, not measurements.
- **Candidates revisited from R3:** R3 C5 BPO financeiro (killed on K12) was re-checked under R4's relaxed K12 and dies again, this time on the leverage test. R3 #1 US sales-tax filing and R3 C11 licitações were **not** revived, because their still-valid kills (K11 remittance/liability; live bidding = negotiation) are unaffected by R4's changes.

## 1. Summary table

| # | Candidate | Paid evidence (price × freq + URL) | DFY competitors & price floor | Human h/customer/mo (est.) | Verdict | Decisive reason |
|---|---|---|---|---|---|---|
| 1 | Google Business Profile (GBP) management, US | Agencies $125–400/mo per profile (https://www.merchynt.com/post/google-my-business-management-pricing) | Very many agencies. Software that does the work: Renew Local **$30/mo** self-serve (https://renewlocal.com/prices/); Merchynt Paige **$99/mo**, also white-labelled to agencies (https://www.merchynt.com/paige) | ~1 with AI (DIY 5–10, per a Merchynt claim) | KILL | Leverage test fails: today's providers already run the same AI tool (white-label Paige). Price floor is software at $30–99. Commodity + K3 |
| 2 | GBP management, Brazil | Freelancers R$599–700/mo (https://escoladeseo.com/opiniao-de-profissionais-quanto-cobrar-em-servicos-de-google-meu-negocio/) | Local agencies and freelancers; PT-language AI review tools (Localo, Semrush Local, RepScan: https://www.repscan.com/pt-pt/responder-avaliacoes-com-ia/) | ~1 (a freelancer's own pricing framework assumes 4 h) | KILL (near-miss) | Commodity + AI-wrapper (hard constraints). Sold by WhatsApp/6-month contracts, not checkout. No proof of ≥50% leverage over freelancers who use the same tools |
| 3 | Google review-response management | ReplyClerk $99–199/mo; one DFY $249/mo + $350 setup (search snippet, UNVERIFIED mapping) | CommentAssist / ReplyVera $29/mo; GBPPromote $5.33/location (https://gbppromote.com/google-review-autoresponder-tool/) | <0.5 | KILL | K1: fully automated at $5–29. No human remainder to sell |
| 4 | Local citation / listings management | DFY cleanup $300–1,200 one-off (https://vettted.com/local-citation-building-services/, snippet) | BrightLocal from $39, Yext $199/mo (https://reputationstacker.com/brightlocal-vs-yext/) | <0.5 after build | KILL | K1 + K15 (the work is mostly a one-off build) |
| 5 | Social media posting DFY | $99 Social: $99–279/mo, self-serve checkout, claims 10,000+ SMBs since 2012 (https://www.99dollarsocial.com/) | $99 Social includes an account manager, a content specialist and QA at $99. Many others | 2–4 | KILL | Saturated at a $99 floor with a staffed team. Commodity + K3 |
| 6 | Email newsletter DFY (realtors) | AgentReach $49/$99/$199 per month, written for the agent (https://www.tryagentreach.com/real-estate-email-newsletter) | AgentReach, Hoppy Copy (AI), KCM, Fast Newsletters from $13 (https://www.fastnewsletters.com/) | 1–3 | KILL | Saturated productised DFY at $49–199. AI content (K3) |
| 7 | Podcast editing / production | We Edit Podcasts $249–549/mo for 5 episodes, no contract (https://weeditpodcasts.com/pricing/, snippet); premium $2,000/episode (https://www.volubilitypodcasting.com/podcast-pricing) | Many; freelance $75–250/episode (snippet, UNVERIFIED) | 5–10 (1–2 per episode even with AI) | KILL | Capacity: fits only ~4–8 customers. No ≥50% leverage over offshore teams that already use AI editors |
| 8 | WordPress care plans | Basic $30–100/mo, standard $100–300 (https://fatlabwebsupport.com/blog/website-maintenance/wordpress-care-plan-pricing/) | WP Buffs, Seahawk from $49 (snippet), hundreds more | <0.5 basic | KILL | Already automated (ManageWP-style bulk updates). Floor $30–49, commodity |
| 9 | Shopify "unlimited tasks" store maintenance | $50–1,000+/mo (https://brainspate.com/blog/shopify-maintenance-cost-guide/, snippet) | Many agencies | Unbounded (dev work) | KILL | Scope is open-ended dev and design work: capacity model fails, leverage unprovable |
| 10 | Monthly SMB bookkeeping | Bench from $199/mo (https://www.bench.co/); RemoteBooksOnline from $150 (https://www.remotebooksonline.com/pricing) | Very many; Maxim Liberty from $75 (https://bookkeeping-services.com/pricing/) | 2–5 | KILL | Saturated. Providers already heavily automated. Bench, the "software + human at scale" model with 35k customers (https://nanoglobals.com/productized-service-websites/), collapsed Dec 2024 with >$65M debt (https://www.geekwire.com/2024/bench-accounting-to-be-acquired-by-employer-com-following-abrupt-shutdown/) |
| 11 | Bookkeeping catch-up | $150–1,200 per month behind (https://www.sdocpa.com/catch-up-bookkeeping-cost-guide/, snippet) | Many | n/a | KILL | K15: one-off |
| 12 | BPO financeiro (Brazil, micro firms), R3 C5 re-check | R$800–1,800/mo for micro firms (https://finanservsul.com.br/blog/bpo-financeiro-o-que-e) | Very many BPO firms and accounting firms (Contabilizei sells it via consultation: https://www.contabilizei.com.br/contabilidade-online/bpo-financeiro/). Provider software: BPO Suite R$159–199/mo (https://bposuite.com.br/empresas/planos-e-precos/), Nibo Open Finance reconciler (https://www.nibo.com.br/conciliador-open-finance) | 6–12 | KILL | Leverage test fails: incumbent BPO firms already run Open Finance auto-reconciliation. Bill-payment authority/bank access (K11 risk). Sold via WhatsApp/consultation |
| 13 | AR follow-up / collections DFY | $300–700/mo fixed, usually bundled with books (https://growthy.com/blog/accounts-receivable-outsourcing, snippet); Steph's Books from $350/mo (https://stephsbooks.com/our-services/accounts-receivable-services) | AI tools that chase by email/SMS/phone for a flat fee (https://accountsreceivable.ai/) | 2–6 | KILL | Phone calls to debtors are core (forbidden). Negotiation (K12 still-kill). K1 automation |
| 14 | Chargeback dispute DFY | Chargeflow 25% of recovered amount, no monthly fee (https://www.chargeflow.io/pricing) | Chargeflow, Chargeback.io, etc. | ~0 | KILL | K1: fully automated, success-fee priced. Recovery pattern (R2) |
| 15 | US sales-tax filing DFY (R3 #1) | Accountant $70–300+/mo (vendor claim) | DAVO $57.99/mo (R3) | n/a | KILL (not revived) | K11 (remitting tax money) + filing liability. R4 does not relax these |
| 16 | **COI tracking, full-service, for small GCs / property managers** | Full-service **$5–15+/vendor/mo** (https://coverwarden.com/learn/coi-tracking-software-cost); CertFocus full-service $13–29/vendor/yr **with $10k annual minimum** (https://www.vertikalrms.com/article/how-much-does-coi-tracking-software-cost-2026-pricing-guide/); bcs full-service **$10k minimum**, quote only (https://www.getbcs.com/pricing-and-plans) | Full-service is enterprise-only (minimums). Self-serve software: bcs **free** tier with AI extraction and automated requests; SmartCOI $79/mo (search snippet) | 1–2 for ~50 vendors (est.) | **UNCERTAIN** | Clear price gap below the $10k minimums, and the work fits the capacity model. But no evidence that small buyers pay humans for this, and free AI tools already chase vendors |
| 17 | **Provider credentialing maintenance (CAQH re-attestation, expirables, recredentialing)** | $30–60/provider/mo (https://physicianpracticespecialists.com/credentialing-maintenance-service/); $50–200/provider/mo (https://www.supanote.ai/blog/best-credentialing-services-for-mental-health-providers and search snippets, UNVERIFIED) | Many offshore/RCM firms (PPS, Medicotech, IntelliRCM, MedSole, Credex…), almost all quote/call-based. Software $15–50/provider/mo (snippet) | 0.5–1 per provider | **UNCERTAIN** | Real recurring DFY spend, low human time, fits the capacity model. Weak on self-serve buying, payer phone follow-up, portal work with no API (K13-ish) and a crowded offshore market |
| 18 | Therapist payer enrollment | GetPaneled $79/payer, $349 for 5 payers, online checkout (https://www.getpaneled.com/pricing) | GetPaneled; free via Headway/Grow/SonderMind (https://www.supanote.ai/blog/best-credentialing-services-for-mental-health-providers) | n/a | KILL | K15 (one-off) + K1 (free platform route) + already productised at $79 |
| 19 | DOT compliance for small trucking fleets | My Safety Manager $49/driver/mo (https://www.mysafetymanager.com/, snippet); Evergreen $349/yr, 5-min checkout (https://www.evergreencomply.com/compliance/owner-operators) | Many; Vertical Identity $85/yr (https://verticalidentity.com/pricing/) | <0.5 per driver | KILL | Saturated productised DFY at low floor. Drug-testing consortium needs C/TPA registration + MRO (licensed, K11/K12) |
| 20 | Business-license / annual-report managed service | Harbor Compliance: managed licensing quote-only; software suite $399–799 (https://ecommerceparadise.com/harbor-compliance-pricing-2026/, snippet) | Harbor, CT Corp, registered agents | n/a | KILL | K15 (annual per license) + K6 (quote/sales) |
| 21 | Amazon account management | $900–2,500/mo (https://sellercandy.com/amazon-account-management-services, https://parker-lambert.com/services/amazon/full-service-amazon-account-management/) | Many agencies | 10–20+ | KILL | Capacity (daily monitoring) + K12 (strategy, ads) + K13 (Seller Central) |
| 22 | Etsy shop management | Monthly packages exist; price UNVERIFIED (https://www.etsy.com/listing/4359161368/monthly-etsy-shop-management-seo-listing) | Upwork "from $20" (https://www.upwork.com/services/ecommerce-management/get/etsy) | 3–8 | KILL | Commodity at freelance rates; strategy/ads judgement |
| 23 | Restaurant delivery-app menu management | Integration software ~$115/mo; ChowNow $199 (search snippet, UNVERIFIED) | Stream, KitchenHub, Otter sync menus from the POS (https://www.streamorders.com/) | ~0 | KILL | K1/K9: POS-to-app sync software. No DFY spend found |
| 24 | DMCA / leak takedowns for creators | Subscriptions $59–299/mo (https://copyrightshark.com/pricing/, https://fanlock.com/blog/dmca-protection-cost-guide) | Many (Ceartas, Rulta, Copyright Shark…) | <1 | KILL | Saturated, already automated scanning + templated notices |
| 25 | Trademark watch | $59.95/mo basic (snippet); $597/yr (https://www.branddiplomacy.com/post/trademark-monitoring-services-are-they-worth-it) | Law firms, Corsearch, TM TKO | <1 | KILL | Paid value is attorney analysis (licensed, K12 still-kill) |
| 26 | Personal data-broker removal | DeleteMe $129/yr (https://www.security.org/data-removal/deleteme/) | Incogni, Optery, etc. | ~0 | KILL | K10: consumer, ~$10/mo |
| 27 | Grant reporting retainer (nonprofits) | Retainers $1,500–8,000/mo (https://fundingforgood.org/nonprofit-consulting-retainer/, snippet) | Consultants | 10–20 | KILL | Capacity + writing/relationship judgement + reports mostly quarterly/annual (K15) |
| 28 | Licitações assessoria (Brazil), R3 C11 | Per R3 | ConLicitação, Effecti (R3) | n/a | KILL (not revived) | Live pregão bidding is negotiation (still-kill) + K1 (R3) |

**Result: 28 candidates. 0 SURVIVE, 2 UNCERTAIN (#16 COI full-service for small buyers, #17 credentialing maintenance), 26 KILL.**

## 2. Per-candidate notes

### 1–2. Google Business Profile management (US and Brazil)
- **Paid evidence:** US agencies charge $125–400/mo per profile, plus about $499 setup (https://www.merchynt.com/post/google-my-business-management-pricing). Brazil: named freelancers charge R$600/mo maintenance plus R$900 setup, R$600–700, and "from R$599 with a 6-month minimum" (https://escoladeseo.com/opiniao-de-profissionais-quanto-cobrar-em-servicos-de-google-meu-negocio/). A Brazilian agency blog says R$500–1,500 for small firms (https://www.beonmarketingfortaleza.com.br/blog/gestao-perfil-empresa-google-quanto-custa.html, snippet).
- **R4 hypothesis check:** this is the clearest case of buyers paying humans while cheap tools exist. Renew Local ($30/mo, self-serve, AI replies and post automation) and Paige ($99/mo, "manages your Google Business Profile for you", G2 4.9) sit next to $125–400 agency retainers. **But** Merchynt also sells Paige white-label to agencies "to manage dozens or even hundreds of profiles" (https://www.merchynt.com/gmb-management-services-white-label). So today's human providers already have the leverage. A new entrant would not cut their time by ≥50%.
- **Deliverable:** weekly posts, photos, review replies, Q&A, monthly report. All AI-generatable, which makes it the AI-wrapper and commodity shape the founder excluded.
- **Brazil variant:** it has the most interesting price (R$600 ≈ €97/mo, about 1 h of software-assisted work). It still dies: it is commodity; it is sold by WhatsApp with 6-month contracts; PT-language AI review tools already exist; and nobody showed that Brazilian freelancers work slower than a software-assisted operator would. **KILL, near-miss.**

### 3. Review-response management
Tools cover it end to end: GBPPromote $5.33/location, CommentAssist $29–79, ReplyVera $29 (https://www.commentassist.com/blog/services-manage-google-reviews). No human remainder is worth €100+. **KILL (K1).**

### 4. Citation / listings management
BrightLocal from $39 and Yext $199/mo (https://reputationstacker.com/brightlocal-vs-yext/). The DFY work is a one-off cleanup. **KILL (K1, K15).**

### 5. Social media posting DFY
$99 Social: $99–279/mo, 10–30 posts, online checkout, "10,000+ small businesses", with an account manager, content specialist and QA specialist per account (https://www.99dollarsocial.com/). **This proves the R4 business model works at scale.** It also shows that the market sets a $99 floor with a staffed team. A solo operator can't undercut that, and AI content is K3. **KILL.**

### 6. Newsletter DFY
AgentReach writes custom local-market newsletters for realtors at $49/$99/$199 (https://www.tryagentreach.com/real-estate-email-newsletter). Generic DFY email marketing is quoted at $300–1,500/mo (https://www.lyfemarketing.com/email-marketing-pricing/), but the vertical productised floor is $49. **KILL.**

### 7. Podcast editing
We Edit Podcasts sells 5 episodes/month from $249 with no contract (https://weeditpodcasts.com/pricing/, snippet). Even with AI editors, each episode needs 1–2 h of human listening and fixing, so 5–10 h per customer. At $249 that is ~$25–50/h, but only 4–8 customers fit in 43 h. No ≥50% leverage over existing teams. **KILL.**

### 8. WordPress care plans
Basic plans at $30–100/mo are already automated (updates, backups, monitoring) (https://fatlabwebsupport.com/blog/website-maintenance/wordpress-care-plan-pricing/). Hundreds of providers. **KILL.**

### 9. Shopify maintenance subscriptions
Open-ended development and design work at $50–1,000+/mo (https://www.charleagency.com/articles/shopify-support-maintenance/). Human time is unbounded and the value is skilled judgement. **KILL.**

### 10–11. Bookkeeping (monthly and catch-up)
- Monthly: $150–400 (Bench $199, RemoteBooksOnline $150, 1-800Accountant $395 per https://1800accountant.com/blog/7-best-online-bookkeeping-services-for-small-businesses, snippet). Human 2–5 h/mo per client even with bank feeds. Offshore and software-leveraged competitors are everywhere.
- **Cautionary data point:** Bench, the flagship "software plus human bookkeeping at scale" productised service (35,000+ customers), shut down on 27 Dec 2024 and filed for bankruptcy with over $65M of debt (https://www.geekwire.com/2024/bench-accounting-to-be-acquired-by-employer-com-following-abrupt-shutdown/, https://en.wikipedia.org/wiki/Bench_Accounting). The model sells, but margins at ~$200/mo are hard even with heavy software.
- Catch-up is one-off (K15). **Both KILL.**

### 12. BPO financeiro (Brazil), R3 C5 re-checked under R4
- **Why revisit:** R3 killed it mainly on K12 (trust, paying bills), which R4 relaxes.
- **Evidence:** micro firms (≤50 transactions/mo) pay R$800–1,800/mo; small firms pay R$1,800–4,500 (https://finanservsul.com.br/blog/bpo-financeiro-o-que-e). Another guide gives R$800–3,000 (https://blog.bpospace.com.br/post/tabela-precos-bpo-financeiro-guia-completo-contadores).
- **Capacity:** at R$1,000 (~€160) you need ~6–7 clients for €1k, so ≤6.5 h each. That is plausible for a micro firm with ~50 transactions.
- **Why it still dies:** (a) **Leverage test.** Incumbent BPO firms already use Nibo's Open Finance reconciler ("concilie milhares de lançamentos em segundos") and BPO Suite at R$159–199/mo, sold to them as "more clients without more staff" (https://www.bposuite.com.br/blog/open-finance-no-bpo-financeiro-como-funciona-na-pratica/). A newcomer has no ≥50% edge. (b) Paying bills needs bank credentials or payment authority (K11 risk; the R3 concern stands). (c) Buyers expect WhatsApp contact daily and hire through a consultation, not a checkout (Contabilizei routes to a specialist). **KILL.**

### 13. AR follow-up / collections
Priced at $300–700/mo, usually bundled with bookkeeping. Steph's Books "from $350/mo" includes "direct follow-up emails **and calls**" (https://stephsbooks.com/our-services/accounts-receivable-services). The value is phoning and negotiating with debtors, both forbidden. The email/SMS part is automated by tools. **KILL.**

### 14. Chargebacks
Chargeflow: 25% of recovered amount, no monthly fee, automated (https://www.chargeflow.io/pricing). **KILL.**

### 15. US sales-tax filing (not revived)
R3's K11 (holding and remitting tax money) and filing liability are not changed by R4. **KILL.**

### 16. COI tracking, full-service for small buyers: UNCERTAIN, see §3

### 17. Credentialing maintenance: UNCERTAIN, see §3

### 18. Therapist payer enrollment
Already productised with online checkout: GetPaneled $79/payer, $349 for 5 payers, with a 6-month guarantee (https://www.getpaneled.com/pricing). Headway, Grow and SonderMind credential therapists for free. It is also one-off (K15). **KILL.**

### 19. DOT compliance for small fleets
My Safety Manager $49/driver/month; Evergreen Comply $349/yr for owner-operators with a "five-minute checkout" (https://www.evergreencomply.com/compliance/owner-operators). The anchor service (random drug-testing consortium) requires C/TPA registration and an MRO. **KILL.**

### 20. Business licence / annual reports
Annual per filing (K15). Harbor's managed licensing is quote-only (https://www.harborcompliance.com/business-licensing-service). **KILL.**

### 21. Amazon account management
Seller Candy $997–2,500/mo; Parker-Lambert $900–1,100/mo. Daily monitoring, strategy and Seller Central-only work mean the capacity, K12 and K13 kills all apply. **KILL.**

### 22. Etsy shop management
Monthly packages exist on Etsy, Fiverr and Upwork; Upwork shows "from $20" (https://www.upwork.com/services/ecommerce-management/get/etsy). Commodity, and the value is marketing judgement. **KILL.**

### 23. Delivery-app menu management
POS-to-marketplace sync software (Stream, KitchenHub) removes the job (https://www.trykitchenhub.com/developer). No evidence of a DFY recurring spend. **KILL.**

### 24. DMCA takedowns for creators
$59–299/mo subscriptions with "unlimited takedowns" (https://copyrightshark.com/pricing/). Crowded and already automated. **KILL.**

### 25. Trademark watch
Cheap monitoring ($59.95/mo) exists. The paid value is an attorney deciding whether to oppose (licensed). **KILL.**

### 26. Data-broker removal
DeleteMe $129/yr, part human, part automated (https://www.security.org/data-removal/deleteme/). Consumer pricing, far below the band. **KILL.**

### 27. Grant reporting
Retainers of $1,500–8,000/mo, "up to two grant deliverables per month" (https://fundingforgood.org/nonprofit-consulting-retainer/, snippet). Writing, funder relationships, and reports that are mostly quarterly or annual. **KILL.**

### 28. Licitações (not revived)
R4's relaxation doesn't reach the core: live pregão bidding is negotiation, and ConLicitação/Effecti cover search and documents (R3 C11). **KILL.**

## 3. Deep-dive: the two UNCERTAIN candidates

### #16 COI tracking as a done-for-you service for small GCs and property managers

**The gap.** Full-service COI management (humans read certificates and endorsements, chase vendors, handle deficiencies) exists, but only above a minimum: bcs full-service needs **$10,000/yr** and a custom quote, with 6–8 weeks onboarding (https://www.getbcs.com/pricing-and-plans); CertFocus full-service also needs a **$10,000 minimum** plus a $3,500–4,800 implementation fee (https://www.vertikalrms.com/article/how-much-does-coi-tracking-software-cost-2026-pricing-guide/). A small GC or property manager with 30–100 vendors can't buy it. They get software (bcs free, SmartCOI $79/mo) or do it by hand.

**Must-answer questions**
1. **Who pays a human today, how much, how often?** Large portfolios pay full-service providers about $5–15+/vendor/month (https://coverwarden.com/learn/coi-tracking-software-cost), monthly and ongoing. Vertikal claims admins spend "20+ hours per week" on certificate tracking in larger firms (vendor claim). **Small buyers paying humans for this: NOT evidenced.** The R3 insurance-agency VA teams ($3,449/mo, https://www.agencyva.com/pricing) are on the *issuing* side, not the tracking side.
2. **Why not the cheap tool?** No evidence either way for small buyers. The best argument is structural: free tools still leave a person to read endorsement pages and decide on deficiencies. Coverwarden says the key question is "who reads [the endorsement pages] and how long does it take?". That residual is what full-service sells.
3. **Human time and capacity.** Offer: $250/mo for up to 50 vendors ($5/vendor, the bottom of the full-service range). Each vendor renews ~1–3 certificates a year, so ~4–10 certificates arrive per month. With AI extraction plus automated email chasing, each certificate takes ~5–10 min of review; add deficiency emails. That gives **~1–2 h per customer per month**. 5 customers × $250 ≈ €1.07k MRR at ~5–10 h/month, well inside 43 h. Leverage vs a manual in-house admin or a full-service analyst: plausibly ≥50%, since extraction and chasing are automated. But full-service firms already run software, so the leverage edge over *them* is unproven.
4. **How a buyer finds and buys it without a call.** Search ("COI tracking service small contractor", "vendor insurance compliance property manager") and a pricing page with vendor-count tiers and checkout. Delivery contact is email with the customer and with vendors or their insurance agents (async written, allowed by R4). No phone.

**Risks that could kill it:** (a) K1 in its R4 form: free bcs and $79 SmartCOI already "chase vendors for you", so small buyers may never pay a human premium. (b) Liability/K12: approving a deficient certificate has real consequences. Full-service firms staff CIC/CPCU-credentialed reviewers. This is not formally licensed sign-off, but it is close. (c) Small buyers may not feel the pain enough to pay €200+/mo (K5).
**Next evidence needed:** buyer posts from small GCs/PMs paying a VA or a service for COI chasing (founder manual sweep: Upwork "COI tracking", r/PropertyManagement, r/Construction).

### #17 Provider credentialing maintenance (small US practices)

**Must-answer questions**
1. **Who pays a human today, how much, how often?** Small practices and clinicians pay monthly per-provider fees: $30–60/provider/mo (PPS, which covers CAQH attestation, expirables tracking, recredentialing and Medicare revalidations: https://physicianpracticespecialists.com/credentialing-maintenance-service/), and "$50–200 per provider" per guides (https://www.supanote.ai/blog/best-credentialing-services-for-mental-health-providers; the snippet figure is UNVERIFIED). The spend is monthly and recurring. The underlying work is lumpy: CAQH every 120 days, payer recredentialing every 2–3 years, licence/DEA/malpractice renewals.
2. **Why not the cheap/free tool?** CAQH itself is free and sends reminders, and tracking software costs $15–50/provider. Clinicians still pay because the work is portal data entry they don't want to do, and a lapse stops payer access (claims held). This is the R4 "take it off my plate" pattern. The evidence is vendor-side only (many vendors sell it), not buyer quotes.
3. **Human time and capacity.** Estimate per provider per month: CAQH re-attestation ~15 min × 3/yr (~4 min/mo); expirables automated; recredentialing ~2–4 h per payer per 2–3-year cycle × ~5 payers (~0.3–0.5 h/mo); ad hoc updates ~0.2 h. **≈0.5–1 h per provider per month.** At $60/provider, 15 providers (e.g. 5 practices × 3) ≈ $900 ≈ €830 at ~8–15 h/month. It fits the 43 h budget, with room to grow to ~40 providers. Leverage: software can pre-fill, track and draft, but CAQH and payer portals have no API for small practices (CAQH bulk upload is for groups of 50+ providers: https://www.caqh.org/hubfs/43908627/drupal/solutions/proview/guide/practice-manager-user-guide.pdf). The human still does portal entry, so the ≥50% cut is **plausible but unproven**.
4. **How a buyer finds and buys it without a call.** Search ("CAQH re-attestation service", "credentialing maintenance per provider") and therapist or small-practice communities, with checkout per provider. GetPaneled shows clinicians will buy credentialing online by checkout (https://www.getpaneled.com/pricing). **No maintenance-only self-serve subscription was found**: incumbents (PPS, Medicotech, IntelliRCM, MedSole) all route to calls or quotes. That is both the gap and a warning.

**Risks that could kill it:** (a) Payer follow-up in recredentialing is often by phone (GetPracticeHelp calls a 2-weekly payer follow-up cadence "standard": https://www.getpracticehelp.com/credentialing/credentialing-pricing-cost-guide/). That breaks the no-phone rule unless scope is limited to CAQH, expirables and portal-only payers. (b) Sensitive provider data (SSN, DEA, licences) is a security burden (K11-adjacent). (c) The provider stays legally responsible for attested data (https://resources.instafill.ai/docs/credentialing/caqh-proview-management-guide), which keeps us out of licensed sign-off but carries error risk. (d) A crowded offshore RCM market at $25–60/provider sets the price. (e) Therapists, the largest self-serve segment, can get credentialed free via Headway/Grow. (f) The founder has no US healthcare domain background (UNVERIFIED assumption).
**Next evidence needed:** clinician posts (r/therapists, r/PrivatePractice, SimplePractice/Facebook groups) paying monthly for CAQH/maintenance, and whether any payers in scope need phone follow-up.

## 4. Segment finding

1. **The R4 business model is proven, but the proven niches are already full.** Fixed-price, checkout-bought, software-plus-human services exist at scale: $99 Social (10k+ SMBs at $99), AgentReach ($49–199), We Edit Podcasts ($249+), WordPress care plans ($30+), Bench (35k customers before collapse), Evergreen Comply ($349/yr). In every niche where a productised DFY offer is easy to find, **the DFY price floor has already dropped close to the tool price.** The competitor is now another software-leveraged DFY shop, not a slow human.
2. **The leverage test is the new decisive kill.** Where buyers clearly pay humans despite cheap tools (GBP management, BPO financeiro, bookkeeping), the human providers **already use the same automation** (white-label Paige, Nibo Open Finance, bank feeds). A newcomer gains no ≥50% time cut over them. R4's relaxed K12 revives nothing by itself.
3. **Where a gap exists, it is a minimum-size gap, not a missing-product gap.** COI full-service (enterprise minimums ~$10k/yr) and credentialing maintenance (quote/call-only incumbents) are the two places where small buyers can't easily buy DFY online. Both fit the capacity model on paper (≤2 h/customer/mo for COI; ≤1 h/provider/mo for credentialing). Neither has buyer-side evidence that small customers pay for it.
4. **The still-kill rules bite often:** phone contact (AR collections, payer follow-up), negotiation (licitações, collections), licensed judgement (trademark, DOT MRO), money handling (sales tax, BPO bill-pay).

## 5. Evidence gaps

- **No buyer-side quotes** ("I pay someone $X/mo for COI/CAQH/GBP despite tool Y"). Reddit, Upwork and Fiverr were not readable. This is the key test of the R4 hypothesis, and it belongs to the founder's manual sweep (`../R4-MANUAL-SWEEP.md`). Suggested searches: Upwork "COI tracking" / "certificate of insurance" ongoing; Upwork "CAQH" / "credentialing maintenance" ongoing; r/PropertyManagement "COI"; r/therapists "CAQH service".
- **Human-hours figures are estimates**, not measurements, for every candidate, including the two UNCERTAIN ones.
- **Several prices are search-snippet only** (marked UNVERIFIED): SmartCOI $79, credentialing $50–200/provider, We Edit Podcasts $249, My Safety Manager $49/driver, ReplyClerk, restaurant menu tools.
- **Indie Hackers productised-service interviews (403)** could not be read, so revenue/hours-per-client figures from real operators are missing.
- **No check of the price elasticity** of small GCs/PMs for a $150–300/mo COI service, or of small practices for maintenance-only credentialing.

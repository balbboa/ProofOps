# R6 — Synthesis: Sub-niche Selection (any niche, proven money)

> Date: 2026-09-24. Tools: WebSearch only. **Play Store, App Store, iTunes API and TrustMRR were all blocked (HTTP 403) in this session**, so store-level incumbent data (installs, ratings, last update) could not be collected.
> Direction changed mid-round (founder, 2026-09-24): "any niche, no criteria, no moral filter, money first, solo, €1k+ MRR, minimal effort." That is the R5 brief, so R6 continued R5's pending step (UD-013: pick a sub-niche). The B2B pass run under `../CHARTER.md` earlier in this round is recorded in §3 for reference.

## 1. Verdict

**One candidate is worth a cheap real-world test: a multi-card "meses sin intereses" (MSI) instalment tracker for Mexico.** It copies a payment-verified earner (Parceladinho, BR, $2.07k MRR, 444 subs) into a new country where the same behaviour is larger and no dedicated app turned up in search.

**Status: GO for validation (≤ 2 weeks, ≤ €100). NOT a GO to build the full product.** Profit can't be guaranteed. This is the best-evidenced bet, not a sure one.

## 2. The candidate: MSI tracker (Mexico), then cuotas trackers (CO/CL/AR)

| Item | Evidence / answer |
|---|---|
| Proven model | Parceladinho: credit-card instalment ("parcelas") tracker, BR, **$2,066 MRR, 444 subs, launched 2026**, found through ASO plus how-to SEO. Verified by RevenueCat on TrustMRR (R5-A). |
| Same problem abroad | Mexico: **~50% of buyers planned to use MSI in Buen Fin 2025** ([marketing4ecommerce](https://marketing4ecommerce.mx/mexicanos-compras-meses-sin-intereses-buen-fin/)). **19.3% of card credit balance is MSI** (Banxico via [El Financiero](https://www.elfinanciero.com.mx/mis-finanzas/2025/11/08/buen-fin-2025-que-conviene-comprar-a-meses-sin-intereses-y-que-no-tips-para-finanzas-personales-sanas/)). **>30% of cardholders have paid late; 42.1% carry a revolving balance** ([El Demócrata](https://www.eldemocrata.com/el-error-financiero-que-cometen-4-de-cada-10-mexicanos-meses-sin-intereses-anos-de-deuda-el-costo-del-buen-fin-y-como-salir-de-el/)). CONDUSEF warns about stacked MSI ([CONDUSEF](https://www.condusef.gob.mx/index.php?p=contenido&idc=438&idcat=1)). |
| Competition found | Only each bank's own app (BBVA, Nu, Klar, Stori, RappiCard, Mercado Pago), which shows **its own card only**. No dedicated multi-card MSI tracker surfaced across 3 searches, and a Promodescuentos thread asks for one ([thread](https://www.promodescuentos.com/discusiones/ayuda-app-para-control-tarjetas-de-credito-312776)). Argentina: Qota (free, pre-launch on Google Play). **No search result ≠ no competitor.** General budgeting apps (Fintonic, Wallet, Monefy) are not checked store-side. |
| Why us | Banks never show *other* banks' cards. A multi-card view sits outside each bank's scope. Department-store cards (Liverpool, Coppel) are included. |
| Why now | **Buen Fin 2026 (mid-November, ~7 weeks away)** is the yearly MSI peak, followed by the "January hangover" of stacked instalments. Seasonal search spike = free acquisition window. |
| Channel | ASO ("meses sin intereses", "control tarjetas de crédito") plus how-to SEO per bank ("cómo ver mis meses sin intereses BBVA/Nu/Liverpool"), the tactic Parceladinho used in PT. |
| Price hypothesis | MXN 49/mo or MXN 399/yr (≈ $2.7 / $22), 7-day trial. Parceladinho's observed ARPU is ~$4.65. **€1k MRR ≈ 300–400 subs.** |
| MVP (≤ 4 weeks part-time) | Manual entry of MSI purchases + statement cut-off/payment dates per card. A "this month you owe X; free from debt on date Y" view. Payment reminders. Paywall after 2 cards or 5 purchases. Optional later: photo/PDF statement reading (LLM, cents per scan). Expo/React Native + RevenueCat, local-first storage (no bank credentials). |
| Cost / ops | Apple $99/yr, Google $25 once, RevenueCat free <$2.5k MTR, domain ~€1/mo → **~€10/mo**. Ops 1–2 h/week (reviews, email). No calls. |
| Top risks | (1) Store-level competitor check not done (blocked). (2) Parceladinho's revenue is months old and may be a launch spike. (3) A bank or PFM app adds a multi-card MSI view (Open Finance in Mexico is slow, which lowers this risk). (4) Low ARPU needs volume; base rate is 1 in 3–5 apps working. (5) Spanish copy: founder is a PT speaker (manageable). |
| Expansion | Same app, local strings: Colombia/Chile (cuotas on almost every card purchase), Argentina (cuotas sin interés; weak currency lowers ARPU). |

### Validation plan (thresholds fixed before starting)

1. **Founder manual store check (15 min, blocked for the agent):** search the MX App Store and Google Play for "meses sin intereses", "MSI", "control tarjetas", "cuotas". **Kill** if an app with ≥ 100k installs, rating ≥ 4.3 and an update in the last 6 months already does multi-card MSI tracking.
2. **Smoke test (≤ €100, ~1 week):** a Spanish landing page ("Todos tus meses sin intereses, de todas tus tarjetas, en un solo lugar") showing the price, a waitlist and a "pre-order the yearly plan at 50% off" button. Run €50–100 of Google/Meta ads in MX on MSI keywords.
   - **GO to build** if ≥ 20% of visitors join the waitlist **and** ≥ 5 pre-orders (or ≥ 3% of visitors click the paid option).
   - **KILL** if < 5% join the waitlist after ≥ 500 visitors.
3. If GO: ship the MVP before Buen Fin (Nov 2026). Success is **≥ 100 paying subs by end of January 2027**. Stop if < 30.

## 3. What else was killed this round

| Candidate | Why killed | Source |
|---|---|---|
| Mercado Livre fee/freight audit | Hunter HUB, Go Smarter, Marketize and Polivision already do it self-serve. It is also reconciliation (the NO-GO category). | [Hunter HUB](https://hunterhub.com.br/) |
| TLS 200/100/47-day certificate renewal | CertKit free to $99/mo, plus CA-native tools | [CertKit](https://www.certkit.io/pricing) |
| FinCEN real-estate reports | Rule vacated 19 Mar 2026; Qualia gives the feature away free | [Foley](https://www.foley.com/insights/publications/2026/03/federal-court-vacates-fincen-residential-real-estate-reporting-rule/) |
| EUDR SME due diligence | EUDRReady free/€29, TracePlot €59, osapiens, IntegrityNext | [Coolset](https://www.coolset.com/academy/best-6-eudr-compliance-tools-for-2026-supply-chain-due-diligence) |
| NR-1 psychosocial risk (BR) | NR Guard free ≤5 staff, and many others | [NR Guard](https://nrguard.com.br/nr-1/) |
| US container D&D invoice checks | Freight-audit platforms and Cubic already cover it; mid-market buyers | [FMC](https://www.fmc.gov/articles/fmc-publishes-final-rule-on-detention-and-demurrage-billing-practices/) |
| Shared-solar credit management (BR) | Sunne, Wattio, GDASH, Digital Grid, PowerRev, etc. | search results |
| Brazil Apple link-out checkout | Link-outs still cost a 15% fee; RevenueCat/Stripe absorb | [MacMagazine](https://macmagazine.com.br/post/2025/12/23/apple-permitira-compras-externas-e-lojas-alternativas-a-app-store-no-brasil/) |
| California DROP compliance for small data brokers | DataGrail, Transcend, Ketch, OneTrust, UnsubCentral; hash matching is a one-off script; Aug 2026 deadline already passed | [DataGrail](https://www.datagrail.io/solutions/drop-compliance/) |
| Google Play 12-tester requirement | Testers Community $15, PrimeTestLab $19.99 | [Testers Community](https://www.testerscommunity.com/) |
| EU CRA vulnerability reporting | Micro/small makers exempt from reporting fines; free DIY route | [ENISA](https://www.enisa.europa.eu/news/the-cra-single-reporting-platform-is-launched) |
| Direct-sales reseller / "fiado" apps (BR) | Minhas Vendas, Revendi, Minha Revenda, Fiado Fácil, Meu Fiado, Venda Fácil + free brand apps | search results |
| Domestic-worker payroll (BR) | Free eSocial Doméstico gov app + Doméstica Legal, Doméstica App, Hora do Lar, NOLAR | [gov.br](https://www.gov.br/esocial/pt-br/empregador-domestico/app-esocial-domestico) |
| Self-managed landlord app (BR) | Aluga Fácil covers it exactly with no fee; QuintoAndar, Imobia, Luvi | [Aluga Fácil](https://www.alugafacil.app/) |
| Miles/points expiry tracker (BR) | AwardWallet free + program apps + FlipMilhas etc. | search results |
| CNH theory-test prep (BR) | Free government app with full course + a dozen simulado apps | [Congresso em Foco](https://www.congressoemfoco.com.br/noticia/114645/nova-cnh-governo-lanca-app-com-curso-teorico-gratuito) |
| Independent driving-instructor finder (BR) | Government CNH do Brasil app does it; Achei Instrutor, Meu Instrutor Legal, EasyCNH | [Agência Brasil](https://agenciabrasil.ebc.com.br/geral/noticia/2026-05/governo-lanca-plataforma-para-facilitar-obtencao-da-cnh) |

## 4. Findings

1. **Obvious Brazil-only niches are already filled**, usually with a free government app on top (eSocial Doméstico, CNH do Brasil, Receita Saúde). R5's earners won by beating *weak* incumbents, and judging weakness needs store data. Next time, collect it with the founder's own browser or in a session where the stores are reachable.
2. **Copying a verified earner into a new geography beats inventing a Brazil niche.** The problem is proven (someone already pays), and the only open question is local competition, which is cheap to check.
3. **Every B2B regulatory "why now" drew cheap tools within months** (EUDR, NR-1, 47-day TLS, DROP). Under the strict B2B charter this round found no survivor either (cumulative R1–R6: ~310 candidates).

## 5. Addendum: website-only niches (founder question, 2026-09-24)

Context: store data is blocked here, but web-search results *are* visible, so web niches are easier to check in this session. R5-D already killed ad/SEO-funded sites (20 candidates: AI answers in search, low PT ad earnings per view, public P&Ls under $728/mo). This pass tested **subscription or paid websites** copying verified earners.

| Candidate | Model copied (verified) | Result | Why |
|---|---|---|---|
| **MSI tracker as a web app (Mexico)** | Parceladinho ($2.07k MRR) | **SURVIVES to validation** | Search results for MSI calculator/tracker queries are weak: generic US loan calculators, a Medium post, one small page ([sokonet](https://sokonet.mx/msi/)) and a **paid Gumroad MSI spreadsheet** ([plantilla msi](https://sprluis.gumroad.com/l/plantilla_msi)). That is evidence that people pay for this job. Caveat: the search tool is US-based, not Google Mexico. |
| Portugal citizenship civics test prep | Francopass ($1.5k MRR) | KILL | Test in law since 19 May 2026 but its format isn't defined yet. Already ≥3 prep sites (Provacidadania €49 one-time, ciple.org, prep2go). One-time payment, not MRR. The residence period rose to 7–10 years, which shrinks the applicant flow. |
| Online legal-notice letters with proof of receipt (BR) | Send Letters Online UK ($5.5k/30d) | KILL | The Correios' own e-Carta/Telegrama online service, AR Online (since 2014, 50M ARs), Arbitralis, Escrybe. |
| Spanish WhatsApp invitations (MX) | Convitede ($1.24k MRR) | KILL | Canva free, invitar.com.mx, Invitio ($29.99/event), invitiapp. |

**Web vs app for the MSI candidate:**
- **Web first is cheaper to validate.** The landing page *is* the product's first page. Build per-bank SEO pages ("cómo ver mis meses sin intereses BBVA/Nu/Liverpool") plus a free MSI calculator as the entry point. Take payment on the web (Paddle/Stripe) and keep the ~15–30% store fee.
- **Trade-off:** it loses app-store search, which is Parceladinho's main channel. Reminders need email or web push instead of native notifications.
- **Recommendation:** web app (PWA) first for the smoke test and SEO. Wrap it for the stores only if paid conversion clears the R6 §2 thresholds.

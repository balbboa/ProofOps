# R2 Stage B/C: Construction pre-flight / readiness-gate candidates

> Date: 2026-09-23. Method: `.specs/discovery/R2-CRITERIA.md` (K1–K11, mandatory economic-transaction evidence, must-prove table).
> Research limits: the session's web-search budget (200 calls) ran out partway through. After that, WebFetch was rate-limited, so some prices come only from search-result snippets. Those are marked **(snippet)**. A claim is **UNVERIFIED** where I could not open the primary page.
> Bottom line: **0 survivors.** Every candidate fails at least one hard kill criterion, and most fail K1: a cheap self-serve tool already does the exact check.

## 1. Summary table

| # | Candidate | Verdict | Decisive reason | Economic transaction found? | Cheapest exact self-serve competitor + price |
|---|---|---|---|---|---|
| 1 | Sub monthly pay-app packet (G702/G703, SOV math, retainage, waivers, backup) pre-submission check | **KILL** | K1: PayAppPro sells self-serve G702/G703 packages with "AI Quality Checks" (tie-out, retainage, missing docs, SOV mismatch) for **$7.99/pay app** or $79–249/mo, "no sales call required". K2/K8: GC portals (GCPay, Textura, Procore Pay) already validate or generate at submission. | **Y**: billing specialists ~$47k/yr ([ZipRecruiter](https://www.ziprecruiter.com/Salaries/Construction-Billing-Specialist-Salary)); median 50 days from pay app to payment, ~32 of them process friction ([Built](https://getbuilt.com/blog/subcontractor-payment-delays/)); Textura charges subs 0.22% of contract, capped at $5k ([search result citing Oracle docs](https://docs.oracle.com/cd/E97083_01/na/10310223.htm)) | PayAppPro, $7.99/pay app; $79/mo SMB ([payapppro.com](https://payapppro.com/)). PAYearned: free tier, $89/mo, or $67/mo annual (snippet, [payearned.com/pricing](https://payearned.com/pricing/)) |
| 2 | Certified payroll (WH-347 / state) prevailing-wage pre-check | **KILL** | K1 + K8: LCPtracker is **free to contractors** and runs 50–80+ validations on the prime's or agency's side. CertifiedPayrollPro is self-serve at **$49/mo + $5/report**, with automatic prevailing-wage checks. K11: worker PII (SSNs, wages). | **Y**: Points North $175/mo + $7.50/report + $995 setup (snippet, [contractorforeman.com](https://contractorforeman.com/certified-payroll-reporting-tools-top-5-options/)); managed payroll services exist, price UNVERIFIED | CertifiedPayrollPro, $49/mo + $5/report ([certifiedpayrollpro.com](https://www.certifiedpayrollpro.com/)); LeaveSheet $19/mo (snippet, UNVERIFIED, [tabletemplates.com](https://tabletemplates.com/certified-payroll-software/)); LCPtracker, $0 to contractor ([lcptracker.com/subcontractors](https://lcptracker.com/subcontractors/)) |
| 3 | Submittal packet completeness vs spec sections | **KILL** | K1 + K3: Deviation Check does exactly this for subs before submission at **$35/review**, with no login and no demo. InspectMind starts at $50 per check. BuildSync and iFieldSmart also exist. Anything new would be "more AI". | Partial: 30–40% of first submittals are rejected (vendor claim, [BuildSync](https://buildsync.ai/resources/why-submittals-get-rejected)); no direct spend figure | Deviation Check, $35/review ([deviationcheck.com](https://deviationcheck.com/)) |
| 4 | Closeout package completeness before final payment / retainage | **KILL** | K5: the pain comes once per project, not weekly. K1/K8/K9: closeout is a module in Autodesk Build and Procore. Closeout Pro "Genie" already detects missing deliverables. Submittal.app compiles O&M packages and has a free start. | **Y** (retainage): retainage release often slips 30–60 days, and retainage can be most of a project's profit ([search summary incl. Siteline/TCG](https://www.siteline.com/blog/guide-to-construction-retainage)); Closeout Pro claims 80–200 admin hours per closeout ([closeout-pro.com](https://www.closeout-pro.com/)) | Submittal.app, free to start; paid price UNVERIFIED ([submittal.app](https://www.submittal.app/guides/o-and-m-manuals-and-closeout)) |
| 5 | Change-order / T&M ticket backup packet | **KILL** | K1: BenchMarx is **free** (4 users, 2 projects), with Pro at $29/user/mo. It merges signed T&M tickets into a change order. Clearstory has a free Basic tier and builds COR packages from T&M tags plus backup. K9: this is a feature of field/PM suites. | Partial: FOUNDATION T&M features from $400/mo (snippet, [Rhumbix](https://www.rhumbix.com/blog/tm-billing-software-construction)); no direct labour/leakage number verified | BenchMarx, free / $29 per user per month (snippet, [softwarefinder](https://softwarefinder.com/construction/benchmarx)) |
| 6 (added) | Public-works bid packet "responsiveness" pre-check (addenda acknowledged, bid bond, required forms) | **KILL** (medium confidence) | K8: e-bid platforms enforce this themselves. PlanetBids blocks submission until all addenda are acknowledged. K1/K3: RFPCheck and ContraVault already cross-check bids against RFP requirements. The economic loss (losing a low bid) is real but rare per bidder (K5). | Partial: nonresponsive-bid rejections are well documented ([GAO B-190286](https://www.gao.gov/products/b-190286), [EJCDC](https://ejcdc.org/bid-responsiveness-correction-of-bid-deficiency-by-hugh-anderson/)); no frequency or cost figure found | RFPCheck, price UNVERIFIED ([rfpai.io](https://www.rfpai.io/?lang=en)); PlanetBids built-in, free to vendors (UNVERIFIED) |
| 7 (idea, not assessed) | Residential builder → lender construction-loan draw packet | **NOT ASSESSED** | The search budget ran out before any evidence was gathered. The lender side is already served by Built / Land Gorilla (from prior knowledge, UNVERIFIED). | n/a | n/a |

## 2. Per-candidate sections

### C1: Subcontractor monthly pay-application packet

**Pain evidence (real and recurring: monthly, per project)**
- Rejections come from a predictable set of causes: SOV tie-out, a missing or incorrect lien waiver, the wrong form, retainage errors, over-billing the SOV, unapproved COs ([PayAppPro](https://payapppro.com/learn/why-pay-applications-get-rejected.php), [Levelset](https://www.levelset.com/blog/5-payment-application-mistakes-subcontractors-make/), [Siteline](https://www.siteline.com/blog/reasons-for-construction-payment-delays)).
- The median time from pay-app submission to payment is 50 days (average 57), and ~32 of those days are process/document friction such as waivers and pay-app assembly and review ([Built](https://getbuilt.com/blog/subcontractor-payment-delays/)). Billd's 2026 survey (600+ subs) gives a 51-day average (cited by Built).
- A "missing lien waiver is the #1 cause of final payment delays" is attributed to ASA surveys in a search snippet. **UNVERIFIED** primary source.
- Job postings list the task explicitly: "preparing AIA G702/G703 progress billings… coordinating all required lien waivers" ([Glassdoor AIA billing jobs](https://www.glassdoor.com/Job/construction-billing-specialist-requires-aia-billing-jobs-SRCH_KO0,52.htm), [Indeed: 600 AIA billing specialist jobs](https://www.indeed.com/q-Aia-Construction-Billing-Specialist-jobs.html)).

**Economic transaction (MANDATORY): found**
- Labour: Construction Billing Specialist, avg $47,241/yr, range $38.5k–$52k ([ZipRecruiter](https://www.ziprecruiter.com/Salaries/Construction-Billing-Specialist-Salary)). AIA-billing postings pay $24–30/h (same source set).
- Portal fees paid by subs: Textura charges 0.22% of contract value, with a $5,000 cap for projects after 19 Jan 2023. A $50k contract costs $110 ([Oracle docs](https://docs.oracle.com/cd/E97083_01/na/10310223.htm), per search result).
- Software spend: PayAppPro $79–249/mo, PAYearned $67–89/mo, Knowify $149–399/mo (snippet, [Siteline blog](https://www.siteline.com/blog/best-construction-billing-software-for-subcontractors)), plus Siteline at a custom annual price tied to billing volume, with implementation fee ([siteline.com/pricing](https://www.siteline.com/pricing)).
- Outsourced: Auteri ("autonomous back office" for subs: assembles pay apps on the GC's form, reconciles SOV and retainage, attaches waivers, submits through the portal, with human review). Price not public ([auteriai.com](https://auteriai.com/resources/why-pay-applications-get-rejected)). Integrative Systems sells outsourced AR/AIA billing ([integrativesystems.com](https://www.integrativesystems.com/accounts-receivable-services-for-construction/)); price UNVERIFIED.

**Competitors**

| Name | Price | Self-serve? | Side | Covers exact job (pre-submission check)? |
|---|---|---|---|---|
| PayAppPro | $7.99 per package; $79 / $129 / $249 per mo ([payapppro.com](https://payapppro.com/)) | Yes, "No sales call required" | Sub | **Yes**: "AI Quality Checks" for tie-out, retainage consistency, missing docs, SOV mismatch |
| PAYearned | Free limited; $89/mo; $67/mo annual (snippet, [payearned.com](https://payearned.com/pricing/)) | Yes | Sub | Mostly: auto-calc makes math errors impossible; no explicit completeness check (UNVERIFIED) |
| Siteline | Custom, by billing volume + implementation fee ([pricing](https://www.siteline.com/pricing)) | No (quote/demo) | Sub | Yes, plus 23k+ GC forms, waivers, compliance ([siteline.com](https://www.siteline.com/)) |
| Auteri | Not public; "free audit" | No | Sub | Yes, done-for-you with human review |
| GCPay | Pricing not public | GC-mandated portal | GC (subs submit) | Validates the application "as it is created" against SOV, contract, required docs ([GCPay blog](https://ww3.gcpay.com/blog-prevent-pay-application-rejections/)) |
| Oracle Textura | Sub pays 0.22% of contract, $5k cap ([Oracle](https://docs.oracle.com/cd/E97083_01/na/10310223.htm)) | GC-mandated | GC | Enforces required fields and compliance in the portal (UNVERIFIED detail) |
| Procore Pay | Not verified | GC-mandated | GC | Auto-generates and regenerates state-compliant waivers when the amount changes ([Procore support](https://support.procore.com/products/online/procore-pay/tutorials/generate-lien-waivers-on-project-invoices)) |
| Trimble Pay (Flashtract) | Not verified | GC-mandated | GC | Automates billing calculations, compliance and waivers ([Trimble](https://www.trimble.com/en/products/trimble-pay)) |

**K1–K11**
- K1 **HIT**: PayAppPro already sells the exact "pre-flight" at $7.99/pay app, self-serve.
- K2 **HIT**: a sub on a GCPay/Textura/Procore job must use the GC's portal, which validates at entry. Subs without a portal just use PAYearned or PayAppPro.
- K3 **HIT**: all that is left to add is more detection, better AI, or a nicer UI.
- K4: no. The sub's controller or owner pays.
- K5: no. The pain is monthly and economic.
- K6: partial. The self-serve competitors show that no-sales-call selling is possible.
- K7: partial. GC-specific forms (Siteline has 23k) are a long tail.
- K8 **HIT**: GC portals already validate.
- K9 **HIT**: this is a feature of pay-app software.
- K10: borderline. $79/mo is the price anchor.
- K11: no.

**Economics:** protecting €300–5,000/mo is plausible (one rejected pay app on a $100k draw costs a month of float). But the ceiling for charging €50–200/mo is set by PayAppPro at $79/mo, and a checker alone competes with a $7.99 per-package price. **Verdict: KILL.**

### C2: Certified payroll (WH-347 / state forms) pre-submission check

**Pain evidence:** the new WH-347 (effective 15 Jan 2025) adds fringe breakdown, journeyworker/apprentice fields and new data validation. The old form is invalid after 30 Sep 2026 ([Points North](https://www.points-north.com/trends-and-insights/still-using-the-old-wh-347-deadline-is-september-2026), [eMars](https://emarsinc.com/blog/what-changed-on-the-2025-wh-347-certified-payroll-form-and-why-it-matters), [Lumberfi](https://www.lumberfi.com/blog/the-new-wh-347-form-what-construction-companies-need-to-know-about-2025-certified-payroll-changes)). The work is weekly on public jobs. Admins reject payrolls in LCPtracker and send feedback ([lcptracker.com](https://lcptracker.com/subcontractors/)).

**Economic transaction: found.** Points North $175/mo + $7.50/report + $995 setup; Miter and Criterion from $50/mo + $6.50/employee (snippet, [contractorforeman.com](https://contractorforeman.com/certified-payroll-reporting-tools-top-5-options/)). Managed services exist (Points North, eBacon managed tier) but the price is UNVERIFIED ([certifiedpayrollpro.com/certified-payroll-services](https://www.certifiedpayrollpro.com/certified-payroll-services)).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| LCPtracker | **$0 to contractors**; the agency or prime pays ([lcptracker.com](https://lcptracker.com/subcontractors/), [ND DOT FAQ](https://www.dot.nd.gov/sites/default/files/documents/civil-rights/FAQ%20LCPtracker%207%20mar%202024.pdf)) | Mandated | **Yes**: 50+ validations including Davis-Bacon rate, fringe, OT and apprentice checks; 80+ math/compliance checks |
| CertifiedPayrollPro | $49/mo + $5/report; $99 + $3; $249 + $1; 14-day trial ([certifiedpayrollpro.com](https://www.certifiedpayrollpro.com/)) | Yes | **Yes**: "auto-check prevailing wage compliance" against the Jan 2025 WH-347 and the county wage determination |
| LeaveSheet | $19/mo (snippet, UNVERIFIED) | Yes | WH-347 and fringe reconciliation |
| Points North (ADP RUN) | $175/mo + $7.50/report + $995 setup (snippet) | Partly | Yes |
| Payroll providers (ADP, Paychex, Gusto integrations) | Bundled | Yes | Partly |

**K1–K11:** K1 **HIT** (free LCPtracker validations and $49 CertifiedPayrollPro). K2 **HIT** (the payroll provider or mandated portal does it). K8 **HIT**. K9 **HIT** (a payroll feature). K11 **HIT** (SSNs, wages, DOL certification liability). **Verdict: KILL.**

### C3: Submittal packet completeness vs spec sections

**Pain evidence:** "30–40% of construction submittals get rejected on first submission" ([BuildSync](https://buildsync.ai/resources/why-submittals-get-rejected); a vendor claim with no primary study). The work recurs per spec section across a project and is bursty early in each job, not steady weekly.

**Economic transaction:** partial. Vendors sell at $1,500/project/mo and $4,500/mo firm suites ([deviationcheck.com](https://deviationcheck.com/)), which shows GC/sub willingness to pay. I found no labour-cost figure.

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| Deviation Check | **$35/review**; $1,500/project/mo; $4,500/mo ([deviationcheck.com](https://deviationcheck.com/)) | Yes: no login, no demo, "drop two files" | **Yes**: substitutions, performance gaps, missing certifications, package incompleteness; severity-rated with verbatim spec quotes; for subs *before* submission and for GCs |
| InspectMind | From $50/check, $100 first-check credit ([inspectmind.ai](https://www.inspectmind.ai/checkers/submittal)) | Yes | Yes; claims 2,000+ accounts |
| BuildSync | Not verified ([buildsync.ai](https://buildsync.ai/)) | ? | Yes |
| iFieldSmart Submittal AI | Not verified ([ifieldsmart.com](https://www.ifieldsmart.com/solutions/submittal-ai)) | ? | Log and compliance review |
| Autodesk AutoSpecs | Bundled in ACC, quote ([Autodesk](https://construction.autodesk.com/tools/autospecs-construction-submittal-log/)) | No | Generates the submittal log from specs; suggests missing submittals |
| Submittal.app | Free start ([submittal.app](https://www.submittal.app/guides/o-and-m-manuals-and-closeout)) | Yes | AI package builder from a spec section |

**K1–K11:** K1 **HIT** ($35/review self-serve). K3 **HIT** (anything new is "more AI"). K8/K9 **HIT** (AutoSpecs/ACC, Procore). K5 partial (bursty, not weekly). An AI-heavy spec-interpretation job also conflicts with "AI dependence optional/bounded". **Verdict: KILL.**

### C4: Closeout package completeness before final payment / retainage release

**Pain evidence:** subs demobilize, so O&M manuals, warranties and final waivers are hard to collect, and incomplete packages delay retainage and final payment ([BuildSync closeout guide](https://buildsync.ai/resources/construction-closeout-submittlas-checklist), [Document Crunch](https://www.documentcrunch.com/blog/construction-project-closeout)). Retainage release often takes 30–90 days, and 30–60-day slips are common. Roughly 1 in 3 subs have used personal or retirement savings to cover slow pay (Billd 2025, via search summary; [Siteline retainage guide](https://www.siteline.com/blog/guide-to-construction-retainage), [TCG](https://terrapincg.com/news/retainage-release-mechanics-2026)).

**Economic transaction: found (large per event).** Retainage is typically 5–10% of contract (UNVERIFIED rate for this doc). Closeout Pro claims closeout takes 80–200 admin hours ([closeout-pro.com](https://www.closeout-pro.com/)).

**Competitors:** Closeout Pro (AI "Genie" extracts closeout requirements and "detect[s] missing deliverables"; price not public; [closeout-pro.com](https://www.closeout-pro.com/)). Submittal.app (compiles O&M, warranties and as-builts by spec section; free start; [submittal.app](https://www.submittal.app/guides/o-and-m-manuals-and-closeout)). Autodesk Build Closeout ([Autodesk](https://construction.autodesk.com/tools/closeout/)). Pype Closeout. Cushing Closeout Docs ([cushingco.com](https://cushingco.com/closeout-tools)). Linarc ([linarc.com](https://www.linarc.com/buildspace/construction-closeout-digital-punch-list-software)).

**K1–K11:** K5 **HIT**. A sub runs perhaps a handful to dozens of closeouts a year, so a €50–200/mo subscription doesn't match the usage pattern. K8/K9 **HIT** (a module of ACC and Procore, and GCs drive closeout). K1 likely (Submittal.app free start; paid price UNVERIFIED). K7 partial (spec-driven requirements differ per project). **Verdict: KILL.**

### C5: Change-order / T&M ticket backup packet

**Pain evidence:** out-of-contract work is lost when tickets go unsigned or lack backup ([Clearstory tips](https://www.clearstory.build/construction-blog/sc-7-tips-0), [Zurel](https://zurelsoft.com/blog/what-is-a-tm-ticket-and-why-does-it-matter/)). The work recurs weekly on active jobs.

**Economic transaction:** partial. FOUNDATION T&M features from $400/mo (snippet via [Rhumbix](https://www.rhumbix.com/blog/tm-billing-software-construction)). Clearstory charges per user plus a platform fee per project ([clearstory.build/pricing](https://www.clearstory.build/pricing); amounts not public).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| BenchMarx | Free (4 users, 2 projects); Pro $29/user/mo (snippet, [softwarefinder](https://softwarefinder.com/construction/benchmarx)) | Yes | **Yes**: merges signed T&M tickets into a CO with preset rates |
| Clearstory | Basic **free**; Standard/Pro quoted ([capterra](https://www.capterra.com/p/179134/Clearstory/)) | Partly | **Yes**: builds the COR package with all T&M tickets, backup and photos ([clearstory.build](https://www.clearstory.build/subcontractor-software)) |
| Zurel | Not verified | ? | Flags rate/markup deviations, attaches backup ([zurelsoft.com](https://zurelsoft.com/products/tm-tickets/)) |
| Rhumbix, Procore CO tools | Not verified | – | Yes / partially |

**K1–K11:** K1 **HIT** (free tiers). K9 **HIT**. K3 **HIT**. The real problem is capturing signatures in the field, which is a mobile field-app job, not a document pre-flight. **Verdict: KILL.**

### C6 (added): Public-works bid packet responsiveness check

**Pain evidence:** a missing addendum acknowledgment or a missing or defective bid bond makes a bid nonresponsive, and even a low bid is rejected ([GAO B-190286](https://www.gao.gov/products/b-190286), [GAO B-188100](https://www.gao.gov/products/b-188100), [EJCDC](https://ejcdc.org/bid-responsiveness-correction-of-bid-deficiency-by-hugh-anderson/), [VT Construction Contracting](https://pressbooks.lib.vt.edu/constructioncontracting/chapter/bid-and-proposals/)). The loss per event is high (the whole job), but I found no data on how often it happens per bidder.

**Economic transaction:** not quantified. Bidding labour is real, but I have no verified figure. **UNVERIFIED.**

**Competitors:** PlanetBids "will validate that addenda have been acknowledged" and requires this before e-bid submission (search result citing [PlanetBids vendor support](https://home.planetbids.com/vendor-support) and the [Inglewood instructions](https://www.cityofinglewood.org/DocumentCenter/View/20163/PlanetBids-eBidding-Instructions-rev-12624)). QuestCDN online bidding ([questcdn.com](https://www.questcdn.com/online-bidding/)). RFPCheck cross-checks bids against RFPs for missing mandatory requirements; price not shown ([rfpai.io](https://www.rfpai.io/?lang=en)). ContraVault builds compliance matrices ([contravault.com](https://www.contravault.com/)).

**K1–K11:** K8 **HIT** (e-bid platforms enforce the most catastrophic checks). K1/K3 likely (RFPCheck, ContraVault). K5 **HIT** (a catastrophic but rare event, hard to charge monthly for). K7 partial (every agency's forms differ). **Verdict: KILL (medium confidence;** the paper-bid market share was not verified).

### C7 (idea, not assessed): Residential builder → lender draw packet
The search budget ran out, so no evidence was collected. From prior knowledge (UNVERIFIED), lender-side draw platforms (Built, Land Gorilla) set the requirements, which would suggest K2/K8. If the funnel needs more construction candidates, revisit this in a later round.

## 3. Survivors / uncertain: what Stage D must verify

**None survive.** No candidate is rated UNCERTAIN, because each of C1–C5 has a verified cheap self-serve or free competitor for the exact job, or a mandated platform that absorbs it.

The uncomfortable question, answered for the strongest-pain candidate (C1, pay apps):
> *Who already pays for this exact job today?* Subcontractors' billing specialists (~$47k/yr), sub-paid portal fees (Textura 0.22% of contract), and pay-app software (PayAppPro $79–249/mo, PAYearned $67–89/mo, Siteline at a custom price).
> *Why wouldn't they simply use the existing product?* They would. PayAppPro already sells the exact pre-submission quality check for $7.99 per pay app, and GC portals validate at entry. A standalone checker would be a feature competing against a $7.99 price anchor. **Same failure mode as the previous dead idea.**

### Pattern observed (useful for other R2 tracks)
Construction document pre-flight has been heavily funded and built out in 2024–2026. Each sub-workflow (pay apps, payroll, submittals, closeout, T&M) now has either a GC- or agency-mandated portal that validates at entry, or an AI self-serve checker priced per document ($7.99–$50). In construction, the "readiness gate" wedge is already commoditized. For the pre-flight direction, look instead at verticals where no mandated portal exists and the counterparty rejects by email or paper.

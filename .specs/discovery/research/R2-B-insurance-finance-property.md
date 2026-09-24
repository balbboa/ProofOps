# R2 Stage B/C — Insurance, Finance, Property: "pre-flight / readiness gate" candidates

> Date: 2026-09-23. Criteria: `.specs/discovery/R2-CRITERIA.md` (K1–K11, mandatory economic transaction, must-prove table).
> Method: web research (search + fetch of vendor pages). Posture: adversarial; a candidate survives only if no cheap self-serve tool does the exact job and the incumbent cannot easily absorb it.
> Research limits: the session's WebSearch budget ran out partway through. Candidates 6–7 (auto dealer CIT, property-management move-out) rely on fewer sources and are marked as such. Anything not backed by a fetched source is marked **UNVERIFIED**.

## 1. Summary

| # | Candidate | Verdict | Decisive reason | Economic transaction found? | Cheapest exact competitor + price |
|---|---|---|---|---|---|
| 1 | Insurance agency commercial submission packet (ACORD 125/126/140 + loss runs) | **KILL** | K1: a self-serve tool already does "gap alerts before you submit" for $49/mo, and Indio/Talage are free. K8/K9: AMS vendors (Applied owns Indio and Tarmika) absorb it. | Y, but indirect (CSR time, 10–50% quote-decline rates). No direct per-file spend found. | AgencyAssist: free for 1 submission, **$49/mo Solo** ([agencyassist.io](https://www.agencyassist.io/)) |
| 2 | Roofing/restoration insurance supplement packet | **KILL** | K1: self-serve AI scope scanners already exist: AiScopeSCANNER at **$79.95/scan**, RoofGenius at $149–497/mo. The real value is in negotiating with the carrier, not in a pre-flight check. | **Y, strong**: supplement services charge 8–15% of the increase, or 10% with no minimum | AiScopeSCANNER **$79.95 per scan** ([p1mitigators.com](https://p1mitigators.com/ai-scope-scanner)) |
| 3 | Real estate brokerage transaction-file compliance review | **KILL** | K1: ListedKit $14.99/intake, Upfront Docs $4–20/transaction, DocJacket $29/mo. K2/K8: SkySlope, Paperless Pipeline and Dotloop already have checklists and audits. | **Y, strong**: TCs charge $300–500/file; an in-house reviewer costs $50–65k/yr | Upfront Docs **$4–20/transaction** (not fully self-serve yet); ListedKit **$14.99/intake** (self-serve) |
| 4 | SBA 7(a) / commercial loan broker packet completeness | **KILL** | K1: Levr gives brokers a **free** plan. K5: low deal count per broker. K11: tax returns and SSNs (GLBA-type data). K9: Kaaj, Aloan, Biz2X, Centrex, nCino. | Y: packaging fees of $2,000–4,000 per loan | Levr **$0** core broker plan ([levr.ai](https://levr.ai/)) |
| 5 | Mortgage broker pre-underwriting completeness (conditions) | **KILL** | K2/K8/K9: the LOS and point-of-sale stack own conditions (Floify, Maxwell, Blend, Ocrolus, Addy). K11: GLBA and NPI data. K7: needs LOS integration to be useful. | Y: processors and per-file processing (amounts **UNVERIFIED**) | Floify **$79–149/user/mo** (third-party figure) |
| 6 | *(added)* Property-management move-in/move-out packet (deposit deduction readiness) | **KILL** | K1: RentCheck $1/unit/mo, self-serve, 14-day trial, with AI Damage Assist. K8: AppFolio and similar platforms integrate it. | Y: security-deposit disputes (amount **UNVERIFIED**) | RentCheck **$1/unit/mo** ([getrentcheck.com/pricing](https://www.getrentcheck.com/pricing)) |
| 7 | *(added)* Auto dealer "contracts in transit" funding packet | **KILL (provisional, under-researched)** | K2/K8/K9: funding goes through Dealertrack/RouteOne e-contracting, which run lender validation (**UNVERIFIED**, search budget exhausted). K6: dealer groups buy through sales and DMS relationships. K11: consumer credit PII (GLBA/FTC Safeguards Rule). | Plausible (floor-plan interest, rejected contracts). **UNVERIFIED** | Not established |

**Net: 0 SURVIVE, 0 UNCERTAIN, 7 KILL.** This fits the funnel's expectation. The pattern repeats in every case. Wherever there is a real, paid-for job (supplements, TC file review, SBA packaging), an AI "readiness check" for that exact document set already exists in 2025–2026. It is usually self-serve and often priced below or inside the €30–200/mo band.

---
## 2. Per-candidate analysis

### C1. Independent agency commercial-lines submission packet (ACORD 125/126/140 + loss runs + supplementals)

**Pain evidence**
- 64% of agents in the First Connect 2025 survey reported quote-decline rates of 10–50%, and 71% struggle to understand carrier appetite. That is an appetite problem more than a completeness problem. Source: search-result summary of [Carrier Management, 2025-10-09](https://www.carriermanagement.com/news/2025/10/09/280302.htm). Exact figures not re-verified on the page, so **partially UNVERIFIED**.
- In the 2025 Ivans connectivity survey, 72% of agencies named the commercial submission process as the top area where they want more automation ([Ivans press release](https://www.ivans.com/news/press-releases/2025/majority-of-agent-respondents-say-real-time-risk-appetite-information-is-the-1-factor-in-carrier-selection-in-2025-insurance-agency-carrier-connectivity-trends-survey-report/)).
- Note that the #1 carrier-selection factor is real-time **appetite**, not packet completeness (same Ivans source). The main cause of declines is sending to the wrong market, which a completeness gate does not fix.

**Economic transaction**
- The job is done by CSR and account-manager time. No market for an outsourced "submission QA" service with public per-file prices was found (**UNVERIFIED** that none exists).
- Agencies already pay for AI intake: Cara at $299–899/mo and Stella at $199–699/mo ([asceroai buyer's guide](https://asceroai.com/guides/best-ai-tools-insurance-agents-2026); third-party figures).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| AgencyAssist | Free (1 submission); $49 Solo / $99 Small / $199 Agency per month ([agencyassist.io](https://www.agencyassist.io/)) | Yes: 30-day trial, no card | **Yes**: "Underwriting gap alerts before you submit", generates ACORD PDFs |
| Indio (Applied) | Free for agencies ([asceroai](https://asceroai.com/guides/best-ai-tools-insurance-agents-2026)) | Yes | Partly: structured intake and ACORD population |
| Talage | Free for agencies (same source) | Yes | Partly: small-commercial intake |
| Semsee Essential | Free: appetite checking plus multi-carrier submission ([QuoteSweep review](https://www.quotesweep.com/blog/semsee-review-2026)) | Yes | Adjacent: appetite and submission |
| InsurGrid | Demo / contact sales ([insurgrid.com](https://insurgrid.com/features/acord-form-generator)) | No | **Yes**: "Flag missing or conflicting values before submission"; integrates HawkSoft, EZLynx, AgencyZoom |
| Cara / Stella | $199–899/mo (third-party figures) | Yes per guide | Yes: AI ACORD-aware intake |
| Nomad Data Doc Chat, FurtherAI, Pibit | Enterprise | No | Yes, but carrier and wholesaler side ([Nomad](https://www.nomad-data.com/doc-chat/eliminating-bottlenecks-in-acord-form-intake-how-ai-transforms-new-business-submission-workflows-for-brokers-agency-principal-property-homeowners-auto-commercial-auto), [FurtherAI](https://www.furtherai.com/blog/submission-automation-seamless-integration)) |

**K1–K11**
- K1 **HIT**: AgencyAssist does exactly this at $49/mo, self-serve.
- K2 **HIT**: free Indio or Semsee is the natural move.
- K3 **HIT**: the only possible differentiator is "better AI detection".
- K4: clear (agency principal).
- K5: frequent at commercial agencies.
- K6: agencies can be reached through communities, but AMS vendors dominate.
- K7: agencies expect AMS integration (InsurGrid lists four).
- K8 **HIT**: Applied owns Indio and Tarmika ([QuoteSweep](https://www.quotesweep.com/blog/semsee-vs-tarmika-vs-quotesweep)).
- K9 **HIT**.
- K10: possible on price, but a crowded field.
- K11: commercial data is moderate risk; loss runs are fine.

**Economics:** saving CSR hours could plausibly be worth €300+/mo. But the price ceiling is already set at $0–49 by existing products.
**Verdict: KILL** (K1, K2, K8, K9).

---

### C2. Roofing/restoration insurance claim supplement packet

**Pain evidence**
- The industry claims supplements recover about $7,000–8,000 per claim on average (search summary of [IA Solutions 2026 guide](https://www.iasolutions.claims/blog/roofing-insurance-supplements-2026-guide-independent-adjusters); vendor claim, not independent).
- Xactimate supplements are said to recover the "20 to 40%" contractors leave on the table ([IA Solutions Xactimate guide](https://www.iasolutions.claims/blog/xactimate-supplement-guide-roofing-contractors); vendor claim).
- US roof claim costs exceeded $30B in 2024 ([Verisk PDF](https://s29.q4cdn.com/767340216/files/doc_news/U-S--Roof-Claims-Costs-Reached-Over-30-Billion-In-2024-Underscoring-Evolving-Risks-2025.pdf)).

**Economic transaction: strongest in this batch**
- Estimate on Demand charges 10% of the increase with no minimum, or $2,999/mo plus 8%. Non-supplement estimates cost $79–99 ([estimateondemand.com](https://estimateondemand.com/estimate-supplement-pricing/)).
- Market range: 8–15% of the recovered amount, flat $150–500 per submission, or retainers of $500–2,500/mo (search summary of [ProLine](https://useproline.com/average-cost-of-roofing-supplement-services/); page returned 403, so **partially UNVERIFIED**).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| AiScopeSCANNER (P1Mitigators) | **$79.95/scan**, free with a work authorization ([p1mitigators.com](https://p1mitigators.com/ai-scope-scanner)) | Yes: email, upload, pay | **Yes**: missing line items, under-scoped quantities, $0 entries, recoverable depreciation |
| RoofGenius | $149/mo retail; supplement plans from $497/mo ([roofgenius.ai](https://roofgenius.ai/answers)) | Yes | **Yes**: scans the carrier estimate, cites IRC code (e.g. R908.3), writes the supplement letter |
| CapOut | Flat per-claim pay-as-you-go; first claim free ([capout.ai](https://capout.ai/resources/compare/best-roofing-estimating-software)) | Yes | Partly: PDF to ESX, plus an AI claim assistant for denied items |
| XBuild | Not captured | **UNVERIFIED** | Partly: insurance-style scopes and supplements ([x.build](https://x.build/roofing-estimating-software)) |
| RestorationAI / EstimatePortal | Services plus self-serve calculators ([estimateportal.com](https://estimateportal.com/)) | Partly | Partly |
| Supplement services (EOD, RISE, Supplement Experts, American Roof Supplements) | 8–15% | Done-for-you | Yes, including negotiation |

**K1–K11**
- K1 **HIT**: $79.95 per scan, self-serve, is the exact job.
- K2: contractors buy outcomes (recovered dollars) from percentage-fee services. A checker does not replace negotiation with the adjuster, which is where the fee is earned.
- K3 **HIT**: we would be one more AI scope scanner.
- K4: clear (contractor owner).
- K5: frequency is seasonal, following storms.
- K6: fine (Facebook groups, YouTube).
- K7: needs Xactimate/ESX knowledge; Xactimate itself costs about $200–350/mo ([CapOut guide](https://capout.ai/resources/compare/best-roofing-estimating-software)).
- K8: Xactimate, Verisk and roofing CRMs could absorb it.
- K9: RoofGenius already bundles it.
- K10: OK on price.
- K11: homeowner PII only, low.

**Economics:** the value per claim is large (thousands of dollars), so willingness to pay exists. But the work that gets paid is advocacy and negotiation (8–15%), which a solo "no support" product cannot deliver. The pure pre-flight part has already been commoditized to about $80 per scan.
**Verdict: KILL** (K1, K3).

---

### C3. Real estate brokerage transaction-file compliance review before commission disbursement

**Pain evidence**
- Brokers of record carry legal liability and face state-mandated file review cadences ([Empower: broker-of-record liability](https://www.empowertransactions.com/broker-of-record-compliance-responsibility/), [review by state](https://www.empowertransactions.com/broker-file-review-by-state/)).
- The work is per transaction and recurring (daily at mid-size brokerages).

**Economic transaction: strong**
- Outsourced TCs cost $300–500 per file, averaging about $350–450 ([ProfileTM 2026](https://profiletm.com/2026/03/21/transaction-coordinator-cost-2026/), [Quill](https://www.quilltc.com/blog/how-much-does-a-transaction-coordinator-cost); via search summary).
- An in-house compliance reviewer costs about $50–65k fully loaded, and outsourced review is billed per file ([Empower](https://www.empowertransactions.com/real-estate-compliance-outsourcing/)).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| ListedKit AI | **$14.99/intake**, no monthly fee ([listedkit.com](https://www.listedkit.com/best-tc-software)) | Yes | **Yes**: scans for missing signatures, blank fields, mismatched dates |
| Upfront Docs | **$4–20/transaction** ([myupfront.com](https://www.myupfront.com/ai-compliance)) | Not yet (gated rollout) | **Yes**: signatures, initials, dates, required forms, math consistency |
| ReBillion | $199/mo AI toolkit; $499/mo with an assistant ([rebillion.ai](https://rebillion.ai/ai-real-estate-compliance)) | Yes (partly) | **Yes**: signatures and dates, state disclosures, 10 states |
| DocJacket | $29/mo (listedkit comparison) | Yes | Doc management and checklists |
| Dotloop | $34.99/mo | Yes | Checklists and review queue |
| Paperless Pipeline | $69+/mo | Yes | Required-document gates, two-stage review |
| SkySlope | $340+/mo | Demo | Quick Audit, checklists |
| Joymore | Value-based ([joymore.com](https://www.joymore.com/compare/best-real-estate-compliance-software)) | **UNVERIFIED** | Yes |
| Empower Transactions, Closenex | Per-file (price not public) | Done-for-you | Yes |

**K1–K11**
- K1 **HIT** (ListedKit, Upfront).
- K2 **HIT**: brokerages already pay for SkySlope, Dotloop or Paperless Pipeline and will use their review queues or add-ons.
- K3 **HIT**.
- K4: clear (broker of record).
- K5: frequent.
- K6: OK.
- K7: the transaction-management platform holds the files, so an integration is needed from day one.
- K8 **HIT**: SkySlope and Lone Wolf can absorb it trivially.
- K9 **HIT**.
- K10: at $4–20 per transaction, ARPU collapses.
- K11: low.

**Verdict: KILL** (K1, K2, K8, K9). This is the most crowded candidate in the batch.

---

### C4. SBA 7(a) / commercial loan broker packet completeness

**Pain evidence:** lenders will not start underwriting without complete financials, SBA forms and legal docs, and most delays come from missing or inconsistent items ([Biz2X](https://www.biz2x.com/sba-loan-software/automated-document-processing-sba-loans/), vendor claim).

**Economic transaction:** packaging fees run $2,000–4,000. Outside packagers above $2,500 must itemize hours on SBA Form 159 ([Starfield & Smith](https://starfieldsmith.com/2025/12/understanding-sba-7a-loan-fees-and-costs/), [ClearlyAcquired](https://www.clearlyacquired.com/blog/sba-loan-fees-breakdown-of-costs); via search summary). The money is real but concentrated in a few deals per broker per month (**UNVERIFIED** deal counts).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| Levr | **$0** core broker plan, no commission split ([levr.ai](https://levr.ai/)) | Yes | Mostly: intake, lender-criteria matching, doc requests and follow-ups |
| Kaaj | Custom, volume-based ([kaaj.ai/pricing](https://kaaj.ai/pricing)) | No (demo) | **Yes**: "Flags missing documents and lender-specific gaps" ([kaaj.ai](https://kaaj.ai/solutions/brokers)) |
| Centrex | **UNVERIFIED** | **UNVERIFIED** | Broker CRM with SBA doc tracking and multi-lender submission ([centrexsoftware.com](https://centrexsoftware.com/sba-loan-crm/)) |
| Biz2X, nCino, LendingWise, Aloan | Enterprise or lender side | No | Yes, but for lenders ([aloan.ai](https://aloan.ai/solutions/ai-document-collection-commercial-lending)) |
| Crediflow | **UNVERIFIED** | **UNVERIFIED** | Lender-ready file ([crediflow.ai](https://www.crediflow.ai/blog/ai-for-commercial-loan-brokers)) |

**K1–K11**
- K1 **HIT**: Levr is free.
- K2 **HIT**.
- K3 **HIT**.
- K5 **HIT**: low frequency per broker.
- K7: every lender has its own checklist.
- K9: Kaaj and Centrex.
- K10 **HIT**: few brokers at about €100.
- K11 **HIT**: tax returns, SSNs and bank statements bring GLBA Safeguards-type obligations for a solo developer (**UNVERIFIED** as a legal assessment).

**Verdict: KILL.** Equipment-finance brokers were considered and fall to the same competitors (Kaaj explicitly builds "lender-ready equipment deal packages").

---

### C5. Mortgage broker pre-underwriting file completeness (conditions)

**Economic transaction:** loan processors or contract processors per file (amounts **UNVERIFIED**; not researched further because of the kills below). Purelend claims to save "3+ hrs per file" ([purelend.ai](https://www.purelend.ai/)).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| Floify | $79–149/user/mo ([US Tech Automations](https://ustechautomations.com/resources/blog/automate-best-loan-document-software-for-mortgage-brokers-2026), third-party) | Yes (**UNVERIFIED**) | Checklists and real-time doc status |
| Maxwell | $99–199/user/mo (same source) | **UNVERIFIED** | Condition-clearing workflow |
| Addy | Not disclosed ([addy.com](https://addy.com/blog/best-mortgage-ai-tools)) | ChatGPT app | "Processing Checklist… runs product-specific conditions in under five minutes" |
| Purelend | 2-week free trial ([purelend.ai](https://www.purelend.ai/)) | Yes | Yes (Canada-focused) |
| Blend, Ocrolus, Oper | Enterprise | No | Yes |
| LOS (Encompass, Arive, LendingPad, Blue Sage) | Blue Sage $250–500/user/mo (third-party) | Mixed | Conditions are a core LOS object |

**K1–K11**
- K1 **HIT** (Floify, Addy).
- K2 **HIT**: the LOS owns conditions.
- K7 **HIT**: useless without LOS and AUS findings.
- K8 and K9 **HIT**.
- K11 **HIT**: borrower NPI under GLBA, and state licensing and vendor due-diligence reviews.

**Verdict: KILL.**

---

### C6. (Added) Property-management move-in/move-out packet (deposit deduction readiness)

**Economic transaction:** deposit disputes and damage recovery (amounts **UNVERIFIED**; search budget exhausted).

**Competitors:** RentCheck charges $1–1.75 per unit per month, is self-serve with a 14-day no-card trial, and offers AI Damage Assist and AppFolio Realm-X integration ([getrentcheck.com/pricing](https://www.getrentcheck.com/pricing)). zInspector, HappyCo and the inspection modules built into property-management systems also compete (**UNVERIFIED**, not fetched).

**K1–K11**
- K1 **HIT**.
- K2 and K8 **HIT**: AppFolio and Buildium ecosystems.
- K3 **HIT**.
- K5: turnover events are periodic, not daily, for small property managers.

**Verdict: KILL.**

---

### C7. (Added) Auto dealer "contracts in transit" (CIT) funding packet

**Status:** under-researched. The search budget ran out, and Dealertrack and RouteOne pages returned 404 and 403.

**Reasoning (all UNVERIFIED)**
- Funding flows run through Dealertrack and RouteOne e-contracting and DMS vendors (CDK, Reynolds). They are the natural place for pre-funding validation, which triggers K2, K8 and K9.
- Lender-side stip verification (e.g. Informed.IQ) is sold to lenders.
- Dealers buy through DMS and sales relationships (K6).
- Consumer credit applications fall under the FTC Safeguards Rule (K11).

**Verdict: KILL (provisional).** If the coordinator wants certainty, one Stage B pass could confirm the Dealertrack and RouteOne validation features. Prior probability of survival is low.

---

## 3. Survivors and uncertain candidates: Stage D requirements

**None survive.** For the record, here is the answer to the key question for the two candidates with the strongest economic transaction. It shows why they still die.

**C2 Roofing supplements**
- *Who pays today?* Storm-restoration contractors.
- *What do they pay?* 8–15% of the supplement increase, or 10% with no minimum at Estimate on Demand, on claims said to recover about $7–8k.
- *Why not the existing product?* They already can: AiScopeSCANNER at $79.95/scan and RoofGenius at $149–497/mo do the pre-flight scan. The percentage fee pays for negotiation and follow-through, which a no-support solo product cannot offer.

**C3 Real estate file compliance**
- *Who pays today?* Brokers of record.
- *What do they pay?* $300–500 per file for TCs, or a $50–65k reviewer.
- *Why not the existing product?* They already can: ListedKit at $14.99/intake, Upfront Docs at $4–20/transaction, ReBillion at $199/mo, plus the review queues already built into SkySlope, Dotloop and Paperless Pipeline.

### Lessons for the funnel
1. In insurance, finance and property, 2025–2026 has produced an "AI completeness checker" for almost every named document packet. Many are self-serve with public prices at or below €50/mo, or per-file prices of $5–80. For these industries, the pre-flight gate idea is already a commodity category.
2. Where the money is large (supplement %, SBA packaging, TC fees), buyers pay for **outcome and labour** (negotiation, chasing borrowers, coordinating parties), not for detection. A detection-only tool captures only a small slice of that spend.
3. Every candidate sits on top of a system of record (AMS, Xactimate, transaction-management platform, LOS, property-management system, DMS) that owns the files and can absorb the check (K8).
4. If the funnel continues, look for packets that meet all three conditions: (a) no dominant system of record, (b) a counterparty that rejects on objective, published rules, and (c) no vendor already naming the exact packet. None of the seven here meet all three.

### Unverified items worth a quick check only if a candidate is reopened
- The exact First Connect decline-rate figures ([Carrier Management](https://www.carriermanagement.com/news/2025/10/09/280302.htm)).
- ProLine's supplement fee ranges (the page returned 403).
- Floify and Maxwell pricing (third-party figures only).
- Whether Dealertrack and RouteOne e-contracting run pre-funding validation (C7).
- Whether Upfront Docs opens self-serve signup (it would sharpen K1 for C3 further).

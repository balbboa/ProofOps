# R3 — Outsourcing Service Menus + Job Postings (US/UK/EU)

> Date: 2026-09-23. Method: `../R3-CRITERIA.md` (K12–K15) + `../R2-CRITERIA.md` (K1–K11).
> Segment: published outsourcing/BPO price lists and job postings for repetitive back-office roles.

## 0. Research-quota and coverage note (read first)

- **The WebSearch quota was used up before this segment began** (200/200 for the session). Every WebSearch call returned "search not performed". **No adversarial keyword searches ("<deliverable> software / automation / AI") could be run.** Competition checks below come from **direct WebFetch of known vendor pricing pages** and from URLs already cited in R1/R2.
- **The job-posting half of the segment failed.** Indeed, ZipRecruiter, Upwork and BLS all returned HTTP 403, and Salary.com returned 404. **This file contains no salary-range evidence.** Wherever a candidate refers to a "role", treat it as UNVERIFIED.
- Offshore BPO price lists: the one large BPO checked (Flatworld) publishes **no** per-unit prices, only quote-on-request (https://www.flatworldsolutions.com/pricing.php). One insurance-VA firm, Agency VA, publishes monthly team prices (https://www.agencyva.com/pricing). Several niche-firm pages could not be fetched (403/404/TLS errors).
- The result: **19 candidates harvested and assessed, all at lower evidence depth than planned.** The conclusion (0 survivors) is **directionally strong but not exhaustive.**

## 1. Summary table

| # | Candidate | Paid evidence (price × frequency) | Verdict | Decisive reason | Cheapest existing tool |
|---|---|---|---|---|---|
| 1 | US sales-tax return filing (monthly) | Accountant $70–300+/mo, as claimed by a vendor (DAVO); Numeral $75/filing; TaxJar extra filings $50–55 each | KILL | K1: filing is already sold as self-serve done-for-you software | DAVO $57.99/mo per location (https://www.davosalestax.com/pricing/) |
| 2 | Shopping/marketplace product-feed management | Agency labour UNVERIFIED | KILL | K1 | DataFeedWatch $64/mo (https://www.datafeedwatch.com/pricing) |
| 3 | Product listing / description creation (Shopify, Amazon) | Per-listing freelancer fees UNVERIFIED | KILL | K1/K8/K3: platforms include it for free | Shopify Sidekick, included in the plan; Amazon's own gen-AI listing tool |
| 4 | Construction preliminary notices (subcontractors) | Levelset $59 per recipient | KILL | K1, plus per-project frequency (partly K15) | Levelset $59/notice (https://www.levelset.com/pricing/) |
| 5 | Construction lien waivers | Labour UNVERIFIED | KILL | K1: free | Levelset free waivers; Procore Pay generates them |
| 6 | UK CIS monthly return + subcontractor statements | £100 penalty per late month (gov.uk); bookkeeper fees UNVERIFIED | KILL | K1/K9: £5/mo add-on in Xero | Xero £5/mo CIS submission add-on |
| 7 | UK micro-employer payroll / RTI | Bureau fees UNVERIFIED | KILL | K1: HMRC tool is free | HMRC Basic PAYE Tools, free for under 10 employees |
| 8 | Certificate of insurance (COI / ACORD 25) issuance for agencies | Agency VA "trained service teams" from $3,449/mo, covering certificates, renewals and quoting | KILL | K1/K9: free for agents; AMS-integrated | Certificial, free for agents and insureds |
| 9 | ACORD application prep for renewals and remarketing | Bundled in the same VA teams ($3,449/mo) | KILL | K9/K12, plus existing tools (InsurGrid; AgencyAssist $49/mo per R2) | AgencyAssist $49/mo (R2) |
| 10 | Real-estate transaction coordination | $300–700 per file; $500–2,500/mo | KILL | K12 (coordination and relationships) + K1 | ListedKit $14.99 per transaction stage |
| 11 | Process-server affidavits of service | Paid value is the physical serve | KILL | K12 + K9: affidavits come built into software | ServeManager $51.74/mo (75 jobs) |
| 12 | Trucking IFTA fuel-tax reports | Filing-service fees UNVERIFIED | KILL | K15: quarterly (UNVERIFIED citation) + K1 | TruckingOffice $20/mo |
| 13 | Truck dispatch services | % of gross, figure UNVERIFIED (source page redirect-looped) | KILL | K12: the value is load negotiation, not a document | n/a |
| 14 | Trucking invoicing / factoring packets | Labour UNVERIFIED | KILL | K1/K9: in cheap TMS | TruckingOffice $20/mo |
| 15 | Property-management owner statements | Labour UNVERIFIED | KILL | K9/K2: core function of PM software | Buildium from $62/mo |
| 16 | Accounting-firm monthly management report packs | Firm fees UNVERIFIED | KILL | K1 | Fathom Portfolio A$62/mo for 100 companies |
| 17 | Marketing-agency monthly client reports | Agency labour UNVERIFIED | KILL | K1 | AgencyAnalytics $20 per client per month |
| 18 | Amazon FBA reimbursement claims | 25% contingency | KILL | K1 + it is recovery/checking work (the R2 pattern) | GETIDA, 25% with no subscription |
| 19 | Freight carrier onboarding packets | n/a | KILL | It is a checker/gate (killed in R2) + K1 | MyCarrierPortal/MyCarrierPackets (R2) |

**Result: 0 SURVIVE, 0 UNCERTAIN, 19 KILL.**

## 2. Per-candidate sections

### 1. US sales-tax return filing
- **Paid labour:** DAVO says an accountant costs "$70–$300+/month" for this work. This is a vendor claim and self-serving, so treat it as UNVERIFIED as a market price (https://www.davosalestax.com/pricing/). Numeral charges $75 per filing plus $150 per state registration (https://www.numeral.com/pricing). TaxJar charges $39–99/mo, and AutoFile filings beyond the included credits cost $50–55 each (https://www.taxjar.com/pricing). Frequency is monthly for many retailers. Buyers are SMB retailers and e-commerce sellers.
- **Deliverable:** a state return plus remittance. Highly standardisable and fully generated by software today.
- **Competition:** DAVO $57.99/mo per location, with filing and payment guaranteed, integrated with 30+ POS systems (https://www.davosalestax.com/pricing/). Numeral and TaxJar as above.
- **Kills:** K1 (done-for-you self-serve at €50–60/mo already exists), K8 (POS and e-commerce platforms partner with these vendors), K12 (penalty guarantees and liability are part of what the buyer pays for), K11 (holding or remitting tax money is out of a solo developer's reach).
- **Economics:** the spend exists, but incumbents already sit at the target price. **KILL.**

### 2. Product-feed management (Google Shopping, marketplaces)
- **Paid labour:** agencies and VAs, UNVERIFIED (no price list could be fetched).
- **Deliverable:** a transformed product feed. Fully generatable.
- **Competition:** DataFeedWatch $64/mo (1,000 SKUs, 3 feeds) to $239/mo (agency plan), with an AI optimiser included (https://www.datafeedwatch.com/pricing).
- **Kills:** K1 and K3. **KILL.**

### 3. Product listing / description creation
- **Paid labour:** per-listing freelancer fees UNVERIFIED (Fiverr/Upwork blocked).
- **Deliverable:** titles, bullets and descriptions. Generatable, and already commodity AI output.
- **Competition:** Shopify's Sidekick writes product descriptions and "is included with your Shopify plan" (https://www.shopify.com/magic). Amazon offers sellers a gen-AI tool that turns a brief description into listing content (https://www.aboutamazon.com/news/small-business/amazon-sellers-generative-ai-tool). Price not stated; free assumed, UNVERIFIED.
- **Kills:** K1, K3, K8 (the platforms absorbed it). Also mostly one-off per SKU (K15). **KILL.**

### 4. Construction preliminary notices
- **Paid labour:** notice services at $59 per recipient (https://www.levelset.com/pricing/). Notices are sent per project start, so frequency depends on how many projects a subcontractor starts. That is monthly for active subs, but not a fixed monthly job (partial K15).
- **Deliverable:** a statutory notice, generated and mailed.
- **Competition:** Levelset (Procore), with a price-per-notice model already self-serve.
- **Kills:** K1, K9. **KILL.**

### 5. Construction lien waivers
- **Paid labour:** UNVERIFIED.
- **Competition:** Levelset lets users "electronically send a lien waiver right now – for free" (https://www.levelset.com/lien-waivers/). Procore Pay generates waivers on project invoices (https://support.procore.com/products/online/procore-pay/tutorials/generate-lien-waivers-on-project-invoices).
- **Kills:** K1 (free). **KILL.**

### 6. UK CIS monthly returns + payment & deduction statements
- **Paid labour:** bookkeepers charge per-month CIS fees (UNVERIFIED, no price list fetched). The pain is real: returns are due by the 19th of every month, with a £100 penalty at 1 day late rising to £3,000 (https://www.gov.uk/what-you-must-do-as-a-cis-contractor/file-your-monthly-returns).
- **Deliverable:** the CIS300 return plus subcontractor statements. Fully generatable, and truly monthly (this was the strongest frequency in the segment).
- **Competition:** CIS is included on all Xero UK plans ("Automate subcontractor CIS calculations and reports"), and "Submit contractor CIS returns" is a **£5/month** add-on (https://www.xero.com/uk/pricing-plans/). Other accounting packages are assumed similar (UNVERIFIED).
- **Kills:** K1, K2 (the customer's ledger already does it), K9. **KILL.**

### 7. UK micro-employer payroll / RTI submissions
- **Competition:** HMRC Basic PAYE Tools is "free payroll software ... for businesses with fewer than 10 employees" (https://www.gov.uk/basic-paye-tools).
- **Kills:** K1, plus generic payroll (excluded by the brief). **KILL.**

### 8. Certificate of insurance (COI) issuance for agencies
- **Paid labour:** Agency VA sells "Trained Service Teams" from **$3,449/month** for "quoting, renewals, certificates, and phone support" (https://www.agencyva.com/pricing). COIs are therefore bundled into general service labour and not priced per certificate. Job postings for "certificate specialist" were UNVERIFIED (403).
- **Deliverable:** an ACORD 25 generated from policy data. Very standardisable.
- **Competition:** Certificial is "completely free for Insureds, Agents and Brokers". It lets agents issue smart COIs, enable self-service COIs for clients, and integrate with the AMS for automated issuance (https://www.certificial.com/pricing, https://www.certificial.com/). InsurGrid also lists a COI generator (https://insurgrid.com/features/acord-form-generator). Agency management systems (e.g. NowCerts) are assumed to issue COIs natively (UNVERIFIED: page content not retrievable).
- **Kills:** K1 (free), K9 (AMS feature), K13 (the policy data lives in the AMS). **KILL.**

### 9. ACORD application prep for renewals and remarketing
- **Paid labour:** bundled inside the $3,449/mo VA teams (https://www.agencyva.com/pricing).
- **Deliverable:** pre-filled ACORD 125/126/130 applications from dec pages and loss runs. Generatable.
- **Competition:** InsurGrid extracts policy data and generates "review-ready" ACORD forms (demo pricing only; https://insurgrid.com/features/acord-form-generator). R2 found AgencyAssist at $49/mo (`R2-SYNTHESIS.md`, `R2-B-insurance-finance-property.md`).
- **Kills:** K1 (a $49/mo tool exists), K9, K12 (the producer judges and markets the risk). **KILL.**

### 10. Real-estate transaction coordination
- **Paid labour:** "$300–$700 per transaction" per file, "$500–$2,500/month" as a subscription, and "$2,000–$5,000+/month" as a team retainer (https://profiletm.com/2026/03/21/transaction-coordinator-cost-2026/). This is the strongest paid-labour evidence found in the segment.
- **Deliverable:** mostly *coordination* (deadlines, chasing parties, communications), not a generatable artifact.
- **Competition:** ListedKit charges $14.99 per transaction stage and "reads emails, reads contracts, builds timelines ... drafts communications" (https://www.listedkit.com/pricing).
- **Kills:** K12 (the human value is chasing people and holding relationships), K1 (AI TC tool at $15/file). **KILL.**

### 11. Process-server affidavits of service
- **Paid labour:** the fee pays for the physical serve. The affidavit is a byproduct.
- **Competition:** ServeManager $51.74/mo for 75 jobs to $190.43/mo for 300, and it "Create[s] Affidavits & Proofs" (https://www.servemanager.com/pricing).
- **Kills:** K12, K9, K1. **KILL.**

### 12. Trucking IFTA reports
- **Paid labour:** IFTA filing services for owner-operators exist, but no price could be fetched (UNVERIFIED; the ExpressIFTA page had a TLS error).
- **Frequency:** quarterly per general knowledge. The FMCSA page returned 403, so this is UNVERIFIED. It fails K15 as stated.
- **Competition:** TruckingOffice from $20/mo "tracks everything you need for IFTA, including miles by state and fuel gallons by state" (https://softwarefinder.com/fleet-management-software/truckingoffice). ELD vendors typically include IFTA mileage (UNVERIFIED).
- **Kills:** K15, K1, K9. **KILL.**

### 13. Truck dispatch services
- **Paid labour:** percent-of-gross dispatch fees are widely advertised (UNVERIFIED: the Truckstop blog page redirect-looped).
- **Kills:** K12. The paid value is load-board hunting and rate negotiation, not a document. **KILL.**

### 14. Trucking invoicing / factoring packets
- **Competition:** TruckingOffice invoicing from $20/mo (https://softwarefinder.com/fleet-management-software/truckingoffice). R2 found this built into factoring apps and TMS.
- **Kills:** K1, K9. **KILL.**

### 15. Property-management owner statements
- **Competition:** Buildium from $62/mo includes accounting and "Financial Reporting & Standard Reports", with reporting automation on the $192 tier (https://www.buildium.com/pricing/). Automatic owner-statement generation was not confirmed on that page (UNVERIFIED), but it is a core PM-software function.
- **Kills:** K2, K9, K13 (the ledger lives in the PM system). **KILL.**

### 16. Accounting-firm monthly management report packs
- **Competition:** Fathom Pro A$59/mo per company; Fathom Portfolio A$62/mo for 100 companies (https://www.fathomhq.com/pricing).
- **Kills:** K1. **KILL.**

### 17. Marketing-agency monthly client reports
- **Competition:** AgencyAnalytics $20 per client per month, automated and white-labelled (https://agencyanalytics.com/pricing).
- **Kills:** K1. **KILL.**

### 18. Amazon FBA reimbursement claims
- **Paid labour/tool:** GETIDA takes a "25% for every Amazon FBA reimbursement", with no subscription (https://revenuegeeks.com/software/getida/pricing).
- **Kills:** K1. It is also detection and recovery, the R2 pattern. **KILL.**

### 19. Freight carrier onboarding packets
- A gate/checker (killed in R2). MyCarrierPortal "Onboard. Monitor. Protect." (https://mycarrierpackets.com/). **KILL.**

## 3. Survivors / uncertain

**None.** The mandatory question ("Who already pays for this exact job today, what do they pay, and why wouldn't they simply use existing software?") gets the same answer in every case above:

> People do pay. The spend is real: $300–700 per real-estate file, $3,449/mo for insurance service teams, $70–300/mo for sales-tax accountants. **But the part of that spend that is a standardisable, generatable artifact already has self-serve software at or below €50/mo, often free** (Certificial free, Levelset waivers free, HMRC PAYE free, Xero CIS £5/mo, TruckingOffice $20/mo, AgencyAnalytics $20/client, ListedKit $15/file, DAVO $58/mo). **What remains on the human invoice is coordination, judgement or liability (K12).**

### Structural finding for the R3 synthesis
When an outsourcer can publish a **per-unit** price for a back-office deliverable, the deliverable is standardised. Standardised deliverables are exactly the ones vertical SaaS and platforms have already absorbed. Where BPOs price by **team per month** (Agency VA) or by **quote** (Flatworld), the labour is a bundle of judgement and coordination, and it cannot be broken into a single generatable artifact. This segment's source type (service menus) therefore selects *against* the R3 thesis. The only exception would be deliverables whose inputs sit behind a system with no incumbent integration, and none was found.

### Untested leads (quota-blocked). Stage D should look at these only if another segment corroborates them
- **EU Intrastat monthly declarations**: monthly and mandatory above national thresholds, often outsourced to customs brokers. The fee level and the ERP/free-portal coverage are completely UNVERIFIED (both Eurostat and Destatis pages returned 404). Prior: ERP modules cover it (K9), and the buyers are mid-size firms (possibly K6).
- **Franchisee monthly royalty/sales reports**: UNVERIFIED. Prior: franchisor platforms own the intake (K13/K9).
- **Job-posting evidence** for narrow "coordinator/processor" roles: not collected (403 on every job board). This must be redone with a working search or scrape before the segment can be called closed.

### What Stage D would need to verify (if any lead is revived)
1. A fetched price list or posting with a per-unit or monthly price for the exact deliverable (not a bundle).
2. An adversarial search confirming no self-serve tool at ≤€50/mo, and that the buyer's system of record does not do it natively.
3. An API or import path for both input and output (K13).
4. Monthly or more frequent recurrence per customer (K15).

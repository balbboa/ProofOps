# R2 Stage B/C — Professional Services, Government, Healthcare Admin, Other

> Date: 2026-09-23. Method: `R2-CRITERIA.md` (K1–K11, mandatory economic-transaction evidence, must-prove table).
> Stance: adversarial. A candidate survives only if there is a paying job **and** no cheap self-serve tool for that exact job **and** no reason for the customer to just use or switch to the incumbent.
> Research limits: the session's WebSearch budget (200 calls) ran out partway through, and some vendor pages returned 403. Anything not confirmed on a fetched page or in a search snippet is marked **UNVERIFIED**. Several figures come from vendor blogs (marketing sources). They are flagged as such and are treated as weak evidence.

## 1. Summary table

| # | Candidate | Verdict | Decisive reason | Economic transaction found? | Cheapest exact competitor + price |
|---|---|---|---|---|---|
| 1 | Tax preparers: client document intake completeness vs prior year | **KILL** | K1/K2/K8/K9. Prior-year-based checklists with missing-document tracking are already built into TaxDome and Soraban. StanfordTax is free up to 5 returns. The work is also seasonal (K5). | Y. Firms pay $18–25+ per return for intake tools (StanfordTax, Soraban). | StanfordTax: free (≤5 returns), $18/return Premium |
| 2 | Immigration firms: petition evidence-packet completeness before filing | **KILL** | K1/K3. Justee AI does this exact pre-filing RFE-risk and consistency review at $19/mo with a free tier. There are also open-source skills and AI petition tools, and case-management incumbents (Docketwise at $79–109/user/mo) are adding AI. | Y. Attorney review costs $150–500+ per review (vendor claim). RFE rate is about 23–27% (sources disagree). | Justee AI: free (3 reviews/mo), $19/mo paid |
| 3 | Small government contractors: RFP compliance matrix / proposal compliance check | **KILL** | K1/K3. The market is crowded with self-serve AI tools: Vercor at $299–499/mo with a free extraction tier, and others from $75/user/mo with a trial. | Y. Proposal staff and consultants are paid. Tool spend is $75–499+/mo. | "$75/user/mo, 7-day trial" tool (name UNVERIFIED); Vercor free extraction tier |
| 4 | Small nonprofits: grant application / reporting packet compliance | **KILL** | K1/K5/K10. Grant AI tools cost $20–25/mo. Reporting is quarterly or annual (not frequent). Small nonprofits have low willingness to pay, and GrantPipe/GrantVantage already cover federal reporting. | Weak. Nonprofits pay $24–499/mo for grant tools, but not specifically for a pre-submission gate. | Grantable ~$24–25/mo; GrantBoost $19.99/mo |
| 5 | Healthcare admin: prior-auth / claim packet scrub (K11 control) | **KILL** | K11 (HIPAA, BAA), K1 (Office Ally clearinghouse scrubbing is free for participating payers, CoverMyMeds is free), K2/K8 (EHR/RCM absorb it). | Y. Small-practice PA tools cost $500–2,500/mo and SPRY starts at $79/mo. | Office Ally: free (participating payers); CoverMyMeds: free |
| 6 | Staffing agencies: worker compliance/credential packet before placement | **KILL** | K1/K9. Self-serve credential tracking already exists (CredGuard: free trial, no card, Nursys checks, "audit packet"). ATSs like Ceipal and Bullhorn include it. HIPAA-adjacent health records push toward K11. | Y. $30–100 per provider per month, or $200–800/mo flat (buyer guide). | CredGuard (price UNVERIFIED, self-serve trial); flat plans from $49/mo per buyer guide (vendor UNVERIFIED) |
| 7 (added) | Solar installers: utility interconnection / permit packet pre-check | **KILL** | Market shrinking 18–21% in 2026 after 25D expired. SolarAPP+ (free) does instant permit checks in 450+ AHJs. Interconnection paperwork is sold as a done-for-you service (GreenLancer). Rules vary across thousands of utilities (K7-like maintenance). | Y. Permit/interconnection packages cost $250–1,550 each (GreenLancer, installer reports). | SolarAPP+: free (permits). GreenLancer service ~$250+/package |
| 8 (added) | Auto dealers: deal jacket / lender funding packet completeness | **KILL** | K8/K9/K2. Dealertrack includes a "Live Funding Checklist". ComplyAuto DealCheck AI is DMS-agnostic PDF upload. Informed.IQ sells lender-side. Dealer buyers are reached through sales (K6). | Y. Contracts-in-transit cash drag (funding in 10–14 days vs 24–48h, vendor claim). Human deal-jacket auditors are paid. | Dealertrack checklist (bundled); ComplyAuto DealCheck AI (price UNVERIFIED) |
| 9 (added) | Exporters (incl. Brazil): LC / export document set pre-presentation check | **KILL** | K1. TradingDocs.AI offers a free LC discrepancy check. SmartLC and ovrseas (14-day trial) are self-serve. There is an open-source UCP600 checker. Traydstream/Loamist serve larger exporters. | Y. 60–75% of first LC presentations are discrepant. Banks charge $50–250 per discrepant presentation. | TradingDocs.AI: free |

**Result: 9/9 KILL. No survivors, no UNVERIFIED-pending candidates.** The recurring pattern: once a pre-flight check sits in front of a regulated or financial submission, either (a) the vertical's system of record already has a checklist feature, or (b) 2024–2026 AI startups already sell a cheap self-serve checker, often with a free tier. The only difference we could offer is "AI + better detection", which is K3.

---

## 2. Per-candidate analysis

Legend for K-checks: **HIT** = kill criterion triggered; **risk** = partial or likely; **ok** = not triggered; **n/a**.

### C1. Tax preparers / small accounting firms: client document intake completeness vs prior year

**Pain evidence**
- Vendors say staff usually find missing documents only when prep starts, often weeks later, which forces follow-ups and resets timelines (vendor marketing): https://www.soraban.com/automate-tax-client-intake-what-growing-firms-need-to-know
- The workflow is standard enough that TaxDome ships a full client-facing "document checklist" with "reason missing" fields: https://client-help.taxdome.com/article/document-checklist
- Strength: real and recurring, but tied to the tax season (Jan–Apr, plus extension season), not weekly.

**Economic transaction**
- Firms already pay per return for intake automation. StanfordTax charges $18/return Premium and $25+/return Enterprise: https://stanfordtax.com/pricing. Soraban charges one credit per client per season per product; a secondary source puts it at $25 collect-only or $40 collect+deliver with a 50-return minimum: https://credfino.com/blog/ai-accounting/4-ai-powered-tax-document-collection-tools-compared/ (secondary, UNVERIFIED on Soraban's site), https://curatesuite.com/accounting/tools/soraban
- Conclusion: the money exists, but it already goes to tools that do this exact job.

**Competitors (exact job = "compare this year's received docs against last year's return and list what is missing")**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| TaxDome | per-user subscription (pricing page 403, UNVERIFIED) | Yes (trial) | **Yes.** The accountant builds a checklist "based on your previous year's return", rolls items over from the prior period, and the client marks missing items with reasons: https://client-help.taxdome.com/article/document-checklist, https://help.taxdome.com/article/document-checklist-management |
| StanfordTax | Free ≤5 returns; $18/return | Yes | **Yes.** Pulls prior-year data from tax software to personalise the questionnaire and document checklist (secondary source): https://credfino.com/blog/ai-accounting/4-ai-powered-tax-document-collection-tools-compared/ |
| Soraban | ~$25–40/return per season, 50-return minimum (UNVERIFIED) | Demo-led (homepage shows no self-serve) https://www.soraban.com/ | **Yes.** "Prior-year-aware intake, missing-item tracking", flags missing or inconsistent data before prep: https://www.soraban.com/tax-planning-software |
| Filed | UNVERIFIED | UNVERIFIED | Partly. Compares source docs against the prepared return: https://www.filed.com/blog/best-ai-tax-prep-platforms |
| Tax-software organizers (UltraTax, Lacerte, Drake) | bundled | n/a | Prior-year carryforward is standard (secondary): https://viasocket.com/discovery/blog/akff5f/7-best-ai-powered-tax-preparation-software |

**K1–K11**
- K1 **HIT**: StanfordTax is free/cheap and self-serve for the exact job.
- K2 **HIT**: the firm's answer is "turn on the TaxDome checklist" (or whatever portal they already use).
- K3 **HIT**: the only room left is "better AI extraction".
- K4 ok: the firm owner pays.
- K5 **HIT**: seasonal, with intake concentrated in roughly 3–4 months.
- K6 ok: SEO/communities work for this audience.
- K7 risk: prior-year comparison needs prior-return import from tax software.
- K8 **HIT**, K9 **HIT**: already a practice-management feature.
- K10 risk: per-return pricing plus seasonality means low MRR per firm outside season.
- K11 risk: taxpayer PII (IRS Pub 4557 / FTC Safeguards Rule obligations; not researched further).

**Economics:** Value per firm can be real (staff chasing documents), but the price anchor is $0–25 per return from incumbents. At €50–200/month year-round we would compete with a free tier on a seasonal job. **Verdict: KILL.**

---

### C2. Immigration law firms: petition evidence-packet completeness before filing

**Pain evidence**
- H-1B RFE rates are reported in the 23–27% range for FY2025/26, although sources conflict (one gives 8.5%): https://www.waylit.com/resources/h-1b-rfe-rates-2026-what-hr-leaders-need-to-know, https://www.davidsonmorris.com/h1b-data/, https://h1bdatahub.com/blog/h1b-rfe-request-for-evidence-guide-2026. Treat the exact rate as UNVERIFIED; the direction (rising since FY2024) is consistent across sources.
- EB-1A/NIW RFE analysis says 72% of RFEs challenge five core criteria: https://www.researchgate.net/publication/392264054_Comprehensive_Analysis_of_EB1A_and_EB2-NIW_RFEs_Trends_Systemic_Challenges_and_Evidence-Based_Response_Frameworks

**Economic transaction**
- Justee positions itself against attorney review costing "$150–500+" (vendor claim): https://justee.ai/compliance-review/visa-documentation
- Firms pay $79–109 per user per month for Docketwise: https://www.docketwise.com/pricing/, https://www.truereview.co/post/docketwise-review
- No hard figure was found for the cost of an RFE to a firm (UNVERIFIED). The LegistAI ROI guide gives only a method: https://www.legistai.com/immigration-software-pricing-guide-how-to-calculate-roi

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| Justee AI (visa documentation review) | Free 3 reviews/mo; paid from $19/mo | Yes, no sign-up for free | **Yes.** About 125 checks, I-129 vs letters/CV/degree-evaluation mismatches, LCA wage alignment, evidence mapped to statutory prongs, form completeness: https://justee.ai/compliance-review/visa-documentation |
| Vera EB suite (open source) | Free | Yes | Yes for EB-1/NIW evidence organisation through RFE: https://github.com/VeraSuperHub/vera-eb-suite |
| AutoPetition, PassRight | UNVERIFIED | UNVERIFIED | Draft and assess O-1/EB-1/NIW petitions: https://www.autopetition.us/, https://www.passright.com/ai-for-o1-eb1a-immigration-cases/ |
| USVisaStack | UNVERIFIED | Yes | RFE responses: https://usvisastack.ai/tools/rfe-response |
| Docketwise | $79–109/user/mo; Pro includes "AI writing and document assistance" | Yes | Partly (questionnaires, document collection) |
| LegistAI | not published | Demo | Itemised evidence checklists, AI drafting: https://www.legistai.com/immigration-client-portal-with-document-and-invoice-tracking-secure-self-service-for-clients/ |
| INSZoom/Mitratech, LawLogix, Casium | not researched (search budget exhausted), UNVERIFIED | — | — |

**K1–K11**
- K1 **HIT** (Justee $19/mo, free tier).
- K2 **HIT**: firms have case management with checklists.
- K3 **HIT**: the only way to beat Justee is better legal-reasoning AI.
- K4 ok: the firm pays.
- K5 risk: H-1B cap is seasonal, though family/employment-based filings run year-round.
- K6 ok.
- K7 ok.
- K8 **HIT**: Docketwise Pro already includes AI document assistance.
- K9 **HIT**.
- K10 ok-ish.
- K11 risk: sensitive immigration PII and unauthorised-practice-of-law exposure for any output that looks like legal judgment.

**Economics:** A single RFE plausibly costs a firm several attorney/paralegal hours (UNVERIFIED), so the €300+/month value is plausible for mid-size firms. The price ceiling is set by a $19/mo self-serve competitor. **Verdict: KILL.**

---

### C3. Small government contractors: RFP compliance matrix / proposal compliance check

**Pain evidence:** Budget tools "leave you building compliance matrices by hand"; enterprise tools assume dedicated compliance staff: https://www.sweetspot.so/blog/govcon-ai-tools-small-business-federal-contractors/. The job is a well-known proposal-management task.

**Economic transaction:** Small teams already buy $75–499/month tools. Vercor charges $299/mo Pro and $499/mo Unlimited, has self-serve signup and a free extraction tier, and targets 8–50-person teams (search snippet): https://vercor.ai/resources/rfp-response/rfp-software-for-small-business. Vercor's page names compliance matrix and requirement extraction as core needs. Another tool starts at $75/user/mo with a 7-day trial (tool name UNVERIFIED; from https://deeprfp.com/blog/best-rfp-tools-comparison/ or https://samsearch.co/blog/best-ai-proposal-generation-tools-for-rf-ps-2026).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| Vercor | $299 / $499 per mo; free extraction tier | Yes | Yes (requirement extraction, compliance matrix) |
| Unnamed tool (UNVERIFIED) | from $75/user/mo | Yes, trial | Likely |
| Procurement Sciences | sales-led | No | Yes (compliance matrix agent): https://www.sweetspot.so/blog/govcon-ai-tools-small-business-federal-contractors/ |
| Sweetspot, GovDash, Vultron, AutogenAI, Civio, ContraVault | mixed | mixed | Yes, market listed 31+ tools: https://deeprfp.com/blog/best-rfp-tools-comparison/, https://www.civio.ai/insights/10-best-government-rfp-response-software-tools |

**K1–K11**
- K1 **HIT**.
- K2 risk.
- K3 **HIT**: the space is saturated with AI tools.
- K4 ok.
- K5 risk: bid volume varies by fiscal year.
- K6 ok.
- K7 ok.
- K8 risk: GovTribe/HigherGov can add compliance features.
- K9 **HIT**: the compliance matrix is one module of every proposal suite.
- K10 ok.
- K11 risk: CMMC/CUI expectations are rising (Sweetspot sells CMMC L2 + SOC 2 as a differentiator), which puts a solo developer at a disadvantage.

**Verdict: KILL.**

---

### C4. Small nonprofits: grant application / grant reporting packet compliance

**Pain evidence:** Federal grant reporting requires SF-425 quarterly (within 30 days) and final (within 90 days) reports, 2 CFR 200 allowable-cost tracking and FFATA subaward reports: https://grantpipe.com/resources/best/best-grant-management-for-federal-awards/, https://www.thompsongrants.com/tools-and-resources/sf-425-federal-financial-report. Real but **quarterly/annual** cadence.

**Economic transaction:** Grantable costs about $24–25/mo, with a $75/mo tier; GrantBoost costs $19.99/mo; Instrumentl costs $179–499/mo: https://grantsights.com/blog/best-ai-grant-writing-tools-2026, https://www.fundrobin.com/articles/how-to-guide/ai-tools-for-nonprofits/best-ai-grant-writing-tools-nonprofits/. GrantPipe (federal compliance) costs $329 / $539 / $1,079 per month: https://grantpipe.com/grant-tracking-software/. The same source says QuickBooks plus spreadsheets can survive an audit below $250k in federal spend, so the smallest orgs use a free workaround.

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| Grantable | ~$24–75/mo | Yes | Application drafting; compliance check partial |
| GrantBoost | $19.99/mo | Yes | Drafting |
| Instrumentl | $179–499/mo | Yes | Pipeline, deadlines, post-award |
| GrantPipe | $329+/mo | Yes (published pricing) | Yes for federal reporting compliance |
| GrantVantage | UNVERIFIED | UNVERIFIED | Automated SF-425 generation, 2 CFR 200: https://www.grantvantage.com/nonprofits/ |
| Submit.com | UNVERIFIED | — | Funder-side: https://submit.com/resources/blog/best-grant-management-software-for-nonprofits-2026/ |

**K1–K11**
- K1 **HIT**.
- K2 risk.
- K3 **HIT**.
- K4 risk: tight budgets; often the ED or a volunteer.
- K5 **HIT**: low frequency, since each funder's requirements differ and applications are episodic.
- K6 ok.
- K7 risk: every funder has its own requirements, which is a rule-maintenance problem.
- K8 risk.
- K9 **HIT**.
- K10 **HIT**: low willingness to pay means many customers are needed.
- K11 ok.

**Verdict: KILL.**

---

### C5. Healthcare admin: prior-authorization / claim packet scrub for small practices (K11 control)

**Pain evidence:** Prior authorisation is the most cited admin burden in US medicine (AMA survey pages returned 403, so figures are UNVERIFIED here). Vendor cost analysis: https://nirmitee.io/blog/true-cost-prior-authorization-data-driven-analysis-cms-ama-caqh/

**Economic transaction:** Entry-level PA tools for small practices cost $500–2,500/mo; SPRY starts at $79/mo: https://www.verifytx.com/best-prior-authorization-software/, https://omnimd.com/blog/ai-prior-authorization-tools/. Money clearly changes hands.

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| Office Ally Service Center | Free for participating payers | Yes | Claim scrubbing before payer submission: https://cms.officeally.com/products/pricing, https://www.capminds.com/blog/the-ultimate-guide-to-using-office-ally-for-managing-claims/ |
| CoverMyMeds | Free to providers | Yes | Pharmacy PA: https://www.verifytx.com/best-prior-authorization-software/ |
| SPRY | from $79/mo | Yes | EMR/RCM + PA automation |
| Insight Health, Prosper AI, Develop Health, Simbie | sales-led | No | PA automation: https://www.insighthealth.ai/blog/top-ai-prior-authorization-software |
| EHR/RCM built-ins | bundled | — | Claim scrubbers are standard in clearinghouses |

**HIPAA burden (explicit):** Any tool that ingests claims, clinical notes or PA packets processes PHI. It needs a Business Associate Agreement with each practice, HIPAA Security Rule safeguards (risk analysis, access controls, audit logs, breach notification) and BAAs with every sub-processor (hosting, LLM provider). Buyers increasingly expect SOC 2/HITRUST. For a solo side project in Brazil with a €35/month budget this is incompatible (K11). General knowledge, not separately sourced here, so mark the legal specifics as UNVERIFIED.

**K1–K11**
- K1 **HIT** (free clearinghouse scrubbing, free CoverMyMeds).
- K2 **HIT**.
- K3 **HIT**.
- K4 ok.
- K5 ok (daily).
- K6 risk: practices buy via RCM vendors or consultants.
- K7 **HIT**: payer rules plus EHR integration.
- K8 **HIT**, K9 **HIT**.
- K10 ok.
- K11 **HIT**.

**Verdict: KILL.** The control behaves as expected: strong pain and money, killed on K11 and incumbents.

---

### C6. Staffing agencies: worker compliance / credential packet before placement (esp. healthcare)

**Pain evidence:** Credential expiry and missing documents delay placements. Vendors frame it as "stop chasing nurses for expired credentials": https://www.credguardapp.com/, https://www.varshealth.com/post/healthcare-staffing-agency-software-for-compliance-and-credentialing. Frequency is high (every placement, every renewal).

**Economic transaction:** Small agencies pay $30–100 per provider per month or $200–800/mo flat (buyer guide, vendor-authored): https://www.varshealth.com/post/credentialing-management-software. The same search snippet lists flat plans at $49/$199/$399 per month billed annually; vendor name UNVERIFIED, likely from https://payerready.com/blog/credentialing-tracking-software-small-practices.

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| CredGuard | not shown; 14-day trial, no card | Yes | **Yes.** Nursys nightly verification, BLS/ACLS, TB, immunisations, background checks, reminders, "instant audit packet generation": https://www.credguardapp.com/ |
| RenewOps | UNVERIFIED | Yes ("lightweight") | Renewal tracking: https://renewops.app/solutions/healthcare-license-tracking-software |
| Vars Health | UNVERIFIED | UNVERIFIED | Credential management: https://www.varshealth.com/credential-management |
| Ceipal, Bullhorn (ATS) | bundled | Sales-led | Credentialing module with Nursys: https://www.ceipal.com/healthcare-staffing-software/credentialing, https://www.bullhorn.com/blog/best-healthcare-staffing-software/ |

**K1–K11**
- K1 **HIT** (CredGuard self-serve, low-cost plans).
- K2 **HIT**: agencies on Bullhorn or Ceipal use the module.
- K3 **HIT**.
- K4 ok.
- K5 ok.
- K6 ok.
- K7 risk: Nursys and state boards.
- K8 **HIT**, K9 **HIT**.
- K10 ok.
- K11 **risk/HIT**: immunisation and health records, plus I-9 data. CredGuard markets itself as "HIPAA-compliant", which signals buyer expectations.

**Verdict: KILL.**

---

### C7 (added). Solar installers: utility interconnection / permit packet pre-check

**Pain evidence:** 30–40% of residential interconnection applications have at least one error on first submission; incomplete single-line diagrams are the top cause. Source is a vendor blog (weak): https://energyscaperenewables.com/post/interconnection-application-errors-why-40-get-kicked-back/, https://energyscaperenewables.com/post/solar-permit-rejected-incomplete-electrical-diagrams/

**Economic transaction:** Installers outsource permit and interconnection packages. GreenLancer packages are quoted at $260–1,550; residential permit packages start around $250 (secondary): https://heavendesigns.in/blog/greenlancer-pricing/, https://www.greenlancer.com/pv-interconnection

**Competitors / structural problems**
- SolarAPP+: free NREL/DOE platform with instant code checks, 450+ AHJs, about a third of the market: https://energyscaperenewables.com/post/solarapp-states-2026-where-instant-permits-work/
- Installer suites include interconnection coordination (SubcontractorHub, Aurora, OpenSolar): https://www.subcontractorhub.com/blog/best-solar-installer-software
- Utilities run their own intake portals with enforced screens (eTRACK+, PowerClerk / Clean Power Research): https://www.anbsystems.com/blog/solar-interconnection-in-the-age-of-electrification/, https://www.cleanpower.com/utility-solutions/interconnection-management/
- Market contraction: 25D expired 31 Dec 2025, 2026 installs forecast down 18–21%, and Freedom Forever filed Chapter 11 in April 2026: https://www.surgepv.com/blog/us-residential-solar-market-trends-2026, https://energynewsbeat.co/solar/the-bust-in-us-home-solar-has-worsened-after-trump-ends-subsidies/

**K1–K11**
- K1 **HIT** for permits (SolarAPP+ free).
- K2 **HIT**: outsourcing to a permit service is the natural response.
- K3 risk.
- K4 ok.
- K5 ok.
- K6 ok.
- K7 **HIT**: utility-specific rules across many territories mean heavy rule maintenance.
- K8 **HIT**: utility portals and installer suites.
- K9 **HIT**.
- K10 risk: shrinking market.
- K11 ok.

**Verdict: KILL.**

---

### C8 (added). Auto dealers: deal jacket / lender funding packet completeness

**Pain evidence:** Incomplete jackets delay title work and funding. Contracts-in-transit funding takes 10–14 days vs 24–48h with a complete "lender-ready" jacket (vendor claim): https://docupile.com/digital-deal-jacket-auto-dealerships/, https://www.movemetalcrm.com/tools/cit-calculator

**Economic transaction:** Cash tied up in CIT, dealer compliance auditors, and consultants such as Calish selling pre-funding AI audits: https://www.calish.com/workflows/compliance-deal-jacket-audit-for-used-car-dealer-group-manager/

**Competitors**
- Dealertrack "Live Funding Checklist" (bundled with e-contracting): https://us.dealertrack.com/content/dealertrack/en/f-and-i/electronic-contracting.html
- ComplyAuto DealCheck AI and Guardian: DMS-agnostic, upload deal PDFs (price UNVERIFIED): https://complyauto.com/dealcheck-ai/
- Informed.IQ (lender side, partnered with defi SOLUTIONS): https://www.businesswire.com/news/home/20250910376299/en/defi-SOLUTIONS-Announces-New-Partnership-with-Informed.IQ-to-Automate-Funding-Process-and-Reduce-Risk
- MoveMetal digital deal file for independent dealers: https://www.movemetalcrm.com/us-dealership-compliance

**K1–K11**
- K1 risk: exact PDF-upload competitor exists; price unknown.
- K2 **HIT**.
- K3 **HIT**.
- K4 ok.
- K5 ok (daily).
- K6 **HIT**: dealers are reached through reps and 20-group relationships (UNVERIFIED, typical).
- K7 risk: lender-specific stip rules.
- K8 **HIT**, K9 **HIT**.
- K10 ok.
- K11 risk: GLBA/FTC Safeguards Rule on consumer credit data.

**Verdict: KILL.**

---

### C9 (added). Exporters (including Brazilian SMEs): LC / export document set pre-presentation check

**Pain evidence:** 60–75% of LC presentations are discrepant on first try (ICC estimate quoted by vendors); DC-Pro's 2005 survey found 56%: https://docshipper.com/glossary/discrepancy-letter-credit-definition-logistics/, https://ovrseas.io/blog/lc-document-rejection-why-most-fail-first-try

**Economic transaction:** Banks charge $50–250 per discrepant presentation, plus payment delay: https://ovrseas.io/blog/lc-document-rejection-why-most-fail-first-try. Clear money-before-release gate.

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| TradingDocs.AI | **Free** check (100 page credits); paid pricing not shown | Yes | **Yes.** LC vs invoice/packing list/B/L/certificates under UCP 600 and ISBP 821: https://tradingdocs.ai/free-check.html |
| SmartLC | not shown | UNVERIFIED | Yes. LC terms, UCP 600, Field 47A, cross-document consistency: https://smartlc.ai/ |
| ovrseas | 14-day trial | Yes | Prevents discrepancies at creation (single data entry) |
| portable-genai trade-finance-checker | Free (open source) | Yes | Yes: https://github.com/portable-genai/trade-finance-checker |
| Traydstream, Loamist, Conpend | enterprise | No | Yes: https://traydstream.com/for-exporters, https://www.loamist.com/ |

Brazil-specific angle (DU-E vs NF-e vs commercial invoice consistency): could not be researched because the search budget was exhausted. **UNVERIFIED.** The prior assumption is that customs brokers (despachantes) and export ERPs already do this job, which would be K2/K9, but that is unproven.

**K1–K11**
- K1 **HIT**.
- K2 risk: freight forwarders and banks check documents.
- K3 **HIT**.
- K4 ok.
- K5 risk: LC usage is per shipment and a minority of SME trade (UNVERIFIED).
- K6 ok.
- K7 ok.
- K8 risk.
- K9 risk.
- K10 ok.
- K11 ok.

**Verdict: KILL.**

---

## 3. Survivors / uncertain: Stage D requirements

**None survive.** For the record, the uncomfortable question, answered for the strongest-looking losers:

- **Tax intake:** Firms pay $0–40 per return to TaxDome, StanfordTax and Soraban, which already build checklists from the prior-year return. They would simply use those.
- **Immigration evidence review:** Firms pay attorney/paralegal time, and applicants pay $150–500+ for review (vendor claim). Justee does the exact pre-filing check for $19/mo with a free tier, and Docketwise Pro bundles AI assistance.
- **LC document check:** Exporters pay $50–250 per discrepancy plus delay. TradingDocs.AI checks for free.

**Cross-cutting lesson for R2:** In professional services, gov, healthcare and trade, "pre-flight completeness check before submission" was a crowded AI-startup category by 2025–2026, and vertical platforms own the checklist. A surviving wedge probably needs all three of these:
1. A document set that spans parties no single platform owns.
2. Rules that are public and stable (not per-utility or per-funder).
3. A buyer without a dominant vertical system.

None of the 9 candidates here meet all three.

**Optional low-cost follow-ups (only if the coordinator wants them; not expected to change verdicts):**
- Brazil export DU-E/NF-e consistency check: confirm whether despachantes and ERPs (e.g. Conexos, Softcomex, Bysoft; names UNVERIFIED) already cover it.
- ComplyAuto DealCheck AI pricing.
- CredGuard pricing.

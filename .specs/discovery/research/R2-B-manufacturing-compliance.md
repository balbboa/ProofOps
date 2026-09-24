# R2 Stage B/C: Manufacturing, Wholesale, Product/Trade Compliance

> Date: 2026-09-23. Method: R2-CRITERIA.md (K1–K11, mandatory economic-transaction evidence). Adversarial: each candidate had to survive a competitor search before it could pass.
> Research limitation: the session's WebSearch budget ran out partway through (200/200) and WebFetch was briefly rate-limited. Claims without a URL are marked UNVERIFIED.

## Summary

| Candidate | Verdict | Decisive reason | Economic transaction found | Cheapest exact competitor + price |
|---|---|---|---|---|
| 1. MTR/CoC receiving check vs PO/spec | KILL | K1 + K3: self-serve AI cert checking already exists; 8+ AI entrants | Y: 15–25 min/cert QA labour; MetalTrace $5k or $500/mo | SmartCert: free (10 certs/mo), Basic from $30/mo |
| 2. Amazon compliance packets (CPC/CPSIA/GPSR) | KILL | K5 (event-driven per ASIN) + K8 (Amazon owns opaque criteria) | Y: $100/ASIN document review; consultants from €149; CPSIA tests $500–1,500 | ComplianceGate from $199/yr (templates and requirements); Amazon Compliance Reference free |
| 3a. CBAM supplier data readiness | KILL | K1 + K5 (annual declaration) + K10 (50 t threshold removes SMEs) | Y (qualitative); consultant prices UNVERIFIED | CarbonChain free self-serve tier |
| 3b. EUDR supplier packets | KILL | Not live until 30 Dec 2026; repeatedly amended; Coolset covers the full chain (K3); geodata (K7) | N (no live obligation yet) | Coolset (price not public); free scope checker |
| 4. Food import FSVP / supplier packets | KILL | K5 (per supplier, 3-year re-evaluation) + K2/K9 (food QMS suites) | Partial: FSVP services exist, prices UNVERIFIED | UNVERIFIED (vendor sites blocked) |
| 5. Vendor onboarding (W-9/bank/insurance) | KILL (control) | K1/K9: bundled in AP suites | Y: Tipalti from $99/mo includes it | Tipalti AP from $99/mo |
| 6. PPAP/FAI packages (added) | KILL | K5 (per part or change) + K9 | Y: 1factory QC $75/user/mo (5-user min) | 1factory (demo-led) |
| 7. Export screening / hazmat DG / cosmetics CPNP (added, brief) | KILL | CSL free API (K1); DG liability and carriers (K8/K11); CPNP one-off per product (K5) | Partial | CSL: free |

**Bottom line: 0 survivors, 0 UNCERTAIN.** In this segment, frequent checks already have cheap self-serve AI tools. Checks without such tools are infrequent, not yet in force, or judged by a platform owner.

---

## 1. Receiving inspection: MTR / CoC checked against PO and spec

### Pain evidence
- AS9100 auditors specifically check that companies "don't just receive and file" CoCs and raw-material certs. Reports must be evaluated against requirements before use (Elsmar Cove threads: https://elsmar.com/elsmarqualityforum/threads/as9100-verification-of-raw-material-supplier-test-reports.42438/ , https://elsmar.com/elsmarqualityforum/threads/as9100-rev-d-question-about-8-4-3-k-supplier-certificates.71423/).
- Practitioners say every mill cert's chemistry must be compared to the applicable spec and PO (https://elsmar.com/elsmarqualityforum/threads/material-certification-for-steel-we-receive.39760/).
- Recurring: this happens on every receipt of material, so it is daily or weekly in a fabricator or machine shop.

### Economic transaction
- "Manual MTR review by a procurement engineer averages 15 to 25 minutes per certificate" (vendor claim, Pathnovo: https://pathnovo.com/solutions/procurement-intelligence/mtr-automation).
- Buyers already pay for MTR software: MetalTrace costs $5,000 as a one-time licence, or $500/month SaaS (https://sourceforge.net/software/product/MetalTrace/ , https://www.softwareadvice.com/manufacturing/metaltrace-profile/). **Y.**

### Competitors
| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| SmartCert | Free (10 certs/mo); Basic from $30/mo with AI review, extraction and compliance flagging (https://www.smartcert.tech/pricing/) | Yes, free signup | Yes: extracts MTR data, validates specs and flags issues (https://www.smartcert.tech/) |
| MTR.AI | Not public; early access (https://www.mtr.ai/) | No (early access) | Yes: element-by-element pass/fail against spec, with PO override |
| Magenta AI | Not public; demo (https://www.withmagenta.com/) | No | Yes: supplier data packages and CoCs checked against PO and quality clauses, with missing docs flagged |
| Pathnovo | Credit-based (Starter 1,000 credits/mo; 2 credits/page); price not public (https://pathnovo.com/solutions/procurement-intelligence/mtr-automation) | Semi (demo-first) | Yes: PO line matching and spec validation |
| Certivo | Not public (https://www.certivo.com/blog-details/certivo-simplifies-mill-test-report-analysis-with-ai-powered-compliance-tools) | No | Yes |
| Aekam AI, DocumentIQ, Star Software, Datagrid (Procore) | Not public (https://aekam.ai/pages/mtr-automation.html , https://starsoftware.co/mtr-automation/ , https://datagrid.com/blog/ai-agents-material-test-report-validation) | No | Yes / partial |
| MetalTrace | $5k licence or $500/mo | Trial | Storage and traceability; partial on validation |

### K1–K11
- **K1 HIT**: SmartCert already sells this self-serve, free up to 10 certs and from $30/mo.
- **K3 HIT**: at least 8 AI-first entrants appeared in 2025–26. Any new entrant could only differ on AI, UI or price.
- K2/K8/K9 partial: ERPs for metals and QMS tools (MetalTrace, service-centre ERPs) hold heat and cert traceability. UNVERIFIED how much validation they include.
- K5 pass (frequent). K6 partial (the aerospace-focused vendors are demo-led, but SmartCert shows self-serve works). K7 pass. K11 pass, except ITAR customers (Magenta markets ITAR).

### Economics
- Plausible saving: 20 certs/day × 20 min ≈ 6.7 h/day of QA time. The value is real, and competitors are already capturing it.

### Verdict: **KILL** (K1, K3)

---

## 2. Amazon / marketplace compliance document packets (CPC, CPSIA, GPSR, SDS)

### Pain evidence
- Amazon can request compliance documents "at any time", including months or years after listing (https://www.compliancegate.com/amazon-product-compliance-document-requests-removals/).
- Common rejection causes: mismatches between documents (e.g. the manufacturer on the CPC differs from the test report, or the importer differs from the seller account), and uploading a GCC where a CPC is required (search summary citing https://www.goatconsulting.com/amazon-policy/amazon-childrens-product-certificate-cpc and https://salesduo.com/blog/amazon-compliance-documents/ ; exact wording UNVERIFIED on page).
- Amazon reportedly gives a 90-day response window; missing it means ASIN suppression (https://nventory.io/blog/amazon-product-compliance-documents-2026).
- Seller forum threads dispute CPC requests (https://sellercentral.amazon.com/seller-forums/discussions/t/7a3e67cc-2ac1-4953-8cad-bc6407eef99d).

### Economic transaction
- A seller was quoted "document review only, was $100 per ASIN" by a review provider (https://sellercentral.amazon.com/seller-forums/discussions/t/5faa6400-4635-4467-9d2a-0a45bcb06814).
- CPSIA testing costs $500–1,500 per product (https://nventory.io/blog/amazon-product-compliance-documents-2026). A CPC from a lab costs $500–1,200 (https://www.jjrlab.com/news/how-much-does-an-amazon-cpc-certificate-cost.html).
- Consultants: SPACEGOATS compliance consulting from €149 (https://spacegoats.io/product-compliance-consulting/). **Y.**

### Competitors
| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| ComplianceGate platform | from $199/year (requirements lists, certificate templates, label tool, consultant tickets) (https://www.compliancegate.com/amazon-product-compliance-document-requests-removals/) | Yes | Largely: it builds correct CPC/GCC docs so they pass |
| Amazon Compliance Reference (in Seller Central) | Free (https://www.sellerassistant.app/blog/amazon-seller-compliance-documents/) | Yes | Partial: requirements lookup |
| Seller Assistant restriction checker | Not disclosed; 14-day trial | Yes | Partial |
| GC GPSR Compliance (Shopify app) | UNVERIFIED (https://apps.shopify.com/gpsr-compliance-dashboard) | Yes | GPSR docs, Shopify-side |
| Apify GPSR Catalog Compliance Auditor | pay per result (https://apify.com/formnexa/gpsr-catalog-compliance-auditor) | Yes | Partial: listing-level GPSR |
| Labs and consultants (SGS, Intertek, UL, QIMA; SPACEGOATS; Goat Consulting) | $100/ASIN review; from €149 | No | Yes (done-for-you) |

### K1–K11
- **K5 HIT**: a request comes once per ASIN (at listing, or on a random audit or category change). For a typical SME seller the check is event-driven, not weekly. Large catalogs are the exception, and those sellers use consultants or agencies.
- **K8 HIT**: Amazon is the gatekeeper and its acceptance criteria are opaque and change often; it runs its own automated checks (nventory mentions an AI system rejecting documents). A third-party pre-flight cannot guarantee acceptance, and Amazon can add the check itself.
- **K1 partial**: ComplianceGate at $199/year already sells templates and requirement lists that stop malformed CPCs being created in the first place.
- K2: the natural response is to pay the lab or consultant who issued the documents to fix them, or to use the lab's CPC template.
- K4 clear (the seller pays). K6 clear (communities exist). K10 risk: at $30/mo with churn tied to one-off events.

### Economics
- The value per event is real (a suppressed ASIN means lost sales), but it is episodic. Paying $100 per ASIN review as a one-off beats paying €50/month.

### Verdict: **KILL** (K5, K8; K1 partial)

---

## 3. EU importers: CBAM and EUDR supplier data packets

### 3a. CBAM (definitive regime)

#### Regulatory timeline (2026)
- The definitive regime has applied since 1 Jan 2026: authorisation, reporting, and purchase and surrender of CBAM certificates (https://taxation-customs.ec.europa.eu/carbon-border-adjustment-mechanism_en).
- Only importers above a single 50-tonne-per-year mass threshold must become authorised CBAM declarants (https://taxation-customs.ec.europa.eu/carbon-border-adjustment-mechanism/cbam-definitive-regime_en). The widely reported claim that this exempts ~90% of importers while covering ~99% of emissions is **UNVERIFIED** here: the page does not state it.
- Importers may use Commission **default values** (Excel) instead of actual installation data, and actual data requires verification (same URL). This matters: an SME can avoid the supplier-data problem entirely by paying for default values.
- First annual declaration deadline (believed 30 Sep 2027 for 2026 imports) and certificate sales start (believed Feb 2027): **UNVERIFIED**, not stated on the fetched pages.

#### Pain / economic transaction
- Obliged importers bear real costs (certificates, verification, consultants). But the SME importers the founder could reach are mostly below 50 t, and the rest can fall back to default values. **Y (qualitative)**; no public price for consultant CBAM data review was captured (UNVERIFIED).

#### Competitors
| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| CarbonChain | Free tier ("CBAM for declarants – Try free", free Supplier Catalogue, free calculator); paid tiers not public (https://www.carbonchain.com/cbam) | Yes | Yes: supplier outreach, data tracking, validation of actual emissions by an in-house expert team |
| Coolset | Not public; demo (https://www.coolset.com/cbam) | No | Partial or unclear |
| Commission default values + guidance | Free (https://taxation-customs.ec.europa.eu/carbon-border-adjustment-mechanism/cbam-guidance-and-legislation_en) | Yes | Free workaround (skip supplier data) |

#### K1–K11
- **K5 HIT**: the declaration is annual, and supplier data is collected once per installation or product and then reused. The readiness gate does not recur weekly.
- **K1 HIT**: CarbonChain offers a free self-serve tier for this exact job.
- **K10 HIT**: the 50 t threshold pushes the long tail of SMEs, the founder's natural buyers, out of scope.
- K11 partial: verification and accreditation rules add liability to anyone who calls data "complete enough to file".
- Regulatory risk: high. The rules were simplified once already (the threshold), and more changes are plausible.

**Verdict: KILL** (K1, K5, K10)

### 3b. EUDR

#### Regulatory timeline (2026)
- Application was delayed again: large and medium operators from **30 Dec 2026**, micro and small from **30 Jun 2027**. The regulation was amended in Dec 2024 and Dec 2025 to reduce burdens (https://environment.ec.europa.eu/topics/forests/deforestation/regulation-deforestation-free-products_en).
- Coolset's scope checker references further "May 2026 simplifications" (https://www.coolset.com/eudr). Details are UNVERIFIED.
- As of this date the obligation has **not yet applied to anyone**. No one pays today for a recurring check against a live obligation. The market is pre-regulatory and the rules keep shifting.

#### Competitors
| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| Coolset EUDR | Not public, "no setup fees"; free scope checker (https://www.coolset.com/eudr) | Partial (self-guided tour, demo) | Yes: supplier requests for GPS, harvest date and legality docs; AI document verification; satellite deforestation check; DDS generation and TRACES submission |
| EU EUDR Information System (TRACES) | Free (same Commission URL) | Yes | Filing channel |
| Many others (osapiens, Preferred by Nature, etc.) | UNVERIFIED | UNVERIFIED | UNVERIFIED |

#### K1–K11
- **Regulatory-timeline HIT**: twice delayed and still being simplified, with no live obligation in Sep 2026.
- **K3 HIT**: a funded incumbent (Coolset) already covers the whole readiness chain including geolocation, so an entrant could only differ on AI or UI.
- K7 risk: a real check needs geospatial deforestation data, which is not a document-only MVP.
- K4 unclear, since the Dec 2025 amendments reportedly reduce obligations for downstream operators and traders (UNVERIFIED).

**Verdict: KILL** (timeline, K3, K7)

---

## 4. Food importers: FDA FSVP / prior notice / supplier packets

### Pain / cadence
- FSVP requires records per **food–supplier pair**: hazard analysis, supplier approval, verification activities and corrective actions. Re-evaluation is required **at least every 3 years**, annual onsite audits apply only to SAHCODHA hazards, and other verification runs on a risk-based schedule (https://www.fda.gov/food/food-safety-modernization-act-fsma/fsma-final-rule-foreign-supplier-verification-programs-fsvp-importers-food-humans-and-animals).
- So the "packet" is built at supplier approval and refreshed periodically. It is **not** a per-shipment gate. Prior notice is per shipment, but it is a short filing done by customs brokers or in FDA's Prior Notice System Interface (UNVERIFIED on cost; brokers typically bundle it).

### Economic transaction
- FSVP agent and FSVP-plan services are sold by regulatory firms such as Registrar Corp; their site blocked fetching (403, https://www.registrarcorp.com/), so **prices are UNVERIFIED**.
- Food-safety QMS or supplier-management suites (TraceGains, SafetyChain, FoodReady) sell supplier document collection and expiry tracking. Their sites blocked fetching or returned 404, so **pricing is UNVERIFIED**.

### K1–K11
- **K5 HIT**: the cycle is per supplier (a 3-year re-evaluation, annual at most), not weekly.
- **K2/K9 HIT**: supplier-document management is a core module of food-safety QMS suites; an importer who needs it buys the suite or an FSVP consultant, who also carries the "qualified individual" judgment.
- **K11 partial**: the output is a food-safety legal determination by a qualified individual, which is liability-heavy for a solo developer.

**Verdict: KILL** (K5, K2/K9; K11 partial). Evidence quality is lower here because competitor pricing could not be fetched.

---

## 5. Supplier/vendor onboarding packet (W-9/W-8, bank, insurance, certs): control case

### Economic transaction
- AP automation already bundles it: Tipalti Accounts Payable **from $99/month** includes self-service supplier onboarding, W-9/W-8 tax form collection and validation of tax IDs "across 62 countries against 3,000+ rules" (https://www.tipalti.com/pricing/).
- Track1099 now redirects to Avalara's 1099 product (https://www.track1099.com/ → avalara.com), a sign of incumbent consolidation. Its W-9 pricing is UNVERIFIED.

### K1–K11
- **K1 HIT** (Tipalti $99/mo includes it). **K2/K8/K9 HIT**: it is a feature of AP, spend and procurement platforms (Tipalti, and UNVERIFIED for Ramp, Bill, Coupa). K5 is borderline (a one-off per vendor).

**Verdict: KILL**. The control case behaves as expected.

---

## 6. Added: PPAP / FAI packages for small automotive or aerospace suppliers

- Incumbent pricing is public: 1factory includes PPAP (PFMEA, control plans, Gage R&R), AS9102 FAI and CoC management in incoming inspection. QC plan $75/user/month (5-user minimum); supplier collaboration $20 per connected supplier/month (https://www.1factory.com/pricing.html). Demo-led.
- Cadence: a PPAP is produced per new part or engineering change, which is event-driven rather than weekly for a small supplier (UNVERIFIED frequency data; reasoning from the PPAP trigger definition). The customer (OEM or Tier 1) dictates format and portal. An Elsmar thread shows material certs are part of PPAP submissions (https://elsmar.com/elsmarqualityforum/threads/material-certification-for-ppap.8688/).
- **K5 HIT, K9 HIT** (a module in QMS suites like 1factory), K2 (the customer's portal or template dictates the format).

**Verdict: KILL**

## 7. Added (brief screens): export controls, hazmat paperwork, cosmetics CPNP/PIF

- **Export screening**: the US Consolidated Screening List has a free search, a free API and daily-updated downloadable files (https://www.trade.gov/consolidated-screening-list). **K1 HIT.** ECCN classification is done once per SKU (**K5**).
- **Hazmat / DG shipping paperwork**: DG software such as DGOffice exists (https://www.dgoffice.net/, page content not retrievable; pricing UNVERIFIED). Carrier and shipping platforms validate DG entries at label creation (UNVERIFIED). There is also liability: trained-shipper certification sits with a person. **K8/K11 risk. KILL (low evidence).**
- **Cosmetics EU CPNP/PIF**: notification and dossier are prepared once per product before it goes on sale, and are done by the Responsible Person or consultants (Commission CPNP page returned 404; UNVERIFIED). **K5 HIT. KILL.**

---

## Stage D handoff

**No survivors and no UNCERTAIN candidates in this segment.**

Answer to "Who already pays for this exact job today, what do they pay, and why wouldn't they simply use the existing product?", for the strongest candidate (MTR/CoC receiving check):
- **Who pays:** QA and receiving staff at AS9100/ISO 9001 fabricators, machine shops and EPC contractors. They spend about 15–25 min per cert (Pathnovo), buy MetalTrace ($5k or $500/mo), or buy AI MTR tools.
- **Why they wouldn't buy ours:** SmartCert already offers the exact job self-serve (free for 10 certs/mo, from $30/mo). At least seven other AI-first vendors (MTR.AI, Magenta, Pathnovo, Certivo, Aekam, DocumentIQ, Datagrid/Procore) target the same job. A new entrant would differ only on AI, UI or price (K3).

**Pattern across the segment (useful for the funnel):**
1. Where the check is **frequent** (MTRs on every receipt), an AI-extraction gold rush started in 2025–26 and self-serve tools already exist.
2. Where **no** cheap tool exists (FSVP, PPAP, CPNP, CBAM), the check is **infrequent** (per supplier, per part or per product, or annual) or the regulation is **not yet live** (EUDR).
3. Where a **platform owner** judges the documents (Amazon), it controls the acceptance criteria.
Frequency and no cheap competitor did not occur together anywhere in this segment. The kill criteria removed each candidate for a different reason, not all for the same one.

**If the coordinator wants one thread to keep:** a narrower MTR angle, EN 10204 3.1 certs for small EU or LatAm fabricators outside the US-aerospace focus of current vendors. This is weak: SmartCert's free tier and generic LLM document tools already cover it. Recommend not pursuing without new evidence.

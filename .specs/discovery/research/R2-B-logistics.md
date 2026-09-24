# R2 Stage B/C: Logistics & Trade Readiness Gates

> Date: 2026-09-23. Method: `R2-CRITERIA.md` (K1–K11, mandatory economic-transaction evidence). Adversarial pass.
> Research limit: the session's web-search budget ran out partway through. Candidate 5 and the added Candidate 6 got less competitor research than the others, and the gaps are marked **UNVERIFIED**. Prices come only from the cited pages. Where a page did not show a price, the report says so.

## 1. Summary

| # | Candidate | Verdict | Decisive reason | Economic transaction found? | Cheapest exact competitor + price |
|---|---|---|---|---|---|
| 1 | Shipment packet consistency check (CI vs PL vs B/L vs SLI) | **KILL** | K3/K8/K9. Forwarding platforms (Magaya, CargoWise add-ons, Tier2, Wove) already cross-check these documents with AI. Exporters avoid the mismatch by generating every document from one dataset (IncoDocs from $27/mo). A new product would differ only by "AI + cheaper". | Y. Demurrage runs $75–300 per container per day when documents hold cargo. Third-party filing costs $50–125 per shipment. | TradingDocs.AI: free tier (100 page credits); paid from $299/mo. Prevention instead of checking: IncoDocs $0 / $27 / $62 / $167 per month. |
| 2 | LC (UCP 600) presentation pre-check for SME exporters | **KILL** | K1 + K3 + K5. A free self-serve LC checker already exists (TradingDocs.AI). SmartLC, Loamist and V7 cover the same job. A typical SME presents LCs rarely. | Y. 60–75% of first presentations are discrepant. Bank fees are about $50–250 per presentation. Outsourced presentation service starts around £125. | TradingDocs.AI free LC checker (100 free pages, no card). SmartLC 30-day free trial (paid price not shown). |
| 3 | Trucking billing packet (RC + BOL + POD + accessorials) before factoring | **KILL** | K2 + K8 + K9 + K10. The factoring company already reviews the packet for free. Factor apps have AI document scanning. Carrier TMSs start at $20/mo and include packet assembly. Owner-operators have low willingness to pay. | Y. Each rejected invoice costs $10–20 in labour plus 1–5 days of cash delay. Factoring costs about 2.8% per invoice. | Factor apps (RTS Pro, OTR Solutions): free with factoring. TruckingOffice from $20/mo. Datatruck (automated document verification; price not shown). |
| 4 | ISF 10+2 / entry data completeness pre-filing | **KILL** | K1 + K2 + K9 + K11. A full ISF filing done for you costs $25–50. Broker ABI/ISF software validates the data elements. Filing runs through CBP ACE. | Y. Liquidated damages are up to $5,000 per late or inaccurate ISF. | RocketISF ($25 in the search snippet, $50 on its page). EZ-ISF $50 filing + $75 bond. |
| 5 | Broker carrier onboarding packet (authority, W-9, COI) | **KILL (control)** | K1 + K9. MyCarrierPackets / MyCarrierPortal, RMIS and Highway are the category standard. | Y (brokers pay these vendors; amounts UNVERIFIED) | MyCarrierPackets (pricing not shown; UNVERIFIED) |
| 6 (added) | SME importer/exporter: forwarder freight-invoice pre-approval check (invoice vs quote/contract) | **UNCERTAIN → leaning KILL** | Strong economic signal, but the freight-audit category is mature (Freehand, Loamist). K7 risk: the quote or contract rates must be loaded. K3 risk. The adversarial search for self-serve competitors was **not completed**. | Y (vendor-claimed). 80% of freight invoices have a discrepancy. Overcharges average 8–10%. 1.5–2.5% of forwarder spend is recoverable. | Freehand (demo-led, price not shown). Self-serve SME competitor: UNVERIFIED. |

**Bottom line:** no clean survivor in logistics and trade. Candidates 1–5 all hit at least one K criterion, and most hit several. Candidate 6 is kept as UNCERTAIN only because competitor research for it is incomplete. It is not a recommendation.

---

## 2. Per-candidate analysis

### C1. Shipment document packet consistency check (freight forwarder / SME exporter)

**Pain evidence**
- Customs officials use the packing list to check the freight against the commercial invoice and B/L, so the quantities and descriptions must agree ([Shipping Solutions](https://shippingsolutionssoftware.com/blog/bill-of-lading-vs-packing-list), [Maersk](https://www.maersk.com/logistics-explained/shipping-documentation/2023/08/27/important-shipping-documents)).
- Missing or inaccurate documents hold up cargo at port and burn free days, which leads to demurrage ([GoFreight](https://gofreight.com/blog/freights-snap/detention-and-demurrage-charges.html), [NexDriver](https://www.nexdriver.com/nexpertise/import-export-document-errors)).
- The pain is real and frequent for forwarders, since it comes up on every shipment.

**Economic transaction**
- Demurrage is about $75–300 per container per day ([FreightRight](https://www.freightright.com/kb/demurrage) via search summary; figure UNVERIFIED on the page itself).
- Exporters pay forwarders $50–125 per shipment to file export data ([Shipping Solutions](https://shippingsolutionssoftware.com/blog/export-documentation-software), via search summary).
- Forwarders employ document and ops staff for this work. No specific salary data was collected (UNVERIFIED).

**Competitors**

| Name | Price | Self-serve? | Covers exact job? |
|---|---|---|---|
| TradingDocs.AI | Free tier (100 page credits). Paid "from $299/mo" ([site](https://tradingdocs.ai/)) | Yes | Yes. Cross-document consistency validation of CI, B/L and CoO |
| Tier2 Systems (BL/Invoice agents) | Not shown ([blog](https://tier2systems.com/en/blog/shipping-document-discrepancies/)) | Demo | Yes. Extracts CI/PL/B/L and "surfaces only what doesn't match" |
| Wove | Not shown ([site](https://wove.com/document-extraction)) | Demo | Yes. Cross-document validation; syncs to CargoWise/Magaya |
| Magaya Broker AI Assistant | Bundled with Magaya ([Magaya](https://www.magaya.com/how-customs-brokers-can-use-ai-without-compromising-compliance/)) | No (platform) | Yes. Flags missing fields and inconsistencies in CI/PL/entry data |
| iCustoms, TurboLens, Super.ai, Docsumo, Veryfi | Various, mostly not shown ([iCustoms](https://www.icustoms.ai/blogs/ai-document-processing-trade-invoices-waybills-packing-lists/), [TurboLens](https://www.turbolens.io/blog/2026-02-06-automating-bills-of-lading-and-shipping-documentation-with-ai)) | Mixed | Partly or fully |
| IncoDocs (prevention: one dataset → all documents) | $0 / $27 / $62 / $167 per month ([pricing](https://incodocs.com/pricing)) | Yes | Removes the problem for documents the exporter creates |
| Ovrseas (enter once, sync across documents) | 14-day trial; price not shown ([ovrseas](https://ovrseas.io/blog/lc-document-rejection-why-most-fail-first-try)) | Yes | Same prevention approach |

**K-check**
- K1 hit (partial): a free self-serve cross-check exists, and self-serve document generators remove the root cause for $27/mo.
- K2 hit: forwarders would use the AI features in CargoWise or Magaya. Exporters would switch to IncoDocs.
- K3 hit: the only possible angle is "cheaper/simpler AI checker".
- K4 clear.
- K5 clear.
- K6 partly clear (forwarder buyers are often sold to via demos).
- K7 clear for a standalone upload tool.
- K8 hit (Magaya already absorbed it).
- K9 hit.
- K10 borderline.
- K11 clear.

**Economics:** a forwarder could plausibly protect €300+/month through avoided holds. But the incumbents already give them this.

**Verdict: KILL.**

### C2. Letter-of-credit presentation pre-check (SME exporter)

**Pain evidence**
- 60–75% of first presentations are refused, and the rate has not improved since UCP 600 took effect in 2007 ([tradefinance.training](https://www.tradefinance.training/blog/articles/discrepancy-rates-under-ucp-600/), [doccredit.world](https://www.doccredit.world/discrepancy-rates-under-ucp-600/)).
- A 2025 study of Bangladeshi banks catalogues the common discrepancies ([ResearchGate](https://www.researchgate.net/publication/395705058_COMMON_DISCREPANCIES_IN_LETTER_OF_CREDIT_EXPERIENCE_FROM_SELECTED_BANKS_IN_BANGLADESH)).

**Economic transaction**
- Published bank discrepancy fees, per the search summary of bank tariffs: Crédit Agricole CIB USD 80 per set ([tariff](https://www.ca-cib.com/sites/default/files/2021-12/Tariff%20EN%2020211221.pdf)), Standard Chartered USD 120 ([Scribd](https://www.scribd.com/document/648179409/STANDARD-CHARTERED-Tarrifs-and-fees)), Federal Bank USD 100 ([Federal Bank](https://www.federal.bank.in/documents/d/guest/forex-and-trade-service-charges-with-effect-from-07-08-2026)).
- Ovrseas cites $50–250 per presentation ([ovrseas](https://ovrseas.io/blog/lc-document-rejection-why-most-fail-first-try)).
- Outsourced LC presentation service (LC Expedite) starts at about £125 per presentation ([Global Treasurer, 2010](https://www.theglobaltreasurer.com/2010/09/21/outsourcing-the-letters-of-credit-function/)). UK firm Exporter Services sells LC support, price on request ([site](https://www.exporter-services.co.uk/services/letters-of-credit/)).
- Payment delay is the larger cost but was not quantified (UNVERIFIED).

**Competitors**

| Name | Price | Self-serve? | Exact job? |
|---|---|---|---|
| TradingDocs.AI free LC checker | Free (100 page credits, no card). Paid from $299/mo ([site](https://tradingdocs.ai/)) | Yes | Yes. LC + documents vs UCP 600/ISBP 821, discrepancy report |
| SmartLC | 30-day free trial, no card; paid price not visible ([site](https://smartlc.ai/)) | Trial + demo | Yes. LC terms, UCP 600, 47A conditions, cross-document checks |
| Loamist | Not shown; enterprise, SOC 2 ([site](https://www.loamist.com/)) | No | Yes |
| V7 Go trade-finance agent | Not shown ([V7](https://www.v7labs.com/agents/ai-agent-for-trade-finance-officers)) | Partly | Yes |
| Open-source checker | Free ([GitHub](https://github.com/portable-genai/trade-finance-checker)) | Dev only | Yes |
| Bank checking and outsourced agents | £125+ per presentation (above) | No | Yes (human) |

**K-check**
- K1 hit (a free self-serve tool exists).
- K3 hit.
- K5 hit: most SME exporters use LCs occasionally rather than weekly, and open account dominates. This is UNVERIFIED for any specific share.
- K10 hit (would need many low-frequency customers).
- K2, K4, K6–K9 and K11 are not decisive.

**Economics:** avoided fees of about $100 per presentation, times a few presentations a month, comes to well under €300/month unless the delay cost is counted.

**Verdict: KILL.**

### C3. Trucking billing packet readiness before factoring or invoicing

**Pain evidence**
- Missing POD is the #1 rejection reason. Missing rate confirmations, wrong load numbers and unreadable paperwork follow ([trucking-receivables.com](https://trucking-receivables.com/prevent-invoice-rejections-trucking)).
- BasicBlock rejects loads for "missing paperwork, incorrect BOLs, or unverified load details" ([BasicBlock FAQ](https://basicblock.io/faq/)).

**Economic transaction**
- Datatruck: $10–20 labour per rejection plus 1–5 days of cash delay. Its example 20% rejection rate on 100 invoices a day equals 50–100 hours a week ([Datatruck](https://www.datatruck.io/blog/automated-document-processing-invoice-rejection); vendor claim).
- Average small-carrier factoring rate is about 2.8% per invoice ([Dashdoc](https://www.dashdoc.com/en-US/blog/freight-invoice-factoring-vs-tms), via search summary).

**Competitors**

| Name | Price | Self-serve? | Exact job? |
|---|---|---|---|
| Factor's own review (BasicBlock, RTS, OTR) | Included in the factoring fee ([BasicBlock](https://basicblock.io/faq/)) | Yes | Yes, done after submission within about 30 min |
| OTR Solutions app | Free with factoring; "AI-powered document scanning" ([TruckingWay](https://www.truckingway.com/otr-solutions-factoring-review/), [OTR](https://otrsolutions.com/blog/otr-capital-updated-mobile-app)) | Yes | Largely |
| RTS Pro app | Free with factoring ([App Store](https://apps.apple.com/us/app/rts-pro/id705434007)) | Yes | Largely |
| TruckingOffice | $20/mo for 1–2 trucks ([Software Finder](https://softwarefinder.com/fleet-management-software/truckingoffice), via search summary) | Yes | Packet assembly |
| Vektor TMS | About $25–30 per truck per month; RTS integration ([Datatruck comparison](https://www.datatruck.io/blog/vektor-tms-alternatives-compared-for-carriers-in-2026), [Vektor](https://www.vektortms.com/integrations/rts-factoring)) | Yes | Packet + submission |
| Datatruck | Not shown; automated PO, address, page and signature checks ([Datatruck](https://www.datatruck.io/blog/automated-document-processing-invoice-rejection)) | Yes | Yes |
| Fintruck, OverTheRoad.ai | Trial; price not shown ([Fintruck](https://www.fintruck.io/blog/best-invoicing-software-for-trucking-that-factor-loads), [OverTheRoad.ai](https://overtheroad.ai/guides/trucking-invoice-template)) | Yes | Packet attach + tracking |

**K-check**
- K1 hit (free or $20/mo).
- K2 hit ("the factor checks it").
- K3 hit.
- K8 hit (factors are adding AI scanning).
- K9 hit.
- K10 hit: owner-operators pay about $20/mo for a whole TMS, so €50–200 for a checker is implausible.

**Verdict: KILL.**

### C4. ISF 10+2 / entry data completeness pre-filing

**Pain evidence**
- Liquidated damages are up to $5,000 per late or inaccurate ISF, and the ISF is due 24 hours before vessel loading ([Abady Law](https://www.customsesq.com/importer-security-filing-isf-penalty/), [Platton](https://www.platton.ai/insights/customs/isf-filing-penalty/), [CargoEZ](https://cargoez.com/blog/isf-filing-penalty)).

**Economic transaction**
- The penalty exposure is real.
- The job itself is sold cheaply as a service: EZ-ISF charges $50 filing + $75 bond ([EZ-ISF](https://www.ezisfusa.com/isf-filing-fee)). RocketISF charges $50 per its page ([RocketISF](https://www.rocketisf.com/)); a search snippet showed $25.
- The typical range is $30–150 per filing ([FreightAmigo](https://www.freightamigo.com/en/blog/logistics/importer-security-filing-isf-everything-you-need-to-know/), via search summary).
- Brokers file through per-transaction ABI software such as CustomsCity ([CustomsCity](https://customscity.com/isf-importer-security-filing-102-pricing/)).

**K-check**
- K1 hit: done-for-you filing costs less than a month of the product.
- K2 hit.
- K8 and K9 hit: filing software already enforces the required elements.
- K11 partial (ACE / ABI certification to file).
- K5: per importer, ISF volume is often low.

**Verdict: KILL.**

### C5. Freight-broker carrier onboarding packet (control)

- The category is served by MyCarrierPackets / MyCarrierPortal ("Onboard. Monitor. Protect.", demo-led) ([site](https://mycarrierpackets.com/)), plus RMIS and Highway.
- Prices were not retrieved. **UNVERIFIED**, because the search budget was exhausted.

**K-check:** K1, K2 and K9 hit by definition of the control case.

**Verdict: KILL**, confirming the control.

### C6 (added). SME shipper forwarder freight-invoice check before approving payment

**Pain and economics**
- Freehand claims 80% of freight invoices have a discrepancy, overcharges average 8–10%, and 1.5–2.5% of forwarder spend is recoverable ([Freehand](https://www.freehand.ai/articles/freight-forwarder-invoices); vendor claim, treat as upper bound).
- Loamist cites 3–8% of freight spend lost to billing errors ([Loamist](https://www.loamist.com/)).
- An SME with €20k/month freight spend at 1.5% recoverable would protect about €300/month. That is on the threshold.

**Competitors**
- Freehand is enterprise and demo-led, with no public price.
- Loamist does freight-fee monitoring, also enterprise.
- The freight-audit industry is long-established (names beyond these UNVERIFIED this session).
- **Adversarial search for self-serve SME freight-invoice audit was not performed** because the search budget ran out.

**K-check**
- K3 at risk.
- K7 at risk: the user must upload quotes or rate sheets for comparison.
- K2 at risk (the user might just dispute the invoice with the forwarder directly).
- K4 clear (SME finance/logistics manager).
- K6 unclear.

**Verdict: UNCERTAIN, leaning KILL.**

---

## 3. What Stage D must verify (C6 only; all others dead)

1. Run the adversarial competitor search: "freight invoice audit small business self-serve", "forwarder invoice checker", "freight audit software pricing SMB". Also check whether Freightos, Flexport and similar platforms, or the AP tools SMEs already use, include quote-vs-invoice matching. If a self-serve tool under about $100/mo exists, **KILL**.
2. Find independent (non-vendor) evidence of SME forwarder-invoice error rates, and of whether SMEs actually recover disputed amounts.
3. Check the input: do SMEs receive the forwarder quote and invoice as PDFs by email, so the MVP needs zero integrations?
4. Check frequency: are invoices received weekly? Is the monthly freight spend high enough (€15k+) for €300+/month in protected value?

**The uncomfortable question, so far:**
- **Who pays today?** Mid and large shippers pay freight-audit firms (Freehand and others), probably on contingency or SaaS terms (UNVERIFIED). SMEs mostly pay with staff time, or silently absorb overcharges (UNVERIFIED).
- **What do they pay?** Unknown. No public price was found.
- **Why wouldn't they use the existing product?** Plausibly because the enterprise tools are demo-led and sized for large spend. But that is exactly the pattern where a cheap self-serve tool may already exist and simply was not found. **Not answered. Do not advance without step 1.**

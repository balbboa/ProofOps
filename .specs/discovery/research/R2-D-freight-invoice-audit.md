# R2 Stage D: C6 freight-invoice pre-payment check for small shippers

> Date: 2026-09-23. Stage D kill-or-confirm deep dive on the last uncertain candidate from R2-B.

## Verdict: **KILL** (moderate confidence)

**Decisive reason:** the candidate splits into two slices, and each one dies on a different criterion.

**Slice A: parcel and US domestic LTL/TL invoices.** The K1 kill rule is triggered.
- Lojistic offers a **free, self-serve** account with "ongoing carrier invoice audit … All modes supported" ([lojistic.com/pricing](https://www.lojistic.com/pricing)).
- Its paid tiers are 29% contingency, or **$99/mo + 19%** of refunds.
- 71lbs and Refund Retriever are self-serve on contingency. Refund Retriever also covers LTL/TL through Freight Cowboy.

**Slice B: SME importers checking forwarder (ocean/air) invoices against the quote.** No confirmed cheap self-serve tool was found, but the slice fails the economics and differentiation tests.
- **K5/K10 (economics).** Sources written by auditors and accountants, not vendors, say that below about **$500K/yr freight spend** a manual checklist is "genuinely the right call" ([GingerControl](https://gingercontrol.com/blog/freight-invoice-audit-guide)). Audit software is only justified from "the low six figures of annual spend and up" ([beancount.io](https://beancount.io/blog/2026/09/21/freight-invoice-audit-recover-overcharges-duplicate-charges-guide)). The shippers small enough to buy self-serve at €30–200/mo are exactly the ones told not to buy.
- **K6.** The shippers with real recoverable value (above $1M spend) are served by sales-led or contingency firms: Eller, Ocean Audit, Freehand, OpenEnvoy, Senvo.
- **K3.** A funded AI startup, **CostClaw**, targets exactly this job for SME importers ($1M–$20M freight spend). It does quote normalisation, a pre-payment audit and dispute drafting, with input from email or shared folders ([costclaw.ai](https://costclaw.ai/)). At the low end, importers are already told to paste quotes into a general AI tool ([All-Forward](https://www.all-forward.com/Blogs/AI-Import-Export)). A solo entrant's only differentiation would be "cheaper, self-serve, AI". That is K3 by definition.

**Why confidence is only moderate:** the WebSearch quota was exhausted before this dive started. See "Search limitations" below. Two things were not verified: (a) whether Lojistic can ingest forwarder PDF invoices and check them against ad-hoc quotes; (b) whether a small self-serve forwarder-invoice checker exists outside the results I could reach. Neither would revive the candidate, because the K5/K3 reasoning holds either way.

---

## Search limitations (read first)

- **The WebSearch tool quota was exhausted (200/200) for this session** before this Stage D began. No WebSearch calls succeeded.
- Workarounds were tried through WebFetch:
  - DuckDuckGo returned a CAPTCHA, Bing returned no results, and Mojeek returned 403.
  - **Brave Search worked for 7 queries, then rate-limited (429).**
  - Reddit is blocked for fetching, so community threads are cited from Brave snippets only.
- Every vendor claim below was checked by fetching the vendor's own page, unless marked otherwise.

## Competitor table

| Name | Model / price | Self-serve? | Covers exact job (SME forwarder invoice vs quote, pre-payment)? | Source |
|---|---|---|---|---|
| **Lojistic** | Free account (audit included); 29% contingency; $99/mo + 19%; $389/mo + 9%; $5,959/mo + 0% | Yes ("Create Free Account", no card) | **Partly.** Claims all modes (parcel, LTL, FTL, air, ocean, rail) and audits for "invoice errors, duplicate charges, … invalid charges". Ingestion is carrier-credential connectors or EDI, so forwarder PDF vs quote is **UNVERIFIED**. | [pricing](https://www.lojistic.com/pricing) |
| **71lbs** | Contingency ("we only get paid when you save"), % not disclosed | Yes | No. FedEx/UPS parcel only. | [71lbs.com](https://71lbs.com/) |
| **Refund Retriever** (+ Freight Cowboy) | Contingency, no upfront fees | Yes (sign-up page) | No for forwarders. Parcel, plus LTL/TL through its partner. | [refundretriever.com](https://www.refundretriever.com/), [freightcowboy.com](https://www.freightcowboy.com/) |
| **Intelligent Audit, Catalyst** | 90-day free trial, then price not public | Sign-up, then "our team reaches out" | No. Parcel only (UPS/USPS/DHL/FedEx). | [catalyst](https://www.intelligentaudit.com/catalyst) |
| **CostClaw** | Not disclosed | **No** ("request early access", pilot customers) | **Yes, exactly.** SME importers with $1M–$20M spend, ocean from Asia into US/EU/CA. Quote normalisation, pre-payment audit, dispute emails. Phase-1 input is email or shared folders. | [costclaw.ai](https://costclaw.ai/) |
| **Freehand** | Not public. Guarantee: "find $500K in wasteful spend in 30 days" | No (demo) | Yes, but for enterprises above $1B revenue. "4-way matching across every freight forwarder invoice, ingesting from EDI, PDF, and email". | [freehand.ai](https://www.freehand.ai/), [article](https://www.freehand.ai/articles/freight-forwarder-invoices) |
| **OpenEnvoy** | Quote only | No (demo) | Yes for mid-market and enterprise ("500 or 500,000 shipments a month") | [openenvoy.com](https://www.openenvoy.com/automated-freight-audit-software) |
| **Eller Audit** (ocean) | Contingency; "first audit is free" | No ("Talk with us") | Ocean invoice audit for mid-market and enterprise (examples: $28M ocean spend) | [elleraudit.com](https://www.elleraudit.com/ocean-freight-audit) |
| **Ocean Audit** | Contingency ("a portion of the funds I've recovered") | No (consultation) | Ocean post-audit; Fortune 100 clients | [oceanaudit.com](https://oceanaudit.com/) |
| **Senvo** | Not public | No (demo, 2–4 week onboarding) | 3PLs and high-volume shippers | [senvo.ai](https://www.senvo.ai/) |
| **FreightPOP** | Tier prices shown ($7/$29/$79 labels) but "custom solution pricing requires a quick conversation" | No | Invoice vs "original shipment quotes", for mid-market and enterprise shippers | [pricing](https://www.freightpop.com/pricing) |
| **Transmate** (EU TMS) | Free / €600/yr / €1,010/yr / Enterprise | Yes | Partly. Audit against "agreed-upon rate cards", with scanned-invoice parsing. Which tier includes the audit is **UNVERIFIED**. It is rate-card and TMS-centric, not ad-hoc forwarder quotes. | [pricing](https://www.transmate.eu/pricing/), [solution](https://www.transmate.eu/solutions/freight-invoice-audit/) |
| **Wove** | Not public | No (demo) | AP invoice automation. Segments include "Manufacturers & Importers". | [wove.com](https://www.wove.com/) |
| **Landara** | Free tier | Yes | No. It is Shopify landed-cost/COGS: it ingests forwarder invoices but does not compare them with quotes. | [landara.co](https://landara.co/) |
| General LLMs (ChatGPT etc.) | Free–$20/mo | Yes | A manual substitute: "paste them into an AI tool and ask it to summarize and compare" | [All-Forward](https://www.all-forward.com/Blogs/AI-Import-Export) |
| Freightos / Flexport / Forto portals | n/a | n/a | **UNVERIFIED** whether they reconcile invoices against quotes for shippers. A Reddit title (snippet only) shows a Freightos-marketplace forwarder adding a $1,600 fee on a $2,600 quote, which suggests the marketplace does not fully prevent add-ons. The Forto page shows no invoice-reconciliation feature. | [Reddit via Brave snippet](https://www.reddit.com/r/FulfillmentByAmazon/comments/nh5a7x/my_freight_forwarder_from_freightos_is_now/), [forto.com](https://forto.com/en/) |

## K1–K11 check

| K | Result | Evidence |
|---|---|---|
| K1 cheap self-serve exists | **HIT for parcel/LTL; UNVERIFIED for forwarder slice** | Lojistic free / $99 + 19% "all modes" ([pricing](https://www.lojistic.com/pricing)); 71lbs, Refund Retriever on contingency |
| K2 "use existing system" | At risk | Forwarders allow 30–60 day dispute windows, so the customer's natural move is to email the forwarder ([Tier2](https://tier2systems.com/en/blog/freight-invoice-surprises-importers/)) |
| K3 differentiation = AI + UI | **HIT** | CostClaw, OpenEnvoy and Freehand all sell AI invoice audit; LLM paste is the free substitute |
| K4 payer unclear | Clear | Importer's logistics coordinator or finance |
| K5 infrequent / non-economic | **HIT for the self-serve-sized segment** | Manual is advised below ~$500K/yr ([GingerControl](https://gingercontrol.com/blog/freight-invoice-audit-guide)); software from "low six figures" ([beancount.io](https://beancount.io/blog/2026/09/21/freight-invoice-audit-recover-overcharges-duplicate-charges-guide)) |
| K6 sales-call channel | **HIT for the segment with value** | Every vendor serving shippers above $1M is demo-, consultation- or pilot-led (table) |
| K7 many integrations | Clear | Importers get "a single PDF with 15 to 30 line items" ([Tier2](https://tier2systems.com/en/blog/freight-invoice-surprises-importers/)); CostClaw's phase 1 is email/folders only |
| K8 platform absorbs | Partial | Lojistic already bundles audit free; digital-forwarder behaviour UNVERIFIED |
| K9 feature of incumbent | Partial | Audit is a feature inside TMS/FAP suites (FreightPOP, Transmate, Lojistic) |
| K10 path to €1k MRR | Weak | Only ~5–10 customers at €100–200 are needed, but those customers (≥$0.5–1M spend) are the ones reached by sales and contingency firms |
| K11 regulatory | Clear | No special certification found |

## Economics

- **Recoverable rate, from auditors (not neutral, but not the AI vendors):**
  - 1.5–3% of spend ([Eller](https://www.elleraudit.com/ocean-freight-audit), per Brave snippet of [elleraudit.com/freight-audit](https://www.elleraudit.com/freight-audit)).
  - Ocean Audit averages 3.3% ([oceanaudit.com](https://oceanaudit.com/)).
  - Trax cites 5–7%, and AFS ocean post-audit 4–6% on enterprise spend (both quoted by [Eller](https://www.elleraudit.com/ocean-freight-audit)).
- **Error-rate claims are weak:**
  - Freehand's "80% of invoices contain a discrepancy, overcharges 8–10%" is attributed to *American Shipper* without a link ([Freehand](https://www.freehand.ai/articles/freight-forwarder-invoices)).
  - GingerControl says "the freight-audit stat everyone repeats does not exist". It cites Tompkins' 5–10% of invoices with errors as "an experience-based estimate … not a measured study" ([GingerControl](https://gingercontrol.com/blog/freight-invoice-audit-guide)).
- **Quote vs invoice gap is not the same as recoverable overcharge:**
  - Importers "pay 15 to 25% more than their initial freight quote" ([Tier2](https://tier2systems.com/en/blog/freight-invoice-surprises-importers/), a vendor).
  - Much of that is legitimate charges left out of the quote: THC, demurrage, exams, documentation. The customer cannot recover these, only anticipate them.
- **What people pay today:**
  - Contingency is "commonly in the 20 to 50 percent range" of recoveries ([beancount.io](https://beancount.io/blog/2026/09/21/freight-invoice-audit-recover-overcharges-duplicate-charges-guide)).
  - Senvo illustrates 40% ([senvo.ai blog via Brave snippet](https://www.senvo.ai/blog/freight-audit-payment)).
  - Lojistic takes 29% ([pricing](https://www.lojistic.com/pricing)).
  - Below that, shippers pay with staff time or absorb the loss. No per-invoice fee price was found (UNVERIFIED).
- **Worked example:**
  - An SME with €20k/month (€240k/yr) spend recovers 1.5–3%, about **€300–600/month** gross.
  - An audit firm would take 20–50% of that, which is €60–300/month.
  - That spend level sits below the thresholds where the guides say to buy anything.
- **Frequency: about 3–10 forwarder invoices per month (inference, UNVERIFIED).** Invoices arrive per shipment, and an SME at that spend might run a few containers or LCL loads a month. That is weekly at best, not daily.

## The uncomfortable question

- **Who pays for this exact job today, and what do they pay?** Importers with roughly $1M+ freight spend. They pay contingency firms 20–50% of recoveries, or enterprise AI platforms at undisclosed prices. US parcel and LTL shippers can get it free or at 29% contingency (Lojistic).
- **Why wouldn't they use the existing product?**
  - Shippers with value use the contingency firms or CostClaw-type tools.
  - US parcel and LTL shippers use Lojistic.
  - Small importers without value follow the free advice: a manual checklist, or pasting the documents into ChatGPT.
- **No segment was found that has both enough recoverable money and self-serve buying behaviour.**

## Remaining unknowns (none expected to reverse the verdict)

1. Whether Lojistic's free audit ingests forwarder PDF invoices and ad-hoc quotes, or only carrier EDI and portal data.
2. CostClaw's eventual price and whether it goes self-serve.
3. Whether digital forwarders (Flexport, Freightos, Forto) show quote-vs-invoice variance to shippers.
4. Independent (non-vendor) measured error rates specifically for SME forwarder invoices. None were found.
5. A full adversarial search for small self-serve forwarder-invoice checkers. This was blocked by the search quota.

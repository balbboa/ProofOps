# R1 — Synthesis & Wedge Scoring (Discovery Round 1)

> Date: 2026-09-23. Inputs: `R1-competitors-pricing.md`, `R1-demand-pain.md`, `R1-api-feasibility.md`, `R1-billing-brazil-costs.md`.
> Status: desk research only. **Desk research ≠ proof of willingness to pay.**
> Known gap: Reddit could not be crawled. No keyword-volume data (autocomplete only).

---

## 1. Round 1 verdict

**Status: no GO for implementation.** Discovery goes on only for a cheap, time-boxed validation step.

The brief's #1 risk is **confirmed**. "Reconcile two systems and classify exceptions" already exists as cheap, self-serve products:

| Analogue | Pairs | Price | Overlap with ProofOps |
|---|---|---|---|
| Reconciler | Stripe/PayPal/Square/bank ↔ QBO/Xero | $49–399/mo | Missing, duplicate, incorrect and unrecorded items, plain-language evidence, human confirmation |
| Fastero | Stripe ↔ HubSpot/Salesforce | free tier, then $20+/mo | "Detection, not sync", scheduled digests |
| Truence | Shopify/Stripe/Amazon ↔ bank | $79–449/mo | "Verify sales vs deposits", listed in the Shopify App Store |

Xero and QBO are also absorbing bank-line matching with native AI. The 7-category exception taxonomy is a refinement of existing features, not a new category.

The pain itself is real, at least for one pair: **Shopify → QuickBooks Online** records that go missing or duplicate silently. The Intuit connector forced migration (January 2026) left a burst of 1★ reviews, and one review reports 11% of orders lost over 12 months. Failures are silent and are discovered weeks later.

The unresolved question: **who pays for a separate checker?** The most-affected merchants are price-sensitive, and the natural fix is to switch sync apps. Merchants on paid sync apps already get some reconciliation from their vendor. Bookkeepers are the most plausible payer, but that is a **hypothesis with no direct evidence**.

---

## 2. Wedge scoring

Scale 1–5 (5 = favourable). Scores are judgement calls drawn from R1 evidence, not measurements. "Competition" = 5 means little competition. "Complexity" = 5 means simple.

| Wedge | Pain | WTP | Search / distribution | API feasibility | Competition | Complexity | Total /30 | Hard-constraint issue |
|---|---|---|---|---|---|---|---|---|
| Shopify → QBO (sync auditor) | 4 | 2 | 3 | 2 | 2 | 2 | **15** | Shopify public app: App Store review, protected customer data, Shopify billing, >60-day order approval |
| Stripe → QBO/Xero | 2 | 3 | 3 | 4 | 1 | 3 | 16 | Entry prices $12–19, below the €19 floor. Pain is fee mapping, not record drift. |
| Stripe → own SaaS DB | 4 | 1 | 1 | 3 | 4 | 3 | 16 | **Fails GTM:** developer buyers, DIY with cron/open source, near-zero search demand, production-DB trust ask |
| Payouts → bank deposits | 2 | 2 | 3 | 3 | 1 | 3 | 14 | Native AI (Xero JAX, QBO) plus Reconciler/Truence |
| Shopify → Xero | 2? | 2 | 3 | 2 | 2 | 2 | 13 | Under-researched. Xero Core tier may need certification (10 beta customers). |
| Stripe → HubSpot | 2 | 2 | 2 | 3 | 1 | 3 | 13 | Fastero covers it exactly. HubSpot caps unlisted apps at 25 installs. |
| Zapier/Make/n8n generic | 3 | 1 | 2 | 3 | 2 | 2 | 13 | Not pair-specific; cheap substitutes |
| EU-local stacks (lexoffice/sevdesk/Moneybird) | ? | ? | ? | ? | 4? | ? | — | **Not researched.** Needs a German/Dutch-language sweep. |

**Reading:** no wedge scores above 16/30. The pair with the strongest pain (Shopify → QBO) has the heaviest distribution burden. The easiest pair to build (Stripe → QBO) is the most crowded. Nothing clears the bar for a GO.

---

## 3. Key insight: validate without integrations

The expensive part of every wedge is the **OAuth integration plus platform review**. The unproven part is **willingness to pay**. These can be separated.

**A free CSV reconciliation check** ("Upload your Shopify order export and QuickBooks sales export and see which orders are missing") would:

- need no Shopify app review, Intuit questionnaire or OAuth;
- be able to run **entirely in the browser**, so no business data is stored (brief §19; no customer-data-handling exposure);
- serve as the SEO page and lead magnet the brief already calls for (§7, §24);
- test the real hypotheses: do people come, do they find discrepancies, do they ask for monitoring, will they pay or join a waitlist;
- cost about 1–2 weekends plus about €0–8/month (static hosting or a small VPS).

It also tests the bookkeeper hypothesis cheaply: "check a client file in 2 minutes" is a natural bookkeeper workflow.

Weakness: CSV exports are manual, which is exactly what monitoring removes. The tool validates the pain and the demand, not the recurring subscription.

---

## 4. Supporting decisions from R1 (provisional)

| Area | Finding | Provisional recommendation |
|---|---|---|
| Billing | Stripe Managed Payments, Polar and Lemon Squeezy don't serve Brazil well. Stripe Brazil direct means about 9% fees plus self-filed foreign VAT and sales tax. | **Paddle** (5% + $0.50, accepts individuals, MoR); **Creem** as the alternative. Confirm payout fees. |
| Entity | MEI is not allowed for software. ME/Simples Anexo III, about 3% effective on export revenue (unverified). An accountant costs about €31–42/month, which exceeds the budget pre-revenue. | Start as **pessoa física + carnê-leão**, and open an ME once revenue is steady. **Confirm with a contador.** |
| Infra | Hetzner VPS + Docker/Coolify + Postgres + pg-boss costs about €8/month at 0–20 customers. Vercel Hobby forbids commercial use. | Hetzner VPS (if/when a GO). The CSV-check validation can run on static hosting. |
| Matching model | A2X-style tools post one summary journal per payout, not per order. | The reconciliation model must support **payout-level ↔ deposit/journal matching**, not only order ↔ transaction. |
| Least privilege | The QBO accounting scope is read/write with no confirmed read-only scope. | Enforce read-only in code; state it clearly in the security posture. |
| Jev / Xero | Xero's terms ban AI/ML training on Xero data. | Jev must not train on customer data; check Jev's terms before use with any Xero data. |

---

## 5. Options for the founder

| Option | What | Cost | Risk |
|---|---|---|---|
| **A. NO-GO now** | Stop. Evidence shows a crowded category with unproven WTP for a separate checker. | 0 | Might miss a real bookkeeper or EU niche |
| **B. Round 2: cheap validation (recommended)** | Build the browser-only CSV check for Shopify ↔ QBO (maybe also Xero), with an SEO page, waitlist and a "monitor automatically" CTA with pricing shown. Post in the Shopify, QuickBooks and bookkeeper communities. Set explicit success thresholds up front and time-box to about 4–6 weeks. | About 2 weekends plus €0–8/month | The Intuit-migration pain window may close. Low traffic may give an inconclusive result. |
| **C. Research the EU-local stack wedge first** | German/Dutch sweep: Shopify/Stripe → lexoffice/sevdesk/Moneybird. | About 1 research round, no build | May find the same crowding |
| **D. Reframe** | Automation-agency "proof-of-health" reporting for Zapier/Make/n8n clients (outcome verification sold to agencies). | Research round | Generic, crowded with small tools |

**Recommendation: B, with C as a parallel research-only task.** B is the smallest step that produces the evidence the brief demands (§27 Hypotheses 1–2) without building the product. Proposed Round 2 success thresholds (to be confirmed):

- ≥ N free checks completed by distinct visitors within the time box;
- ≥ X% of completed checks surface at least one discrepancy;
- ≥ Y waitlist/pre-order signups at a shown price (€29–49/month), with a bookkeeper segment tracked separately.

Proposed N, X and Y are left for the founder; see `00-DISCOVERY-LOG.md` UD-008.

Note: Option B is a **validation artifact**, not the MVP. It would get a mini-spec and a mini planning gate. It does not trigger the full Planning Gate.

---

## 6. Open questions carried forward

1. Traction of Reconciler, Truence and Fastero (Similarweb, G2, Product Hunt, founder posts): is anyone winning here?
2. Do bookkeepers managing 10+ Shopify clients pay per client, self-serve, for a watchdog?
3. Do merchants shown a discrepancy report keep monitoring, or switch sync apps?
4. Real keyword volumes (a free trial of a keyword tool, or Google Search Console after launching the check page).
5. Manual Reddit sweep (r/Bookkeeping, r/shopify, r/QuickBooks), which the agent couldn't access.
6. Shopify ↔ Xero and the EU-local stacks: same review/forum sweep as for QBO.
7. Paddle payout fees for Brazil; Creem payout-fee contradiction.
8. QBO read-only scope existence; Stripe App fees/unlisted distribution; Xero Core certification requirement.

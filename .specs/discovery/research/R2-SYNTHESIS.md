# R2 — Synthesis: "Pre-flight / Readiness Gate" Opportunity Search

> Date: 2026-09-23. Method: `../R2-CRITERIA.md`. Inputs: `R2-B-logistics.md`, `R2-B-construction.md`, `R2-B-insurance-finance-property.md`, `R2-B-manufacturing-compliance.md`, `R2-B-services-other.md`, `R2-D-freight-invoice-audit.md`.

## 1. Verdict

**NO-GO. 0 of ~36 candidates survived.** No workflow met all of these at once: a frequent check, a clear payer, an existing economic transaction, and no cheap self-serve tool or incumbent that already covers it.

**The direction itself ("a narrow self-serve pre-flight gate for a B2B document packet") is not a viable wedge in 2026 as framed.** Every named packet with money at stake already has an AI completeness checker (usually self-serve, often $0–50/month or $8–80 per check), or a platform that validates at entry.

## 2. Results by segment

| Segment | Candidates | Survived | Typical kill |
|---|---|---|---|
| Logistics & trade | 6 | 0 | Built into forwarding software/TMS/factoring apps (K2/K8/K9). Free AI letter-of-credit checker (K1). $50 done-for-you ISF filing. |
| Construction | 6 | 0 | PayAppPro $7.99/pay app with AI checks. LCPtracker free. Deviation Check $35. GC/agency portals validate at entry. |
| Insurance / finance / property | 7 | 0 | AgencyAssist $49/mo. ListedKit $14.99/intake. RentCheck $1/unit. Loan origination systems own mortgage conditions. GLBA/SSN burden (K11). |
| Manufacturing / compliance | ~9 | 0 | SmartCert free / $30+ for mill test reports. CBAM, FSVP, PPAP and Amazon packets are infrequent (K5). EUDR not yet in force. |
| Services / other | 9 | 0 | Justee AI $19/mo (immigration). StanfordTax free/$18/return. Office Ally free (HIPAA control, as expected). Dealertrack funding checklist. |
| Stage D: freight invoice audit | 1 | 0 | Lojistic free self-serve (parcel/LTL, K1). Forwarder-invoice audit only pays off above ~$500k/yr freight spend, where buyers purchase through demos or on contingency (K5/K6). |

## 3. Why it fails: four patterns

1. **Detection is commoditised.** Since 2025, LLM document checking has made "tell me what's missing or inconsistent in this packet" a cheap feature. Vertical AI checkers exist for nearly every named packet. K3 ("differentiation = AI + detection") now kills most detection-only ideas by default.
2. **Where the money is large, customers pay for outcomes, not detection.** Roofing supplement services (8–15% of the increase), freight audit (20–50% of recoveries) and transaction coordinators ($300–500/file) sell labour, negotiation and responsibility. A detector captures little of that spend, and selling outcomes means a services business (conflicts with solo/low-touch).
3. **Where no cheap tool exists, there is a structural reason.** The check is rare (closeout, CBAM, PPAP, Amazon listing), the rule is not in force yet (EUDR), or a platform controls acceptance (Amazon, GC portals, the loan origination system, Dealertrack).
4. **Mandated portals absorb the gate.** When the receiving party runs a portal (Textura, GCPay, PlanetBids, factoring apps), validation happens at entry for free.

## 4. What a surviving wedge would probably need (derived, unvalidated)

All of the following at once:

- documents that **span several parties, with no single platform owning the flow** (no portal to absorb it);
- **public, stable rules** (checkable deterministically, not opaque platform judgement);
- a buyer with **no dominant vertical system**;
- a **weekly/daily** frequency;
- spend today on **labour** (not on outcomes a detector can't deliver).

None of the ~36 candidates met all five.

## 5. Method notes and confidence

- **Kills are high-confidence even though search was limited.** A kill needs one counterexample (a cheap exact competitor), and those were found and cited. A survival would need an exhaustive search, which was not possible.
- Limits:
  - The WebSearch quota (200 calls) was exhausted in every Stage B agent, so later candidates rely on direct fetches and some search snippets.
  - Reddit was unreachable.
  - Several vendor pages returned 403.
  - Some figures come from vendor blogs (flagged in the files).
- **Provisional or unverified kills:** auto dealer contracts in transit (insurance agent), the Brazil export-declaration-vs-invoice angle (not researched), and residential builder draw packets (not assessed).

## 6. Implication for the next step

Top-down brainstorming of "obvious" workflows mostly surfaces problems that others have already productised; that is why they are obvious. If the search continues, the method should change:

- **Bottom-up from existing spend, not from pain.** Start from evidence of repeated paid labour (recurring Upwork/Fiverr gigs, niche job postings for a repetitive task, offshore back-office service menus, per-file outsourcing prices), then check whether software already exists. The economic transaction is proven first by construction.
- **Markets under-served by English-first AI tools.** For example, Brazilian or Portuguese-language B2B bureaucracy, where the founder has a language/context edge. Caveats: pricing power in BRL, a different competitor set (e.g. Brazilian fiscal-document software is itself crowded), and the same kill criteria still apply. **Hypothesis only.**
- **Accept that K1/K3 will kill most detection ideas.** Future candidates should be jobs where software *does the work* (produces the filing/output), not merely checks it.

These are proposals for how to search, not candidate ideas. No GO is implied.

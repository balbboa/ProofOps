# R3 — Synthesis: Bottom-Up Search from Paid Repetitive Labour

> Date: 2026-09-23. Method: `../R3-CRITERIA.md`. Inputs: `R3-marketplaces-global.md`, `R3-outsourcing-jobs.md`, `R3-brazil.md`.

## 1. Verdict

**NO-GO, low confidence. 0 of 59 candidates survived; 1 is weakly UNCERTAIN.**

Unlike R2, this is **not a clean falsification.** The evidence was starved:

- The WebSearch quota (200 calls) was exhausted **before** all three agents started, so no adversarial competitor searches ran.
- Fiverr, Upwork, OnlineJobs.ph, Indeed, ZipRecruiter, Workana/99Freelas prices and most vendor pricing pages were blocked (403/404/429).
- Competitor checks relied on tools already known by name. Paid-labour evidence came mainly from Freelancer.com, PeoplePerHour, published outsourcing price pages and the ASSCON 2026 fee table (Brazil).

**Kills are still reasonably reliable** (each cites a cheap existing tool or a hard structural rule). **The search for survivors was not thorough.**

## 2. Results by segment

| Segment | Harvested | Survived | Uncertain | Typical kill |
|---|---|---|---|---|
| Global freelance marketplaces | 20 | 0 | 0 | Clears at $2–9/hr or $10–60/deliverable, so buyers spend ≤ our price (K10). Cheap tools exist (Matrixify $20, A2X $29, DocuClipper $20, Metricool €16–29). Work happens inside Seller Central/ADP/Tally (K13). |
| Outsourcing menus + job posts | 19 | 0 | 0 | Generatable deliverables already have free or cheap tools (Certificial free, Levelset free, UK CIS add-on £5, DAVO $58, DataFeedWatch $64, ListedKit $15). The remaining human bill is coordination/judgement/liability (K12). Job-posting half not executed. |
| Brazil | 20 | 0 | 1 | Accounting-firm tasks are billed R$50–365 each, below the R$300 floor (K10). Firms already use HubCount, Sittax, Qive, Acessórias, Alterdata, suaCND (R$3.50/CNPJ). SERPRO Integra Contador API gives every incumbent the same access. |

**UNCERTAIN (weak):** Brazil C17, recurring NCM + IBS/CBS product tax-classification upkeep, sold to accounting firms. Risks: the large reform clean-up is one-off (K15), it relies on AI classification (K3), and ERPs and accounting suites may already suggest codes (K8). **Not worth a Stage D until search works again.**

## 3. Structural patterns (R2 + R3 combined)

1. **The pricing squeeze.** If an outsourcer can publish a per-unit price, the deliverable is standard enough that software already covers it cheaply. If they price by team or by quote, the value is judgement/coordination that software can't replace (K12). A solo self-serve SaaS fits in the gap between the two, and that gap is thin.
2. **Standardised work clears cheaply.** Global freelance rates ($2–9/hr) and Brazilian per-obligation fees (R$50–365) cap what the buyer spends at or below a €50–200 subscription.
3. **"Portuguese is under-served" is false for fiscal and accounting work.** Brazil's accounting-automation market is mature, AI-enabled and has shared government API access.
4. **The one recurring anomaly: buyers pay humans even though cheap tools exist.** Examples: real-estate transaction coordinators ($300–700/file) despite ListedKit ($15), Amazon reimbursement managers despite contingency services, and insurance-agency VA teams ($3,449/mo) despite free certificate tools. Buyers are paying for **responsibility being taken off their plate**, not for the document. That is a done-for-you service, and it competes with humans, not with tools. It usually trips K12/K14 (coordination and judgement don't shrink to ≤30 min per customer per month). It is still the only place R3 saw money consistently above the tool price. **Hypothesis only.**

## 4. What R3 does and does not establish

- **Does:** bottom-up search through *published* prices mostly finds work already standardised and tooled. Brazil's fiscal back office is not an open niche.
- **Does not:** it doesn't show that no opportunity exists in paid-labour data. The richest sources (Upwork/Fiverr buyer posts with budgets over $500/month, job postings) were unreadable in this session.

## 5. Decision for the founder

Across R1–R3, about 95 candidates were evaluated and none survived. Desk research is now hitting two ceilings:

1. **Tooling ceiling:** search quota exhausted, and key sources are blocked for automated access.
2. **Method ceiling:** desk research cannot prove willingness to pay; only market contact can.

Options:

| Option | What | Note |
|---|---|---|
| A. Pause and rerun R3 properly | After the quota resets: Upwork/Fiverr buyer-side posts with budgets over $500/mo, job postings, plus Stage D on C17 | Marketplace 403s are anti-bot measures, not quota-related, and may persist. Manual browsing by the founder (about 2–3 h) would be more reliable than agents for these sites. |
| B. Relax one constraint deliberately | Most evidence points to **async contact with early customers** (declined for R3) or to **done-for-you service with a human share above 10%** | Per the founder's own rule: if R3 fails, relax one or two constraints deliberately rather than keep searching for an exception. |
| C. Stop | Accept that the combined constraints are unlikely to yield a solo SaaS reaching ~€1k MRR in the areas searched | A legitimate outcome of a Planning Gate |

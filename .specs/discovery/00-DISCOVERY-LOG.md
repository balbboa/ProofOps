# ProofOps — Discovery Log

> Persistent record of Discovery rounds. Source of truth for decisions made before REQUIREMENTS.md exists.
> Product brief: see conversation brief (to be copied into `.specs/discovery/PRODUCT-BRIEF.md`).
> Process: Master Prompt — Autonomous Spec-Driven Development Factory.

Current phase: **DISCOVERY — Round 6 (validation of one candidate pending)**
Planning Gate target: **GO / NO-GO decision only. No implementation before a GO.**

---

## Round 1 — Product & constraints (2026-09-23)

| # | Topic | Decision | Status |
|---|-------|----------|--------|
| Q1 | Jev / Treg | Both are third-party APIs and optional. ProofOps must function correctly without either. Ambiguous matching: deterministic first → manual review queue; Jev (if available) is an extra signal only; Jev failure/timeout → manual review; "AI unavailable" never means "records match". | DECIDED |
| Q2 | Evidence | Desk research first. Real-world validation (landing-page smoke test, community posts, waitlist, free check, async conversations) only if Round 1 finds a promising wedge. **Desk research ≠ proof of willingness to pay.** | DECIDED |
| Q3 | Integration pair | No assumed founder edge or audience. Select pair objectively: pain × willingness to pay × search/distribution × API feasibility × low competition × low implementation complexity. Research broader than initial candidates. Chosen pair must be developable/testable with sandbox data only. | DECIDED (method) |
| Q4 | Founder constraints | Solo developer, side project, low-touch/self-service, no sales calls, minimal customer interaction, low ops burden, ~€35/month budget, goal ~€1k MRR, smallest possible MVP. | PARTIAL |
| Q5 | Billing | Compare Stripe vs merchant-of-record (Paddle, Lemon Squeezy, others). Founder is based in Brazil: research Brazilian tax/entity implications, provider support, payouts, VAT/sales tax. Not finalized in Round 1. | RESEARCH |
| Q6 | Process end point | Planning up to the Planning Gate only (GO / NO-GO). Implementation only after an explicit GO. | DECIDED |

---

## UNRESOLVED_DECISIONS

| ID | Decision | Why it matters | Blocks |
|----|----------|----------------|--------|
| UD-001 | Hours per week available | Sizes MVP scope and timeline | Planning Gate |
| UD-002 | MVP deadline (4 / 6 / 8 / 12 weeks) | Sizes MVP scope | Planning Gate |
| UD-003 | Initial integration pair | Drives data model, OAuth, GTM, SEO | Requirements |
| UD-004 | Billing provider (Stripe vs MoR) | Billing spec, legal/tax setup | Requirements |
| UD-005 | Jev/Treg docs (cost, latency, privacy, limits) | Feasibility of Jev signal | Architecture (non-blocking for MVP core) |
| UD-006 | Jev confidence thresholds | Business rule for auto-match vs review | Requirements (if Jev in MVP) |
| UD-007 | Round 1 outcome: A (NO-GO) / B (CSV validation) / C (EU research) / D (reframe) — see `research/R1-SYNTHESIS.md` §5 | Determines next phase | Everything |
| UD-008 | Round 2 success thresholds N / X / Y (if option B) | Pre-commits to an objective GO/NO-GO | Round 2 |

## Round 1 result (2026-09-23)

All four research files done. Synthesis: `research/R1-SYNTHESIS.md`.
Verdict: **NO GO for implementation.** Category crowded (Reconciler, Fastero, Truence analogues); pain real for Shopify→QBO; willingness to pay for a separate checker unproven. Recommended next step: option B (browser-only CSV check as validation) + option C research in parallel. Awaiting founder decision UD-007.
**Founder decision (2026-09-23): ProofOps two-system reconciliation = NO-GO, not to be revived.** New direction: "pre-flight / readiness gate" opportunity search under hard kill criteria — see `R2-CRITERIA.md`. Output: `research/R2-*.md`.
**Round 2 result (2026-09-23): NO-GO. 0/~36 pre-flight/readiness-gate candidates survived** (see `research/R2-SYNTHESIS.md`). Direction not viable as framed: document detection commoditised by AI checkers; large-money jobs pay for outcomes, not detection. Next step (founder decision UD-009): stop, or rerun the search bottom-up from evidence of repeated paid labour.
Founder reading of R2 (2026-09-23): R2 falsified a search heuristic (checker/gate SaaS), not the business goal. Proposed R3: bottom-up from money already paid to humans/outsourcers for repetitive work whose deliverable software could generate. Candidate constraint relaxations under consideration (not yet approved): async/occasional human contact for first 0–5 customers; software-90% + human-10% transitional service; ≤15 min per-customer setup. Pending: UD-010 (approve R3 + which relaxations).
R3 decisions (2026-09-23): approved = software 90% + human 10% (exit ≤30 min/customer/month @20 customers), ≤15 min setup, Brazil/PT market. NOT approved = async customer contact. Criteria: `R3-CRITERIA.md`.
**Round 3 result (2026-09-23): NO-GO, low confidence. 0/59 survived, 1 weak UNCERTAIN (Brazil NCM/IBS-CBS classification upkeep for accounting firms).** Evidence starved: search quota exhausted, marketplaces/job boards blocked. See `research/R3-SYNTHESIS.md`. Pending UD-011: A rerun R3 properly / B relax a constraint (async contact or done-for-you share) / C stop.
**Founder decision (2026-09-23): A + B.** Rerun paid-labour search properly (R4) with done-for-you services allowed (human share >10%). Service capacity: ~10 h/week (≈43 h/month) — resolves UD-001 for service work. Criteria: `R4-CRITERIA.md`; manual sweep template: `R4-MANUAL-SWEEP.md`. Blocker: session WebSearch budget exhausted (200/200) → needs `CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION` raised + session restart.
Provisional (not final): billing Paddle (Creem alt); start as pessoa física (confirm with contador); Hetzner VPS if GO.

---

## Constraints (hard)

- No real customer data during development — sandbox/test data only (org data-handling policy + brief §19).
- No sales calls, demos, or founder-led onboarding (brief §25).
- Infra + tooling budget ≈ €35/month until revenue.
- Unable-to-verify must never be reported as verified (brief §21).

---

## Round 1 research workstreams

Outputs in `.specs/discovery/research/`:

| File | Scope |
|------|-------|
| `R1-competitors-pricing.md` | Competitive landscape, pricing, integration coverage, gaps, per candidate pair |
| `R1-demand-pain.md` | Complaints, community discussions, reviews, search-demand signals, manual workflows, willingness-to-pay signals |
| `R1-api-feasibility.md` | API/OAuth/scopes/sandbox/rate limits/app-review requirements/security per candidate system |
| `R1-billing-brazil-costs.md` | Stripe vs MoR from Brazil, Brazilian tax/entity implications, infra cost model within €35/mo |

Synthesis → `R1-SYNTHESIS.md` (candidate wedge scoring + recommendation).

## Round 4 — run log (2026-09-23)

Search budget raised to 800 (`CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION`). Founder manual sweep (`R4-MANUAL-SWEEP.md`) not yet filled; R4 agents run without it, and the sweep merges into the synthesis later.
Workstreams (~150 searches each): `research/R4-A-freelance-buyers.md` (global freelance buyer posts), `R4-B-productised-services.md` (existing productised DFY services), `R4-C-anomalies-jobs.md` (R3 anomalies re-tested + job postings), `R4-D-brazil-dfy.md` (Brazil DFY + C17 re-check). Synthesis → `research/R4-SYNTHESIS.md`.
**Round 4 result (2026-09-24): NO-GO for implementation. 0/99 survived, 8 UNCERTAIN** (see `research/R4-SYNTHESIS.md`). Two recur across segments: DFY certified payroll for small US public-works subs (A+C) and DFY COI tracking for small GCs/PMs (B+C). R3 C17 killed. The leverage test (≥50% cut vs today's provider) is the main kill: incumbents already use the same automation. The money paid to humans despite cheap tools pays for synchronous third-party phone chasing. Cumulative R1–R4: ~194 candidates, 0 survivors. Buyer-side evidence is still missing (marketplaces and Reddit blocked).
Pending **UD-012**: A stop / B smoke-test certified payroll (landing page + ~€100 ads, thresholds fixed first) / C manual sweep first, then A or B (recommended). Also pending if B: confirm async written customer contact; rule on written email to customers' third parties.

## Round 5 — Any niche, proven money (2026-09-24)

Founder decision: niche restriction and moral filter removed (any legal niche, incl. adult, B2C, "useless"). R1–R4 only covered B2B back-office. New method: replicate niches where ≥2 independent solo operators already earn ≥$1k/mo, plus a concrete newcomer distribution gap. Criteria: `R5-CRITERIA.md`. Assumptions kept from earlier rounds (not re-confirmed): solo, no sales calls, ≤5 h/week ops; running cost relaxed to ≤€100/mo (flag). Workstreams: `research/R5-A-verified-revenue.md`, `R5-B-consumer-platforms.md`, `R5-C-adult-stigmatised.md`, `R5-D-boring-content-data.md`.
**Round 5 result (2026-09-24): first survivor, conditional.** Pattern: Brazil-only consumer "life-admin" apps in PT-BR, found via ASO/SEO, paid by in-app subscription (verified earners Parceladinho $2.07k, Enxovaly $1.79k, Convitede $1.24k, Pluma $1.34k MRR; same pattern in DE/FR/BG). The gap is Brazil-only problems, NOT PT translations of global categories (tarot, calorie and Bible apps are already localised; tarot survivor killed by a Play Store scrape of 97 apps). Base rate warning: 17.3% of new subscription apps reach $1k/mo in 2 years, so plan a small portfolio. See `research/R5-SYNTHESIS.md`.
Pending **UD-013**: approve R6 (sub-niche selection: 30–50 Brazil-only problems scored on demand vs weak store incumbents, pick 2–3, one-page specs) or stop.

## Round 6 — Sub-niche selection (2026-09-24)

Founder issued a strict B2B charter (`CHARTER.md`), then changed direction mid-round: **any niche, no criteria, no moral filter, money first**. R6 therefore continued R5's pending step (UD-013). Play Store, App Store and TrustMRR were blocked (403) in this session; only WebSearch worked.
**Round 6 result: 1 candidate for cheap validation. It is a multi-card "meses sin intereses" (MSI) tracker for Mexico,** a copy of the verified Parceladinho model (BR, $2.07k MRR) into a larger instalment market with no dedicated app found. Buen Fin (Nov 2026) is the timing hook. 17 other candidates killed (B2B charter pass + Brazil sub-niches). See `research/R6-SYNTHESIS.md`.
Pending **UD-014**: (a) founder does the 15-min MX store check; (b) approve a ≤€100 smoke test with the thresholds fixed in R6 §2; (c) or stop.

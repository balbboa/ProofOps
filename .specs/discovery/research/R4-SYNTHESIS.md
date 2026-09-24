# R4 — Synthesis: Paid-Labour Search, Done-for-You Allowed

> Date: 2026-09-24. Method: `../R4-CRITERIA.md`. Inputs: `R4-A-freelance-buyers.md`, `R4-B-productised-services.md`, `R4-C-anomalies-jobs.md`, `R4-D-brazil-dfy.md`.
> Founder manual sweep (`../R4-MANUAL-SWEEP.md`): **not yet done**. It isn't reflected here.

## 1. Verdict

**NO-GO for implementation. 0 of 99 candidates survived; 8 are UNCERTAIN (2 of them recur across segments).**

Unlike R3, this round had a working search budget (~307 WebSearch across 4 agents, ~117 WebFetch). Kills are well grounded. The remaining weakness is the same as R3: **no buyer-side evidence.** Upwork, Fiverr, OnlineJobs.ph, Reddit and Indie Hackers stayed blocked, so almost every price is seller-side, and nearly all hours figures are agent estimates.

## 2. Results by segment

| Segment | Candidates | Survive | Uncertain | Typical kill |
|---|---|---|---|---|
| A. Global freelance buyer posts | 28 | 0 | 3 | Visible budgets clear at $3.50–16/h. Where a public fixed per-unit price exists, the productised DFY market already exists. |
| B. Existing productised DFY services | 28 | 0 | 2 | The model is proven ($99 Social, AgentReach, We Edit Podcasts), but DFY prices have fallen to near tool prices and providers already use the same automation, so the leverage test fails. |
| C. R3 anomalies + job postings | 22 | 0 | 4 | TC, insurance-agency service and FBA reimbursement all die. The un-tooled human value is **live phone chasing of third parties** plus fast SLAs. |
| D. Brazil/PT DFY (+ C17 re-check) | 21 | 0 | 2 | Money sits in BPO financeiro, but it needs bank access, WhatsApp SLAs and 30–75-day onboarding. Providers use R$2–3k/mo assistants serving 10–15 clients with Nibo/Omie. C17 is KILLED (ClassTrib R$97 lifetime, Omie IA Fiscal, Bling auto-fill). |

No R3 kill is revived by R4's relaxed rules.

## 3. The UNCERTAIN list, ranked

| Rank | Candidate | Found by | Fits capacity? | Main blockers |
|---|---|---|---|---|
| 1 | **DFY certified payroll (WH-347 / CA DIR eCPR) for small US public-works subcontractors** | A #1 and C #9 (independently) | Yes: ~3–4 h/customer/mo, 4–5 × €200–300 ≈ 14–20 h | No published small-sub DFY price. LCPtracker's "30 min/week" undercuts the value. Buyers may switch to Miter/Payroll4Construction (K2). US-only. Needs E&O insurance. Churn when projects end. Weekly deadlines vs a 10 h/week side project. |
| 2 | **DFY COI tracking for small GCs / property managers** | B #16 and C #8 | Yes: 1–4 h/customer/mo | No evidence small buyers pay a human. Free BCS / $39 tools. Endorsement review is close to the liability line. Needs **written email to third parties** (not yet ruled on); email-only response rate ~60%/30 days. |
| 3 | Provider credentialing maintenance (US small practices) | B #17 | Yes: ~0.5–1 h/provider/mo | Payer follow-up often by phone. No API. Sensitive data (SSN/DEA). Offshore market at $25–60/provider. |
| 4 | GBP / review management (BR/PT) | D10 | Yes: 2–4 h/customer/mo | Seller-side prices only. Commodity. Google's native AI replies. |
| 5 | Prequalification-portal upkeep (ISN/Avetta) | A #2 | Yes | Leverage likely 20–40% (no API). Needs US safety expertise. Phone-first buyers. |
| 6 | Legal e-billing for insurance-defence firms | A #3 | Borderline | No published price. Appeals ≈ negotiation. Trust barrier. |
| 7 | Contratada portal document uploads (BR) | D9 | Unknown | No priced transaction. No API. LGPD health data. |
| 8 | AR-portal invoice upload / pay apps | C #16, #10 | — | No spend evidence. Pay apps only as an add-on to #1. |

## 4. Structural findings (R2 + R3 + R4 combined)

1. **The pricing squeeze has three layers, not two.** In R3 it ran from tools to humans. R4 adds a middle layer: **tools → productised software-leveraged DFY → quote-only managed service / in-house human.** Where a public fixed DFY price exists, it already sits at or below €100–500/mo (MLS input $15/listing, DQ files $30/driver, Intrastat €89, lodging tax $27/property, COI issuance $3–7/cert).
2. **The leverage test, not capacity, is what kills.** Every niche where buyers clearly pay humans already has providers running the same automation (white-label Paige, Nibo Open Finance, BPO Suite, bank feeds). A newcomer can't show a ≥50% cut against *them*. The cut is only plausible where the destination portal accepts a file (XML/CSV/LEDES).
3. **R3 pattern #4 ("pay humans despite cheap tools") is real, but it is paid for synchronous work.** Take apart what the human does all day: the part tools don't cover is live phone chasing of lenders, carriers, agents and clerks, plus 30-minute-to-same-day SLAs. That is exactly what R4 excludes and what a 10 h/week Brazil-based founder can't supply.
4. **The only open gap is a size gap:** enterprise-minimum managed services (~$10k/yr, ~$1,200/mo) above, $12–49 self-serve tools below, nothing in between. Both top candidates (#1, #2) sit here. The unanswerable desk-research question: **is the gap empty because small buyers won't pay €200+ for what a $39 tool plus 30 min/week handles?**
5. **Quote-only incumbents may reflect buyer preference for a phone relationship,** not a missing checkout. No evidence either way.

## 5. What R4 does and does not establish

- **Does:** with a working search budget, the done-for-you relaxation doesn't produce a clean survivor. Across R1–R4, **~194 candidates, 0 survivors.** The failure pattern is consistent and explained (§4), not random.
- **Does not:** it doesn't prove there is no demand at the two recurring UNCERTAINs. That question now **requires market contact.** More desk research will keep returning seller-side evidence.

## 6. Decision for the founder (UD-012)

| Option | What | Cost | Note |
|---|---|---|---|
| **A. Stop** | Accept the Planning Gate NO-GO across R1–R4 | 0 | Legitimate. The constraints (solo, 10 h/week, no calls, self-serve, €35/mo, Brazil-based) are consistently too tight for where the money is. |
| **B. Smoke-test #1 (certified payroll) without building** | Landing page with fixed price + "reserve / join waitlist" checkout intent. Small search-ad budget (e.g. €50–100) on "certified payroll service" / "WH-347 service" / "DIR eCPR help". Pre-committed thresholds decided *before* launch. | ~€100, ~6–10 h | Only candidate found independently by two segments. Requires accepting: US market, E&O insurance if GO, weekly deadlines. The founder must also rule on async written customer contact (R4 assumption). |
| **C. Manual sweep first, then A or B** | Founder does `R4-MANUAL-SWEEP.md` (2–3 h), aimed at the gaps in §5 of each R4 file (Upwork "certified payroll", "COI tracking"; r/Construction, r/PropertyManagement) | 2–3 h | Cheapest way to get buyer-side evidence. Could upgrade #1 or #2, or kill them. |

**Recommendation: C, then decide between A and B.** The manual sweep is cheap and targets exactly the missing evidence. If it finds no buyer paying ≥$200/mo for #1 or #2, choose A. Don't start a smoke test for #1 without first fixing N/X/Y thresholds (as in UD-008).

### Pending founder rulings (needed only if B is chosen)
- **Async written contact with the customer during delivery** is allowed (R4 assumption, unconfirmed).
- **Written email to the customer's third parties** (subs, insurance agents) is allowed. #2 depends on it.

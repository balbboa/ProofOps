# Discovery Charter (canonical, v1 — 2026-09-24)

> Founder-issued requirements. **Supersedes** the per-round criteria files (R2–R5) wherever they conflict.
> Every future round, candidate evaluation and Planning Gate is judged against this file.
> Kill codes (`C-xx`) are used in research files to cite which requirement killed a candidate.

## 1. Business objective
1. Find a solo-developer product that can plausibly reach ~€1,000 MRR. This is a target, not a forecast.
2. Take the smallest credible path. Prefer **few customers at meaningful ARPU** over hundreds or thousands of low payers.
3. There must be a credible **economic** reason to pay. Painful or interesting alone is not enough.

## 2. Founder constraints
Solo developer, alongside a job, limited time. ~€35/month initially. Cheap infra, familiar tech. No team, contractors, agencies or upfront capital.

## 3. Customer / business model
- Self-service SaaS. No sales calls, demos, founder-led onboarding, custom proposals or procurement-heavy sales.
- Minimal communication and support. Customers discover, understand, activate and pay without help.
- Recurring revenue, recurring problem. B2B or prosumer with clear economic value.
- Acquisition via SEO/search intent, integrations/templates, communities, content, referrals, PLG/free trial, other async channels.

## 4. Hard anti-ProofOps requirements (fatal if failed)
| Code | Requirement |
|---|---|
| C-01 | Real problem or complaints alone are never a reason to recommend. |
| C-02 | A **specific payer** is identified before any GO. |
| C-03 | The payer has **existing economic behaviour** around the problem: pays for software, pays employees, outsources, loses revenue, incurs costs, penalties or risk. |
| C-04 | Clear reason to buy ours instead of using/switching to an existing solution. |
| C-05 | Not a cheaper/prettier/AI/more-accurate/more-automated/dashboard version of a solved commodity problem without a structural wedge. |
| C-06 | Generic AI, "AI-powered" and "more exception types" are not differentiation. |
| C-07 | Monitoring an existing system is not enough if the natural action is to replace that system. |
| C-08 | Incumbent can trivially absorb the feature = major negative. |
| C-09 | "Second tool to monitor the first tool" must be explicitly proven vs switching. |
| C-10 | A payer that is only inferred is marked **unvalidated**. |
| C-11 | Several cheap self-service products already doing the same job → normally **kill**. |

## 5. Competition requirements
Research before implementation: direct and adjacent competitors, pricing, free tiers, self-service onboarding, integrations, target customers, positioning, acquisition channels, complaints and gaps, whether the proposed differentiator already exists, and incumbent platform moves. Include SaaS, marketplaces, native platform features, agencies/services, spreadsheets/manual workflows, outsourcing and internal tools.
**No search result ≠ no competitor. Absence of competitors is never evidence of opportunity on its own.**

## 6. Economic validation
Establish the consequence (revenue, cost, labour, delays, rejections, deadlines, bottlenecks, lost opportunities, expensive errors). Quantify value, frequency, number of affected customers, current spend and plausible WTP. Prefer protecting hundreds or thousands of €/month for a fraction of that. **Derive price from value; never pick €19–49 to make the arithmetic work.**

## 7. Product
One narrow, expensive, recurring job. One workflow, one vertical, one major integration or input type. A concrete outcome, not information: `input → processing → decision/action/output`, not `data → dashboard`. Sit at an economically meaningful decision boundary ("Is this ready to proceed?"). Measurable ROI. No features for looking sophisticated. No broad platforms, ecosystems or marketplaces.

## 8. Technical
Feasible for one developer, fast MVP, light infra. No proprietary datasets, expensive AI APIs, high-volume inference, distributed systems, workflow engines, ERP/CRM/accounting rebuilds or data warehouses. Minimal integrations; prefer APIs with sandbox, sane auth, stable docs, predictable pricing and manageable rate limits. Solo-compatible security, minimal customer data, read-only where possible.

## 9. AI
Optional, never the thesis. Deterministic first. AI only with a defined job, a safe fallback, and never as unverified truth in high-consequence flows. Core product works without AI. **Jev**: allowed for bounded classification/decision; not a hard dependency unless Discovery justifies it. **Treg**: never a hard dependency.

## 10. Distribution
A plausible non-sales channel with identified acquisition intent (customers already searching). Investigate search-demand evidence. No cold outreach dependence, personal-reputation dependence or custom explanation per customer.

## 11. Operations
Low support, onboarding and maintenance. No manual fulfilment, manual review of customer data, services disguised as SaaS, per-customer integrations or configuration. Automated after setup; async support.

## 12. Validation
Discovery before implementation, and it may conclude NO-GO. Sunk cost is not a reason. Don't rescue weak ideas with features. No coding while fundamental commercial questions are open. Separate problem / payer / competitive / distribution / technical validation. Desk research starts it but never proves WTP; promising candidates go to real-world validation (landing page, waitlist, community post, free tool, paid pilot, pre-order, transaction).

## 13. Scoring / elimination
Large candidate pool, multiple industries, aggressive elimination. **One fatal failure kills**; no compensation by other scores. Potentially fatal: no clear payer; cheap incumbent; customer would switch incumbent; no distribution; low frequency; weak value; platform absorbs; integration complexity; needs sales calls; needs manual ops. Numerical scores only for prioritisation.

## 14. "Why us?" (every survivor)
Structural answers only: incumbent systems don't handle the workflow; incumbent can't operate at this decision boundary; customer doesn't want to replace the incumbent; works across several systems; too niche for the incumbent; economic event outside the incumbent's scope. **Not**: UI, AI, cheaper, more alerts, analytics, dashboard.

## 15. "Why now?" (every serious candidate)
Regulation, platform/API change, AI-created workflow, rising labour cost, new fragmentation, new APIs, new business model, emerging operational burden. "AI is growing" is not enough.

## 16. MVP (only after passing Discovery)
One customer type, one painful workflow, one outcome, minimum integrations, minimal UI, self-service, measurable value, easy onboarding, low support. No mobile app, SSO, complex RBAC, marketplace, multi-agent, elaborate dashboards, many integrations, autonomous agents or advanced analytics.

## 17. Planning Gate (formal GO / NO-GO, 32 items)
1 Validated problem · 2 Specific payer · 3 ICP · 4 JTBD · 5 Current workflow · 6 Existing workaround · 7 Existing spending/economic behaviour · 8 Competitive landscape · 9 Competitor pricing · 10 Competitive gap · 11 Why customers won't switch to incumbent · 12 Differentiation · 13 Why now · 14 Acquisition channel · 15 Self-service funnel · 16 Pricing hypothesis · 17 Economic ROI · 18 MVP scope · 19 MVP non-goals · 20 Technical feasibility · 21 API feasibility · 22 Security requirements · 23 Operational burden · 24 Support burden · 25 AI necessity · 26 Jev role · 27 Treg role · 28 Real-world validation evidence · 29 Major risks · 30 Kill criteria · 31 Acceptance criteria · 32 Final GO / NO-GO.

## Relationship to earlier rounds
- R1 (ProofOps reconciliation): NO-GO, not revived.
- R4's done-for-you relaxation is **withdrawn** by §11 ("no manual fulfilment, no services disguised as SaaS").
- R5's relaxations (any niche, B2C, €100/mo running cost) are **withdrawn** by §1–§3 (few customers, meaningful ARPU, B2B/prosumer, €35/mo). The R5 survivor is re-judged in R6.

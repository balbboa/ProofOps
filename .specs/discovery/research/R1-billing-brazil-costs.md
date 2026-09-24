# R1 — Billing provider, Brazil tax/entity, infra cost model

Discovery Round 1, desk research. Researched 2026-09-23. Sources were read on that date. Anything I could not confirm from a primary source is marked **UNVERIFIED**.

> **Not legal or tax advice.** Section 3 is desk research to help the founder prepare questions. Confirm every point marked **[CONTADOR]** with a Brazilian contador (and, for the entity decision, possibly a tax lawyer) before acting on it.

---

## 1. Summary and recommendation

1. **Use a Merchant of Record (MoR) you can open from Brazil today. Paddle is first choice and Creem is second.** Both accept Brazil-based sellers and individuals/sole traders. Both collect and remit VAT, GST and US sales tax. Fees are Paddle 5% + $0.50 and Creem 3.9% + $0.40. Dodo Payments is a viable third option (4% + $0.40, plus 1.5% on international cards and 0.5% on subscriptions).
2. **Not available to a Brazil-based seller today:**
   - **Stripe Managed Payments.** Brazil is not an eligible business location.
   - **Polar.sh.** Brazil is not in its Stripe Connect Express payout list.
   - **Lemon Squeezy.** Only PayPal payouts would work, and the product is being folded into Stripe Managed Payments. Poor long-term bet.
3. **Stripe Brazil direct is the worst fit.** Stacked fees (3.99% + R$0.39 + 2% international card + ≥2% FX + 0.7% Billing + 0.5% Tax) come to about 9%. You also have to register and file VAT and sales tax abroad yourself. Brazil accounts accept Visa and Mastercard only.
4. **Entity: MEI is not an option**, because software activities are not allowed MEI occupations. The realistic path is an **ME under Simples Nacional (SLU)**.
   - By the letter of LC 123, "licenciamento ou cessão de direito de uso de programas de computação" is taxed in **Anexo III (6% nominal in faixa 1) without Fator R**. Confirm the CNAE and anexo with your contador **[CONTADOR]**.
   - Export revenue drops the PIS, COFINS and ISS shares. The effective rate is then about **3.05%**. In Anexo V without Fator R it would be about **10.7%**.
5. **The accountant is the largest fixed cost.** Online contadores advertise from **R$195–259/month** (about €31–42). That alone roughly equals the €35 budget. Consider starting as **pessoa física (carnê-leão)** while validating, and open the ME once revenue is repeatable. Check with the contador whether a PF selling SaaS habitually can be treated as a company ("equiparação") **[CONTADOR]**.
6. **Infra: a single Hetzner VPS with Docker/Coolify, Postgres and pg-boss costs about €8–12/month** from 0 to 50 customers. The managed alternatives cost about $15–45/month. **Vercel Hobby is not allowed for a commercial product.** The per-customer marginal cost of hourly reconciliation (5k records/day) is cents. The real limit is **data retention and storage**, not CPU.
7. **Net at €1k MRR** (Paddle or Creem, ME in Anexo III, accountant, Hetzner): about **€820–835/month** before the founder's own income tax on distributions.

---

## 2. Billing provider comparison

FX assumptions for all conversions in this document: **€1 = US$1.15 = R$6.20**. These are placeholders, not live rates. Recompute before deciding.

| Provider | Brazil-based seller? | Individual OK? | MoR? | Headline fees | Payout to Brazil | Tax handled | B2B SaaS subs | KYC / approval | Notes |
|---|---|---|---|---|---|---|---|---|---|
| **Paddle** | **Yes.** Not in the unsupported list [P1] | **Yes.** Business verification is skipped for individuals and sole traders [P5] | Yes | 5% + $0.50 per checkout transaction. Currency conversion and international payments included [P2] | Monthly. Minimum threshold $100 (configurable). Wire (SWIFT), Payoneer, or services like Wise. No Paddle fee for most countries, but a **$15 SWIFT fee may apply** in some countries (whether Brazil is one is UNVERIFIED) [P3] | VAT, GST and US sales tax as MoR [P2] | Yes. Built for SaaS [P2] | Domain review (live HTTPS site, T&Cs naming the seller) plus identity check. Manual review in about 5–7 business days [P5] | Custom pricing for products under $10 [P2]. Mature checkout and customer portal. |
| **Creem** | **Yes.** Brazil is listed, with local bank transfer [C3] | **Yes.** Individual onboarding needs an individual payout account [C2] | Yes | 3.9% + $0.40. No monthly fee [C1] | Payouts on the 1st and 15th. Bank payout fee is **€/$7 or 1%, whichever is higher**. USDC payout 2% [C2]. The pricing page says "0% payout for several payout methods" [C1], which **conflicts** with the docs. UNVERIFIED which applies to Brazil | Says it covers EU, UK, US states and others [C4] | Yes | UNVERIFIED (not researched in depth) | Younger company (founded around 2024). Third-party reviews list surcharges for splits, affiliates and cart recovery [C4]. |
| **Dodo Payments** | **Likely yes.** Eligibility follows the country of the ID document. Brazil is not in the unsupported list [D2] | Likely yes (eligibility is based on the ID document) [D2]. UNVERIFIED | Yes | 4% + $0.40 (US domestic). **+1.5%** international cards/APMs. **+0.5%** subscriptions [D1] | Standard payout free. **USD SWIFT $25**. **$5 fee on payouts under $1,000** [D1]. Local BRL payout rail UNVERIFIED | Claims 190+ countries [D2] | Yes. Digital goods and SaaS only [D3] | UNVERIFIED | Supports Pix for Brazilian buyers [D3]. |
| **Stripe Brazil (direct) + Stripe Tax** | Yes. Stripe BR account [S1] | Yes. PF with CPF, or PJ with CNPJ. **Tax ID and business type cannot be changed after verification** [S1][S3] | **No.** You are the seller | 3.99% + R$0.39 domestic card. **+2%** international card. Currency conversion **from 2%**. Billing **0.7%**. Stripe Tax 0.5% (no-code) or $0.50/tx (API), charged only where you are registered [S2][S4] | BRL only, to a Brazilian bank account in the same CPF/CNPJ [S1] | **Calculation only.** You register, collect and file (UK VAT, EU OSS, US states) [S4] | Yes. One secondary source reports "restrictions on subscription billing for non-Brazilian customers" [S5] (UNVERIFIED) | Standard Stripe KYC | Brazil accounts accept **Visa and Mastercard only** [S6]. Remittances go through authorized FX channels [S6]. |
| **Stripe Managed Payments** | **No.** The eligible business locations are US, CA, most of the EEA plus CH/GB/NO/LI, AU, HK, JP and SG [SM1] | n/a | Yes (Stripe) | Standard Stripe processing **+3.5%** per transaction [SM2] | n/a | Sales tax, VAT and GST in 80+ countries [SM1] | Yes (SaaS tax codes) [SM1] | Eligibility review. Public preview/waitlist in 2026 [LS1][LS3] | Lemon Squeezy says more countries are planned "later in 2026" [LS2]. Watch this. |
| **Lemon Squeezy** | Partly. **No Stripe bank payout for Brazil. PayPal only** [LS4] | Yes | Yes | 5% + $0.50. **+1.5%** international. **+1.5%** PayPal. **+0.5%** subscriptions [LS5] | PayPal: **3% capped at $30** per payout outside the US [LS5] | Yes | Yes | Signup still open. Being migrated toward Stripe Managed Payments [LS2][LS1] | Direction is to converge with SMP [LS1]. **Not recommended** for a new build. |
| **Polar.sh** | **No.** Brazil is missing from the Stripe Connect Express payout list (which does include AR, CL, CO, MX, UY and others) [PO2] | Yes, where Connect Express supports individuals [PO2] | Yes | Starter 5% + $0.50. Pro 3.8% + $0.40 (paid plan). +1.5% non-US cards. Payout $2/month + 0.25% + $0.25 [PO1] | n/a for Brazil | Yes | Yes | n/a | Developer-friendly, but not usable from Brazil. |
| **FastSpring** | UNVERIFIED | UNVERIFIED | Yes | **Not published.** Third parties cite about 5.9% + $0.95, up to 8.9% for low volume [F1] (UNVERIFIED) | Third parties cite a 45-day hold on first payouts [F1] (UNVERIFIED) | Yes | Yes | Sales-led onboarding | Enterprise orientation. Poor fit for €19–99 self-serve. |
| **Gumroad** | Yes. Bank via Stripe or PayPal [G2] (details UNVERIFIED) | Yes | Yes, since 2025-01-01 [G1] | **10% + $0.50** direct sales [G1] | UNVERIFIED | Yes [G1] | Possible, but creator-oriented | Light | Too expensive and not a B2B SaaS checkout. |

**Takeaways**
- Among providers usable from Brazil, **Creem is cheapest on paper, then Paddle, then Dodo**. At €40 average price, the three are within about €15/month of each other at €1k MRR (see section 4). Paddle has the longest track record and clearest documentation, which matters when you have no support staff.
- **Checkout quality** (qualitative, not tested): Paddle, Creem and Dodo all offer hosted and overlay checkouts, localized currencies and a customer portal. Stripe Checkout is the benchmark, but on a Brazil account it accepts only Visa and Mastercard [S6].
- **Re-check Stripe Managed Payments in Q4 2026 and Q1 2027.** If Brazil is added, it becomes a strong option (Stripe Checkout plus MoR, about 3.5% on top of processing) [SM2][LS2].

---

## 3. Brazil tax and entity (research, not advice)

### 3.1 Receiving as pessoa física (PF)
- A Brazilian resident PF who receives income from sources abroad must pay IRPF monthly through **carnê-leão** at the progressive table (7.5% to 27.5%) [T1].
- **Law 15.270/2025** exempts monthly income up to **R$5,000**, with a progressive discount between R$5,000.01 and R$7,350 [T1]. At €1k MRR ≈ R$6,200/month, income would fall in the discount band. The exact tax is not computed here (UNVERIFIED).
- Paddle and Creem both accept individuals [P5][C2], so PF is **operationally possible**.
- **Risks [CONTADOR]:**
  - Habitual, organized commercial activity by a PF may be treated as a company for income tax ("equiparação à pessoa jurídica"). UNVERIFIED how this applies to SaaS licensing.
  - Possible INSS as a contribuinte individual. UNVERIFIED.
  - A Stripe BR account opened with a CPF can never be converted to a CNPJ [S3].

### 3.2 MEI: not allowed
- Programming, software development and licensing are **not permitted MEI occupations**. CNAEs 6201-5/01, 6203-1/00 and 6311-9/00 are not on the MEI list [T2][T3].

### 3.3 ME under Simples Nacional: Anexo III vs V
- **Primary law (LC 123/2006, art. 18):**
  - **§5-B** puts these directly in **Anexo III**: "IV – elaboração de programas de computadores… desde que desenvolvidos em estabelecimento do optante" and "**V – licenciamento ou cessão de direito de uso de programas de computação**".
  - **§5-M**, the Fator R rule that pushes activities into Anexo V when payroll is below 28% of revenue, applies only to §5-B items XVI, XVIII–XXI and to §5-D [T4].
  - **So by the statute, licensing a SaaS product appears to be Anexo III regardless of Fator R.**
- **In practice:**
  - Many accounting blogs treat all "intellectual" tech activities as Fator R dependent [T5], and custom development (6201-5/01) is commonly placed under Fator R (6% vs 15.5%) [T3].
  - Which CNAE best fits SaaS (6203-1/00 licensing of non-customizable software, 6311-9/00 hosting/data processing, or both) and how the municipality and Receita treat it is **[CONTADOR]**.
- **Anexo III table** (RBT12 = gross revenue over the last 12 months) [T5]:

  | RBT12 band | Nominal rate | Deduction |
  |---|---|---|
  | Up to R$180k | 6.00% | – |
  | R$180k–360k | 11.20% | R$9,360 |
  | R$360k–720k | 13.50% | R$17,640 |

- **Anexo V** (for comparison) [T4]: 15.50% up to R$180k, then 18.00% (deduction R$4,500).
- Faixa 1 tax-share breakdowns:
  - **Anexo III** [T6]: IRPJ 4.00%, CSLL 3.50%, COFINS 12.82%, PIS 2.78%, CPP 43.40%, ISS 33.50%.
  - **Anexo V** [T4]: IRPJ 25%, CSLL 15%, COFINS 14.10%, PIS 3.05%, CPP 28.85%, ISS 14%.
- **Pró-labore:** even in Anexo III without Fator R, the partner may need a pró-labore, with 11% INSS on it (minimum-wage basis, value UNVERIFIED) **[CONTADOR]**.

### 3.4 Export of services (ISS, PIS, COFINS relief)
- In Simples, export revenue is reported separately, and the **PIS, COFINS and ISS shares are removed** from the rate [T7][T8]. IRPJ, CSLL and CPP remain [T8].
- **Conditions** [T7][T8]:
  - The buyer is resident or domiciled abroad.
  - There is an **effective inflow of foreign currency (ingresso de divisas)**.
  - For ISS, the service's **result happens abroad**.
- **Solução de Consulta COSIT 73/2025** held that a virtual service provided by a Simples company to a foreign buyer is an export "if the benefit is used abroad", even when the work is done in Brazil [T9]. This is persuasive, but it concerns administrative services, not SaaS.
- **Effective rate (my calculation, faixa 1):**
  - Anexo III: 6% × (1 − 0.1282 − 0.0278 − 0.335) = **3.05%**.
  - Anexo V: 15.5% × (1 − 0.141 − 0.0305 − 0.14) = **10.67%**.
  - **[CONTADOR]**
- **Paperwork:** issue an NFS-e for each export. One source mentions the DU-E/Siscomex process [T8]. UNVERIFIED whether a DU-E is required for services. Keep the MoR agreement, invoice or payout statements, and the FX contract (contrato de câmbio) from an institution authorized by the Central Bank [T10].

### 3.5 How MoR payouts are characterized
- With an MoR, **the MoR (for example Paddle, a UK/Ireland entity) buys or resells the software**. The founder's company has **one foreign customer: the MoR** [T11].
- This works in the founder's favor:
  - one export NFS-e per payout (monthly for Paddle, twice a month for Creem)
  - a foreign payer
  - inflow of foreign currency through a Central Bank–authorized FX channel
- **[CONTADOR] questions:**
  1. Is the taxable base the MoR's gross sale or the net payout the ME receives? This depends on the MoR contract (reseller vs agent).
  2. Does the export treatment hold for MoR sales to **end customers located in Brazil**? Consider excluding Brazil at checkout, or selling to Brazil from the ME directly.
  3. Payoneer or Wise vs a direct SWIFT transfer to a Brazilian bank: is the FX contract/certificate available for each route [T10]?
  4. Does money settled by **Stripe Brasil in BRL** count as ingresso de divisas at all? If not, Stripe BR revenue may be fully taxed domestically. UNVERIFIED.

### 3.6 Accountant (contador) cost
- Online accounting firms for an ME in Simples with no employees [T12]:
  - Contabilizei from **R$195/month** (≈ €31)
  - Agilize Basic **R$259/month** (≈ €42)
  - Typical market range R$189–600 [T12]
- Confirm that the plan covers **export NFS-e and foreign-currency receipts**. Some plans charge extra for this (UNVERIFIED).
- **This alone consumes or exceeds the €35/month budget.** The ME only makes sense once revenue covers it, or it has to be funded out of pocket.

### 3.7 Tax reform (IBS/CBS)
- Exports of goods and services are **immune from IBS and CBS** under LC 214/2025, though interpretive gaps remain for services [T13].
- 2026 is a test year with symbolic rates (CBS 0.9%, IBS 0.1%). Simples companies join the new model in **2027**, and may opt to pay IBS/CBS under the regular regime (hybrid) [T13].
- Implication: an **export-only Simples ME should see little change**, but the rules on proving an export under IBS/CBS are still being settled **[CONTADOR]**.

---

## 4. Net revenue example at €1,000 MRR

**Assumptions**
- 25 customers × €40 average. Prices exclude tax, so the MoR adds VAT/sales tax on top.
- 50% US / 50% non-US cards.
- 25 transactions/month.
- FX as stated in section 2.
- Bank FX spread on receipt **1% (placeholder, UNVERIFIED)**.
- ME in Anexo III with export treatment, 3.05%, applied to the amount received [CONTADOR].
- Accountant R$195 (€31.45).
- Pró-labore INSS 11% of an assumed minimum wage ≈ **€28.80 (UNVERIFIED, may not apply)**.
- Infra Stack A, €9.

| Line (€/month) | **Paddle** | **Creem** | **Dodo** (worst-case payout) | Stripe BR direct (for contrast) |
|---|---|---|---|---|
| Gross MRR | 1,000.00 | 1,000.00 | 1,000.00 | 1,000.00 |
| % fee | −50.00 (5%) | −39.00 (3.9%) | −52.50 (4% + 0.5% subs + 1.5% on half) | −79.00 (3.99% + 2% intl + 2% FX) |
| Fixed per-transaction fee | −10.87 | −8.70 | −8.70 | −1.57 |
| Billing / Tax add-ons | incl. | incl. | incl. | −7.00 Billing (Stripe Tax +€5 where registered) |
| Payout fee | −13.04 ($15 SWIFT, if applied) | −9.52 (1%, min €7) | −21.74 ($25 SWIFT) | 0 (BRL) |
| **Received from provider** | **926.09** | **942.78** | **917.06** | **912.43** |
| Bank FX spread (1%, UNVERIFIED) | −9.26 | −9.43 | −9.17 | incl. in FX fee |
| Simples DAS (3.05% export) | −28.28 | −28.79 | −28.01 | −54.75 if **not** treated as export (6%) [CONTADOR] |
| Accountant | −31.45 | −31.45 | −31.45 | −31.45 |
| INSS on pró-labore (if applicable) | −28.80 | −28.80 | −28.80 | −28.80 |
| Infra (Stack A) | −9.00 | −9.00 | −9.00 | −9.00 |
| **Net to company** | **≈ 819** | **≈ 835** | **≈ 811** | **≈ 788** (plus self-filing of foreign VAT and sales tax, which is **not** priced here) |

**Sensitivity**
- If the ME lands in **Anexo V without Fator R**, subtract about €70 more (10.67% vs 3.05%).
- Operating as **PF** removes the accountant fee and the DAS but adds carnê-leão IRPF. At R$6.2k/month this is inside the 2026 discount band; exact value UNVERIFIED.
- A lower average price (for example €19) increases the weight of the fixed per-transaction fees.

---

## 5. Infra stack options

### 5.1 Workload model
- **Records:** up to 5k records/customer/day, reconciled hourly, so about 210 records/customer/hour. At 50 customers that is about 250k records/day (about 3 records/s on average). CPU is trivial for this. The bottleneck will be the **external APIs' rate limits**, not your compute.
- **Storage** (assuming about 1 KB/record including indexes, an assumption):
  - about 5 MB/customer/day
  - about 150 MB/customer/month if every record is retained
  - at 50 customers, **about 7.5 GB/month of growth**
  - **A retention/rollup policy is the main cost lever.**
- **Queue/scheduler:** use **pg-boss or graphile-worker on the same Postgres**. No Redis needed at this scale, which saves a service.

### 5.2 Unit prices used

| Item | Price | Source |
|---|---|---|
| Hetzner CX23 (2 vCPU shared / 4 GB) | €5.49/month excl. VAT (after the 15 Jun 2026 increase). Primary IPv4 +€0.50/month | [I1][I2] |
| Hetzner CX33 | €8.49/month excl. VAT | [I1] |
| Hetzner automatic backups | 7 daily slots [I3]. Price is 20% of the server price (**UNVERIFIED** after the 2026 changes) | [I3] |
| Vercel Hobby | **Non-commercial only.** "Any method of requesting or processing payment" counts as commercial | [I4] |
| Vercel Pro | $20/month with $20 included usage credit | [I5] |
| Railway Hobby | $5/month incl. $5 usage. $20/vCPU-month, $10/GB-RAM-month, $0.15/GB volume, $0.05/GB egress | [I6] |
| Render | Starter web/worker $7/month. Postgres from $6/month. Free Postgres expires after 30 days [I7]. Workspace fee changed in 2026 (Pro $25/month flat) [I8]. Pricing changed repeatedly in Aug 2026, so **re-verify** | [I7][I8] |
| Fly.io | shared-cpu-1x: 256 MB ≈ $0.67, 512 MB ≈ $1.10, 1 GB ≈ $1.97 per month (base region). Volumes $0.15/GB | [I9] |
| Neon | Free: 0.5 GB/project, 100 CU-h/project. Launch: $0.106/CU-h, $0.35/GB-month, no minimum | [I10] |
| Supabase | Free: 500 MB DB, pauses after 1 week of inactivity, no backups. Pro: $25/month (8 GB disk, $10 compute credit, 7-day daily backups) | [I11] |
| Resend | Free: 3,000/month, **100/day**. Pro: $20/month for 50k | [I12] |
| Postmark | Free: 100/month. Basic: $15/month for 10k | [I13] |
| Amazon SES | $0.10 per 1k (à la carte). New-account credits up to $200 | [I14] |
| Sentry Developer | Free: 5k errors/month, 1 user, 30-day lookback. Team: $26/month (annual) | [I15] |
| Cloudflare R2 (off-site backups) | 10 GB-month free, free egress, then $0.015/GB-month | [I16] |
| AWS KMS | $1/key/month. $0.03 per 10k requests. 20k requests/month free | [I17] |
| Domain | about €1/month amortized (.com at a Cloudflare-style at-cost registrar). **UNVERIFIED exact price** | – |

### 5.3 Stack A: single VPS (recommended for the budget)
Hetzner CX23, running Docker with Coolify (self-hosted, free) or plain docker-compose. Next.js app, worker and Postgres run on the same box. Also in the stack: pg-boss, nightly `pg_dump` to R2, Hetzner backups, Resend free tier, Sentry free tier, Cloudflare DNS.

| €/month | 0 customers | 20 customers | 50 customers |
|---|---|---|---|
| VPS | 5.49 (CX23) | 5.49 | 8.49 (CX33, for headroom and disk) |
| IPv4 | 0.50 | 0.50 | 0.50 |
| Hetzner backups (20%, UNVERIFIED) | 1.10 | 1.10 | 1.70 |
| R2 off-site dumps | 0 | 0 | 0 to about 0.2 |
| Email | 0 (Resend free) | 0 | 0, or about 17 if the 100/day cap bites (Resend Pro) |
| Sentry | 0 | 0 | 0 |
| Domain | ~1 | ~1 | ~1 |
| **Total** | **≈ €8** | **≈ €8** | **≈ €12** (≈ €29 with Resend Pro) |

- **Pros:** cheapest. Matches the Docker hypothesis. No cold starts. Postgres and the queue live together.
- **Cons:** you are the DBA, you handle patching, and there is a single point of failure. CX23 has 40 GB of disk (UNVERIFIED for the current plan), so a retention policy is mandatory.
- Hetzner customers outside the EU are normally not charged EU VAT (UNVERIFIED for Brazil).

### 5.4 Stack B: Railway (managed PaaS, low ops)
Railway Hobby running the web service, a worker service and Railway Postgres, with pg-boss. Email and monitoring as in Stack A.

| $/month (estimate) | 0 | 20 | 50 |
|---|---|---|---|
| Plan (includes $5 usage) | 5 | 5 | 5 |
| Usage above credit (web 0.5 GB + worker 0.5 GB + PG 0.5–1 GB RAM, low CPU, volume) | ~10–15 | ~12–18 | ~18–28 (volume grows with retention) |
| Email, Sentry, domain | ~1 | ~1 | ~1–21 |
| **Total** | **≈ $16–21 (€14–18)** | **≈ $18–24** | **≈ $24–54** |

Usage is **estimated** from Railway's unit rates [I6]. Actual RAM idle usage is UNVERIFIED.

### 5.5 Stack C: Vercel Pro + Neon + separate worker
Vercel Pro hosts Next.js (Hobby is not allowed [I4]). Neon provides Postgres. The worker and cron run on a Fly.io machine or Railway, because long-running hourly reconciliation fits poorly in serverless functions.

| $/month (estimate) | 0 | 20 | 50 |
|---|---|---|---|
| Vercel Pro | 20 | 20 | 20 (+ overage unlikely) |
| Neon | 0 (Free) | ~5–10 (Launch: an hourly job keeps compute waking, storage 3 GB) | ~10–20 (storage 7.5 GB/month growth × $0.35) |
| Worker (Fly 512 MB–1 GB) | ~1–2 | ~2 | ~2–4 |
| Email, Sentry, domain | ~1 | ~1 | ~1–21 |
| **Total** | **≈ $22–23 (€19–20)** | **≈ $28–33** | **≈ $33–65** |

- **Pros:** best Next.js DX, preview deploys, managed DB branching.
- **Cons:** already about 60% of the budget at zero customers. Two or three vendors to manage.

### 5.6 Marginal cost per customer (hourly reconciliation, 5k records/day)
- **Compute:** about 24 short jobs/day. On a VPS it is effectively €0 until the box saturates, which is well beyond 50 customers for this load.
- **Storage:**
  - about 150 MB/month/customer if raw records are kept forever
  - Neon: about **$0.05/customer per retained month**, accumulating
  - Hetzner: it consumes local disk
  - With 30–90 day raw retention plus rollups, this stays under 1 GB per customer.
- **KMS** (if used, with per-customer data keys and hourly decryption): 50 × 24 × 30 = 36k requests/month. That is about 16k above the free tier, so **≈ $0.05/month**, plus $1/month per CMK [I17].
- **Email:** a handful per customer per month. Free tier until the Resend 100/day cap is reached.
- **Bottom line:** **< €0.25/customer/month** at this scale, excluding third-party API costs, which are not researched here.

### 5.7 Secret storage (customer API tokens)
- **Option 1: app-level envelope encryption.**
  - How: one master key (KEK) from an env var or Docker secret, per-tenant data keys (AES-256-GCM, for example with libsodium or node:crypto), key version stored per row.
  - Cost €0. Rotate by re-wrapping the data keys.
  - Risk: the KEK lives on the same VPS as the database.
- **Option 2: AWS KMS as the KEK** (GenerateDataKey/Decrypt with caching). About $1–2/month [I17]. This separates key custody from the database host, which is a better story for B2B security questionnaires.
- **Recommendation:** start with option 1, **designed behind an interface** so KMS can be added later.

---

## 6. Open questions and decisions for the founder

1. **PF first or ME from day one?**
   - PF avoids about €31–42/month in accounting costs while validating.
   - ME gives the export regime and a cleaner story for the MoR contract.
   - Ask the contador about equiparação and INSS risk for PF **[CONTADOR]**.
2. **CNAE and anexo:** 6203-1/00 (licensing) → Anexo III without Fator R per LC 123 §5-B V? Or does the contador insist on Fator R/Anexo V? Is a pró-labore required? **[CONTADOR]**
3. **Taxable base with an MoR:** gross MoR sale or net payout? Is export treatment valid for MoR sales to Brazilian end customers? **[CONTADOR]**
4. **Paddle vs Creem:** Paddle is more mature. Creem is about €16/month cheaper at €1k MRR, but its payout fee documentation is contradictory. Ask both, in writing, about Brazil payout rail, fees and FX before building.
5. **Payout route:** SWIFT directly to a Brazilian bank, Payoneer, or Wise? Each needs a proper câmbio contract for export proof [T10].
6. **Pricing floor:** keep plans at or above €19. Paddle requires custom pricing for products under $10 [P2], and fixed fees hurt more at low prices.
7. **Sell to Brazilian customers?** If yes, decide whether they buy through the MoR (tax treatment unclear) or directly from the ME with a domestic NFS-e.
8. **Data retention policy** for reconciliation records (raw 30/90 days plus rollups). This sets the storage cost and the VPS size.
9. **Watch Stripe Managed Payments** for Brazil eligibility ("more countries later in 2026") [LS2].
10. **Budget reality:** infra fits in €8–12/month, but **accountant plus infra ≈ €40–55/month** once an ME exists. Decide when to open the ME: for example after the first 5 paying customers, or a first payout above R$X.

---

## Sources

**Billing**
- [P1] Paddle – supported countries: https://www.paddle.com/help/start/intro-to-paddle/which-countries-are-supported-by-paddle
- [P2] Paddle – pricing: https://www.paddle.com/pricing
- [P3] Paddle – when and how do I get paid: https://www.paddle.com/help/manage/get-paid/when-and-how-do-i-get-paid
- [P5] Paddle – account verification / domain review / business identification: https://www.paddle.com/help/start/account-verification , https://www.paddle.com/help/start/account-verification/what-is-domain-verification , https://www.paddle.com/help/start/account-verification/what-is-business-verification
- [C1] Creem – pricing: https://www.creem.io/pricing
- [C2] Creem – payouts: https://docs.creem.io/merchant-of-record/finance/payouts
- [C3] Creem – supported countries: https://docs.creem.io/merchant-of-record/supported-countries
- [C4] Creem review (competitor-authored, treat with care): https://dodopayments.com/blogs/creem-io-review ; Creem MoR guide: https://www.creem.io/blog/best-merchant-of-record-saas-2026
- [D1] Dodo Payments – pricing: https://dodopayments.com/pricing
- [D2] Dodo – merchant acceptance countries: https://docs.dodopayments.com/miscellaneous/accepted-countries-and-territories ; global payouts blog: https://dodopayments.com/blogs/global-payouts
- [D3] Dodo – Brazil / Pix: https://dodopayments.com/payments-in/brazil , https://dodopayments.com/payment-methods/pix
- [S1] Stripe – Brazil-specific info to open an account: https://support.stripe.com/questions/brazil-specific-information-to-open-a-stripe-account
- [S2] Stripe Brazil pricing: https://stripe.com/br/pricing
- [S3] Stripe – updating tax information for Brazil accounts: https://support.stripe.com/questions/updating-tax-information-for-stripe-accounts-in-brazil
- [S4] Stripe Tax pricing: https://stripe.com/tax/pricing
- [S5] Secondary (US LLC vendor, biased): https://usllcglobal.com/stripe-alternative-brazil
- [S6] Stripe – supported currencies (payment methods in Brazil, FX-control note): https://docs.stripe.com/currencies
- [SM1] Stripe Managed Payments – eligibility: https://docs.stripe.com/payments/managed-payments/eligibility ; overview: https://docs.stripe.com/payments/managed-payments
- [SM2] Stripe Managed Payments – product page (+3.5%): https://stripe.com/managed-payments
- [LS1] Third-party summary of SMP/LS status: https://dodopayments.com/blogs/lemon-squeezy-vs-stripe ; https://fungies.io/lemon-squeezy-stripe-acquisition-saas-founders-2026/
- [LS2] Lemon Squeezy – 2026 update: https://www.lemonsqueezy.com/blog/2026-update
- [LS3] Lemon Squeezy – 2025 update: https://www.lemonsqueezy.com/blog/stripe-lemon-squeezy-update-2025
- [LS4] Lemon Squeezy – supported countries: https://docs.lemonsqueezy.com/help/getting-started/supported-countries
- [LS5] Lemon Squeezy – fees: https://docs.lemonsqueezy.com/help/getting-started/fees ; pricing: https://www.lemonsqueezy.com/pricing
- [PO1] Polar – fees: https://polar.sh/docs/merchant-of-record/fees
- [PO2] Polar – supported countries: https://polar.sh/docs/merchant-of-record/supported-countries
- [F1] FastSpring pricing (third-party estimates): https://dodopayments.com/blogs/fastspring-pricing-explained , https://www.vendr.com/marketplace/fastspring
- [G1] Gumroad – pricing: https://gumroad.com/pricing
- [G2] Gumroad – getting paid: https://gumroad.com/help/article/13-getting-paid

**Brazil tax**
- [T1] Carnê-leão 2026 / Lei 15.270: https://www.contabilizei.com.br/contabilidade-online/carne-leao-2026/ , https://razonet.com.br/contabilidade-digital/carne-leao-2026-quem-paga-como-calcular-e-lancar-no-irpf
- [T2] Developer cannot be MEI (2026): https://contabilidade.com/blog/desenvolvedor-pode-ser-mei-em-2026-veja-como-abrir-cnpj-escolher-o-cnae-ideal-e-pagar-menos-impostos/
- [T3] CNAE 6201-5/01 and Fator R: https://contabilidade.com/blog/cnae-6201501-desenvolvimento-de-programas-de-computador-sob-encomenda-simples-nacional-fator-r-e-abertura-de-empresa/ ; IBGE CONCLA 6203-1/00: https://concla.ibge.gov.br/busca-online-cnae.html?subclasse=6203100&view=subclasse
- [T4] LC 123/2006 (art. 18 §§5-B, 5-D, 5-J, 5-M; Anexo V): https://www.planalto.gov.br/ccivil_03/leis/lcp/lcp123.htm
- [T5] Anexo III table 2026: https://www.contabilizei.com.br/contabilidade-online/anexo-3-simples-nacional/
- [T6] Anexo III partilha (Receita Federal): https://normas.receita.fazenda.gov.br/sijut2consulta/anexoOutros.action?idArquivoBinario=48432 (and contabeis.com.br table: https://www.contabeis.com.br/tabelas/simples/anexo3)
- [T7] PIS/COFINS on service exports in Simples: https://tributodevido.com.br/isencao-pis-cofins-exportacao-servicos-simples-nacional/
- [T8] Taxes on Simples exports: https://www.remessaonline.com.br/blog/quais-sao-os-impostos-que-incidem-sobre-exportacao-simples-nacional/
- [T9] Solução de Consulta COSIT 73/2025 (summary): https://www.lacerdagama.com.br/post/receita-federal-reconhece-como-exporta%C3%A7%C3%A3o-servi%C3%A7o-virtual-prestado-por-empresa-do-simples-nacional
- [T10] Receiving from abroad, authorized FX channels, documents: https://ndmadvogados.com.br/artigo/cuidados-receber-dinheiro-do-exterior/ ; https://wise.com/br/blog/emitir-nota-fiscal-exterior
- [T11] MoR and Brazil (vendor blog): https://dodopayments.com/blogs/merchant-of-record-brazil
- [T12] Accounting prices: https://www.contabilizei.com.br/quanto-custa-contabilizei/ , https://agilize.com.br/quanto-custa-agilize/ , https://agilize.com.br/artigos/custo-contabilidade-microempresa-simples-nacional/
- [T13] IBS/CBS and exports / Simples: https://netcpa.com.br/colunas/imunidade-de-ibs-e-cbs-na-exportacao-de-servicos-desafios-e-duvidas-na-lc-214/25228 , https://www.reformatributaria.com/opiniao/ibs-e-cbs-em-2026-como-funciona-a-convivencia-com-os-tributos-atuais-segundo-a-lc-no-214-2025/ , https://www.contabeis.com.br/artigos/73075/o-pulo-do-gato-sobre-o-simples-nacional-e-a-reforma-tributaria-lc-214-2025/

**Infra**
- [I1] Hetzner price adjustment 15 Jun 2026: https://docs.hetzner.com/general/infrastructure-and-availability/price-adjustment/
- [I2] IPv4 €0.50 note: https://www.bitdoze.com/hetzner-cloud-cost-optimized-plans/
- [I3] Hetzner backups/snapshots: https://docs.hetzner.com/cloud/servers/backups-snapshots/overview/
- [I4] Vercel fair use (commercial usage): https://vercel.com/docs/limits/fair-use-guidelines
- [I5] Vercel pricing: https://vercel.com/pricing
- [I6] Railway pricing: https://railway.com/pricing
- [I7] Render pricing summaries: https://www.srvrlss.io/provider/render/ , https://kuberns.com/blogs/render-postgres-pricing-setup-limits/
- [I8] Render 2026 pricing changes: https://bex.co/blog/2026/09/04/render-price-changes-cost-sheet
- [I9] Fly.io pricing: https://docs.fly.io/about/pricing/
- [I10] Neon pricing: https://neon.com/pricing
- [I11] Supabase pricing: https://supabase.com/pricing
- [I12] Resend pricing: https://resend.com/pricing
- [I13] Postmark pricing: https://postmarkapp.com/pricing
- [I14] Amazon SES pricing: https://aws.amazon.com/ses/pricing/
- [I15] Sentry pricing: https://sentry.io/pricing/
- [I16] Cloudflare R2 pricing: https://developers.cloudflare.com/r2/pricing/
- [I17] AWS KMS pricing: https://aws.amazon.com/kms/pricing/

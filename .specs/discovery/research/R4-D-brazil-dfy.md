# R4-D — Brazil/PT: Done-for-You Recurring Services (R$600–3,000/month)

> Date: 2026-09-23. Method: `../R4-CRITERIA.md` (capacity model, leverage test, relaxed K12, reinterpreted K1), with `../R3-CRITERIA.md` (K13, K15, ≤15 min setup, Brazil/PT) and `../R2-CRITERIA.md` (K1–K11). Prior segment: `R3-brazil.md`; synthesis: `R3-SYNTHESIS.md`.
> Segment: Brazilian (plus one Portuguese data point) done-for-you services that small businesses buy monthly at ~R$600–3,000 (≈ €100–500 at R$6.2/€).
> Capacity reference: ~43 h/month for ~R$6,200 MRR, so the founder needs about **R$143 per human hour or better**. Examples: 5 × R$1,240 at ≤8.6 h each, or 10 × R$620 at ≤4.3 h each.

## 0. Coverage / quota note

- **About 93 WebSearch calls** (budget 150) and **about 30 WebFetch calls**. The search quota worked this time; R3's starvation did not recur.
- **Blocked or thin sources.** 99Freelas project pages opened, but budgets are hidden ("Aberto, mínimo R$60"). Workana and GetNinjas gave no usable prices. Glassdoor salary snippets are inconsistent (annual and monthly are mixed up). Most DFY providers publish **no price** and sell through "diagnóstico gratuito" or WhatsApp. Prices below come from the minority that publish. Where a number comes only from a search-engine summary and not from a fetched page, it is marked (snippet).
- **Revived R3 kills.** Several R3 kills were re-examined because R4 relaxes K12 and reinterprets K1: C5 BPO financeiro, C7 marketplace management, C11 licitações, C12 condomínio, C18 clinic assistant. **None revives.** Each fails on a rule R4 keeps: ≤15 min setup, phone or real-time work, licensed sign-off or legal liability, or K11.
- C17 was re-checked under R4 (§3.3). It is now **KILL**.

## 1. Summary table

**Verdict: 0 SURVIVE, 2 UNCERTAIN (both weak), 19 KILL (21 candidates).**

| # | Candidate | Paid evidence (price × freq + URL) | DFY competitors & price floor | Human h/customer/mo (provider today → with software) | Verdict | Decisive reason |
|---|---|---|---|---|---|---|
| D1 | BPO financeiro (AP/AR, conciliação, relatórios) | Levits R$1,079 / 1,559 / 3,119 per month for ≤100 transactions and 1 bank account (https://levitsbpo.net/planos/); FinBits from R$599/mo (https://www.finbits.com.br/blog/post/bpo-financeiro-para-pequenas-e-medias-empresas-vale-a-pena); market R$800–1,200 basic, R$1,500–3,000 intermediate (https://www.bposuite.com.br/blog/quanto-cobrar-bpo-financeiro/) | Thousands of solo BPOs and firms. Floor: Contabilizei accounting + BPO at R$589 (2021, https://pt.linkedin.com/pulse/bpo-financeiro-r-349-entenda-estrat%C3%A9gias-envolvidas-em-pedro-nery); FinBits R$599 | Solo analyst runs up to 10 clients (https://andersonhernandes.com.br/quanto-ganha-um-bpo-financeiro/), 10–15 in job posts (snippet) → **~11–17 h**. Software cut to ~6–9 h: fits 5 × R$1,240 only at the upper edge | **KILL** | Onboarding takes **30–75 days** (https://www.bposuite.com.br/blog/implantacao-de-bpo-financeiro/), far beyond the ≤15 min setup rule. Bank logins and payment scheduling (K11). Reconciliation is the founder's NO-GO. Providers already use Nibo/Omie/BPO Suite, so ≥50% leverage against them is unproven. WhatsApp SLA of 2 h |
| D2 | Marketplace full management (ads, SEO, pricing, reputation) | Mercato Flux R$1,080–1,242/mo; first month R$299.90 (https://mercatoflux.com.br/); consultoria R$3,000–12,000/mo (https://gosmarter.com.br/consultoria-para-marketplace-quanto-custa-e-quando/) | Dozens of assessorias. Mercado Livre gives free certified-agency support to stores with >R$150k/mo revenue (https://www.ecommercebrasil.com.br/noticias/mercado-livre-lanca-servico-de-assessoria-gratuita-para-vendedores-e-estima-ate-70-de-crescimento) | Daily operation plus a daily WhatsApp group plus monthly meetings; ≥15 h (estimate) | **KILL** | The core value is judgement over ad spend and performance, not assembly work, so K12 still applies. Daily real-time operation plus meetings breaks the no-calls and capacity rules |
| D3 | Marketplace SAC / pre-sale questions (written) | Buyer post "Atendimento para marketplace (SAC – Mercado Livre)" drew **411 proposals**; budget open, min R$100 (https://www.99freelas.com.br/project/atendimento-para-marketplace-sac-mercado-livre-629889) | Labour oversupply. GoBots AI answers ML questions pre- and post-sale (https://gobots.ai/solucao-inteligencia-artificial-para-mercado-livre/); UpSeller/ERP SAC apps | Volume-driven; SLA is minutes, not async | **KILL** | K1 (bots plus ERP apps). K10: the price floor sits at VA rates. Platform SLAs force near-real-time work |
| D4 | Product/listing cadastro (catalogue) | R$6 per product; R$197 per 20 products; R$700 per 50 listings (https://integrando-se.lojaintegrada.com.br/servicos/implantacao/cadastro-de-produto/); R$15–60 per item (snippet) | Loja Integrada partner marketplace; Bling "Agente de Anúncios" (R3) | Per item, mostly one-off | **KILL** | K15 (one-off). K10: the floor is R$6/item. K1 |
| D5 | NF-e/NFS-e + boleto issuance outsourced (standalone) | Only bundled in BPO; "~R$2k/mo for 100 notes with full financial management" (snippet, https://mandaprofinanceiro.com.br/como-terceirizar-a-emissao-de-boletos-e-notas-fiscais/); standalone prices hidden (https://planejabpo.com.br/servicos/emissao-nota-fiscal) | NFE.io R$190/mo for 250 notes (R3); Asaas collection rules at ~R$0.50 per WhatsApp (snippet, https://www.asaas.com/regua-de-cobranca) | <2 h | **KILL** | K1/K10 standalone. As a bundle it collapses into D1 |
| D6 | Written collections (cobrança) for SMBs | Contingency 10–20% of amount recovered (snippet, https://www.abrasuacobranca.com.br/post/precifica%C3%A7%C3%A3o-para-empresas-de-cobran%C3%A7a-quanto-cobrar-pelo-servi%C3%A7o-de-recupera%C3%A7%C3%A3o-de-cr%C3%A9dito) | Asaas/InfinitePay automatic dunning; CDL/SPC platforms | Variable | **KILL** | Negotiation is the core value (a K12 still-kill). Phone is the norm. CDC limits on fees. Automated dunning covers the written part |
| D7 | Licitações: edital search + habilitação documents | AM Consulte: daily search R$120/mo; habilitação R$100–160 per bid; proposal R$120–260; success fee 0.5% (https://amconsulte.com.br/index.php/precos/) | ConLicitação, Effecti (R3); many assessorias; analyst salary ~R$2,777–3,574/mo (https://br.indeed.com/career/analista-de-licita%C3%A7%C3%A3o/salaries) | Per bid; live bidding sessions | **KILL** | The recurring monthly piece is R$120 (K10). Value sits in pricing and bid strategy and in appeals (K12 still-kill: quasi-legal work). Real-time lance sessions break async delivery |
| D8 | Third-party (SST/labour) document control, buyer = contratante | Only enterprise BPO/platforms: Bernhoeft, Sertras "BPO + tecnologia" (https://www.sertras.com/); prices not public | Bernhoeft, Sertras, WeHandle, Tesseg, SESI, GD3 | n/a | **KILL** | K6 (sales-led enterprise). Buyer is not an SMB. The contratante's subsidiary labour liability rests on the check, so this is legal-liability value |
| D9 | **Monthly document submission to client portals, buyer = small contratada** (new) | Job-post duty "incluir documentação dentro dos portais dos clientes" (snippet, https://br.indeed.com/q-assistente-de-documenta%C3%A7%C3%A3o-vagas.html). Bernhoeft contracts oblige suppliers to upload payroll/DARF/ponto monthly by day 11/30 (https://www.bernhoeft.com.br/blog/portal-bernhoeft-ferramenta-de-apoio-a-gestao/); payment is blocked if pending (https://www.bernhoeft.com.br/blog/gestao-de-terceiros-na-cadeia-de-suprimentos/). **No price found** | None found selling this as a productised service to contratadas (UNVERIFIED) | Est. 2–5 h per contratada with ~2–4 client portals | **UNCERTAIN (weak)** | Real, monthly, deadline-driven, and payment-blocking. But there is no priced transaction (fails "paid labour first"). Portals have no API (K13), so the leverage test is doubtful. Documents come from the accountant or DP |
| D10 | **Google Business Profile (GBP) / review management** | Agencies R$400–1,200/mo isolated; Be On from R$600 (https://www.beonmarketingfortaleza.com.br/blog/gestao-perfil-empresa-google-quanto-custa.html); Portugal: Netwods €80 / €150 per month (https://netwods.com/gestao-de-google-business-profile/) | Freelancers (99Freelas buyer posts: min R$60, mostly one-off, e.g. https://www.99freelas.com.br/project/gestor-de-google-meu-negocio-614902). Tools: Semrush Local from $30/location/mo with AI posts and auto-replies (https://www.semrush.com/pricing/local/, snippet). Google is testing native AI replies in Brazil (https://searchengineland.com/google-business-profile-test-reply-to-reviews-with-ai-472167) | Provider estimate **9–14 h/mo** (Be On). With scheduling and AI drafts: ~2–4 h | **UNCERTAIN (weak)** | Fits capacity, written-only, no licence, setup is a manager invite (≤15 min). But the evidence of recurring buyers is seller-side only. Commodity, K3, and K8 (Google's native AI replies) are strong kill risks |
| D11 | Contract / renewal tracking for SMBs | No paid DFY evidence; only software and SEBRAE advice (https://sebraepr.com.br/web-stories/como-fazer-gestao-de-contratos-em-pequenos-negocios/) | GestãoClick, ERP modules | <1 h | **KILL** | No priced transaction (K4/K5). K1 |
| D12 | Tax-credit recovery (recuperação tributária, monofásico etc.) | Success fee % of credit (https://www.contabeis.com.br/artigos/78498/recuperacao-tributaria-guia-completo-para-empresas/) | Law and accounting firms | One-off | **KILL** | K15 (5-year look-back, one-off). Lawyer/accountant sign-off (a still-kill) |
| D13 | Condomínio back-office for síndicos / small administradora | Síndico profissional R$1,500–4,000+/mo (snippet, https://blog.townsq.com.br/sindicos/quanto-custa-contratar-um-sindico-profissional/); administradora R$15–40 per unit (snippet, https://condominizando.com.br/blog/noticias-3/quanto-custa-uma-administradora-de-condominio-em-2026-27) | Superlógica, TownSq, uCondo; Residente Online R$550/mo (snippet) | High; visits and assemblies | **KILL** | In-person work and assemblies. The síndico's civil liability. Payroll and eSocial for porteiros. Monthly audit of the pasta needs a **CRC** accountant (https://blog.townsq.com.br/financeiro/auditoria-em-condominios/) |
| D14 | Clinic remote secretary (non-clinical admin) | Yoog Saúde R$725 (100 interactions) / R$1,060 / R$1,690 per month (https://yoogsaude.com.br/planos-e-precos/) | Remottas, Proagille, H&H, AI bots (Yara from R$299) | Real-time | **KILL** | The plans include **phone calls** and real-time scheduling. Sensitive health data (K11). AI bots already sell for R$299 |
| D15 | "Reembolso assistido" (health-plan reimbursement filing) | Offered for a % fee (UNVERIFIED) | — | — | **KILL** | Using patients' plan logins is treated as fraud; insurers win in court (https://www.sindsegsp.org.br/site/noticia-texto.aspx?id=35710). Legal liability and health data |
| D16 | Chargeback contestation for e-commerce | Price hidden; "our team assembles the package" (https://contestacaodechargeback.com.br/como-contestar-chargeback) | Acquirer/PSP tools | Per event | **KILL** | No priced transaction. Only ~10% of cases are contestable (same source). Event-driven, not monthly |
| D17 | Social-media management (control) | Freelancers R$500–1,200/mo, agencies from R$1,200 (snippet, https://azzagencia.com.br/blog/redes-sociais/gestao-de-redes-sociais-preco/) | Huge freelancer supply | 10–20 h | **KILL** | Commodity (a hard R3 constraint). Creative judgement. No leverage advantage |
| D18 | Alvarás / licenças / AVCB upkeep | R$2,500–3,500 per process (snippet, 2020, https://www.licencas.net/servicos/alvara/) | Despachantes, accountants | Event | **KILL** | K15 (validity 1–5 years). On-site inspections |
| D19 | Fleet fines (indicação de condutor, recursos) | Price hidden | Frota Certa captures from 100+ agencies (https://frotacerta.com.br/gestao-de-multas/); Frota 162; Localiza includes it | Event-driven | **KILL** | K1. Appeals are quasi-legal. Small fleets have low volume |
| D20 | Imobiliária listing upkeep on portals | No DFY price found | ImobiBrasil from R$74.99/mo with portal integration (snippet, https://www.imobibrasil.com.br/); Lais AI | Low | **KILL** | K1 (integrations push listings automatically) |
| D21 | R3-C17 NCM + IBS/CBS classification (DFY variant) | ASSCON R$150–250/mo maintenance; R$1,200–7,000 one-off review (R3) | **ClassTrib self-serve R$97–197 lifetime for 4k–40k queries** (https://classtrib.com/novo/); **Omie IA Fiscal R$199.90–1,299.90/mo native** (https://store.omie.com.br/apps/omie-ia-fiscal); Bling auto-fills IBS/CBS (https://ajuda.bling.com.br/hc/pt-br/articles/33954454841751-Como-emitir-NF-e-com-os-dados-da-Reforma-Tribut%C3%A1ria-no-Bling) | Wave, then minutes per month | **KILL** | K1/K9 now confirmed. K15 (one-off wave). The classification decision carries tax liability, up to 75% fines (https://www.contabeis.com.br/noticias/74339/cbs-e-ibs-em-2026-exigem-revisao-do-cclasstrib-nas-nf-e/) |

## 2. Per-candidate notes

### D1. BPO financeiro (revisits R3-C5)
- **Who pays, how much.** SMEs pay fixed monthly plans banded by transaction volume:
  - Levits: R$1,079 (Crescimento), R$1,559 (Gerencial, "70% of clients choose"), R$3,119 (Estratégico), each for ≤100 transactions and 1 bank account, month-to-month, with a WhatsApp SLA of 2 h, monthly or biweekly meetings and a phone line.
  - Unick/SeuBPO has an MEI tier (60 transactions, 15 invoices) with a hidden price, "100% digital, no setup fee" (https://seubpo.com.br/planos/).
  - Market guides quote R$900–1,800 for micro businesses (≤120 títulos) and R$1,800–3,500 for small businesses (snippet, https://www.creisconsultoria.com/post/quanto-custa-contratar-um-bpo-financeiro-guia-de-pre%C3%A7os-roi-e-compara%C3%A7%C3%A3o-de-propostas).
- **Why not tools.** Conta Azul and Nibo do the reconciliation (R3). The buyer pays for someone to chase documents, schedule payments and explain the numbers. This is the R3 "responsibility" pattern. The evidence is strong that buyers ignore the tools: BPO is billed at about 3× the accounting fee (Hernandes).
- **Labour economics.** A BPO assistant earns about R$2,000–2,800/month (snippet, https://br.indeed.com/career/assistente-financeiro/salaries) and handles 10–15 clients. Provider labour cost is therefore about R$200 per client per month. A solo operator at 10 clients × R$1,000 is working full time, about 16 h per client.
  - For the founder, 5 × R$1,240 needs ≤8.6 h per client, a cut of roughly 46–50%. That is at the edge of the leverage test, and it is measured against providers who **already** use BPO software (BPO Suite, PlayBPO, Nibo). The founder's advantage over them is therefore unproven.
- **Kill.** Four problems:
  - **Onboarding** takes 30–75 days: collecting bank logins and the digital certificate, then diagnosis, then ERP set-up and balance migration, then a month of assisted operation. That breaks the ≤15 min rule.
  - **K11:** bank logins and payment scheduling; "muitos clientes possuem resistência" (BPO Suite).
  - **Founder NO-GO:** the heart of the job is reconciliation.
  - **Liability exposure:** Reclame Aqui complaints about missed payment deadlines and notes issued in the wrong period (https://www.reclameaqui.com.br/marvee/falhas-e-atrasos-em-servico-de-bpo-financeiro-e-contabilidade-descumprime_K8_rzZGf2buV0SQu/).
- **Licensing.** Not an issue. BPO financeiro does not require CRC registration (https://planning.com.br/bpo-financeiro-contabilidade-tradicional/).

### D2–D4. Marketplace/e-commerce (revisits R3-C6/C7)
- **D2, full management.**
  - Mercato Flux publishes a checkout-like offer: first month R$299.90, then R$1,080–1,242/month, no lock-in. But it is sold through WhatsApp and includes a daily WhatsApp group plus monthly meetings.
  - What the buyer pays for is ads and SEO execution against revenue targets. That is judgement over spend, which R4 still kills, not "assembling/finishing work".
  - Agency analyst salary is about R$3,050/month (Jooble snippet, https://br.jooble.org/salary/analista-de-marketplace). One posting lists "gestão completa de 2 contas", which implies many hours per account (snippet).
- **D3, SAC.** 411 proposals on one ML SAC post shows extreme labour oversupply. GoBots and ERP apps automate question answering.
- **D4, cadastro.** Listing work clears at R$6 per product on the Loja Integrada services marketplace, and it is one-off.

### D5–D6. Invoicing and collections
- Standalone issuance has no published market price. It is either bundled into BPO or already cheap as a tool (NFE.io, Asaas).
- Collections are contingency-priced and centred on negotiation and phone work. Automated dunning (Asaas) covers the written reminders.

### D7–D9. Licitações and contractor documentation
- **D7.** The per-item AM Consulte menu shows the monthly recurring part (daily edital search) at R$120/month. The rest is per bid, and the value is in pricing, appeals and live sessions.
- **D8.** Contratante-side contractor compliance is an enterprise market (Bernhoeft, Sertras) with sales-led platforms and labour-liability stakes.
- **D9, contratada side.** Small service firms (cleaning, maintenance, security) that sell to large companies must upload payroll, DARF, FGTS, ponto and ASO monthly to each client's portal. Late or incorrect uploads block payment (WeHandle guide: https://wehandle.com.br/blog/gestao-de-documentos-de-colaboradores-guia-prestador-de-servico).
  - This is recurring, deadline-driven and written, with no licence required.
  - **But:** (a) no priced DFY offer was found, so it fails "paid labour first"; (b) portals have no API, so a human uploads, and software leverage is limited to collecting, renaming and checking the pack (leverage test doubtful); (c) the source documents are produced by the client's accountant or DP, so pendências often need them to fix things.
  - **Kept UNCERTAIN only as a lead for the manual sweep.**

### D10. Google Business Profile / reviews
- **Paid evidence (seller-side).**
  - Be On Digital: R$400–1,200/month isolated, R$800–2,500 in local-SEO packages, and warns "desconfie de propostas abaixo de R$300". It estimates **9–14 h/month** per profile: posts 2–3 h, review replies 3–4 h, monitoring 1–2 h, photos 1–2 h, reporting 1–2 h.
  - Portugal: Netwods €80/month (1 post plus basic replies) and €150/month (4 posts plus full review management).
- **Buyer-side evidence is weak.** 99Freelas GMN posts are mostly one-off optimisations with a minimum of R$60 and 7–17 proposals. Some are agencies subcontracting.
- **Tools.** Semrush Local from $30/location/month includes AI post scheduling, auto-replies and a "GBP AI Agent". Google itself is testing AI review replies, with Brazil among the test markets (Search Engine Land, March 2026). Reviewax sells review-request automation plus AI replies to Brazilian SMEs (price hidden, snippet).
- **Capacity.** At R$600 (€97), about 10 customers need ≤4.3 h each. Software could plausibly bring the 9–14 h down to 2–4 h (drafted replies, batch-produced posts, a monthly photo request by WhatsApp). The capacity test is therefore passable.
- **Kill risks.**
  - Commodity (a hard R3 constraint).
  - K3: the differentiation is AI plus automation.
  - K8: Google's native AI replies.
  - Price floor: the same tools are available to every R$60 freelancer.

### D11–D20 (short)
- **D11** contracts/renewals: no one sells it as DFY to SMBs.
- **D12** tax recovery: one-off, and the lawyer or accountant signs.
- **D13** condomínio: in-person work, síndico liability, a CRC-signed audit, and ERP incumbents.
- **D14** clinic secretary: the phone is intrinsic.
- **D15** reembolso assistido: judicially treated as fraud.
- **D16** chargebacks: event-based with no price.
- **D17** social media: commodity.
- **D18** licences: multi-year.
- **D19** fleet fines: tooled.
- **D20** imobiliária listings: tooled.

## 3. Survivors / uncertain deep-dive

### 3.1 D10 — GBP/review management (UNCERTAIN, weak)
1. **Who pays, how much, how often.** Local SMBs (restaurants, clinics, trades) pay agencies R$400–1,200/month in Brazil and €80–150/month in Portugal. **All price evidence is seller-side.** No invoice, buyer post with a monthly budget or community thread confirming recurring spend was found. Buyer posts on 99Freelas are mostly one-off.
2. **Why not the cheap tool.** No evidence either way. The argument is "owners don't log in", but Semrush Local ($30) and Google's native AI replies attack exactly that.
3. **Human time with leverage.** Estimated 2–4 h/month against a provider estimate of 9–14 h, a cut of ≥65%. At R$600 × 10 customers that is 20–40 h, which fits.
4. **Self-serve purchase.** Plausible: fixed-price plans and a Google-manager invite (setup ≤15 min). Local SEO content is a natural channel.
- **What would kill it:** Google rolling out AI replies and post suggestions broadly, or evidence that buyers churn once the tools are free. **What would move it forward:** buyer-side proof of monthly spend above R$400 (manual sweep: Workana/GetNinjas buyer posts, Facebook groups of restaurant or clinic owners).

### 3.2 D9 — Contratada portal document submission (UNCERTAIN, weak, evidence-starved)
1. **Who pays.** Unknown. The work is done in-house by an assistente administrativo (~R$2,000–2,700/month) or by the accountant.
2. **Tool.** Contratante-side platforms (Bernhoeft, WeHandle) don't do the contratada's uploads. No tool for the contratada was found.
3. **Hours.** Est. 2–5 h/month per contratada with 2–4 portals. At R$600–900/month that would fit, but only if priced there.
4. **Self-serve.** Plausible via searches such as "pendência Bernhoeft", but unproven.
- **Blocking issues:** no priced transaction; portals without API (K13 means manual work, so the leverage test likely fails); reliance on the accountant's documents; LGPD (employee personal data, ASOs are health data, K11).

### 3.3 Stage D re-check of R3-C17 (NCM + IBS/CBS classification upkeep) under R4 — **KILL**
Answers to R3's five Stage D questions:
1. **Do the ERPs suggest codes? Yes.**
   - Omie sells **Omie IA Fiscal**, which "automatiza a classificação fiscal de mercadorias, sugere a tributação correta" including IBS/CBS. Priced by SKU count: R$199.90 (≤100 items) up to R$1,299.90 (≤5,000).
   - Bling auto-fills IBS/CBS on NF-e, defaulting to CST 000 / cClassTrib 000001, which can be customised by natureza de operação.
2. **Self-serve classifiers exist and are cheap.** ClassTrib: NCM → cClassTrib/CST in batch from CSV, SPED or XML, R$97–197 **lifetime** for 4,000–40,000 queries, aimed at accounting firms. It claims 10,000 items in 2 h 46 min.
3. **Separate billing by accounting firms:** still only the ASSCON reference (R3). With ClassTrib at R$97, a firm has no reason to outsource.
4. **Monthly volume after the wave:** new SKUs per month for an SMB means minutes of work, so the recurring value is below the floor. Even the DFY framing (R4) gives one-off-wave revenue (K15).
5. **Liability:** the classification is "decisório". Wrong codes attract fines of up to 75% (Contábeis). Taking on that liability is a still-kill under R4.
- **Verdict: KILL** (K1/K9 confirmed, K15, liability).

## 4. Segment finding

1. **Brazilian SMBs *do* pay humans R$600–3,000/month for DFY back-office, even though tools exist.** BPO financeiro is the clearest case: R$599–3,119 plans, about 3× the accounting fee, despite Conta Azul and Nibo. R3 pattern #4 (paying for responsibility) holds in Brazil.
2. **But the Brazilian DFY market runs on very cheap labour that is already software-leveraged.** Assistants earn R$2,000–3,000/month and serve 10–15 clients each, so provider labour is about R$200 per client per month. Providers already use the same software (BPO Suite, Nibo, Omie, Semrush). The R4 leverage test (≥50% cut versus *today's* provider) is therefore very hard to meet, because incumbents have already taken the easy automation.
3. **The DFY money attaches to exactly what R4 still excludes or what the founder refuses:**
   - long onboarding (30–75 days)
   - bank logins and payment authority (K11)
   - reconciliation (founder NO-GO)
   - live channels (phone, WhatsApp SLAs of 2 h, daily WhatsApp groups, monthly meetings)
   - real-time work (ML SAC, bidding sessions)
   - negotiation (collections)
   - licensed or quasi-legal sign-off (condomínio audit, tax recovery, classification liability)
   
   The DFY services that avoid all of these (GBP, cadastro, SAC answers) are commodities that clear at R$6–60 per unit or face 400+ competing freelancers.
4. **Acquisition is sales-led even for productised offers.** Almost every provider sells through a WhatsApp diagnosis or a "Falar com especialista" button; published checkout prices are rare. Mercato Flux's R$299.90 trial is the nearest thing to self-serve. A checkout-first DFY would be a differentiator, but no evidence shows buyers purchase this way.
5. **Net:** nothing in Brazil/PT DFY clears all R4 gates. The two UNCERTAINs are weak. D10 is a commodity at risk from Google itself. D9 is a genuine monthly pain with no price found.

## 5. Evidence gaps (UNVERIFIED)
- **Buyer-side monthly budgets.** For GBP and review management, BPO financeiro for MEIs and contratada portal submission: 99Freelas hides budgets; Workana, GetNinjas and Facebook groups were not reachable. This is the priority for the founder's manual sweep.
- **Price of any productised "envio de documentação a portais de clientes" service for contratadas** (D9). Also whether accounting firms charge extra for it.
- **Actual hours per client at BPO providers** come from blogs and job posts (10–15 clients per analyst), not time studies.
- **Hidden prices:** Reviewax, GoBots, WeHandle, Bernhoeft, Sertras, Localo, and Semrush Local in BRL. The Semrush $30 figure is from a snippet.
- **Google AI review replies:** rollout status in Brazil (test since March 2026) is not confirmed as general availability.
- **Social media, síndico and administradora figures** are from search snippets only, not fetched pages.
- **Portugal** was only spot-checked (Netwods GBP €80–150/month). A fuller PT sweep was not done.

# R3 — Brazil: Paid Repetitive Labour

> Date: 2026-09-23. Method: `../R3-CRITERIA.md` (K12–K15) + `../R2-CRITERIA.md` (K1–K11). Segment: Brazil, paid repetitive labour.
> **Search-quota note:** the session's WebSearch budget (200/200) was **exhausted before this segment started**. Evidence was gathered with direct WebFetch of known URLs, a few Brave/Bing result pages fetched through WebFetch (Brave then rate-limited with HTTP 429), and one PDF price table. Freelance marketplaces (Workana and Fiverr returned 403; 99Freelas hides budgets) gave **no public gig prices**. Price evidence therefore relies mainly on a published fee table and job-salary pages. Every gap is marked UNVERIFIED.

## 1. Summary

**Verdict: 0 SURVIVE, 1 weak UNCERTAIN, 19 KILL (20 harvested).**

| # | Candidate | Paid evidence (price × frequency) | Verdict | Decisive reason | Cheapest existing tool |
|---|---|---|---|---|---|
| C1 | CND issuance and monitoring | R$200–250 per "consulta fiscal e emissão de CND", ad hoc to monthly (ASSCON) | KILL | K1: self-serve at R$3.50 per CNPJ/month; 12+ vendors | suaCND R$3.50/CNPJ/month |
| C2 | DCTFWeb / EFD-Reinf monthly transmission | R$200/month DCTFWeb, R$350/month EFD-Reinf (ASSCON); a recurring 99Freelas gig | KILL | K2/K9: done inside accounting suites; K12: the accountant carries the responsibility; e-CNPJ handling (K11) | Accounting suites (Domínio/Alterdata/Questor, price UNVERIFIED); SERPRO Integra Contador API |
| C3 | PGDAS-D / DAS (Simples apuração) | R$200/month (R$130 sem movimento) (ASSCON) | KILL | K1/K9: Sittax automates apuração and DAS transmission | Sittax (price not public) |
| C4 | Parcelamento guias (monthly issue and delivery) | R$50–75 per recalculated guia; Regularize R$550+ one-off (ASSCON) | KILL | K1: HubCount controls "Parcelamento do Simples Nacional … without opening any portal" | HubCount (price not public) |
| C5 | BPO financeiro (AP/AR, reconciliation) | R$350/hour (ASSCON) | KILL | K12 (trust, paying bills), K11 (bank access), K2 (Nibo/Conta Azul) | Conta Azul with automatic reconciliation (price not captured) |
| C6 | Marketplace product listing / cadastro | Analista de cadastro R$3,295.63/month salary; freelance gigs mostly one-off | KILL | K1/K8: Bling sells an AI "Agente de Anúncios"; K15 for gigs | Bling R$57/month + add-on |
| C7 | Marketplace management / Ads | Recurring 99Freelas gigs, budgets hidden | KILL | K12: strategy and judgement | n/a |
| C8 | NFS-e / NF-e avulsa issuance | R$50 per NFS-e, R$100 per NFA-e (ASSCON) | KILL | K1 | NFE.io R$190/month for 250 notes |
| C9 | CT-e / MDF-e issuance | Per-document fee UNVERIFIED | KILL | K1: Bsoft claims 32,232 customers and 83,220 CT-e/day | Bsoft emissor (price not public) |
| C10 | TISS insurer billing / glosas (clinics) | Faturista hospitalar R$2,337.85/month | KILL | K1 (TISS built into clinic software), K11 (LGPD sensitive health data), K12/K13 (glosa appeals in operator portals) | iClinic R$99–299/professional/month |
| C11 | Licitações (edital search, documents, índices) | Assistente de licitação R$2,319.42/month; "Índices para licitações" R$450–850 per event | KILL | K1 (ConLicitação 20k+ companies, Effecti), K12, K15 | Effecti (free trial, price hidden) |
| C12 | Condomínio monthly prestação de contas | R$1,200/month (ASSCON) | KILL | K9/K2: administradoras' ERP (Superlógica) produces it | Superlógica (price not captured) |
| C13 | Imobiliária repasses / DIMOB | DIMOB R$665/year (ASSCON) | KILL | K15 (annual); K9 (Superlógica Imobiliárias) | Superlógica |
| C14 | Carnê-Leão for liberal professionals | R$50/month (ASSCON) | KILL | K10: spend is below the R$300 floor; K8: government Receita Saúde (UNVERIFIED) | Carnê-Leão Web (free, gov) |
| C15 | Municipal ISS declarations (DES etc.) | R$260/month (ASSCON) | KILL | K13/K7: fragmented municipal portals | n/a (UNVERIFIED) |
| C16 | IBS/CBS pilot-year "apuração assistida" (DF-e × ERP) | R$500–2,500/month (ASSCON) | KILL | This is reconciliation/detection (ProofOps NO-GO; R2 lesson); K9 (Qive 210k CNPJs, Sittax RT, ERPs); K5 (2026 is informational) | Qive / Sittax RT (price not public) |
| C17 | NCM + IBS/CBS (cClassTrib/CST) product classification upkeep | R$150–250/month maintenance; R$1,200–2,500 per ≤200-item review (ASSCON) | **UNCERTAIN (weak)** | Economics fail (K10) for SMB direct buyers, and the one-off wave is K15. Only the accounting-firm-as-buyer variant is untested | Systax (enterprise, price not public); ERP suggestions UNVERIFIED |
| C18 | Clinic virtual assistant (collections, rescheduling, receipts) | Recurring 99Freelas gig, 261 proposals | KILL | K12 (relationships); K1 (clinic software with reminders) | iClinic R$99+/month |
| C19 | Alvará / licenças renewals | R$250–450 per event, annual (ASSCON) | KILL | K15 | n/a |
| C20 | Payroll per employee | R$87.30–165.50 per vínculo/month (ASSCON) | KILL | K9 (accounting suites), K12, eSocial | Accounting suites |

## 2. Structural finding (read this first)

1. **In Brazil, "paid repetitive labour" for B2B bureaucracy sits almost entirely inside the accounting firm.** SMEs pay a bundled retainer, e.g. R$250–1,050/month for a Simples service company (https://www.ohub.com.br/precos/contabilidade-mensal), and firms price individual obligations at R$50–365 each (ASSCON 2026 table, below). **Almost every single unbundled item is priced *below* the R$300–1,200 target**, so no single obligation replaces 2–5× the software price for an SME buyer (structural K10).
2. **The accounting firm, the only buyer with aggregated volume, is a saturated SaaS market.** Several products each automate the per-client jobs: Acessórias, HubCount ("+250 mil empresas", https://www.hubcount.com.br/), Sittax (https://sittax.com.br/), Qive (210k+ CNPJs, https://qive.com.br/), SIEG, suaCND, Alterdata, IOB, Questor and Dootax. The accounting suites (Domínio, Alterdata, Questor) sit underneath them. SERPRO's **Integra Contador** API exposes PGDAS-D, DCTFWeb, SITFIS, parcelamentos, PGMEI, DASN-SIMEI and Caixa Postal (https://apicenter.estaleiro.serpro.gov.br/documentacao/api-integra-contador/). That removes K13 for federal filings, but it also means every incumbent already has the same rails.
3. **The "Portuguese is under-served by English-first AI" thesis did not hold for this segment.** The Brazilian incumbents are local, speak Portuguese, and already ship AI: Bling "Agente de Anúncios/Imagens" (https://www.bling.com.br/planos-e-precos), ConLicitação "Dr. Licita"/ConLicita IA (https://www.conlicitacao.com.br/), Nibo's Open Finance reconciler (https://www.nibo.com.br/) and Conta Azul's AI expense capture (https://contaazul.com/planos/). Even a BPO financeiro firm is setting up its own Claude projects via 99Freelas (https://www.99freelas.com.br/projects?q=bpo+financeiro).
4. **Labour is cheap.** Faturista R$2,565.74/month, assistente fiscal R$2,653.87, assistente de licitação R$2,319.42 (Catho links in C2/C10/C11). One 99Freelas VA posting drew 261 proposals. A task has to take a large share of an FTE to justify R$300+/month.

## 3. Anchor price evidence: ASSCON 2026 reference fee table
Source: "ASSCON — Tabela Referencial de Honorários Contábeis, vigência 01/01–31/12/2026", PDF hosted at https://shimizucontabil.com.br/wp-content/uploads/2026/01/Tabela-de-Honorarios-Contabeis-de-2026.pdf.pdf (issuer www.asscon.org.br). **Caveat:** these are *reference* prices from an association, typically above what small offices actually collect. The oHub market ranges are lower. No Sescon/CRC table could be retrieved (sescon.org.br shows no public table: https://www.sescon.org.br/).
- Retainers (no employees): Simples ME ≤R$180k/yr R$800–1,350/month; Lucro Presumido ME R$950–1,750; condomínio R$1,200/month.
- Monthly per obligation: DCTFWeb/MIT R$200 (R$130 sem movimento); PGDAS-D R$200 (R$130); EFD-Reinf R$350; eSocial R$350; DES municipal R$260; GIA/GIA-ST R$365; EFD ICMS/IPI R$350; EFD-Contribuições R$350; Carnê-Leão R$50.
- Payroll: R$165.50 per vínculo (≤2) down to R$87.30 (>40).
- Ad hoc: CND R$200–250; guia recalculation R$50–75 per guia; NCM classification maintenance R$150–250; índices para licitações R$450–850; cadastros comerciais/bancários R$250; NFA-e/NF-e via SEFAZ R$100 each; NFS-e R$50 each; alvará R$250; licenças R$350–450.
- Annual: DIMOB R$665; DMED R$665; DEFIS R$1,200; RAIS R$329+; DASN-SIMEI R$250; LCDPR R$3,111.
- Hourly: BPO financeiro R$350/h.
- Tax reform: "Apuração assistida IBS/CBS – ano-piloto 2026" R$500–2,500/month; "Revisão e parametrização fiscal (NCM, CFOP, CST…)" up to 200 items R$1,200–2,500, 200–1,000 items R$3,000–7,000.

## 4. Per-candidate sections

### C1. CND issuance and monitoring
- **Paid labour:** CND consultation and issuance R$200–250 per event (ASSCON). It recurs because certidões expire and are needed for bids, credit and suppliers (https://www.alterdata.com.br/contabil/cnd).
- **Deliverable:** fully standardisable (PDFs from federal, state and municipal portals).
- **Competition:** suaCND is **self-serve at R$3.50 per CNPJ/month**, covering 7 certificate types (https://www.suacnd.com/). Also Alterdata CND, IOB, Questor, Sittax Monitora (https://www.agilizza.com/), Dootax, HubCount, Master DEC-CND and others (Brave results page, fetched 2026-09-23). Infosimples sells per-query APIs for every state and dozens of municipalities (https://infosimples.com/consultas/).
- **Kill:** K1, K3. **KILL.**

### C2. DCTFWeb / EFD-Reinf monthly transmission
- **Paid labour:** R$200/month DCTFWeb and R$350/month EFD-Reinf (ASSCON). A 99Freelas posting asks for "Transmissão mensal … das declarações EFD-Reinf e DCTFWeb" (https://www.99freelas.com.br/projects?categoria=administracao-e-contabilidade; budget hidden).
- **Deliverable:** a structured government filing. An API path exists (Integra Contador), but it needs an e-CNPJ plus an e-CAC procuração (link above).
- **Competition:** every accounting suite does this; the buyer is an accounting firm (UNVERIFIED suite prices). An SME's accountant already includes it in the retainer.
- **Kill:** K2, K9, K12 (the filing's correctness is the accountant's professional responsibility), K11 (custody of clients' e-CNPJ A1 certificates is a security and LGPD burden), K10 (R$200 line item). **KILL.**

### C3. PGDAS-D / DAS
- R$200/month (ASSCON). Sittax: "transmissão automática … da guia DAS" (https://sittax.com.br/). Integra Contador exposes PGDAS-D. **KILL** (K1, K9, K10).

### C4. Parcelamento guias
- Guia recalculation R$50–75 each; PGFN Regularize R$550–1,350 per negotiation (ASSCON; the negotiation is one-off, K15).
- HubCount: "Parcelamento do Simples Nacional controlled without opening any portal"; "+250 mil empresas" (https://www.hubcount.com.br/). The Integra Contador API exposes parcelamentos. **KILL** (K1, K9).

### C5. BPO financeiro
- R$350/hour reference (ASSCON). Market monthly prices: UNVERIFIED (search blocked).
- Deliverable: AP/AR entries, bank reconciliation, cash-flow report. Reconciliation is automated by Conta Azul ("conciliação bancária automaticamente", https://contaazul.com/planos/) and Nibo ("concilie milhares de lançamentos em segundos", https://www.nibo.com.br/). The residual paid value is trust, chasing documents and authorising payments.
- **Kill:** K12, K11 (bank credentials, payment authority), K2, and it is two-system reconciliation (founder NO-GO). **KILL.**

### C6. Marketplace product listing / cadastro
- Analista de cadastro R$3,295.63/month (https://www.catho.com.br/profissoes/analista-de-cadastro/). 99Freelas postings are one-off: "Projeto pontual: migração e cadastro inicial de produtos" and "Criação de anúncios … 6 no Mercado Livre e 12 na Shopee" (https://www.99freelas.com.br/projects?q=cadastro+de+produtos, https://www.99freelas.com.br/projects?q=mercado+livre).
- Competition: Bling (from R$57/month) sells AI "Agente de Anúncios" and "Agente de Imagens" add-ons (https://www.bling.com.br/planos-e-precos). Marketplaces' own AI listing tools: UNVERIFIED.
- **Kill:** K1, K8, K3, K15 (gigs are pontual). **KILL.**

### C7. Marketplace management / Ads
- Recurring gigs ("Gestão de marketplaces para papelaria e presentes", recurring; https://www.99freelas.com.br/projects?q=mercado+livre). The value is strategy and ad optimisation. **KILL** (K12).

### C8. NFS-e / NF-e avulsa issuance
- R$50 per NFS-e, R$100 per NFA-e (ASSCON). NFE.io R$190/month for 250 notes, with API and spreadsheet batch issuance (https://nfe.io/precos/). Conta Azul issues NF-e/NFS-e/NFC-e. **KILL** (K1).

### C9. CT-e / MDF-e issuance
- Per-document outsourced fee: UNVERIFIED. Bsoft sells CT-e and MDF-e emissores plus a TMS and claims 32,232 customers and 83,220 CT-e per day (https://www.bsoft.com.br/). **KILL** (K1).

### C10. TISS insurer billing / glosas
- Faturista hospitalar R$2,337.85/month, including reviewing glosas (https://www.catho.com.br/profissoes/faturista-hospitalar/). Generic faturista R$2,565.74 (https://www.catho.com.br/profissoes/faturista/).
- iClinic includes "Faturamento TISS" at R$99–299 per professional/month (https://iclinic.com.br/precos/).
- The residual work (glosa appeals, operator-specific portals) is judgement plus portal entry. Health data is LGPD "dado sensível" (K11).
- **KILL** (K1, K11, K12, K13 plausible: operator portals UNVERIFIED).

### C11. Licitações
- Assistente de licitação R$2,319.42/month: searches editais, renews cadastros, organises documents (https://www.catho.com.br/profissoes/assistente-de-licitacao/). "Índices para licitações" R$450–850 per event (ASSCON).
- ConLicitação: 20k+ companies, 6,000+ sources, bid robot, document management, AI (https://www.conlicitacao.com.br/). Effecti has a free trial and a consultants plan (https://www.effecti.com.br/planos/).
- **KILL** (K1, K12: bid strategy and pricing; K15 for índices, which are tied to the annual balance sheet).

### C12. Condomínio monthly prestação de contas
- R$1,200/month as an accounting-firm service (ASSCON); administradoras bundle it. Superlógica's ERP for administradoras covers billing, reconciliation and split payments (https://www.superlogica.com/).
- **KILL** (K9, K2, K12: the síndico/conselho approval relationship).

### C13. Imobiliária repasses / DIMOB
- DIMOB R$665 per year (ASSCON). Repasses are monthly, but they are ERP features (Superlógica for imobiliárias, https://www.superlogica.com/). **KILL** (K15 for DIMOB, K9 for repasses).

### C14. Carnê-Leão for liberal professionals
- R$50/month (ASSCON). The spend is far below R$300. Receita Federal's "Receita Saúde" receipt app (since 2025) feeds health professionals' receipts to Carnê-Leão: UNVERIFIED (gov.br pages returned 404 during this session). **KILL** (K10, K8).

### C15. Municipal ISS declarations
- DES R$260/month (ASSCON). Brazil has thousands of municipalities, each with its own ISS portal/layout (UNVERIFIED count of portals without API). The NFS-e Nacional standard is expected to reduce this job (UNVERIFIED). **KILL** (K13, K7).

### C16. IBS/CBS pilot-year "apuração assistida"
- R$500–2,500/month: "conferência mensal da apuração informativa; conciliação DF-e × ERP; relatórios de inconsistências" (ASSCON). This is a genuinely new, recurring, priced job.
- It is reconciliation/detection, which the founder has ruled NO-GO (ProofOps) and which R2 showed is commoditised. Qive (210k+ CNPJs) markets IBS/CBS support (https://qive.com.br/). Sittax sells "Sittax RT" (https://sittax.com.br/). ERPs must compute the new fields themselves. In 2026 the apuração is informational (ASSCON text), so money at risk is low (K5).
- **KILL** (founder NO-GO direction, K1/K9, K5).

### C17. NCM + IBS/CBS classification upkeep: **UNCERTAIN (weak)**
- **Paid labour:** "Classificação de Produtos – NCM (manutenção de classificações)" R$150–250/month; the reform one-off "Revisão e Parametrização Fiscal Completa (NCM, CFOP, CST…; testes IBS/CBS)" costs R$1,200–2,500 for ≤200 items and R$3,000–7,000 for 200–1,000 items (ASSCON). The analista de cadastro role (R$3,295.63) includes product registration (Catho link above).
- **Deliverable:** a classification table (NCM, CEST, IBS/CBS CST and classification code per SKU) exported as a spreadsheet for ERP import. Software can *generate* it, with no government portal (no K13).
- **Competition:** Systax/Vertex (enterprise, 31M rules, sales-led; https://www.systax.com.br/). Bluesoft Cosmos (GTIN→NCM) returned 403, UNVERIFIED. Whether Bling/Tiny/Omie suggest NCM or IBS/CBS codes natively is UNVERIFIED. Accounting firms may get this from their suites (UNVERIFIED).
- **Kill check:**
  - K1/K9: UNVERIFIED, not confirmed.
  - K3: high risk ("LLM classifies products" is an AI-wrapper thesis).
  - K12: partial hit; classification liability rests with the taxpayer and accountant.
  - K15: hit for the big reform re-parametrisation (one-off).
  - K10: hit for SMB buyers, since R$150–250/month maintenance is below 2× R$300.
  - K6: unclear.
  - K11: low (product data only).
- **Why it is not simply killed:** the only variant with aggregated volume is an **accounting firm** re-classifying *all its clients' catalogues* for the IBS/CBS transition during 2026–2027. That could be a monthly volume for a firm with 100+ commerce clients. It is not evidenced, only inferred.

### C18. Clinic virtual assistant
- A recurring 99Freelas posting (psychology practice, ~25 patients: collections, rescheduling, receipt requests) drew 261 proposals (https://www.99freelas.com.br/projects?q=notas+fiscais). The value is relational, and clinic software covers reminders and billing. **KILL** (K12, K1, K10).

### C19. Alvará / licenças renewals
- R$250–450 per event, annual (ASSCON). **KILL** (K15; municipal/Bombeiros portals, K13).

### C20. Payroll per employee
- R$87.30–165.50 per vínculo/month (ASSCON). This is the core of the accounting suites, with eSocial and the accountant's liability. **KILL** (K9, K12).

## 5. Survivor / uncertain: the uncomfortable question

**C17: "Who already pays for this exact job today, what do they pay, and why wouldn't they simply use existing software?"**
- *Who pays:* SMEs pay their accountant for NCM maintenance at a reference R$150–250/month, plus a one-off reform re-parametrisation of R$1,200–7,000 (ASSCON). No actual invoice or market-price evidence was found (reference table only).
- *Why not existing software:* unknown. Enterprise tools (Systax/Vertex) are sales-led. Whether the SMB ERPs (Bling, Tiny/Olist, Omie, Conta Azul) or the accounting suites already fill IBS/CBS classification per SKU is **UNVERIFIED**. If they do, this dies on K2/K9.
- *Honest assessment:* even if it passes, the recurring portion is below the price floor for SMEs. The large portion is a 2026–2027 one-off wave (K15), and the product thesis leans on LLM classification (K3). Expected outcome: KILL.

**What Stage D must verify (if pursued at all):**
1. Do Bling, Tiny/Olist, Omie and Conta Azul, and do Domínio, Alterdata and Questor, auto-suggest NCM and IBS/CBS classification codes per product today? (If yes, KILL.)
2. Are there self-serve Brazilian classification tools (Cosmos/Bluesoft, NCM-by-GTIN APIs) and what do they cost?
3. Do accounting firms bill clients separately for IBS/CBS re-classification, and how many SKUs does a typical commerce client have? This needs real invoices or quotes, not the ASSCON reference.
4. Is there a *monthly* volume after the transition (new SKUs per month × price), or only the one-off wave?
5. Liability: who signs off, and would a firm accept machine-generated classifications with ≤30 min of review per client per month (K14)?

## 6. Evidence gaps (UNVERIFIED)
- No freelance gig prices (Workana and Fiverr 403; 99Freelas hides budgets; GetNinjas quote-based: https://www.getninjas.com.br/).
- No market (non-reference) prices for BPO financeiro, assessoria de licitação, marketplace management or despachante services.
- No vendor prices for Acessórias, HubCount, Sittax, Qive, SIEG (403), ConLicitação, Effecti, Superlógica or the accounting suites.
- Receita Saúde / Carnê-Leão integration, municipal ISS portal fragmentation and NFS-e Nacional impact are from background knowledge only.
- Not investigated for lack of search: agronegócio (CAR is one-off, so likely K15; NF-e de produtor), despachante frota (licensing is annual, likely K15), card/marketplace settlement reconciliation (reconciliation = founder NO-GO).

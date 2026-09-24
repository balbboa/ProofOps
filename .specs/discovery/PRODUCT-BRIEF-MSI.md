# Initial Product Brief

> Origem: Discovery R6 (`research/R6-SYNTHESIS.md`, §2 e §5). Nome provisório: **"MSI Control"** (a definir).
> Status: candidato aprovado apenas para **validação** (smoke test ≤ €100). Não é GO de construção completa.

## 1. O que quero construir

Um **web app (PWA) em espanhol, para o México**, que mostra em um só lugar todas as compras parceladas **"meses sin intereses" (MSI)** de **todas as tarjetas de crédito** do usuário, inclusive cartões de loja (Liverpool, Coppel etc.).

Ele responde três perguntas:

- "Quanto eu devo de MSI **este mês**, somando todos os cartões?"
- "Quanto vou dever nos **próximos meses**?"
- "Em que **data** fico livre dessas parcelas?"

Modelo de negócio: assinatura (mensal/anual) com trial, cobrada na web (Paddle ou Stripe). Aquisição por **SEO**: uma calculadora gratuita de MSI e páginas-guia por banco ("cómo ver mis meses sin intereses BBVA / Nu / Liverpool").

É uma réplica geográfica de um modelo com receita verificada: **Parceladinho** (Brasil, parcelas de cartão, US$2,07k MRR, 444 assinantes, lançado em 2026, crescimento por ASO + SEO).

---

## 2. Problema

- No México, MSI é hábito de massa:
  - ~50% dos compradores planejavam usar MSI no Buen Fin 2025;
  - ~19,3% do saldo de cartão de crédito é MSI (Banxico);
  - >30% dos portadores já atrasaram pagamento;
  - 42,1% não pagam a fatura total.
- As parcelas se **acumulam em vários cartões**, e cada banco só mostra o próprio cartão no seu app. Ninguém vê o total comprometido nos próximos meses.
- Consequências:
  - o "susto de janeiro" (Buen Fin + Natal + fim de ano);
  - pagar só o mínimo e cair em juros rotativos;
  - atrasos com multa e impacto no bureau de crédito.
- Workaround atual: memória, planilha (há uma planilha de MSI sendo vendida no Gumroad) ou abrir o app de cada banco.
- Os resultados de busca para calculadora/controle de MSI são fracos: calculadoras genéricas dos EUA, um post no Medium e uma página pequena.

---

## 3. Usuários

- **Usuário/pagante principal:** pessoa física no México, 22–45 anos, com **2 ou mais cartões de crédito** (incluindo cartões de loja), que compra em MSI com frequência e sente perda de controle.
- **Pico de aquisição:** semanas antes e depois do **Buen Fin** (meados de novembro) e em janeiro ("cuesta de enero").
- **Fora do escopo do MVP:** empresas, contadores, casais/família com conta compartilhada, outros países (Colômbia, Chile e Argentina são expansão futura).
- **Questão aberta:** o usuário com um único cartão tem valor suficiente para pagar? Hipótese: não. O paywall deve mirar quem tem 2+ cartões.

---

## 4. Experiência desejada

- **Primeira tela útil em < 2 minutos, sem cadastro:**
  1. adicionar os cartões (nome, dia de corte, dia de pagamento);
  2. adicionar as compras em MSI (valor total, número de meses, data da compra, cartão).
- **Tela principal:**
  - "Este mês: $X em MSI";
  - linha do tempo dos próximos 12 meses;
  - a "data de liberdade" (quando a última parcela termina).
- **Simulação "antes de comprar":** "se eu comprar $Y em Z meses, como fica cada mês?". É uma decisão no momento da compra, não só um relatório.
- **Lembretes** antes da data de pagamento de cada cartão (e-mail e/ou web push).
- Linguagem simples, espanhol mexicano, mobile-first, instalável como PWA.
- **Paywall claro, depois de gerar valor:**
  - grátis: 1 cartão e poucas compras;
  - pago: múltiplos cartões, projeção completa, lembretes.
- **Nunca** pedir senha de banco nem conectar a contas bancárias.

---

## 5. Funcionalidades que imagino

1. **Calculadora pública de MSI** (sem login). É a página de SEO e a porta de entrada.
2. **Cadastro manual de cartões:** banco/loja, apelido, dia de corte, dia de pagamento.
3. **Cadastro manual de compras MSI:**
   - valor, meses, data, cartão, descrição;
   - regra de corte: uma compra feita depois da data de corte entra na fatura seguinte.
4. **Projeção mensal:**
   - total por mês e por cartão;
   - parcelas restantes;
   - data em que a última parcela termina.
5. **Simulador "e se eu comprar?"**
6. **Lembretes** de data de pagamento.
7. **Conta do usuário:**
   - login por e-mail/magic link, para sincronizar entre dispositivos e habilitar lembretes;
   - **questão aberta:** local-first sem conta até o paywall?
8. **Assinatura:**
   - trial de 7 dias;
   - plano mensal (~MXN 49) e anual (~MXN 399);
   - via Paddle ou Stripe; checkout hospedado pelo provedor.
9. **Páginas-guia SEO por banco/loja** (conteúdo estático).
10. **Exportar dados** (CSV) e **excluir conta**.

---

## 6. Funcionalidades futuras

- Leitura do **estado de cuenta** em PDF ou foto para importar MSI automaticamente (por banco; possivelmente com LLM e validação humana).
- Empacotar para App Store / Google Play (só se a conversão paga validar).
- Outros países: Colômbia e Chile (cuotas), Argentina (cuotas sin interés).
- Compras parceladas fora do cartão: BNPL (Aplazo, Kueski Pay), "pagos quincenales".
- Alertas de "limite comprometido" e metas de quitação.
- Compartilhamento familiar.

---

## 7. O que NÃO quero

- Conexão com bancos (Open Finance, scraping, credenciais bancárias).
- Aconselhamento financeiro/de crédito personalizado, ou qualquer coisa que exija licença.
- App nativo no MVP.
- Anúncios (AdSense) como modelo de receita.
- Dashboard complexo, gráficos sofisticados, analytics avançado.
- Multi-idioma no MVP (só es-MX).
- Suporte por telefone/WhatsApp; onboarding manual; vendas.
- IA como tese do produto. O cálculo de MSI é determinístico.
- Jev ou Treg como dependência.
- Custos fixos acima de ~€35/mês antes de receita.

---

## 8. Stack

Proposta inicial, a validar no Discovery. O fundador deve confirmar a stack com que já tem familiaridade.

- **Front-end:** PWA mobile-first (ex.: Next.js ou SvelteKit), SSR/SSG para as páginas de SEO.
- **Back-end:** API simples no mesmo projeto; Postgres.
- **Hospedagem:** VPS Hetzner (Docker/Coolify), ~€5–8/mês. Vercel Hobby proíbe uso comercial.
- **Auth:** magic link por e-mail.
- **E-mail transacional:** provedor com free tier (ex.: Resend, Brevo) para lembretes e login.
- **Pagamentos:** Paddle (merchant of record, aceita pessoa física no Brasil; recomendação provisória da R1) ou Stripe. **Questão aberta:** suporte a MXN e meios locais (OXXO, SPEI, cartão de débito).
- **Analytics:** privacy-friendly e barato (ex.: Plausible self-hosted ou Umami).
- **Sem IA no MVP.**

---

## 9. Restrições

- Desenvolvedor solo, em paralelo a um emprego; poucas horas por semana.
- Orçamento ~€35/mês até haver receita.
- Fundador no Brasil, vendendo no México. Implicações de impostos e entidade: ver R1 (pessoa física + carnê-leão; confirmar com contador).
- Dados pessoais financeiros de terceiros:
  - aplicar a LFPDPPP (lei de proteção de dados do México) e a LGPD;
  - minimizar dados: sem número de cartão, sem dados bancários; só apelido, datas e valores.
- Idioma do produto: espanhol mexicano. O fundador fala português; os textos precisam de revisão.
- **Prazo:**
  - smoke test em ~1 semana;
  - se aprovado, MVP publicado **antes do Buen Fin 2026 (meados de novembro)**.
- Operação ≤ 1–2 h/semana depois do lançamento; suporte só assíncrono (e-mail).

---

## 10. Objetivo do MVP

Provar que mexicanos com vários cartões **pagam** para controlar seus MSI.

**Gates com limites fixados antes (R6 §2):**

1. **Verificação manual das lojas (15 min, fundador):** matar se já existir, nas buscas por "meses sin intereses", "MSI" e "control tarjetas" na App Store/Google Play México, um app de MSI multi-cartão com **≥ 100 mil instalações, nota ≥ 4,3 e atualização nos últimos 6 meses**.
2. **Smoke test (≤ €100 em anúncios, ~1 semana):** landing em espanhol com preço, waitlist e pré-venda do plano anual com 50% de desconto.
   - **Construir** se ≥ 20% dos visitantes entrarem na waitlist **e** houver ≥ 5 pré-vendas (ou ≥ 3% clicarem na opção paga).
   - **Matar** se < 5% entrarem na waitlist depois de ≥ 500 visitantes.
3. **MVP:** publicado antes do Buen Fin. Sucesso = **≥ 100 assinantes pagantes até o fim de janeiro de 2027**. Parar se < 30.

Meta de longo prazo: ~€1k MRR ≈ 300–400 assinantes.

---

## 11. O que espero de você

Não comece implementando.

Use o Master Prompt fornecido junto deste documento.

Primeiro faça o Discovery.

Questione todas as partes deste briefing que possam gerar:

* ambiguidades;
* decisões arquiteturais incorretas;
* gaps funcionais;
* problemas de segurança;
* problemas de multi-tenancy;
* problemas de UX;
* problemas de escalabilidade;
* problemas de integração;
* problemas de testes;
* problemas de produção.

Não assuma que minha descrição está completa.

Se perceber que alguma funcionalidade ou decisão importante está faltando, questione.

Se houver múltiplas soluções razoáveis, apresente as alternativas e recomende uma.

Seu objetivo é garantir que, antes do Planning Gate, exista uma especificação suficientemente completa para que outro agente, sem acesso ao histórico desta conversa, consiga implementar o sistema corretamente utilizando apenas os artefatos persistidos no projeto.

Depois que o planejamento estiver completo e o Planning Gate for aprovado, execute o processo autonomamente conforme definido no Master Prompt.

# Nexus — Painel de Planejamento WhatsApp

Painel estático (HTML/CSS/JS, sem build, sem dependências de servidor) para planejamento e projeção de resultados de campanhas de tráfego pago com foco em **geração de conversas via WhatsApp** (Click to WhatsApp, QR Code, Bio Link, Orgânico etc.), desenvolvido para a **Nexus Marketing Advisory**.

> Este painel faz parte de um conjunto junto com o [Painel de Planejamento Landing Page](https://github.com/focustrafficcba-ai/nexus-painel-plan-landing-page), mantido em repositório separado.

## 📊 O que o painel faz

Projeta o funil completo de uma campanha voltada à geração de conversas no WhatsApp:

**Alcance → Conversas Iniciadas → Responderam → Qualificados → Vendas → Receita**

## ⚙️ Como usar

1. Abra o arquivo `.html` direto no navegador (ou acesse pelo link publicado).
2. Preencha os **Parâmetros Globais** (orçamento total, meta de conversas, meta de vendas, ticket médio).
3. Clique em **"Nova Ação"** para cadastrar cada campanha/canal com suas taxas estimadas (CTR → WhatsApp, taxa de resposta, taxa de qualificação, taxa de fechamento).
4. O painel calcula automaticamente:
   - Projeção por ação (tabela principal)
   - Projeção consolidada por origem/canal (Meta, Google, Orgânico, LinkedIn, TikTok etc.)
   - Projeção total do mês + ROI estimado
   - Progresso das metas de Conversas e Vendas (verde = atingida, vermelho = abaixo do esperado)
5. Exporte o painel preenchido em **PNG** ou **PDF** pelos botões no topo, para enviar a clientes ou arquivar.

## ⚠️ Importante sobre as projeções

As projeções **não usam dados de mercado, benchmark ou histórico automático** — são um cálculo de funil baseado 100% nas taxas que você insere manualmente em cada campo (CTR, taxa de resposta, qualificação, fechamento etc.).

> Use como ferramenta de **estimativa e simulação** ("se eu investir X com essas taxas, qual o retorno esperado?"), ajustando as taxas conforme o histórico real de cada nicho/cliente. Resultados de tráfego pago nunca são garantidos — trate sempre como cenário hipotético, não como compromisso fechado com o cliente.

## 💾 Armazenamento de dados

Os dados preenchidos ficam salvos via `localStorage`, **no navegador de cada dispositivo/usuário** que acessa o painel — não há banco de dados ou sincronização entre dispositivos. Isso significa:

- Os dados persistem entre sessões no mesmo navegador/computador.
- Limpar o cache do navegador apaga os dados salvos.
- Acessar de outro dispositivo não traz os dados preenchidos anteriormente.
- Para guardar um registro permanente, exporte em PNG/PDF após preencher.

## 🧱 Stack

- HTML + CSS puro (sem framework)
- JavaScript vanilla
- [Chart.js](https://www.chartjs.org/) — gráfico de distribuição por origem
- [html2canvas](https://html2canvas.hertzen.com/) + [jsPDF](https://github.com/parallax/jsPDF) — exportação em PNG/PDF

## 🚀 Deploy

Projeto estático — pode ser publicado em qualquer hospedagem estática (Vercel, Netlify, GitHub Pages etc.) sem necessidade de build ou configuração adicional.

---
Desenvolvido para uso interno da **Nexus Marketing Advisory** — Metodologia AXIS.

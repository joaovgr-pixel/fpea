# Opalus Health Services — Modelo FP&A e Dashboard Financeiro

**Versão:** 1.0  
**Data:** 28 de Julho de 2026  
**Padrão:** FAST Standard (Flexible, Appropriate, Structure, Transparent)  
**Moeda:** BRL (R$)  
**Período de Análise:** Janeiro/2023 a Dezembro/2025  

---

## 1. Visão Geral do Projeto

Este repositório contém o modelo financeiro e o dashboard interativo desenvolvido para a **Opalus Health Services**, uma empresa líder no segmento de Home Care, Internação Domiciliar e Atendimento Particular. O objetivo central do projeto é fornecer uma estrutura robusta de Planejamento e Análise Financeira (FP&A) que permita à gestão acompanhar a performance histórica, avaliar variâncias de orçamento e projetar cenários futuros com precisão.

A solução foi construída seguindo rigorosamente o **FAST Standard**, garantindo que o modelo seja flexível o suficiente para adaptações, apropriado em suas premissas, estruturado de forma lógica e transparente em seus cálculos.

## 2. Estrutura do Projeto

O projeto está dividido em três componentes principais, disponíveis para análise e uso imediato:

1.  **Modelo Financeiro Completo (Excel):** O motor de cálculos contendo a base de dados, estrutura da DRE, KPIs e lógicas de projeção.
2.  **Dashboard Interativo (HTML):** Uma interface visual para apresentação de resultados, sem necessidade de instalação de softwares proprietários.
3.  **Modelo Estrela (CSVs):** Tabelas otimizadas para importação em ferramentas de BI como o Power BI.

### 2.1. Arquivos Disponíveis

| Arquivo | Descrição |
|---------|-----------|
| `Opalus_Health_Services_FP_A_Model.xlsx` | Modelo financeiro completo com 16 abas (Capa, Premissas, Base Financeira, DRE, KPIs, etc.). |
| `Dashboard_Opalus_Health_Services.html` | Dashboard interativo único (autocontido), requer apenas um navegador web para visualização. |
| `Dashboard_Opalus_Health_Services_FINAL.zip` | Pacote contendo o dashboard e as tabelas CSV do modelo estrela. |

## 3. Metodologia e Premissas

A modelagem financeira baseia-se em dados históricos e projeções fundamentadas no comportamento do mercado de saúde suplementar e domiciliar no Brasil.

### 3.1. Premissas Operacionais (Home Care e Internação)

*   **Ticket Médio Home Care:** R$ 4.200/mês.
*   **Ticket Médio Internação:** R$ 8.500/mês.
*   **Ticket Médio Particular:** R$ 6.800/mês.
*   **Base de Pacientes (Jan/2023):** 450 pacientes (Home Care), 85 (Internação) e 120 (Particular).
*   **Crescimento:** Taxa média de ~0.95% mensal (~12% anual), com fatores de sazonalidade aplicados.
*   **Inadimplência:** Taxa fixa de 3.5% sobre a receita bruta.

### 3.2. Premissas Financeiras e Tributárias

*   **Impostos sobre Receita:** ISS (5%), PIS/COFINS (9.25%).
*   **Impostos sobre Lucro:** IRPJ (15% + 10% sobre o excedente de R$ 240k) e CSLL (9%).
*   **Metas de Rentabilidade:** Margem EBITDA alvo de 22% e Margem Líquida alvo de 8%.

## 4. O Dashboard Financeiro

O dashboard foi desenvolvido utilizando a biblioteca **Plotly.js**, resultando em um arquivo HTML totalmente independente (sem dependência de servidores externos ou internet). Ele consolida os dados do modelo Excel em visualizações interativas e de alta qualidade.

### 4.1. Funcionalidades e Navegação

O painel superior exibe os principais indicadores de performance (KPIs) para o ano de 2025, incluindo a Receita Bruta (R$ 47,5M), EBITDA (R$ 6,0M) e Lucro Líquido (R$ 4,6M).

A interface é dividida em 8 abas temáticas:

1.  **Visão Geral:** Análise da Receita Bruta mensal, composição da receita por tipo de atendimento (Home Care, Convênios, Particular), acompanhamento do EBITDA versus a meta de 22% e evolução das margens.
2.  **DRE:** Demonstração do Resultado do Exercício consolidada, evidenciando a transição da Receita Líquida para Custos, Despesas e, finalmente, EBITDA e Lucro Líquido.
3.  **Budget vs Realizado:** Comparativo detalhado entre o orçamento projetado (Budget) e os valores efetivamente realizados (Realizado) para Receita, EBITDA e Lucro, incluindo gráficos de variação percentual.
4.  **Forecast:** Análise de cenários (Base, Otimista +10%, Conservador -8%) para projetar o comportamento futuro da empresa.
5.  **Fluxo de Caixa:** Composição dos fluxos (Operacional, Investimento, Financiamento) e a evolução do saldo acumulado.
6.  **KPIs:** Indicadores de eficiência por paciente, incluindo Receita por Paciente, Custo por Paciente e Ticket Médio.
7.  **Crescimento:** Comparativo histórico anual (2023-2025) evidenciando o crescimento composto da operação.
8.  **Margens:** Evolução das margens Bruta, EBITDA e Líquida com linhas de referência (target lines).

## 5. Estrutura de Dados para Power BI

Para empresas que já utilizam o ecossistema Microsoft, o arquivo ZIP inclui um **Modelo Estrela (Star Schema)** seguindo a metodologia Kimball, pronto para importação no Power BI Desktop:

*   **Tabelas de Fato (Fact Tables):**
    *   `fact_dre.csv`: Dados mensais da DRE.
    *   `fact_financeiro.csv`: Base detalhada de transações (faturamento e custos).
    *   `fact_kpi.csv`: Indicadores operacionais e financeiros mensais.
*   **Tabelas de Dimensão (Dimension Tables):**
    *   `dim_date.csv`: Calendário completo (Ano, Mês, Trimestre, Semestre).
    *   `dim_centro_custo.csv`: Estrutura de centros de custo (Home Care, Internação, Administrativo, etc.).
    *   `dim_conta_contabil.csv`: Plano de contas detalhado.

## 6. Como Utilizar

### Visualizando o Dashboard
Basta fazer o download do arquivo `Dashboard_Opalus_Health_Services.html` e abri-lo em qualquer navegador web moderno (Chrome, Edge, Safari, Firefox). Não é necessário instalar nenhuma dependência ou estar conectado à internet.

### Importando para Power BI
1.  Extraia o arquivo `Dashboard_Opalus_Health_Services_FINAL.zip`.
2.  Abra o Power BI Desktop.
3.  Selecione **Obter Dados > Pasta** e aponte para a pasta extraída.
4.  Conecte as tabelas Fato às tabelas de Dimensão através dos campos de chave primária (ex: `date_key`, `cc_key`).

## 7. Considerações Finais

Este modelo foi projetado para servir como um "single source of truth" para a Opalus Health Services. A separação clara entre premissas, cálculos e outputs garante que futuras atualizações de orçamento ou novas projeções possam ser realizadas de forma ágil e segura, mantendo a integridade dos dados históricos.

---
*Documento gerado para fins de documentação de portfólio FP&A.*

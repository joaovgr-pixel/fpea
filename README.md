#  Health Services — Case FP&A

**Versão:** 1.0  
**Data:** 28 de Julho de 2026  
**Padrão:** FAST Standard (Flexible, Appropriate, Structure, Transparent)  
**Moeda:** BRL (R$)  
**Período de Análise:** Janeiro/2023 a Dezembro/2025  

---

# 1. Visão Geral do Projeto

Este repositório apresenta uma solução completa de **Planejamento e Análise Financeira (FP&A)** desenvolvida para a ** Health Services**, empresa fictícia do segmento de Home Care, Internação Domiciliar e Atendimento Particular.

O projeto integra três pilares principais:

- 📊 **Modelo Financeiro em Excel** seguindo o FAST Standard;
- 📈 **Dashboard Executivo em HTML** desenvolvido com Plotly.js;
- 🐍 **Notebook Python** para Forecast e análises quantitativas.

A solução foi desenvolvida para simular um ambiente corporativo real de FP&A, permitindo:

- Análise histórica de resultados;
- Acompanhamento Budget vs Realizado;
- Projeção de cenários;
- Forecast estatístico;
- Análise de indicadores financeiros e operacionais.

---

# 2. Estrutura do Projeto

## 📊 Modelo Financeiro em Excel

O modelo financeiro representa o núcleo do planejamento financeiro.

O arquivo possui **16 abas estruturadas conforme o FAST Standard**, incluindo:

- Central de premissas editáveis;
- Plano de contas completo;
- Bases detalhadas de receitas, custos e despesas;
- **1.755 transações individuais distribuídas em 36 meses**;
- Demonstração do Resultado do Exercício (DRE);
- Margens financeiras;
- Budget vs Realizado;
- Análise de variâncias;
- Forecast em três cenários;
- Demonstração de Fluxo de Caixa;
- KPIs financeiros e operacionais;
- Modelo estrela (Star Schema) preparado para Power BI.

---

## 📈 Dashboard Financeiro em HTML

Dashboard executivo desenvolvido em **HTML autocontido utilizando Plotly.js**.

Características:

- Arquivo único;
- Funcionamento offline;
- Sem necessidade de instalação;
- Visualizações interativas;
- Navegação por abas.

Indicadores apresentados:

- Receita Bruta;
- EBITDA;
- Lucro Líquido;
- Margem EBITDA;
- Pacientes Ativos;
- Evolução da receita;
- DRE;
- Budget vs Realizado;
- Forecast;
- Fluxo de Caixa;
- KPIs operacionais.

O dashboard possui 8 abas:

1. Visão Geral  
2. DRE  
3. Budget vs Realizado  
4. Forecast  
5. Fluxo de Caixa  
6. KPIs  
7. Crescimento  
8. Margens  

---

## 🐍 Notebook Python — Forecast Analysis

O notebook aplica técnicas quantitativas de previsão financeira.

Inclui:

- Decomposição aditiva de séries temporais;
- SARIMAX(1,1,1)(1,1,1,12);
- Intervalos de confiança de 95%;
- Comparação MAE e MAPE;
- Regressão linear com variáveis sazonais;
- Análise Tornado de sensibilidade;
- Waterfall de variação;
- Projeção financeira de 12 meses.

---

# 3. Arquivos Disponíveis

| Arquivo | Descrição |
|---|---|
| Dashboard_Opalus_Health_Services_FINAL (1).zip | Dashboard HTML autocontido e arquivos CSV do modelo estrela. |
| Excel_modelo_financeiro | Modelo financeiro completo em Excel com 16 abas seguindo FAST Standard. |
| Forecast_Analysis.ipynb | Notebook Python de forecast e análises quantitativas. |
| read_me | Documentação do projeto. |

---

# 4. Metodologia e Premissas

## Premissas Operacionais

- Ticket Médio Home Care: **R$ 4.200/mês**
- Ticket Médio Internação: **R$ 8.500/mês**
- Ticket Médio Particular: **R$ 6.800/mês**

Base inicial:

| Segmento | Pacientes |
|---|---:|
| Home Care | 450 |
| Internação | 85 |
| Particular | 120 |

Premissas:

- Crescimento médio mensal: 0,95%;
- Crescimento anual aproximado: 12%;
- Inadimplência: 3,5%.

---

# 5. Dashboard Financeiro

Principais indicadores de 2025:

- Receita Bruta: **R$ 47,5 milhões**
- EBITDA: **R$ 6,0 milhões**
- Lucro Líquido: **R$ 4,6 milhões**

O dashboard permite:

- Visualização;
- Análise de desempenho;
- Comparação orçado vs realizado;
- Avaliação de cenários futuros.

---

# 6. Estrutura de Dados para Power BI

O projeto utiliza um modelo dimensional **Star Schema**.

## Tabelas Fato

### fact_dre.csv

Dados mensais da DRE.

### fact_financeiro.csv

Base detalhada de receitas, custos e despesas.

### fact_kpi.csv

Indicadores financeiros e operacionais.

## Tabelas Dimensão

### dim_date.csv

Calendário corporativo:

- Ano;
- Mês;
- Trimestre;
- Semestre.

### dim_centro_custo.csv

Centros de custo:

- Home Care;
- Internação;
- Administrativo.

### dim_conta_contabil.csv

Plano de contas financeiro.

---

# 7. Como Utilizar

## Dashboard HTML

1. Extraia:

`Dashboard_Opalus_Health_Services_FINAL (1).zip`

2. Abra o arquivo HTML no navegador.

Não é necessário instalar nenhuma ferramenta.

---

## Modelo Excel

Abra:

`Excel_modelo_financeiro`

Atualize as premissas conforme necessidade.

---

## Notebook Python

Execute:

`Forecast_Analysis.ipynb`

O notebook reproduz:

- Forecast;
- Modelos estatísticos;
- Sensibilidade;
- Projeções.

---

# 8. Considerações Finais

Este projeto representa uma solução completa de FP&A, integrando:

- Financial Modeling;
- Business Intelligence;
- Forecast Estatístico;
- Data Analytics.

A arquitetura foi desenvolvida como um **single source of truth financeiro**, garantindo:

- Transparência;
- Governança;
- Escalabilidade;
- Facilidade de atualização.

---

**Projeto desenvolvido por João Vitor Rodrigues, para demonstração de competências em FP&A.**


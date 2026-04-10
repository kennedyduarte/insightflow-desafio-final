# 🚀 InsightFlow - Análise de Dados de E-commerce

## 📋 Visão Geral do Projeto

Este projeto foi desenvolvido como parte do **Desafio Final de Data Analytics** do Projeto Desenvolve. O objetivo foi transformar dados brutos de e-commerce em insights acionáveis, realizando um ciclo completo de análise de dados.



## 📁 Estrutura do Projeto
insightflow-desafio-final/
│
├── data/
│ ├── ecom_data_raw.csv # Dados brutos
│ └── ecom_data_clean.csv # Dados tratados
│
├── notebooks/
│ ├── 01_geracao_e_etl.ipynb # Sprint 1
│ ├── 02_analise_exploratoria.ipynb # Sprint 2
│ └── 03_modelo_preditivo.ipynb # Sprint 4
│
├── dashboard/
│ ├── dashboard_insightflow.pbix # Dashboard Power BI
│ ├── previsoes_vendas.png # Gráfico de previsões
│ └── sazonalidade_mensal.png # Gráfico de sazonalidade
│
├── database/
│ └── ecom.db # Banco SQLite
│
├── requirements.txt # Dependências Python
└── README.md # Documentação

### 🎯 Objetivos Alcançados

- ✅ **Sprint 1 (ETL):** Limpeza e preparação dos dados com SQLite
- ✅ **Sprint 2 (EDA):** Análise exploratória com segmentação RFM
- ✅ **Sprint 3 (Dashboard):** Criação de dashboard interativo no Power BI
- ✅ **Sprint 4 (Modelo Preditivo):** Previsão de vendas com Regressão Linear

---

## 📊 Principais Insights de Negócio

### 1. Visão Geral das Vendas
| Métrica | Valor |
|---------|-------|
| Período analisado | Janeiro/2023 a Dezembro/2024 |
| Total de vendas | 5.390 transações |
| Receita total | R$ 6.681.842,72 |
| Ticket médio | R$ 1.239.67 |
| Clientes únicos | 300 |

### 2. Performance por Categoria
| Categoria | Receita | % do Total | Ticket Médio |
|-----------|---------|------------|--------------|
| Eletrônicos | R$ 3.302.278,00 | 49,42% | R$ 2.999,34 |
| Casa e Cozinha | R$ 1.374.832,37	 | 20,58% | R$ 1.208,11 |
| Esportes | R$ 927,707,38	 | 13,88% | R$ 901,56 |
| Roupas | R$ 822.199,03	 | 12,30% | R$ 781,56 |
| Livros | R$ 254.825,94	 | 3,81% | R$ 238,16  |

**💡 Insight:** Eletrônicos dominam as vendas, representando quase metade da receita total.

### 3. Sazonalidade
- **Melhor dia da semana:** Sexta-feira foi o dia da semana com maior faturamento total, enquanto Quinta-feira foi o dia com mais transações. Segunda-feira também se destacou
sendo o segundo dia com maior faturamento, e segundo dia com mais vendas.
- **Melhor mês do ano:** Abril foi o mês com maior faturamento e maior número de vendas. Dezembro e Setembro também se destacam.
- **Maior crescimento:** Dezembro de 2024, crescimento de 56,8% em relação ao mês anterior.

**💡 Insight:** Explorar Abril como padrão
Repetir estratégias usadas nesse mês
Criar campanhas sazonais:
“Ofertas de Abril”
“Semana do consumidor inteligente”
👉 Transformar um pico histórico em padrão previsível.

### 4. Segmentação de Clientes (RFM)

| Segmento | Clientes | % | Ticket Médio | Ação Recomendada |
|----------|----------|---|--------------|------------------|
| 🏆 Campeões | 42 | 14% | R$ 1.387,42 | Programa de fidelidade VIP |
| ❤️ Leais | 89 | 29,67% | R$ 1.329,79 | Cross-selling e upsell |
| 🌱 Promissores | 99 | 33% | R$ 1.152,45 | Cupons de desconto |
| 🆕 Novatos | 45 | 15% | R$ 1.119,78 | Onboarding e primeira compra |
| ⚠️ Em Risco | 25 | 8,33% | R$ 990,89 | Campanha de reativação |

**💡 Insight:** 77% dos clientes são valiosos (Campeões + Leais + Promissores). Foco em reter os 15% 'Novatos' e os 8,33% "Em Risco".

### 5. Top 5 Produtos por Receita

| Produto | Categoria | Receita |
|---------|-----------|---------|
| Fone de Ouvido | Eletrônicos | R$ 476,769,45 |
| Teclado | Eletrônicos | R$ 434.338,28 |
| Smartwatch | Eletrônicos | R$ 430.262,94 |
| Caixa de Som | Eletrônicos | R$ 428.116,48 |
| Tablet | Eletrônicos | R$ 394.221,08

Todos os produtos que estão no Top 5 de Maiores Receitas são da categoria Eletrônicos. |

---

## 🔮 Modelo Preditivo - Previsão de Vendas

### Metodologia
- **Modelo:** Regressão Linear
- **Variável preditora:** Tempo (mês sequencial)
- **Variável alvo:** Receita mensal

### Resultados do Modelo

| Métrica | Valor | Interpretação |
|---------|-------|---------------|
| R² | 0.0007 | Modelo explica menos de 50% da variação nas vendas |
| MAE | R$  43.967,86 | Erro médio de previsão |
| MAPE | 16.81%% | 

### Previsões para os próximos 3 meses

| Mês | Previsão de Vendas |
|-----|-------------------|
| Janeiro/2025 | R$ 275.343,85 |
| Fevereiro/2025 | R$ 275.111,72 |
| Março/2025 | R$ 274.879,60 |

**💡 Insight:** Devemos reverter este Coeficiente (inclinação): R$ -232.12 por mês.

---

## 🛠️ Tecnologias Utilizadas

| Ferramenta | Finalidade |
|------------|------------|
| **Python (Pandas, NumPy)** | ETL e análise de dados |
| **SQLite** | Banco de dados relacional |
| **Power BI** | Dashboard interativo |
| **Scikit-learn** | Modelo de regressão linear |
| **Matplotlib/Seaborn** | Visualizações |
| **Git/GitHub** | Versionamento |

------------------


## 🎯 Recomendações Finais para o Negócio

### Curto Prazo (Próximo mês)
1. **Campanha de reativação** para clientes "Em Risco" com cupom de 20% OFF
2. **Reforçar estoque** de produtos Eletrônicos para Black Friday
3. **Aumentar investimento** em marketing aos Finais de Semana.

### Médio Prazo (Próximo trimestre)
1. **Implementar programa de fidelidade** para clientes "Campeões"
2. **Criar combos** entre produtos de alta e baixa rotatividade
3. **Desenvolver coleção sazonal** para meses de pico (Nov/Dez)

### Longo Prazo (Próximo ano)
1. **Expandir catálogo** da categoria Eletrônicos (maior margem)
2. **Investir em CRM** para aumentar recorrência de compra
3. **Monitorar previsões** e ajustar metas trimestralmente

---

## 📈 Como Executar o Projeto

```bash
### 1. Clonar o repositório

git clone https://github.com/kennedyduarte/insightflow-desafio-final
cd insightflow-desafio-final

#2. Criar ambiente virtual:

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

#3. Instalar dependências:

pip install -r requirements.txt

#4. Executar notebooks:

jupyter notebook

#5. Abrir dashboard Power BI:

Abrir arquivo dashboard/dashboard_insightflow.pbix
Atualizar fontes de dados se necessário

------------------------------------------------------------

Este projeto é para fins educacionais.
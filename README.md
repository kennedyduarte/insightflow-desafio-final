# 🚀 InsightFlow - Análise de Dados de E-commerce

## 📋 Visão Geral do Projeto

Este projeto foi desenvolvido como parte do **Desafio Final de Data Analytics** do Projeto Desenvolve. O objetivo foi transformar dados brutos de e-commerce em insights acionáveis, realizando um ciclo completo de análise de dados.



## 📁 Estrutura do Projeto

**insightflow-desafio-final/**
- **data/**
  - `ecom_data_raw.csv` - Dados brutos
  - `ecom_data_clean.csv` - Dados tratados
- **notebooks/**
  - `01_geracao_e_etl.ipynb` - Sprint 1: Geração e limpeza dos dados
  - `02_analise_exploratoria.ipynb` - Sprint 2: Análise exploratória e RFM
  - `03_modelo_preditivo.ipynb` - Sprint 4: Modelo de previsão de vendas
- **dashboard/**
  - `dashboard_insightflow.pbix` - Dashboard Power BI
  - `previsoes_vendas.png` - Gráfico de previsões do modelo
  - `sazonalidade_mensal.png` - Gráfico de sazonalidade por mês
- **database/**
  - `ecom.db` - Banco de dados SQLite
- `requirements.txt` - Dependências do Python
- `README.md` - Documentação completa do projeto

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

--------------

## 🧠 Insights Estratégicos Avançados

### 🧠 1. Concentração de Receita (Risco de Dependência)
Apesar de Eletrônicos representarem quase metade da receita (49,42%), essa concentração pode indicar um **risco estratégico**, já que o negócio depende fortemente de uma única categoria.  
Oscilações de mercado, concorrência ou problemas de estoque nessa categoria podem impactar significativamente o faturamento total.

---

### 💰 2. Relação entre Ticket Médio e Participação
A categoria Eletrônicos não apenas lidera em receita, mas também possui um ticket médio significativamente superior às demais.  
Isso indica que o crescimento do faturamento está mais ligado ao **alto valor por transação** do que ao volume de vendas.

---

### 📦 3. Possível Efeito “Produtos Âncora”
O fato de todos os Top 5 produtos serem da categoria Eletrônicos sugere a presença de **produtos âncora**, que atraem grande parte da receita.  
Esses produtos podem estar funcionando como principal motor de vendas, mas também aumentam a dependência de poucos itens.

---

### 📉 4. Baixa Representatividade de Livros (Oportunidade ou Despriorização?)
A categoria Livros representa apenas 3,81% da receita total, o que pode indicar:

- baixa demanda  
- pouca variedade de produtos  
- falta de estratégia de marketing específica  

Isso pode representar uma **oportunidade de crescimento não explorada** ou uma categoria com baixo potencial estratégico.

---

### 🧠 5. Comportamento Pré-Fim de Semana
O aumento de faturamento na Sexta-feira pode estar associado a um comportamento de consumo voltado ao **lazer**, antecipação do fim de semana ou maior disponibilidade financeira nesse período.

---

### 📊 6. Abril como Pico: Possíveis Causas
O destaque do mês de Abril pode estar relacionado a fatores como:

- campanhas promocionais específicas  
- comportamento pós-início de ano (retomada de consumo)  
- datas comerciais relevantes (como Páscoa)  

Isso sugere que o desempenho pode ser **replicável com estratégias direcionadas**.

---

### 📈 7. Dezembro: Crescimento Acelerado (Efeito Sazonal Clássico)
O crescimento expressivo em Dezembro de 2024 (56,8%) reforça um padrão clássico de e-commerce, impulsionado por:

- festas de fim de ano  
- maior circulação de renda (13º salário)  
- eventos promocionais como Black Friday  

Isso indica forte influência de fatores externos no desempenho.

---

### 🧑‍🤝‍🧑 8. Alta Qualidade da Base de Clientes
A concentração de 77% dos clientes em segmentos valiosos indica uma **base relativamente saudável**, com bom potencial de retenção e monetização.

---

### ⚠️ 9. Risco Futuro: Base Pode Envelhecer
Apesar da boa distribuição atual, a presença de apenas 15% de novos clientes pode indicar um risco de **baixa renovação da base no longo prazo**, caso não haja estratégias consistentes de aquisição.

---

### 📊 10. Volume vs Base de Clientes
Com 5.390 transações para apenas 300 clientes, há uma média de aproximadamente **18 compras por cliente**, indicando um bom nível de recorrência.

---

### 🎯 11. Oportunidade de Cross-Selling Inteligente
Como Eletrônicos dominam as vendas, existe uma oportunidade clara de utilizar esses produtos como **porta de entrada para vendas cruzadas** com outras categorias, aumentando o valor total por cliente.




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
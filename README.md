# Olist E-commerce Analysis

Análise exploratória completa do dataset público da Olist — maior plataforma de marketplace do Brasil — com foco em comportamento de compra, qualidade de entrega e satisfação de clientes.

---

## Contexto

A Olist conecta pequenos lojistas a grandes marketplaces. Este projeto usa dados reais de **~100 mil pedidos realizados entre 2016 e 2018**, disponibilizados publicamente no Kaggle, para responder perguntas de negócio relevantes sobre o ciclo de vendas.

> **Por que isso importa para uma empresa real?**
> Análises como essa permitem identificar gargalos na entrega que afetam a avaliação dos clientes, categorias de produto com alto potencial não explorado, regiões com demanda crescente e baixa cobertura logística, e padrões de churn antes que o cliente seja perdido. Em um e-commerce com os dados reais desta natureza, os insights deste projeto poderiam embasar decisões de estoque, negociação com transportadoras e campanhas de retenção.

---

## Objetivo

Construir um portfólio de análise de dados que demonstre o ciclo completo — da qualidade dos dados até os insights acionáveis — usando ferramentas do ecossistema Python.

---

## Stack

| Ferramenta | Uso |
|---|---|
| `pandas` | manipulação e transformação de dados |
| `numpy` | operações numéricas |
| `matplotlib` | visualizações base |
| `seaborn` | visualizações estatísticas |
| `missingno` | análise visual de valores nulos |
| `ydata-profiling` | relatório automático do dataset |
| `plotly` | gráficos interativos |
| `jupyterlab` | ambiente de desenvolvimento dos notebooks |

---

## Estrutura do projeto

```
olist-ecommerce-analysis/
├── data/
│   ├── raw/          ← CSVs originais do Kaggle (não versionados)
│   └── processed/    ← dados limpos e transformados
├── notebooks/
│   ├── 01_data_quality.ipynb
│   ├── 02_eda_orders.ipynb
│   ├── 03_eda_products.ipynb
│   ├── 04_eda_customers.ipynb
│   └── 05_insights_summary.ipynb
├── reports/
│   └── figures/      ← gráficos exportados
├── src/
│   ├── data_loader.py
│   └── utils.py
├── requirements.txt
└── .gitignore
```

---

## Como reproduzir

**1. Clone o repositório**
```bash
git clone https://github.com/FelipeAraujoBS/olist-ecommerce-analysis.git
cd olist-ecommerce-analysis
```

**2. Crie o ambiente virtual e instale as dependências**
```bash
python -m venv .venv
.venv\Scripts\activate       # Windows
source .venv/bin/activate    # Mac/Linux

pip install -r requirements.txt
```

**3. Baixe os dados**

Acesse [kaggle.com/datasets/olistbr/brazilian-ecommerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), faça o download e extraia os CSVs dentro de `data/raw/`.

**4. Execute os notebooks em ordem**

Abra o JupyterLab ou VS Code e rode os notebooks na sequência numérica.

---

## Progresso

- [x] **01 · Qualidade dos dados** — carregamento dos 9 datasets, mapeamento de nulos, duplicatas e tipos. Identificados padrões esperados: datas ausentes em pedidos cancelados, campos opcionais de reviews sem preenchimento, e 261k duplicatas por design na tabela de geolocalização.
- [x] **02 · Análise de pedidos** — volume por período, sazonalidade, tempo de entrega por estado, correlação entre atraso e avaliação.
- [x] **03 · Análise de produtos** — categorias mais vendidas, ticket médio, relação entre peso e frete, avaliação por categoria.
- [ ] **04 · Análise de clientes** — distribuição geográfica, frequência de compra, segmentação RFM.
- [ ] **05 · Insights e conclusões** — consolidação dos principais achados com recomendações acionáveis.

---

## Impacto potencial em um cenário real

Se esta análise fosse aplicada aos dados reais de uma operação de e-commerce, os entregáveis poderiam incluir:

- **Redução de churn**: identificar clientes com padrão de abandono antes da segunda compra e acionar campanhas de retenção no momento certo.
- **Otimização logística**: mapear os estados com maior índice de atraso e correlacionar com queda na avaliação, embasando renegociação com transportadoras.
- **Gestão de catálogo**: detectar categorias com alto volume mas baixa avaliação — sinal de problema de qualidade ou expectativa mal gerenciada.
- **Expansão geográfica**: cruzar densidade de clientes por região com tempo médio de entrega para priorizar abertura de novos centros de distribuição.

---

## Autor

**Felipe de Araújo Bomfim dos Santos**
Backend developer em transição para análise de dados.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/felipe-de-araujo-b87386231/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:felipearaujobs@hotmail.com)

# 🏋️ Esteira de Aprendizado de Máquina — World Gym & Fitness Trends (2000–2026)

> Projeto acadêmico: pipeline completo de Machine Learning para classificação de crescimento de academias

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange?logo=scikit-learn)](https://scikit-learn.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## 📌 Descrição

Este projeto implementa uma **esteira completa de Aprendizado de Máquina** utilizando o dataset [World Gym & Fitness Trends (2000–2026)](https://www.kaggle.com/datasets), disponível no Kaggle.

O problema abordado é de **classificação multiclasse**: dado um conjunto de características de uma academia (país, tipo, mensalidade, taxa de retenção, PIB per capita, etc.), o modelo prediz se o crescimento de membros será **Alto**, **Médio** ou **Baixo**.

**Algoritmo:** Random Forest Classifier  
**Linguagem:** Python 3.10+  
**Ambiente:** Jupyter Notebook

---

## 🗂️ Estrutura do Repositório

```
ml-fitness-pipeline/
├── ml_fitness_pipeline.ipynb   ← Notebook principal (execute este)
├── README.md                   ← Documentação do projeto
├── requirements.txt            ← Dependências Python
└── imagens/                    ← Gráficos gerados automaticamente
    ├── distribuicoes.png
    ├── exploratorio.png
    ├── confusion_matrix.png
    └── feature_importance.png
```

> *O notebook inclui um gerador de dados sintético: funciona mesmo sem o CSV.

---

## 🔁 Etapas da Esteira

| # | Etapa | Descrição |
|---|-------|-----------|
| 1 | **Carregamento** | Leitura do dataset e visualização inicial |
| 2 | **Estatísticas Descritivas** | `.describe()`, contagem de nulos, distribuições, correlações |
| 3 | **Transformação de Colunas** | Log transform, Label Encoding, feature engineering |
| 4 | **Transformação de Linhas** | Remoção de duplicatas e outliers (IQR) |
| 5 | **Divisão dos Dados** | 70% treino / 15% validação / 15% teste (estratificado) |
| 6 | **Treinamento** | Random Forest com 200 árvores e balanceamento de classes |
| 7 | **Avaliação** | Acurácia + relatório de classificação (precision, recall, F1) |
| 8 | **Matriz de Confusão** | Absoluta e normalizada |
| 9 | **Predição** | Novo exemplo: academia boutique no Brasil (2025) |

---

## ⚙️ Como Reproduzir

### Pré-requisitos

- Python 3.8 ou superior instalado
- `pip` disponível no terminal

### 1. Clone o repositório

```bash
git clone https://github.com/jehpadovani/esteira_World_Gym_Fitness_Trends
cd ml-fitness-pipeline
```

### 2. Instale as dependências

```bash
pip install -r requirements.txt
```

### 3. (Opcional) Baixe o dataset original

Acesse o Kaggle, faça o download do dataset **World Gym & Fitness Trends** e coloque o arquivo `gym_fitness_trends.csv` na raiz do projeto.

Sem o CSV, o notebook usa dados sintéticos automaticamente — nenhuma configuração extra necessária.

### 4. Inicie o Jupyter e execute o notebook

```bash
jupyter notebook ml_fitness_pipeline.ipynb
```

No Jupyter, clique em **Kernel → Restart & Run All** para executar todas as células em ordem.

### 5. Verifique as saídas

Após a execução completa, os seguintes arquivos serão gerados:

| Arquivo | O que mostra |
|---------|-------------|
| `distribuicoes.png` | Histogramas das variáveis numéricas |
| `exploratorio.png` | Distribuição da variável-alvo e mapa de correlação |
| `confusion_matrix.png` | Matriz de confusão (absoluta + normalizada) |
| `feature_importance.png` | Importância relativa de cada feature no modelo |

---

## 📊 Resultados

| Métrica | Valor |
|---------|-------|
| Acurácia (teste) | ~85–90% |
| Classes preditas | Alto / Médio / Baixo |
| Feature mais importante | `retention_rate`, `log_gdp` |

---

## 🛠️ Tecnologias

| Biblioteca | Uso |
|-----------|-----|
| `pandas` | Manipulação de dados |
| `numpy` | Operações numéricas |
| `scikit-learn` | Modelagem, métricas, pré-processamento |
| `matplotlib` | Visualizações |
| `seaborn` | Heatmap de correlação |
| `jupyter` | Ambiente de execução |

---

## 📄 Licença

MIT License — fique à vontade para usar e adaptar.

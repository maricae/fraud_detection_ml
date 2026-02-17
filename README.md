# Detecção de Fraudes em Transações de Cartão de Crédito  
## Comparação de Modelos Supervisionados e Tratamento de Classes Desbalanceadas

> Trabalho de Conclusão de Curso (MBA em Data Science e Analytics – USP/Esalq)  
> Nota: 9,5

---

## ➡️ Objetivo do Projeto

O crescimento das transações digitais ampliou significativamente o risco de fraudes financeiras. Este projeto tem como objetivo desenvolver e comparar modelos de Machine Learning capazes de identificar transações fraudulentas em um cenário altamente desbalanceado.

Mais do que apenas treinar modelos, o foco está em:

- Avaliar o impacto do desbalanceamento de classes
- Comparar desempenho entre diferentes algoritmos
- Analisar trade-offs entre precisão e recall
- Discutir implicações práticas na detecção de fraude

## ➡️ Fonte dos Dados:


A base utilizada foi disponibilizada pela Universidade Livre de Bruxelas (ULB) e está disponível no Kaggle:

🔗 https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Características principais:

- 284.807 transações
- 492 fraudes
- Apenas **0,172%** de registros fraudulentos
- 28 variáveis numéricas transformadas via PCA
- Variável alvo binária (`Class`)

Trata-se de um problema clássico de classificação binária com severo desbalanceamento.

## ➡️ Desafios do Problema

- Forte desbalanceamento entre classes
- Necessidade de minimizar falsos negativos (fraudes não detectadas)
- Trade-off entre bloqueio indevido de clientes legítimos e perda financeira

A escolha das métricas de avaliação foi guiada por essas características.

## ➡️ Metodologia

### 1. Pré-processamento

- Análise exploratória dos dados
- Padronização e normalização das variáveis
- Tratamento do desbalanceamento
- Separação treino/teste

### 2. Modelos Avaliados

- K-Nearest Neighbors (KNN)
- Random Forest
- Gradient Boosting

### 3. Métricas de Avaliação

- Precision
- Recall
- F1-Score

O foco principal foi avaliar o equilíbrio entre precisão e recall, considerando que:

- Recall alto reduz fraudes não detectadas
- Precision alta reduz bloqueios indevidos

## ➡️ Resultados

Os modelos apresentaram desempenhos distintos frente ao desbalanceamento da base.

O KNN demonstrou melhor equilíbrio entre precisão e recall dentro do escopo analisado, apresentando desempenho competitivo na identificação de fraudes.

A análise evidenciou que:

- O tratamento adequado do desbalanceamento impacta significativamente os resultados.
- A escolha da métrica deve considerar o custo associado a cada tipo de erro.
- Accuracy não é uma métrica adequada para este tipo de problema.

## ➡️ Discussões Técnicas

- Problemas desbalanceados exigem métricas apropriadas.
- O uso exclusivo de accuracy pode mascarar baixo desempenho na classe minoritária.
- A seleção de modelo deve considerar não apenas performance estatística, mas impacto prático.

Extensões possíveis incluem:

- Análise de curva ROC e Precision-Recall
- Ajuste de threshold de decisão
- Matriz de custo financeiro
- Modelos baseados em Deep Learning

## ➡️ Tecnologias Utilizadas

### Linguagem
- Python

### Manipulação e Análise
- Pandas
- NumPy

### Visualização
- Matplotlib
- Seaborn

### Pré-processamento
- StandardScaler (Scikit-learn)
- RobustScaler (Scikit-learn)

### Modelagem
- KNeighborsClassifier
- RandomForestClassifier
- GradientBoostingClassifier

### Avaliação
- Precision
- Recall
- F1-Score

## ➡️ Conclusão

Modelos de Machine Learning podem auxiliar significativamente na identificação de fraudes financeiras, especialmente quando avaliados com métricas apropriadas para dados desbalanceados.

A escolha do modelo ideal depende do contexto operacional e dos custos associados a falsos positivos e falsos negativos.

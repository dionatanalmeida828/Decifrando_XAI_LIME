# Decifrando a Caixa Preta: Tornando Modelos de IA Explicáveis com LIME

## 1. Contextualização do Problema
Esta aplicação foi desenvolvida para uma empresa de crédito bancário que utiliza modelos preditivos para classificar clientes como **bom ou mau risco de crédito**.  
Embora o modelo apresente alta precisão, surgiu a necessidade de explicar decisões individuais para **clientes, gerentes e órgãos regulatórios**, garantindo transparência e conformidade.

## 2. Objetivo
- Desenvolver um modelo de machine learning para classificação de crédito.
- Aplicar a biblioteca **LIME** para gerar **explicações locais** das previsões.
- Analisar quais características impactam cada decisão do modelo.
- Discutir limitações, relevância prática e potencial uso para **compliance**.

## 3. Dataset
**Statlog (German Credit Data)** – UCI Machine Learning Repository  
- Conjunto de dados com 1000 amostras e 20 atributos.
- Classificação binária: bom (0) ou mau (1) risco de crédito.  
- [Link para download](https://archive.ics.uci.edu/ml/machine-learning-databases/statlog/german/german.data)

## 4. Modelo Preditivo
- **Random Forest Classifier**  
- **Logistic Regression** (como baseline)  
- Divisão: 80% treino / 20% teste  
- Pré-processamento: variáveis categóricas transformadas em dummies e normalização

## 5. Explainable AI com LIME
- LIME é usado para **explicações locais** (instância por instância)  
- Mostra quais features impactaram a decisão do modelo para cada cliente  
- Permite **transparência** e auxilia em **compliance e comunicação**

## 6. Principais Insights
- Features mais relevantes: idade, histórico de crédito, tipo de conta, duração do crédito.  
- LIME permite **visualizar contribuições positivas e negativas** de cada feature para a previsão.  
- Limitações: sensibilidade a pequenas variações, explicações locais não garantem compreensão global do modelo.

## 7. Como Executar
1. Clonar repositório:
```bash
git clone <link-do-repositorio>
cd nome-do-repositorio

# Decifrando a Caixa Preta: Tornando Modelos de IA Explicáveis com LIME

## Contextualização do Problema

A empresa de análise de crédito precisa compreender **por que** um modelo de classificação de risco nega ou aprova um crédito. Embora o modelo apresente alta precisão, clientes, gerentes e órgãos regulatórios questionam suas decisões, exigindo explicações claras e transparentes.

O objetivo do projeto é aplicar técnicas de **Explainable AI (XAI)** utilizando a biblioteca **LIME**, para gerar explicações locais que indiquem quais características (idade, renda, histórico de crédito, etc.) mais impactaram cada decisão do modelo.

## Objetivos

- Desenvolver um modelo de machine learning para classificação de risco de crédito.
- Aplicar **LIME** para gerar explicações locais das previsões.
- Interpretar e analisar os resultados, destacando a importância de cada feature.
- Discutir limitações, possíveis distorções e a relevância da interpretabilidade em modelos de crédito.

## Dataset Utilizado

- **Statlog (German Credit Data)**
- Fonte: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data))
- Descrição: 1.000 amostras com 20 atributos, classificação binária (bom ou mau risco de crédito).

## Modelo Preditivo

- Escolha do modelo: (ex.: Random Forest, Decision Tree, Logistic Regression)
- Justificativa: (explicar brevemente por que o modelo foi escolhido, desempenho e facilidade de interpretação)
- Métricas avaliadas: Acurácia, Precision, Recall, F1-Score.

## Implementação com LIME

- Aplicação da biblioteca **LIME** para gerar explicações locais de cada previsão.
- Visualização das contribuições de cada feature para a decisão do modelo.
- Exemplo de saída:
  - Gráficos mostrando quais características influenciaram positivamente ou negativamente cada previsão.
  
## Reflexões

- O LIME permite que cada decisão seja compreendida de forma individual.
- Auxilia no compliance e na comunicação com clientes.
- Limitações: explicações locais podem variar com pequenas mudanças nos dados; não substituem uma análise global do modelo.

## Estrutura do Projeto

- `Decifrando a Caixa Preta-1.py` – Código-fonte da aplicação do modelo e LIME.
- `README.md` – Documentação do projeto.
- `requirements.txt` – Dependências do projeto.
- `dataset.csv` (opcional) – Arquivo com os dados utilizados ou link externo para o dataset.

## Como Executar

1. Clonar o repositório:  
```bash
git clone https://github.com/dionatanalmeida828/Decifrando_XAI_LIME.git

# Cesar School | Big Data Foundation

## Projeto em Fundamentos de Big Data  
### Detecção de Transações Fraudulentas com Cartão de Crédito  

## Introdução

O presente projeto tem como tema central a Detecção de Fraudes em Transações de Cartão de Crédito, utilizando um dataset real de operações feitas por clientes europeus em setembro de 2013. O objetivo principal é desenvolver um pipeline de dados robusto capaz de identificar automaticamente transações suspeitas de fraude.

O dataset apresenta desafios críticos:

* Anonimato dos Dados: As variáveis principais (V1 a V28) foram transformadas pela Análise de Componentes Principais (PCA), o que obscurece o significado específico das features.

* Desbalanceamento Extremo: A classe de interesse (fraude) é a minoritária, representando menos de 0.2% do total das transações (492 fraudes em mais de 284 mil transações normais).

## Motivação

A relevância do projeto reside na simulação de um problema típico de Big Data e sua aplicação prática no setor financeiro.

### O Desafio em Contexto de Big Data
Mesmo sendo uma amostra de apenas dois dias, o dataset reflete a complexidade de um sistema real, onde:

* Milhares de transações acontecem a cada segundo e precisam ser analisadas em tempo real para evitar fraudes.

* O desafio é o volume de informações, a velocidade com que os dados chegam e a complexidade das variáveis que precisam ser processadas.

* É um caso onde a quantidade de dados legítimos é enorme comparada às poucas fraudes.

### Justificativa Técnica (Pré-Processamento)
A escolha das técnicas de transformação é estratégica para a modelagem:

*A normalização das features Time e Amount é crucial, pois elas não foram transformadas pelo PCA.

*O RobustScaler é utilizado para a normalização, pois é mais resistente à grande quantidade de outliers e à distribuição assimétrica da coluna Amount.

## Objetivo do Projeto 
Este projeto foi desenvolvido como parte da disciplina **Fundamentos de Big Data**.  
O objetivo é construir um **pipeline de dados** completo da ingestão até a transformação,  
usando Machine Learning em um conjunto de transações com cartões de crédito para detectar **padrões de fraudes**.

---

## Pipeline de Dados  

O pipeline foi implementado em **ambiente simulado (Google Colab + Google Drive)**,  
seguindo as três etapas principais de um fluxo de Big Data:

| Etapa | Descrição | Ferramentas |
|-------|------------|-------------|
| **Ingestão** | Leitura completa do dataset `creditcard.csv` (Kaggle) e verificação de consistência (shape, info, nulos, classes). | Python + Pandas |
| **Armazenamento** | Organização dos arquivos em diretórios no Google Drive (`/BigData/dados/`). | Google Drive |
| **Transformação** | Normalização das colunas `Time` e `Amount` com `MinMaxScaler` (faixa [0,1]). | Scikit-learn |
| **Visualização** | Histogramas das distribuições antes e depois da normalização. | Matplotlib / Seaborn |

---

## Diagrama do Pipeline  

Fluxo:  
**Dataset → Ingestão → Armazenamento → Transformação → Output (Dataset Transformado)**  

---

## Resultados e Visualizações

---

## Conclusões

---

## ⚙️ Tecnologias Utilizadas  
- **Python** – linguagem principal de manipulação e análise de dados.  
- **Pandas** – leitura, exploração e manipulação tabular.  
- **Scikit-learn** – normalização com `MinMaxScaler`.  
- **Matplotlib / Seaborn** – visualização de distribuições.  
- **Google Drive + Colab** – ambiente de execução e armazenamento.

---

## Tecnologias que Poderiam Ser Usadas para Refinamento  
| Área | Tecnologia | Justificativa |
|------|-------------|----------------|
| Ingestão em tempo real | Apache Kafka | Para ingestão contínua de transações (streaming). |
| Armazenamento distribuído | AWS ou Databricks | Para dados em nuvem com alta disponibilidade. |
| Processamento em larga escala | Apache Spark | Permite processamento paralelo de grandes volumes. |
| Visualização de insights | Power BI | Dashboards e monitoramento em tempo real. |

---

## Arquitetura Parcial Implementada (Batch)  

O projeto usa um **ETL em batch** (não streaming) no Google Colab:  

- **Ingestão:** leitura direta do CSV (`/content/drive/MyDrive/BigData/creditcard.csv`).  
- **Transformação:** normalização das colunas `Time` e `Amount` com `MinMaxScaler`.  
- **Armazenamento:** salvamento do resultado em `/dados/transformacao/creditcard_transformado.csv`.  
- **Visualização:** gráficos mostrando as distribuições antes e depois da normalização.  

---

## Equipe Responsável  

*Arthur Lins*\
*Lucas Fernandes*\
*Victor Aroucha*
---

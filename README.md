# Cesar School | Big Data Foundation

## Projeto em Fundamentos de Big Data  
### Detecção de Transações Fraudulentas com Cartão de Crédito  

## Objetivo  
Este projeto foi desenvolvido como parte da disciplina **Fundamentos de Big Data**.  
O objetivo é construir um **pipeline de dados** completo da ingestão até a transformação,  
usando um conjunto de transações com cartões de crédito para detectar **padrões de fraudes**.

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

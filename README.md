⚽ Futebol Analytics Pipeline

Pipeline de engenharia de dados para ingestão, processamento e análise de dados de partidas de futebol utilizando arquitetura Lakehouse (Bronze → Silver → Gold).

O projeto coleta dados de uma API de esportes, processa os dados em diferentes camadas e prepara as informações para análises avançadas e modelos preditivos.

🧠 Objetivo do projeto

Construir um pipeline completo de dados para:

ingestão de dados de partidas de futebol

armazenamento em arquitetura Lakehouse

limpeza e padronização dos dados

criação de datasets analíticos

suporte a análises e modelos de previsão

O projeto simula um ambiente real de engenharia de dados.

🏗 Arquitetura do pipeline
Sports API
    ↓
Bronze Layer (Raw ingestion)
    ↓
Silver Layer (Data cleaning & normalization)
    ↓
Gold Layer (Analytics & features)
🗂 Estrutura do projeto
futebol-analytics-pipeline
│
├ notebooks
│
│   ├ bronze
│   │   01_bronze_ingestion.ipynb
│
│   ├ silver
│
│   └ gold
│
├ README.md
🥉 Bronze Layer

Responsável pela ingestão bruta dos dados da API.

Características:

autenticação via token

paginação automática da API

ingestão incremental

armazenamento em tabelas Delta

Tabelas criadas:

bronze.events
bronze.teams
bronze.players
bronze.player_stats
bronze.predictions
bronze.leagues

Os dados são armazenados sem transformação significativa, preservando o formato original da API.

🥈 Silver Layer

Camada responsável por:

limpeza de dados

normalização de estruturas JSON

tipagem de colunas

criação de chaves

tratamento de valores nulos

Exemplos de transformações:

flatten de objetos JSON

separação de entidades (teams, leagues, events)

padronização de tipos de dados

🥇 Gold Layer

Camada analítica utilizada para:

agregações

métricas avançadas

datasets para dashboards

features para modelos de previsão

Exemplos:

performance de jogadores

métricas por time

estatísticas por campeonato

probabilidades de resultado

📊 Tecnologias utilizadas

Python

PySpark

Databricks

Delta Lake

REST APIs

Git / GitHub

🔄 Pipeline de ingestão

O pipeline executa os seguintes passos:

1️⃣ autenticação na API
2️⃣ extração paginada dos dados
3️⃣ normalização do JSON
4️⃣ criação de DataFrames Spark
5️⃣ persistência em Delta Tables (Bronze)

📈 Possíveis extensões do projeto

criação de dashboards com Power BI

modelos de previsão de resultados

análises de desempenho de jogadores

detecção de padrões de jogo

análises por liga e temporada

👨‍💻 Autor

Cristina Freire

Projeto desenvolvido para estudo de engenharia de dados aplicada a dados esportivos.

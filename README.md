# IoT Data Analysis with Databricks

Este repositório contém um projeto de **análise de dados de dispositivos IoT** usando **Databricks**. O foco principal do projeto é analisar dados ambientais de sensores, como **CO2**, **temperatura**, e **umidade**, para gerar insights sobre as condições climáticas.

## Descrição

Através de **SQL** e **Spark** no **Databricks**, o projeto realiza as seguintes etapas:

- Carregamento de dados de sensores IoT em formato JSON.
- Limpeza e transformação dos dados.
- Análise das métricas de sensores, com ênfase no nível de **CO2**.
- Execução de consultas SQL para extrair os dados mais relevantes e gerar insights sobre o clima.

## Tecnologias Utilizadas

- **Databricks**: Ambiente de análise de dados em nuvem.
- **Apache Spark**: Processamento de dados em grande escala.
- **SQL**: Consultas para análise de dados.
- **IoT (Internet das Coisas)**: Dispositivos de sensores que capturam dados ambientais.

## Estrutura do Projeto

- **Notebook Databricks**: Arquivos com as transformações e consultas SQL.
- **Consultas SQL**: Consultas principais para manipulação e análise dos dados.
- **Dados**: Arquivos de dados de sensores (IoT), como o `iot_devices.json`.

## Consultas SQL

Algumas das consultas SQL implementadas no projeto:

### 1. Seleção do dispositivo com o maior nível de CO2


SELECT * FROM iot
WHERE c02_level = (SELECT MAX(c02_level) FROM iot);





### 2.Consulta dos níveis de CO2, país e umidade ordenados por nível de CO2

SELECT c02_level, country, humidity
FROM iot
ORDER BY c02_level;


### Como rodar o projeto

Clone este repositório para o seu ambiente local:
git clone https://github.com/Gustavo-Pasciano93/iot-data-pipeline-databricks.git

Abra o Databricks e crie um novo notebook.

Importe os dados IoT em formato JSON e carregue-os para análise.

Execute as consultas SQL para começar a explorar os dados e gerar insights.

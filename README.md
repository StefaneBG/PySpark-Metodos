# PySpark
Este repositório contém um script PySpark que realiza várias transformações e análises em dados de uma locadora de carros. O script foi desenvolvido para ser executado em um ambiente Google Colab, mas pode ser adaptado para outros ambientes Spark.

## Descrição do Projeto

O script realiza as seguintes operações:

1. **Importação e Instalação**: Configura o ambiente PySpark no Google Colab, incluindo a instalação do Java e do Spark.
2. **Carregamento de Dados**: Carrega quatro tabelas (Cliente, Aluguel, Carro e Marca) a partir de URLs fornecidas e as converte em DataFrames do PySpark.
3. **Transformações e Análises**: Realiza várias transformações e análises nos dados, como filtragem, junção de tabelas, agregações e cálculos de métricas.
4. **Agendamento**: Inclui um exemplo de como agendar a execução automática das transformações usando o `apscheduler`.

## Pré-requisitos

- Google Colab ou um ambiente Spark local.
- Java 8 instalado (para execução local).
- Python 3.x.
- Bibliotecas Python: `pandas`, `pyspark`, `findspark`, `apscheduler`.

## Configuração do Ambiente

1. **Google Colab**:
   - O script já está configurado para rodar no Google Colab. Basta abrir o notebook no Colab e executar as células.

2. **Ambiente Local**:
   - Instale o Java 8:
     ```bash
     sudo apt-get install openjdk-8-jdk
     ```
   - Baixe e instale o Spark:
     ```bash
     wget https://archive.apache.org/dist/spark/spark-3.1.1/spark-3.1.1-bin-hadoop3.2.tgz
     tar -xvf spark-3.1.1-bin-hadoop3.2.tgz
     export SPARK_HOME=~/spark-3.1.1-bin-hadoop3.2
     export PATH=$PATH:$SPARK_HOME/bin
     ```
   - Instale as bibliotecas Python necessárias:
     ```bash
     pip install pyspark findspark pandas apscheduler
     ```

## Executando o Script

1. **Google Colab**:
   - Abra o notebook no Google Colab.
   - Execute todas as células sequencialmente.

2. **Ambiente Local**:
   - Execute o script PySpark:
     ```bash
     spark-submit pyspark2_stefane.py
     ```

## Estrutura do Código

- **Importações e Instalações**: Configuração do ambiente e instalação das dependências.
- **Carregamento de Dados**: Carrega os dados das tabelas Cliente, Aluguel, Carro e Marca.
- **Transformações e Análises**: Realiza várias operações de transformação e análise nos dados.
- **Agendamento**: Exemplo de como agendar a execução automática das transformações.

## Exemplos de Transformações

- Filtragem de aluguéis após uma data específica.
- Junção de tabelas para adicionar informações de clientes e marcas aos aluguéis.
- Cálculo de métricas como valor médio dos carros alugados e número total de clientes por estado.
- Agendamento de execução automática das transformações.

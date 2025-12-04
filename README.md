# Estudo-de-Caso-Anal-tico-Zuber-Padr-es-de-Viagens-e-Impacto-do-Clima-SQL-e-Teste-Estat-stico-
Este projeto é um estudo de caso analítico completo para a nova empresa de compartilhamento de caronas Zuber (em Chicago). O trabalho envolveu a análise de um grande banco de dados relacional para encontrar padrões de preferência de passageirose, crucialmente, testar o impacto de fatores externos (clima) na frequência e duração das viagens.

🚕 Estudo de Caso Analítico Zuber: Padrões de Viagens e Impacto do Clima (SQL e Teste Estatístico)

Descrição do Projeto

Este projeto é um estudo de caso analítico completo para a nova empresa de compartilhamento de caronas Zuber (em Chicago). O trabalho envolveu a análise de um grande banco de dados relacional para encontrar padrões de preferência de passageiros e, crucialmente, testar o impacto de fatores externos (clima) na frequência e duração das viagens.

O projeto demonstra proficiência em SQL (PostgreSQL) para extração e agrupamento de dados complexos, e em Python para Análise Exploratória de Dados (EDA) e Teste de Hipóteses Estatísticas.

🎯 Perguntas de Negócio Respondidas

Quais são as empresas de táxi mais populares em Chicago (em termos de volume de viagens)?

Quais são os bairros de destino mais populares?

A duração média das corridas do Loop para o Aeroporto Internacional O'Hare muda significativamente em sábados chuvosos? (Teste Estatístico)

Metodologia e Ferramentas

1. Análise SQL e Extração de Dados

Agregação e Grouping: Cálculo do trips_amount por empresa e average_trips por bairro de destino.

Joins Complexos: Conexão entre a tabela de viagens (trips) e a tabela de clima (weather_records) usando o timestamp (ts) como chave, mesmo sem uma conexão direta.

Lógica Condicional: Uso do operador CASE para categorizar o clima em "Bad" (Chuva/Tempestade) e "Good" (Outros).

2. Análise Python e Teste de Hipóteses

EDA: Estudo dos datasets extraídos (top 10 empresas, top 10 bairros de destino) e visualização de distribuições.

Visualização: Geração de gráficos de barras para ranking das empresas e bairros mais populares.

Teste de Hipóteses: Implementação do Teste T de Student (função ttest_ind do SciPy) para comparar a duração média das viagens sob diferentes condições climáticas.

Ferramenta

Uso

SQL (PostgreSQL)

Extração, limpeza e agregação de dados do banco de dados relacional.

Python

EDA, manipulação de dados (Pandas) e Visualização (Matplotlib).

SciPy

Implementação do Teste T de Student para inferência estatística.

💡 Resultados Chave (Insights)

Impacto do Clima Comprovado: O Teste T de Student demonstrou que a duração média das corridas do Loop para o O'Hare muda de forma estatisticamente significativa nos sábados com mau tempo (chuva/tempestade).

Média de duração no Mau Tempo: [Insira sua média aqui] segundos.

Média de duração no Bom Tempo: [Insira sua média aqui] segundos.

Decisão de Negócio: Com o valor P muito baixo (inferior ao alfa de 0.05), a hipótese nula foi rejeitada, fornecendo dados concretos para justificar preços dinâmicos (aumento do multiplicador em dias chuvosos).

<img width="3999" height="3212" alt="image" src="https://github.com/user-attachments/assets/aff89a09-f0e1-4177-a375-bda542faa52b" />

Padrões de Mercado: A análise identificou as empresas de táxi mais populares (e.g., Flash Cab) e os bairros de destino mais recorrentes (e.g., Loop), orientando estratégias de marketing e alocação de frota.

📂 Arquivos

projeto_zuber_python.ipynb: Notebook Jupyter com a EDA, visualizações e o Teste T de Student.


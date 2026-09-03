# 🚕 Análise de Dados de Mobilidade Urbana — Zuber

## 📌 Sobre o projeto

Projeto desenvolvido com o objetivo de analisar dados de corridas de táxi em Chicago para identificar padrões de utilização, distribuição das corridas entre empresas e bairros e possíveis impactos das condições climáticas na duração das viagens.

A análise foi realizada utilizando **SQL para consulta e combinação dos dados em banco de dados** e **Python para análise exploratória, visualização e teste de hipóteses**.

O projeto foi desenvolvido como parte do Sprint 7 do curso de Análise de Dados.

---

## 🎯 Objetivos

- Analisar o volume de corridas por empresa de táxi.
- Identificar os bairros com maior número médio de destinos.
- Explorar padrões de demanda e mobilidade em Chicago.
- Integrar dados de corridas com informações meteorológicas.
- Avaliar a relação entre condições climáticas e duração das corridas.
- Aplicar testes estatísticos para validar uma hipótese sobre o impacto da chuva nas viagens.

---

## 🗄️ Dados utilizados

O projeto utiliza dados provenientes de um banco de dados com informações sobre:

- **Bairros:** identificação e nome das regiões de Chicago.
- **Táxis:** identificação dos veículos e empresas responsáveis.
- **Corridas:** horários, duração, distância e bairros de origem e destino.
- **Clima:** registros horários de temperatura e condições meteorológicas.

Além dos dados consultados via SQL, foram utilizados arquivos CSV contendo resultados de consultas para a etapa de análise exploratória em Python.

---

## 🔎 Etapas da análise

### 1. Coleta e consulta dos dados

Utilização de **SQL** para:

- Filtrar dados por períodos específicos.
- Agrupar corridas por empresa de táxi.
- Identificar empresas com maior volume de corridas.
- Agrupar empresas menos representativas na categoria `Other`.
- Identificar os bairros de origem e destino.
- Combinar dados de corridas e condições meteorológicas utilizando `JOIN`.

### 2. Análise exploratória

Com **Python e Pandas**, foram analisados:

- Tipos e estrutura dos dados.
- Volume de corridas por empresa.
- Média de corridas por bairro.
- Top 10 bairros com maior número médio de destinos.

### 3. Visualização de dados

Foram criados gráficos para analisar:

- Número de corridas por empresa de táxi.
- Top 10 bairros por número médio de corridas.

### 4. Teste de hipótese

Foi analisada a hipótese:

> **A duração média das corridas do Loop para o Aeroporto Internacional O'Hare muda nos sábados chuvosos.**

Para isso, os dados de corridas foram relacionados às condições meteorológicas e foi aplicado um teste estatístico para avaliar se havia diferença significativa na duração das viagens entre as condições analisadas.

---

## 📊 Principais resultados

Os bairros com maior número médio de corridas como destino foram:

| Bairro | Média de corridas |
|---|---:|
| Loop | 10.727,47 |
| River North | 9.523,67 |
| Streeterville | 6.664,67 |
| West Loop | 5.163,67 |
| O'Hare | 2.546,90 |
| Lake View | 2.420,97 |
| Grant Park | 2.068,53 |
| Museum Campus | 1.510,00 |
| Gold Coast | 1.364,23 |
| Sheffield & DePaul | 1.259,77 |

Os resultados indicam uma concentração significativa da demanda em determinadas regiões de Chicago, especialmente em áreas centrais e de grande movimentação.

---

## 💡 Insights

- O volume de corridas não é distribuído de maneira uniforme entre os bairros.
- O **Loop** apresenta a maior média de corridas entre os destinos analisados.
- **River North, Streeterville e West Loop** também apresentam elevada demanda.
- A análise por empresa permite identificar diferenças relevantes na participação de mercado.
- A integração entre dados de corridas e clima possibilita investigar fatores externos que podem influenciar a mobilidade urbana.
- O uso de testes estatísticos permite avaliar se diferenças observadas nos dados são estatisticamente significativas.

---

## 🛠️ Tecnologias utilizadas

- **SQL** — consultas, filtros, agrupamentos e JOINs
- **Python** — análise e tratamento dos dados
- **Pandas** — manipulação e análise de dados
- **Matplotlib** — visualização de dados
- **Jupyter Notebook** — desenvolvimento e documentação da análise

---

## 📁 Estrutura do projeto

```text
zuber-mobility-analysis/
│
├── README.md
│
├── data/
│   ├── project_sql_result_01.csv
│   ├── project_sql_result_04.csv
│   └── project_sql_result_07.csv
│
└── notebook/
    └── zuber_analysis.ipynb

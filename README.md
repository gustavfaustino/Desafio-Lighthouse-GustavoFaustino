# Desafio de Ciência de Dados - Análise Cinematográfica para PProductions

## Sumário
* [Sobre o Desafio](#-sobre-o-desafio)
* [Análise Exploratória e Insights](#-análise-exploratória-e-insights)
* [Modelo Preditivo](#-modelo-preditivo)
* [Como Executar o Projeto](#-como-executar-o-projeto)
* [Estrutura do Repositório](#-estrutura-do-repositório)

---

## 챌 Sobre o Desafio

Este projeto foi desenvolvido como solução para o Desafio de Cientista de Dados da Indicium. O objetivo é atuar como um consultor para o estúdio de Hollywood "PProductions", utilizando uma base de dados cinematográficos do IMDB para orientar a produção do próximo filme do estúdio.

A análise abrange desde a limpeza e tratamento dos dados até a construção de um modelo de Machine Learning para prever a nota de um filme no IMDB!

---

## 🔎 Análise Exploratória e Insights

A análise exploratória dos dados (EDA), contida no notebook `PProductions_analise_filmes.ipynb`, revelou insights importantes para o negócio:

1.  **Qual filme recomendar para um desconhecido?**
    * A recomendação mais segura é um filme com alta nota no IMDB e um número massivo de votos, indicando um consenso geral de qualidade. Filmes como "The Shawshank Redemption" se encaixam perfeitamente neste perfil.

2.  **Fatores para alto faturamento:**
    * A análise de correlação mostrou que o fator mais forte relacionado ao alto faturamento (`Gross`) é o **número de votos (`No_of_Votes`)**. Isso sugere que o engajamento e a popularidade de um filme são mais determinantes para o sucesso financeiro do que a nota da crítica especializada.

3.  **Insights da coluna `Overview`:**
    * Através da análise de texto, identificamos que os filmes de maior sucesso, independentemente do gênero, abordam temas universais como **vida, família e amor**. Além disso, as sinopses de filmes aclamados frequentemente focam em uma **jornada de transformação e superação** do protagonista.

---

## 🤖 Modelo Preditivo

Para prever a nota do IMDB de um filme, foi desenvolvido um modelo de **Regressão**.

* **Variáveis Utilizadas:** `Meta_score`, `No_of_Votes`, `Gross`, `Runtime`.
* **Modelo Escolhido:** `RandomForestRegressor`, um modelo robusto que captura relações complexas nos dados.
* **Performance:** O modelo alcançou um **Erro Médio Absoluto (MAE) de 0.16**, indicando que, em média, suas previsões de nota estão a apenas 0.16 pontos da nota real.

Para o filme de exemplo, **'The Shawshank Redemption'**, o modelo previu uma nota de **8.8 no IMDB**.

---

## 🚀 Como Executar o Projeto

Para executar este projeto em sua máquina local, siga os passos abaixo.

### 1. Pré-requisitos

- Python 3.x instalado
- `pip` (gerenciador de pacotes do Python)

### 2. Instalação

**a. Clone o repositório:**
```bash
git clone https://github.com/gustavfaustino/Desafio-Lighthouse-GustavoFaustino
cd Desafio-Lighthouse-GustavoFaustino
```

**b. Crie um ambiente virtual (Recomendado):**
```bash
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
```

**c. Instale as dependências:**
Todas as bibliotecas necessárias estão listadas no arquivo `requirements.txt`. Instale-as com o seguinte comando:
```bash
pip install -r requirements.txt
```

### 3. Execução

O coração do projeto é o Jupyter Notebook. Para visualizar a análise e o código de modelagem, inicie o Jupyter:

```bash
jupyter notebook
```

No seu navegador, abra o arquivo `PProductions_analise_filmes.ipynb`. Você pode executar todas as células para reproduzir a análise e o treinamento do modelo.

---

## 📁 Estrutura do Repositório

O repositório está organizado da seguinte forma:

```
├── PProductions_analise_filmes.ipynb   # Notebook com toda a análise, EDA e código de modelagem.
├── desafio_indicium_imdb.csv           # Dataset original utilizado no projeto.
├── modelo_imdb.pkl                     # Modelo de Machine Learning treinado e salvo.
├── requirements.txt                    # Lista de dependências do Python para instalação.
└── README.md                           # Este arquivo.
```
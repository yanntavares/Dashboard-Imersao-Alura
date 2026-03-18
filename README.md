# Dashboard Interativo de Atuantes na Área de Tecnologia
====================================================================

## Introdução
-----------

Este projeto visa criar um dashboard interativo utilizando uma base de dados com informações de atuantes na área de tecnologia. A stack utilizada foi o Python com as bibliotecas Pandas, Seaborn, Matplotlib, Plotly e Streamlit.

## Requisitos
------------

* Python (versão 3.8 ou superior)
* Pandas (versão 1.2 ou superior)
* Seaborn (versão 0.11 ou superior)
* Matplotlib (versão 3.4 ou superior)
* Plotly (versão 4.14 ou superior)
* Streamlit (versão 0.86 ou superior)

## Configuração do Projeto
-------------------------

### 1. Instalar as dependências necessárias

```bash
pip install pandas seaborn matplotlib plotly streamlit
```

### 2. Criar um arquivo `data.csv` com as informações de atuantes na área de tecnologia

| Nome | Área de Atuação | Nível de Experiência | Salário |
| --- | --- | --- | --- |
| João | Desenvolvimento Web | Júnior | 4000 |
| Maria | Análise de Dados | Sênior | 8000 |
| Pedro | Inteligência Artificial | Pleno | 6000 |

### 3. Criar um arquivo `dashboard.py` com o código do dashboard

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import plotly.express as px
import streamlit as st

# Carregar os dados
df = pd.read_csv('data.csv')

# Criar um gráfico de barras com a distribuição de atuantes por área de atuação
st.title('Distribuição de Atuantes por Área de Atuação')
fig = px.bar(df, x='Área de Atuação', y='Nome')
st.plotly_chart(fig)

# Criar um gráfico de dispersão com a relação entre nível de experiência e salário
st.title('Relação entre Nível de Experiência e Salário')
fig = px.scatter(df, x='Nível de Experiência', y='Salário')
st.plotly_chart(fig)

# Criar um gráfico de pizza com a porcentagem de atuantes por nível de experiência
st.title('Porcentagem de Atuantes por Nível de Experiência')
fig = px.pie(df, values='Nível de Experiência', names='Nome')
st.plotly_chart(fig)

# Criar um filtro para selecionar a área de atuação
st.title('Filtro por Área de Atuação')
area_de_atuacao = st.selectbox('Selecione a área de atuação', df['Área de Atuação'].unique())

# Criar um gráfico de barras com a distribuição de atuantes por nível de experiência para a área de atuação selecionada
st.title('Distribuição de Atuantes por Nível de Experiência para a Área de Atuação Selecionada')
df_filtrado = df[df['Área de Atuação'] == area_de_atuacao]
fig = px.bar(df_filtrado, x='Nível de Experiência', y='Nome')
st.plotly_chart(fig)
```

## Execução do Projeto
---------------------

### 1. Executar o arquivo `dashboard.py` com o Streamlit

```bash
streamlit run dashboard.py
```

### 2. Acessar o dashboard no navegador

http://localhost:8501

## Conclusão
----------

Este projeto visa criar um dashboard interativo utilizando uma base de dados com informações de atuantes na área de tecnologia. A stack utilizada foi o Python com as bibliotecas Pandas, Seaborn, Matplotlib, Plotly e Streamlit. O dashboard inclui gráficos de barras, dispersão e pizza para visualizar a distribuição de atuantes por área de atuação, nível de experiência e salário. Além disso, inclui um filtro para selecionar a área de atuação e visualizar a distribuição de atuantes por nível de experiência para a área de atuação selecionada.

## Referências
------------

* [Pandas](https://pandas.pydata.org/)
* [Seaborn](https://seaborn.pydata.org/)
* [Matplotlib](https://matplotlib.org/)
* [Plotly](https://plotly.com/)
* [Streamlit](https://streamlit.io/)

## Análise dos Dados
-------------------

### 1. Distribuição de Atuantes por Área de Atuação

O gráfico de barras abaixo mostra a distribuição de atuantes por área de atuação.

```python
import matplotlib.pyplot as plt

plt.bar(df['Área de Atuação'].unique(), df['Nome'].count())
plt.xlabel('Área de Atuação')
plt.ylabel('Quantidade de Atuantes')
plt.title('Distribuição de Atuantes por Área de Atuação')
plt.show()
```

### 2. Relação entre Nível de Experiência e Salário

O gráfico de dispersão abaixo mostra a relação entre nível de experiência e salário.

```python
import matplotlib.pyplot as plt

plt.scatter(df['Nível de Experiência'], df['Salário'])
plt.xlabel('Nível de Experiência')
plt.ylabel('Salário')
plt.title('Relação entre Nível de Experiência e Salário')
plt.show()
```

### 3. Porcentagem de Atuantes por Nível de Experiência

O gráfico de pizza abaixo mostra a porcentagem de atuantes por nível de experiência.

```python
import matplotlib.pyplot as plt

plt.pie(df['Nível de Experiência'].value_counts(), labels=df['Nível de Experiência'].unique(), autopct='%1.1f%%')
plt.title('Porcentagem de Atuantes por Nível de Experiência')
plt.show()
```

## Filtro por Área de Atuação
-----------------------------

O filtro abaixo permite selecionar a área de atuação e visualizar a distribuição de atuantes por nível de experiência para a área de atuação selecionada.

```python
area_de_atuacao = st.selectbox('Selecione a área de atuação', df['Área de Atuação'].unique())
df_filtrado = df[df['Área de Atuação'] == area_de_atuacao]
fig = px.bar(df_filtrado, x='Nível de Experiência', y='Nome')
st.plotly_chart(fig)
```
# Introdução
Este projeto apresenta um dashboard de análise de salários na área de dados, permitindo que os usuários explorem os dados salariais nos últimos anos e refinem sua análise utilizando filtros.

## Stack e Tecnologias
As principais tecnologias e bibliotecas utilizadas neste projeto incluem:
- **Streamlit**: Utilizada para a criação da interface do usuário e para hospedar o aplicativo web.
- **Pandas**: Para manipulação e análise dos dados.
- **Plotly**: Utilizada para a criação de gráficos interativos.
- **Python**: Linguagem de programação utilizada para desenvolver o aplicativo.

## Arquitetura do Projeto
O projeto é composto por um arquivo principal (`app.py`) que contém o código para a criação do dashboard, incluindo a configuração da página, carregamento dos dados, criação de filtros, e exibição de métricas e gráficos. Os dados são carregados de um arquivo CSV hospedado em um repositório GitHub.

## Como Compilar o Sistema
Para compilar e executar o sistema, siga os passos abaixo:

1. **Instale as dependências**: Utilize o arquivo `requirements.txt` para instalar as bibliotecas necessárias. Execute o comando `pip install -r requirements.txt` no terminal.
2. **Execute o aplicativo**: Com as dependências instaladas, execute o comando `streamlit run app.py` no terminal para iniciar o aplicativo.

## Funcionalidades
O dashboard oferece as seguintes funcionalidades:

- **Filtros**: Os usuários podem aplicar filtros por ano, senioridade, tipo de contrato, e tamanho da empresa para refinar a análise.
- **Métricas Principais**: Exibe o salário médio, salário máximo, total de registros, e o cargo mais frequente com base nos filtros aplicados.
- **Análises Visuais**: Inclui gráficos interativos para visualizar o top 10 de cargos por salário médio, distribuição de salários anuais, proporção dos tipos de trabalho, e salário médio de Cientista de Dados por país.
- **Tabela de Dados Detalhados**: Permite que os usuários visualizem os dados detalhados após a aplicação dos filtros.
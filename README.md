# Dashboard de Análise de Salários na Área de Dados
## Introdução
Este projeto visa criar um dashboard interativo para análise de salários na área de dados, utilizando tecnologias como Streamlit, Pandas e Plotly. O objetivo é fornecer uma ferramenta útil para explorar e visualizar dados salariais, permitindo que os usuários filtrem e analisem os dados de acordo com suas necessidades.

## Stack e Tecnologias
- **Streamlit**: Utilizado para criar a interface do usuário e desenvolver o dashboard.
- **Pandas**: Biblioteca para manipulação e análise de dados.
- **Plotly**: Utilizado para criar gráficos interativos e visualizações.

## Arquitetura do Projeto
O projeto é estruturado da seguinte maneira:
- **app.py**: Contém o código principal do aplicativo, incluindo a configuração da página, carregamento dos dados, criação de filtros, análise de dados e visualizações.
- **dados-imersao-final.csv**: Arquivo de dados utilizado pelo aplicativo.
- **requirements.txt**: Lista de dependências necessárias para executar o projeto.

## Como Compilar e Executar o Sistema
1. **Instalar Dependências**: Execute `pip install -r requirements.txt` para instalar todas as dependências listadas no arquivo `requirements.txt`.
2. **Executar o Aplicativo**: Execute `streamlit run app.py` para iniciar o aplicativo.

## Funcionalidades
- **Filtros**: O usuário pode filtrar os dados por ano, senioridade, tipo de contrato e tamanho da empresa.
- **Métricas Principais (KPIs)**: Exibe o salário médio, salário máximo, total de registros e cargo mais frequente com base nos filtros aplicados.
- **Análises Visuais**: Inclui gráficos para visualizar os top 10 cargos por salário médio, distribuição de salários anuais, proporção dos tipos de trabalho e salário médio de Cientista de Dados por país.
- **Tabela de Dados Detalhados**: Exibe a tabela com os dados detalhados após a aplicação dos filtros.
# Projeto de Lançamento Digital - Emagri

Este projeto tem como objetivo analisar os dados de lançamento de um produto digital voltado para emagrecimento. A análise cobre o número de vendas, a quantidade de inscritos na campanha de captação e informações adicionais coletadas por meio de uma pesquisa sobre idade, renda e tempo de acompanhamento do Expert.

## Estrutura do Projeto e Processo ETL/ELT

### Processo ETL Atual
1. **Ingestão de Dados:** Utilização do Jupyter Notebook com Python para ingestão dos dados.
2. **Tratamento de Dados:** Limpeza e manipulação dos dados com o Pandas.
3. **Visualização de Dados:** Carregamento dos dados no Power BI para criação de relatórios e dashboards interativos.

### Arquitetura Ideal
1. **Ingestão de Dados:** Ingestão dos dados via API ou arquivos CSV.
2. **Armazenamento:** Carregamento dos dados em um Data Lake na nuvem, como o Azure Data Lake Storage.
3. **Estrutura Medallion (Bronze, Silver, Gold):** Organização dos dados em camadas para garantir qualidade, acessibilidade e organização:
   - **Bronze (Raw):** Dados brutos, no formato original.
   - **Silver (Refined):** Dados transformados e limpos, prontos para análise intermediária.
   - **Gold (Curated):** Dados finais organizados para análise e consumo no data warehouse.
4. **Processamento e Orquestração:** Utilização do Azure Data Factory para orquestração do fluxo de dados e do Databricks para tratamento e transformação dos dados.
5. **Data Warehouse e Visualização:** Estruturação dos dados no formato de data warehouse, com as relações adequadas. Envio para o Power BI ou outras ferramentas de visualização para análise e insights.

## Insights do Projeto

A análise dos dados revelou os seguintes pontos:
- **Alto número de inscritos**: 84,06% das inscrições foram originadas de campanhas no Facebook Ads.
- **Baixa conversão**: O número de vendas foi relativamente baixo, com uma taxa de conversão de 0,74% em relação ao total de inscritos.
- **Engajamento do Público**: Apesar da baixa conversão, observou-se um engajamento significativo do público durante o lançamento.
- **Segmentação Potencial**: O grupo de idade entre 41 e 45 anos, com renda entre R$1.500,00 e R$3.000,00, demonstrou interesse e pode ser um público promissor para ações de marketing direcionadas, pois é um grupo que conhece o Expert há menos tempo.

## Desafios

O principal desafio foi a ausência de chaves de relacionamento (como IDs) nos dados, o que dificultou a criação de análises cruzadas entre diferentes conjuntos de dados. Como solução, foram desenvolvidas visões independentes para as diferentes camadas de dados:
- Total de inscritos, vendas e resultados da pesquisa em visão geral.
- Visualizações específicas para o desempenho dos criativos das campanhas.

## Design das Telas

O design foi elaborado para proporcionar clareza e destacar as informações principais. As telas priorizam:
- Exibição de totais e métricas essenciais para uma compreensão rápida.
- Visualizações gráficas que facilitam a identificação de insights e direcionamento de ações.

## Sobre o Analista

Neste projeto, utilizei o Python com o Pandas para o tratamento dos dados e utilizei Git e GitHub para o versionamento do código. As visualizações foram feitas no Power BI, com o objetivo de trazer clareza e acessibilidade aos dados e aos insights obtidos.

---

## Acesso ao Projeto

Para visualizar o dashboard e as análises completas no Power BI, [Dashboard do Projeto no Power BI](https://app.powerbi.com/view?r=eyJrIjoiMDM2MTc1NWUtOWFiNC00NDk5LTkwNWMtNTVlMzZiMzMwZmVhIiwidCI6IjEzYjY2NjJlLWYyYjMtNDk3Ny1iNGNlLWEyZmIzMWU5ZjhiZCJ9).

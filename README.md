# Projeto de Clusterização de Transações Semanais de Vendas

Este projeto tem como objetivo identificar padrões ou agrupamentos (clusters) nos dados de transações semanais de vendas utilizando diferentes algoritmos de clusterização. O foco principal é agrupar produtos para gerar insights sobre padrões de compra e otimizar estratégias de vendas.

## Estrutura do Projeto

- **`Sales_Transactions_Dataset_Weekly.csv`**: Arquivo contendo os dados de vendas semanais.
- **`SalesTransactionsWeekly.ipynb`**: Notebook principal com a implementação do projeto.

## Etapas do Projeto

1. **Carregamento e Pré-processamento dos Dados**:
   - Remoção de colunas que começam com "Normalized".
   - Normalização dos dados para garantir que todas as variáveis tenham a mesma influência nos algoritmos de clusterização.

2. **Aplicação de Algoritmos de Clusterização**:
   - **K-Means**: Algoritmo baseado em centroides.
   - **DBSCAN**: Algoritmo baseado em densidade.
   - **Agglomerative Clustering**: Algoritmo hierárquico com diferentes métodos de ligação.

3. **Avaliação dos Resultados**:
   - Cálculo do **Silhouette Score**, **Calinski-Harabasz Index** e **Davies-Bouldin Index** para avaliar a qualidade dos clusters.
   - Comparação dos resultados para determinar o melhor algoritmo.

4. **Visualização**:
   - Visualização dos clusters gerados pelos algoritmos.
   - Análise de padrões de vendas semanais por cluster.

## Resultados

- **Agglomerative Clustering** apresentou o melhor desempenho geral, com o maior **Silhouette Score** e o menor **Davies-Bouldin Index**.
- **K-Means** teve o melhor **Calinski-Harabasz Index**, indicando clusters bem compactos e separados.
- **DBSCAN** apresentou os piores scores, sugerindo que não foi o método mais adequado para este conjunto de dados.

## Requisitos

- Python 3.7 ou superior
- Bibliotecas utilizadas:
  - `pandas`
  - `numpy`
  - `seaborn`
  - `matplotlib`
  - `scikit-learn`

## Como Executar

1. Certifique-se de que o arquivo `Sales_Transactions_Dataset_Weekly.csv` está no mesmo diretório do notebook.
2. Abra o arquivo `SalesTransactionsWeekly.ipynb` em um ambiente como Jupyter Notebook ou JupyterLab.
3. Execute as células sequencialmente para reproduzir os resultados.

## Conclusões

O modelo **Agglomerative Clustering** separou dois grupos bem distintos:
- **Cluster 0**: Produtos de alto volume de vendas.
- **Cluster 1**: Produtos com baixas vendas e maior variabilidade.

Esses insights podem ser utilizados para otimizar estratégias de promoção e gerenciamento de estoque.

## Autor

Este projeto foi desenvolvido como parte de um estudo de clusterização de dados de vendas semanais.

# Projeto de Análise de Vendas com Pandas, Seaborn e Matplotlib

Este projeto de ciência de dados tem como objetivo realizar uma análise exploratória de um dataset de vendas fictício, utilizando as bibliotecas **pandas**, **seaborn** e **matplotlib**. O pipeline completo inclui carregamento de dados, limpeza, visualização e exportação de relatórios, permitindo uma análise robusta do comportamento de vendas.

## Estrutura do Projeto

O projeto está dividido nas seguintes etapas:

1. **Carregamento de Dados**: O dataset de vendas é carregado a partir de um arquivo CSV.
2. **Limpeza e Preparação de Dados**: Os dados são tratados para lidar com valores ausentes e outliers.
3. **Análise Exploratória de Dados (EDA)**: Estatísticas descritivas e análises de correlação são geradas.
4. **Visualizações**: São criados gráficos para explorar as relações entre as variáveis.
5. **Exportação de Relatórios**: Os resultados são exportados para arquivos CSV e imagens.

## Pré-requisitos

### Bibliotecas Python Necessárias

Para rodar o código, você precisará das seguintes bibliotecas Python instaladas:

- `pandas`
- `seaborn`
- `matplotlib`
- `scipy`
- `numpy`

Você pode instalar as bibliotecas necessárias executando o seguinte comando:

```bash
pip install pandas seaborn matplotlib scipy numpy
```

### Arquivo CSV

Baixe o arquivo de dados fictício `sales_data_example.csv` [aqui](sandbox:/mnt/data/sales_data_example.csv) e coloque-o no mesmo diretório do código Python. Este arquivo contém dados simulados de vendas de diferentes categorias de produtos, como `Electronics`, `Clothing`, `Furniture`, e `Toys`.

## Como Executar o Projeto

1. **Clone este repositório** ou copie os arquivos necessários para o seu diretório local.
2. **Baixe o arquivo CSV de exemplo** (fornecido acima) e coloque-o no mesmo diretório que o código Python.
3. **Execute o script** Python. O pipeline será executado automaticamente, incluindo a limpeza, análise e visualização dos dados:

```bash
python analysis_pipeline.py
```

4. **Relatórios e Gráficos**: Após a execução do código, você verá as seguintes saídas:
   - Gráficos exibidos na tela com base nas análises exploratórias.
   - Arquivos exportados para o diretório de execução:
     - `relatorio_descritivo.csv`: Contém uma descrição estatística do dataset.
     - `vendas_categoria.png`: Gráfico de barras mostrando o total de vendas por categoria.

## Estrutura do Código

O código é modular e está organizado nas seguintes funções:

- `load_data()`: Carrega o dataset a partir do arquivo CSV.
- `clean_data(df)`: Realiza a limpeza dos dados, removendo outliers e valores ausentes, e cria uma coluna de faturamento (`revenue`).
- `exploratory_data_analysis(df)`: Exibe estatísticas descritivas e calcula a correlação entre as variáveis.
- `visualize_data(df)`: Cria gráficos para explorar as relações entre as variáveis:
  - Gráfico de barras mostrando a quantidade de vendas por categoria.
  - Scatter plot para a relação entre preço e quantidade vendida, incluindo uma linha de regressão.
  - Gráfico de densidade (KDE) para a distribuição dos preços.
  - Heatmap de correlação entre variáveis.
  - Gráfico de barras mostrando o faturamento total por categoria.
- `export_report(df)`: Exporta relatórios e gráficos para arquivos CSV e PNG.

## Exemplo de Saída

### Gráficos

- **Gráfico de Barras: Total de Vendas por Categoria**

![Total de vendas por categoria barras](https://github.com/user-attachments/assets/60caa280-9c75-4bec-b9e1-4085d2512381)


- **Scatter Plot: Preço vs Quantidade Vendida**

![Preco vs quantidade vendida linha tendencia](https://github.com/user-attachments/assets/48b18c70-a905-4d75-9343-93fd2361d53f)


- **Heatmap de Correlação entre Variáveis**

![heatmap](https://github.com/user-attachments/assets/81dd83ba-43f3-48ef-a8ea-525fdded09e3)


### Arquivo CSV: Relatório Descritivo

O arquivo `relatorio_descritivo.csv` contém a seguinte descrição estatística do dataset:

|          | price    | quantity_sold | revenue   |
|----------|----------|---------------|-----------|
| count    | 100.0    | 100.0         | 100.0     |
| mean     | 75.34    | 201.50        | 15945.78  |
| std      | 28.39    | 102.74        | 10762.91  |
| min      | 5.0      | 2.0           | 11.25     |
| 25%      | 54.89    | 121.50        | 9131.37   |
| 50%      | 75.75    | 201.0         | 15234.57  |
| 75%      | 95.89    | 281.50        | 22877.55  |
| max      | 149.0    | 399.0         | 48111.45  |

## Possíveis Expansões

Este projeto pode ser expandido para incluir análises mais complexas e técnicas de machine learning. Aqui estão algumas sugestões:

- **Predição de Vendas**: Usar algoritmos de regressão para prever a quantidade vendida com base no preço e categoria.
- **Análise de Tendências Temporais**: Analisar como as vendas variam ao longo do tempo, adicionando sazonalidade às análises.
- **Segmentação de Clientes**: Identificar padrões de compra com base em categorias de produtos e comportamento de vendas.

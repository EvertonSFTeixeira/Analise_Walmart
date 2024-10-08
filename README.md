# Previsão de Vendas no Walmart

Este repositório contém a análise e modelagem preditiva de vendas da rede Walmart utilizando técnicas de aprendizado de máquina, com o objetivo de prever as vendas por departamento para diferentes lojas, considerando variáveis como temperatura, promoções e feriados.

## Descrição do Projeto

O objetivo deste projeto é desenvolver um modelo de previsão de vendas por departamento para o Walmart, utilizando dados de vendas históricas e outras variáveis relacionadas, como promoções (`MarkDown`), feriados e clima. O projeto emprega técnicas de Machine Learning, como Random Forest Regressor e Extra Trees Regressor, para gerar previsões e otimizar a precisão dos resultados.

## Estrutura do Projeto

- **Análise Exploratória de Dados (EDA)**: Exploração detalhada do dataset para entender as correlações entre as variáveis e a distribuição dos dados.
- **Pré-processamento de Dados**: Inclui tratamento de valores nulos, codificação de variáveis categóricas, criação de novas features (como tratamento de feriados e markdowns), e transformação de dados.
- **Modelagem**: Treinamento e validação de diferentes modelos, como:
  - Random Forest Regressor
  - Extra Trees Regressor

- **Validação e Avaliação**: Avaliação dos modelos com métricas como RMSE, MAE, R² e WMAE para selecionar o modelo mais adequado.
- **Submissão**: O modelo selecionado é utilizado para fazer previsões sobre o conjunto de teste e as previsões são submetidas para validação final.

## Modelos Utilizados

Os seguintes modelos foram testados:

1. **Random Forest Regressor**:
   - **Melhores Hiperparâmetros**: 
     ```json
     {
       'bootstrap': True,
       'max_depth': 20,
       'min_samples_leaf': 1,
       'min_samples_split': 2,
       'n_estimators': 100
     }
     ```
   - **Resultados**:
     - RMSE: 4540.02
     - MAE: 1670.58
     - R²: 0.960

2. **Extra Trees Regressor**:
   - **Melhores Hiperparâmetros**:
     ```json
     {
       'bootstrap': True,
       'max_depth': 20,
       'min_samples_leaf': 1,
       'min_samples_split': 2,
       'n_estimators': 100
     }
     ```
   - **Resultados**:
     - RMSE: 4789.01
     - MAE: 1753.35
     - R²: 0.956


## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib / Seaborn
- Jupyter Notebook

## Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/EvertonSFTeixeira/Analise_Walmart.git
   ```

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

3. Abra o Jupyter Notebook e execute o arquivo `Projeto.ipynb` para reproduzir as análises e modelos.

## Dados

Os dados utilizados neste projeto podem ser encontrados no seguinte [repositório do Kaggle](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/data).

- **Features**:
  - Loja: Identificador da loja
  - Departamento: Identificador do departamento
  - Semana: Data da semana de vendas
  - Vendas: Vendas realizadas por departamento
  - Variáveis externas como: Temperatura, Feriados, Promoções (`MarkDown`), entre outras.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para fazer um fork deste repositório e enviar pull requests.

## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

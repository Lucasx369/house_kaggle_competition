# Atividade

### Desafio Kaggle Open Challenge

**Critérios de Avaliação**
- Compreensão do desafio House Kaggle, incluindo o contexto e os objetivos do desafio;
- Implementação das soluções do desafio no notebook preparatório de forma que passem nos testes pré-setados;
- Utilização de técnicas, algoritmos e bibliotecas para a resolução dos problemas propostos;
- Submissão das soluções desenvolvidas ao Kaggle Open Challenge;
- Descrição dos requisitos para o desenvolvimento das soluções e compreensão do desafio House Kaggle;
- Explicação detalhada do desenvolvimento das soluções, avaliação, otimização e submissão ao Kaggle utilizando comentários no código;

## O Desafio 

### :dart: Objetivo
O objetivo principal é prever o preço de venda de casas com base em várias características. No total há 79 variáveis sobre casas em Ames, Iowa. Essas características incluem aspectos  físicos da casa (como tamanho e qualidade de construção) e sua localização. A métrica de avaliação é o Root-Mean-Squared-Error (RMSE) entre o logaritmo do preço de venda previsto e o logaritmo do preço de venda observado. 

### :open_file_folder:	Descrição Geral do Dataset

O conjunto de dados inclui arquivos como houses_train_raw.csv (dados de treino) e houses_test_raw.csv (dados de teste). 

Há 79 variáveis sobre as casas, mas os campos de dados principais são:
- `SalePrice`: O preço de venda do imóvel (variável alvo).
- `Características do Imóvel`: Incluem classe de construção (MSSubClass), zoneamento (MSZoning), tamanho do lote (LotArea), qualidade geral (OverallQual), ano de construção (YearBuilt), qualidade do material exterior (ExterQual), e muitas outras características físicas e de localização.
- `Características Internas`: Como qualidade do aquecimento (HeatingQC), tamanho do primeiro andar (1stFlrSF), número de banheiros (FullBath), qualidade da cozinha (KitchenQual), etc.
- `Características Externas`: Como área da garagem (GarageArea), área da piscina (PoolArea), qualidade da piscina (PoolQC), entre outros.

Sendo assim, este conjunto de dados oferece uma rica fonte de informações para modelagem preditiva. 

### Descrição Detalhada
#### :open_file_folder: Data

A pasta `Data` contém os arquivo de dados de teste (`houses_train_raw.csv`) e arquivo de dados de teste (`houses_test_raw.csv`), nos quais permitem que os modelos sejam treinados, e posteriormente testada a sua eficácia, simulando como o modelo irá se comportar com dados não vistos anteriormente.

##### :page_facing_up: houses_train_raw.csv

Este é o arquivo de dados de treinamento. Ele contém as características dos imóveis e seus preços de venda. Este arquivo é usado para treinar o modelo de machine learning. Isso inclui ajustar os parâmetros do modelo para que ele possa aprender a relação entre as características dos imóveis (como tamanho, localização, número de quartos) e seus preços de venda.

##### :page_facing_up: houses_test_raw.csv

Este é o arquivo de dados de teste. Ele contém as características dos imóveis, mas, diferentemente do conjunto de treinamento, não inclui os preços de venda. Este arquivo é usado para avaliar o modelo final, ou seja, após treinar o modelo com o conjunto de treinamento, este conjunto de dados é utilizado para avaliar seu desempenho. 

#### :page_facing_up: houses_kaggle_competition.ipynb

O notebook `houses_kaggle_competition.ipynb` contém o projeto de ciência de dados completo, onde são realizas as previsões dos preços dos imóveis. Abaixo, está detalhada a estrutura geral do código:

##### Imports 

Inicialmente são importadas as bibliotecas que são essenciais para análise e modelagem de dados, como matplotlib, numpy, pandas, seaborn, scipy, xgboost e diversas do scikit-learn. Estas bibliotecas são fundamentais para manipulação de dados, visualização, construção de modelos de aprendizado de máquina, avaliação de modelos, entre outras.

##### Carregamento de Dados

Os dados são carregados a partir do arquivo `houses_train_raw.csv` (dados de treinamento). A coluna SalePrice é separada como variável alvo (y), e as outras colunas formam o conjunto de características (x).

##### Análise Exploratória e Pré-processamento

É realizada uma análise exploratória, examinando as características categóricas, de modo que facilite o processo de decisão sobre quais delas devem passar por codificação one-hot. O pré-processamento inclui imputação e escalonamento min-max para características numéricas, e imputação e codificação one-hot para características categóricas selecionadas.

##### Modelagem

São explorados vários modelos de regressão, como Ridge, KNeighborsRegressor, SVR, DecisionTreeRegressor, RandomForestRegressor, AdaBoostRegressor, GradientBoostingRegressor, além de abordagens de ensemble como VotingRegressor e StackingRegressor. Cada modelo é avaliado usando validação cruzada, e alguns modelos passam por um processo de otimização de hiperparâmetros usando GridSearchCV ou RandomizedSearchCV.








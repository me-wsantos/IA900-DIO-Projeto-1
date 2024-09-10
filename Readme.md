## Formação Microsoft Azure AI Fundamentals (AI-900) - DIO
## Projeto 1 : Modelo de Machine Learning para previsão do Índice Nacional de Preços - IPCA
<br>
<hr>

### :zap: Tecnologias
* Microsoft Azure Machine Learning
<br>
<hr>

## :computer: Descrição
### 1. Definição do Problema
* **Objetivo**: Prever o IPCA (Índice Nacional de Preço ao Consumidor Amplo)
* **Variáveis**: Índice por mês e ano.

### 2. Coleta de Dados
* **Fontes de Dados**: Registro histórico do IPCA disponível no site do [IBGE](https://www.ibge.gov.br/estatisticas/economicas/precos-e-custos/9256-indice-nacional-de-precos-ao-consumidor-amplo.html?=&t=downloads)

### 3. Pré-processamento dos Dados
* **Limpeza de Dados**: Foram removidas linhas em branco e caracteres duplicados para garantir a qualidade, consistência e completude.

### 4. Seleção de Modelo
* **Escolha de Algoritmo**: Foi selecionado o modelo de regressão.

### 5. Ferramentas:
* O modelo foi implementado no Microsoft Azure Machine Learning.

### 6. Documentação:
* Abaixo o registro de cada etapa do processo de implementação. Foi incluído no projeto o arquivo .csv com os registros utilizados e um arquivo PDF com os prints das etapas de implementação do modelo.

#### Basic settings:
  * **Job name**: IPCA série histórica <br>
  * **New experiment name**: Série histórica IPCA<br>
  * **Description**: Machine Learning para previsão do índice IPCA baseado na série histórica registrada pelo IBGE<br>
  * **Tags**: none

#### Task type & data:
  * **Select task type**: Regression
  * **Select dataset**: Foi utilizado um arquivo .csv (presenten nesse projeto) baixado do do site di [IBGE](https://www.ibge.gov.br/estatisticas/economicas/precos-e-custos/9256-indice-nacional-de-precos-ao-consumidor-amplo.html?=&t=downloads)
  * **Data type name**: ipca_historico
  * **Data type description**: Série histórica IPCA
  * **Data type**: Tabular
  * **Data type source**: From local files
  * **Destination storage type**: Azure Blob Storage
  * **Destination storage type name**: workspaceblobstore
  * **MLtable selection**: Upload file ipca_202408SerieHist.csv

#### Task type & data:
  * **Task type**: Upload file ipca_202408SerieHist.csv
  * **Dataset**: Upload file ipca_202408SerieHist.csv
  * **Target column**: index

  * Additional configuration settings:
    * **Primary metric**: NormalizedRootMeanSquaredError
    * **Explain best model**: Unselected
    * **Enable ensemble stacking**: Unselected
    * **Use all supported models**: Unselected. You’ll restrict the job to try only a few specific algorithms.
    * **Allowed models**: Select only RandomForest and LightGBM — normally you’d want to try as many as possible, but each model added increases the time it takes to run the job.
 * Limits:
    * **Max trials**: 3
    * **Max concurrent trials**: 3
    * **Max nodes**: 3
    * **Metric score threshold**: 0.085
    * **eXPERIMENT Timeout**: 15
    * **Iteration timeout**: 15
    * **Enable early termination**: Selected
  * Validation and test:
    * **Validation type**: Train-validation split
    * **Virtual machine type**: CPU
    * **Virtual machine tier**: Dedicated
    * **Virtual machine size**: Standard_DS3_V2
    * **Number of instances**: 1
   
  ### :technologist: Autor
  <a href="https://github.com/me-wsantos">
   <img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/179779189?v=4" width="100px;" alt=""/>
   <br />
   <p><b>Wellington Santos</b></sub></a> <a href="https://github.com/me-wsantos" title="GitHub"></a></p>
  
  [![Linkedin Badge](https://img.shields.io/badge/-Wellington--Santos-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/wellington-lima-dos-santos-13343143/)](https://www.linkedin.com/in/wellington-lima-dos-santos-13343143/) 
  [![Email Badge](https://img.shields.io/badge/-me@wellington--santos.com-c14438?style=flat-square&logo=Gmail&color=11ab3a&logoColor=white&link=mailto:me@wellington-santos.com)](mailto:me@wellington-santos.com)

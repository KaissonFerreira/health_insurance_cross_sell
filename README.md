health Insurance Cross Sell
==============================
## Contexto
Nosso cliente é uma Seguradora que forneceu Seguro Saúde para seus clientes agora eles precisam da sua ajuda na construção de um modelo para prever se os segurados (clientes) do ano passado também terão interesse no Seguro de Veículos fornecido pela empresa.

Construir um modelo para prever se um cliente estaria interessado em Seguro de Veículo é extremamente útil para a empresa, pois ela pode planejar adequadamente sua estratégia de comunicação para alcançar esses clientes e otimizar seu modelo de negócios e receita. **Nesse contexto, é essencial identificar quais clientes tem uma maior propensão à compra de um segundo produto que seria o seguro para veículo, uma vez que a parte comercial só dá conta de fazer 2000 ligações, tendo em vista que existe uma base de 380 mil registros de clientes.**

Cada apólice de seguro custa em média R$ 5.000,00 anual de forma que o seguro para cada apólice é R$ 100.000,00. Levando em consideração o levantamento que o time de analytics da empresa fez sobre o percentual e a probabilidade das pessoas que acabam ganhando o seguro, em média, a cada 100 clientes que compram o seguro de carro, 2 pessoas acabam ganhando o seguro, com um desvio padrão de +/- 1.

Agora, para prever se o cliente estaria interessado em seguro de veículo, você tem informações sobre dados demográficos (gênero, idade, tipo de código de região), Veículos (idade do veículo, danos), apólice (Premium, canal de fornecimento) etc.

## Objetivo do negócio:
* Fazer um ranqueamento das pessoas que tem uma probabilidade para compra do seguro de veículo.

## Entendimento do negócio:
1. Qual a motivação?
    * O pedido para o ranqueamento dos clientes com maiores chances de comprar o seguro foi feito pelo diretor comercial.
2. Qual a causa raíz do problema?
    * Dificuldade em determinar quais seriam as melhores pessoas para fazer ligação sobre a compra do produto, uma vez a base de clientes contava com 300 mil, e o time comercial só havia capacidade para fazer 2000 ligações.
3. Quem é o dono do problema?
    * Diretor Comercial da seguradora.
4. Qual é o formato da solução?
    * **Granularidade:** Previsão por cliente
    * **Tipo do problema:** Classificação e ranqueamento
    * **Potenciais métodos:** Classificação
    * **Formato de entrega:**
        - Lista com os nomes e informações dos clientes que estiverem mais propensos às compras.



Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

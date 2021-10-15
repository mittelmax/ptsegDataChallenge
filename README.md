# Porto Seguro Data Challenge

<p align="center">
  <img src="https://pngimage.net/wp-content/uploads/2018/06/logo-porto-seguro-png-3.png?raw=true" alt="Logo Porto Seguro"/>
</p>

## `Introdução`

Este repositório contém minha solução para o Porto Seguro Data Challenge, que terminou a competetição em terceiro lugar na divisão universitária. A página e leaderboard oficiais estão disponíveis no Kaggle através [deste link](https://www.kaggle.com/c/porto-seguro-data-challenge). Gostaria de ressaltar o grande aprendizado que esta competição me proporcionou, uma vez que busquei aprender e utilizar técnicas fora de minha zona de conforto. Por fim também gostaria de parabenizar a todos os demais participantes por suas soluções, e também à Porto Seguro pela oportunidade proporcionada.

## `Metodologia e Objetivo`
Meu foco principal durante o desafio foi o de implementar uma estratégia de Stacking. Esta foi a primeira vez que me aventurei com Ensemble Learning, e portanto busquei utilizar tal oportunidade como um incentivo para me familiarizar com tal técnica.

## `Requisitos`
Para a execução de minhha estratégia utilizei os seguintes pacotes disponíveis no arquivo `requirements.txt`.
* catboost==0.26
* lightgbm==3.3.0
* numpy==1.21.2
* optuna==2.10.0
* pandas==1.3.3
* pathlib==1.0.1
* scikit-learn==1.0
* xgboost==1.4.2
#### `Disclaimer`
As versões mais recentes do Catboost apresentam um problema que impede a utilização do parâmetro `class_weights` com a métrica de Loss F1. Dessa forma, para a execução da solução é necessário que se realize um downgrade do pacote para a versão 0.26.

## `Estrutura do Repositório`
Aqui está um resumo da estrutura deste repositório. Minha solução original foi construída com base numa série de notebooks do Kaggle. Dessa forma, este repositório é uma implementação alternativa de minha solução, em que me empenhei para tornar mais organizada e reprodutível.

* `ptsegDataChallenge/`
  * `ptsegDataChallenge/`
    * __init__.py
    * config.py
  * `dataPreprocessing/`
    * preprocV1.py
  * `baseModels/`
    * `tuning/`
      * tuningCatboostBase.py
      * tuningLightGBMBase.py
      * tuningXGBoostBase.py
    * `oofPredictions/`
      * oofPredsBernNB.py
      * oofPredsCatboost.py
      * oofPredsJoin.py
      * oofPredsKNN.py
      * oofPredsLightGBM.py
      * oofPredsLogreg.py
      * oofPredsRandomForest.py
      * oofPredsSVC.py
      * oofPredsXGBoost.py
    * `basePredictions/`
      * basePredsBernNB.py
      * basePredsCatboost.py
      * basePredsJoin.py
      * basePredsKNN.py
      * basePredsLightGBM.py
      * basePredsLogreg.py
      * basePredsRandomForest.py
      * basePredsSVC.py
      * basePredsXGBoost.py
  * `stackedModel/`
      * predictionStackedLightGBM.py
      * tuningStackedLightGBM.py
  * `README.md`
  * `requirements.txt`
  * `data/`
    * `raw/`
    * `preproc/`
    * `tuningBase/`
    * `tuningStacked/`
    * `basePreds/`
    * `finalPredictions/`

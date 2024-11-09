# Análise de Classificação do Conjunto de Dados de Vinho

Este repositório contém a análise de três modelos de classificação aplicados ao conjunto de dados "Wine" do `sklearn`. Os modelos avaliados são:

- Árvore de Decisão (Decision Tree)
- Random Forest (Floresta Aleatória)
- K-Nearest Neighbors (KNN)

## Objetivo

O objetivo da análise é avaliar o desempenho de cada modelo de classificação em relação à precisão das previsões para a classificação de tipos de vinho, utilizando as métricas de avaliação mais comuns em aprendizado supervisionado: **Precisão**, **Revocação**, **F1-Score** e **Acurácia**.

## Resultados dos Modelos

Abaixo está o resumo dos resultados obtidos para cada modelo de classificação:

### 1. **Árvore de Decisão (Decision Tree)**

Acurácia: 0.9630

Matriz de Confusão:
```
[[18  1  0]
 [ 0 21  0]
 [ 1  0 13]]
```

Relatório de Classificação:

                   precision recall    f1-score    support
           0       0.95      0.95      0.95        19
           1       0.95      1.00      0.98        21
           2       1.00      0.93      0.96        14

    accuracy                           0.96        54
    macro avg      0.97      0.96      0.96        54
    weighted avg   0.96      0.96      0.96        54

### 2. **Random Forest**

Acurácia: 1.0000

Matriz de Confusão:
```
[[19  0  0]
 [ 0 21  0]
 [ 0  0 14]]
```

Relatório de Classificação:

                   precision recall    f1-score    support
           0       1.00      1.00      1.00        19
           1       1.00      1.00      1.00        21
           2       1.00      1.00      1.00        14

    accuracy                           1.00        54
    macro avg      1.00      1.00      1.00        54
    weighted avg   1.00      1.00      1.00        54

### 3. **K-Nearest Neighbors (KNN)**

Acurácia: 0.9630

Matriz de Confusão:
```
[[19  0  0]
 [ 1 19  1]
 [ 0  0 14]]
```

Relatório de Classificação:

                   precision recall    f1-score    support
           0       0.95      1.00      0.97        19
           1       1.00      0.90      0.95        21
           2       0.93      1.00      0.97        14

    accuracy                           0.96        54
    macro avg      0.96      0.97      0.96        54
    weighted avg   0.97      0.96      0.96        54

## Análise dos Modelos
O KNN apresentou uma boa performance, com alta precisão e recall, mas com um desempenho ligeiramente inferior ao da Árvore de Decisão e Random Forest. A principal limitação foi a revocação para a Classe 1 (0.90), o que resultou em um f1-score um pouco mais baixo em comparação com os outros modelos.

O Random Forest ficou 100% em tudo, o que é perigoso em uma validação de treino, uma vez que pode causar overthinking, que nada mais é do que o vício nos dados de treino. 

A Árvore de Decisão por sua vez teve números muito bons, porém sem o vício dos dados de treino. tendo acurácia boa e erros pequenos distribuidos entre a matriz de confusão, não errando tanto em uma mesma classe

## Conclusões
O Random Forest tem um potancial muito grande, porém corre muito o risco de overthinking em treinamento de novos dados, o que torna a Ávore de decisão que se saiu melhor que o KNN por não errar em uma mesma classe e não visiando nos dados de teste, o melhor modelo análisado para a base de dados wine, observando esse cenário. 

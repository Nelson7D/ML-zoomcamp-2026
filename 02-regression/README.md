# Homework 2: Regressão linear

Dataset: `car_fuel_efficiency_2026.csv` | Target: `fuel_efficiency_mpg`
Notebook: [homework.ipynb](homework.ipynb) | [Abrir no Google Colab](https://colab.research.google.com/drive/1g77auWHbpZQ9Y8i8j-U3V56J_JPF1DDy?usp=sharing)

## Respostas

| Questão | Resultado | Resposta |
|---------|-----------|----------|
| EDA | `fuel_efficiency_mpg` | Ver histograma no notebook |
| Q1 | 877 valores em falta | `horsepower` |
| Q2 | mediana de `horsepower` = 254.0 | **254** |
| Q3 | RMSE com 0 = 2.205; com média = 2.202 | **Com média** |
| Q4 | melhor RMSE = 2.2053 (r = 0) | **0** |
| Q5 | std = 0.029 | **0.029** |
| Q6 | RMSE no teste = 2.236 | **2.236** |

## Notas
- A média usada no Q3 é calculada apenas no conjunto de treino.
- O target não tem transformação logarítmica neste exercício.
- Q4: RMSE arredondado a 4 casas; em caso de empate escolhe-se o menor `r`.

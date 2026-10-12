# Homework 3: Classificação (lead scoring)

Dataset: `course_lead_scoring_2026.csv` | Target: `converted`
Notebook: [homework.ipynb](homework.ipynb) | [Abrir no Google Colab](https://colab.research.google.com/drive/1mV63ZzE9gj5ZrqY5JzAU1N-C_1BJYjDP?usp=sharing)

## Respostas

| Questão | Resultado | Resposta |
|---------|-----------|----------|
| Q1 | moda de `industry` | `technology` |
| Q2 | corr(`interaction_count`, `lead_score`) = 0.916 | `interaction_count` e `lead_score` |
| Q3 | MI: `lead_source` 0.03, `employment_status` 0.02, `industry` 0.00, `location` 0.00 | `lead_source` |
| Q4 | accuracy = 0.645 | **0.65** |
| Q5 | diferenças: `lead_source` 0.003, `number_of_courses_viewed` 0.002, `interaction_count` 0.044 | `number_of_courses_viewed` |
| Q6 | melhor accuracy 0.645 com C = 0.001 | **0.001** |

## Notas
- Valores em falta: categóricas preenchidas com `'NA'`, numéricas com `0.0`.
- Q3 calculado só no conjunto de treino.
- Q4: a accuracy é 0.645; o `round` do NumPy dá 0.64 (arredonda para o par), mas o arredondamento convencional dá 0.65, que é a opção válida.
- Q5: a feature com menor diferença é a menos útil; retirar `interaction_count` custa 0.044 de accuracy.

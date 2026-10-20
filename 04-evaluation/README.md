# Homework 4: Avaliação de modelos (lead scoring)

Dataset: `course_lead_scoring_2026.csv` | Target: `converted`
Notebook: [homework.ipynb](homework.ipynb) | [Abrir no Google Colab](https://colab.research.google.com/drive/1oxsqVYrW4VpeWSTd8sk1NPWVrn2JLq0E?usp=sharing)

## Respostas

| Questão | Resultado | Resposta |
|---------|-----------|----------|
| Q1 | AUC: `lead_score` 0.7882, `interaction_count` 0.7649, `number_of_courses_viewed` 0.723, `annual_income` 0.6082 | `lead_score` |
| Q2 | AUC na validação = 0.732 | **0.732** |
| Q3 | precision e recall cruzam-se em 0.63 | **0.63** |
| Q4 | F1 máximo = 0.7576 | **0.41** |
| Q5 | AUC por fold: 0.7306, 0.7296, 0.7363, 0.7412, 0.7209; std = 0.007 | **0.007** |
| Q6 | média do AUC: C=1e-06 → 0.617, C=0.001 → 0.749, C=1 → 0.732 | **0.001** |

## Notas
- Split com `random_state=1` (60% treino, 20% validação, 20% teste).
- Q1: AUC calculado no treino, invertendo a variável quando o AUC é inferior a 0.5.
- Q3: ignoram-se os thresholds em que precision e recall são ambos 0.
- Q5 e Q6: `KFold(n_splits=5, shuffle=True, random_state=1)` sobre `df_full_train`; `np.std` (desvio padrão da população).

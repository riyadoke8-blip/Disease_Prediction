# Disease Prediction from Medical Data

## Overview

This project uses machine learning to estimate the likelihood of heart disease from structured patient data.

The project compares three classification algorithms and focuses on reducing false negatives because missing a potentially diseased patient can be more costly in a screening scenario.

## Dataset

The project uses the UCI Heart Disease dataset.

The dataset contains structured patient information such as:

- Age
- Sex
- Chest pain type
- Resting blood pressure
- Cholesterol
- Maximum heart rate
- Exercise-induced angina
- ST depression
- Other clinical features

## Machine Learning Models

Three classification algorithms were compared:

1. Logistic Regression
2. Decision Tree
3. Random Forest

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

## Results

Random Forest achieved the highest ROC-AUC:

| Model | ROC-AUC |
|---|---:|
| Logistic Regression | 0.904 |
| Decision Tree | 0.827 |
| Random Forest | 0.925 |

## Threshold Selection

The default Random Forest threshold of 0.50 produced 11 false negatives.

Because false negatives are more costly in a disease-screening scenario, a lower threshold of 0.40 was evaluated.

At a threshold of 0.40:

- False Negatives: 5
- False Positives: 25
- Recall: 95.1%

The lower threshold reduced false negatives from 11 to 5 while increasing recall.

Therefore, Random Forest with a threshold of 0.40 was selected as the final model for this project.

## Final Confusion Matrix

At the 0.40 threshold:

- True Negatives: 57
- False Positives: 25
- False Negatives: 5
- True Positives: 97

## Limitations

This project is an educational machine learning demonstration.

The model:

- Must not be used to diagnose heart disease.
- Must not be used to make medical or treatment decisions.
- Must not replace a qualified medical professional.
- Uses a limited dataset and may not represent all patient populations.
- Has a threshold that is not clinically validated.

Further validation using larger and more diverse clinical datasets would be required before considering any real-world clinical application.

## Project Files

- `Disease_Prediction.ipynb` — Complete analysis, preprocessing, model training and evaluation.
- `model_card.md` — Intended use, limitations and model information.

## Disclaimer

This project is for educational purposes only and is not a medical diagnostic tool.

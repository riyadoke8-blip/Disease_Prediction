# Model Card — Heart Disease Prediction

## Model Overview

This project uses machine learning to estimate the likelihood of heart disease from structured patient data.

Three classification algorithms were compared:

- Logistic Regression
- Decision Tree
- Random Forest

The final selected model is Random Forest with a classification threshold of 0.40.

## Intended Use

This model is intended for:

- Educational purposes
- Demonstrating machine learning classification
- Comparing classification algorithms
- Demonstrating threshold selection when false negatives are costly

## Model Selection

Random Forest achieved the highest ROC-AUC of 0.925.

At the default threshold of 0.50, the model produced 11 false negatives.

Because false negatives are more costly in a disease-screening scenario, the threshold was reduced to 0.40.

At the 0.40 threshold:

- Recall: 95.1%
- False Negatives: 5
- False Positives: 25
- True Negatives: 57
- True Positives: 97

The lower threshold was selected to prioritize sensitivity and reduce missed disease cases.

## Data

The model uses the UCI Heart Disease dataset.

The dataset contains structured patient information including demographic, clinical and examination-related features.

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

## Limitations

The dataset is limited and may not represent all patient populations.

Model performance may change when applied to new or external data.

The threshold of 0.40 has not been clinically validated.

The model may also be affected by missing data, data quality, and differences between the training population and real-world patients.

## What This Model Must Never Be Used For

This model must never be used to:

- Diagnose a real patient.
- Make medical or treatment decisions.
- Replace a qualified medical professional.
- Determine whether a patient should or should not receive medical care.

The predictions are not medically validated and should not be interpreted as a clinical diagnosis.

## Ethical and Safety Considerations

A false negative could result in a potentially diseased patient being missed. For this reason, recall and false-negative rates were given particular importance when selecting the threshold.

A lower threshold can reduce false negatives but may increase false positives. This trade-off should be carefully evaluated before any real-world application.

## Conclusion

This model demonstrates how classification algorithms and threshold selection can be used to prioritize recall in a disease-screening scenario.

However, substantial additional clinical validation would be required before any real-world use.

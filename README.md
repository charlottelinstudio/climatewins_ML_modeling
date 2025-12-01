# Climatewins ML Modeling

<b>ClimateWins: Pleasant Weather Prediction with Multi-Label ML Analysis</b>

This project analyzes 60+ years of European climate data using multi-label classification to predict daily pleasant weather across 15 stations. The analysis compares three model families, including KNN, Decision Tree, and Artificial Neural Network (ANN), with a focus on handling imbalanced labels and capturing station-level variability.

<b>Objectives</b>

Build and evaluate ML models for pleasant-weather prediction

Use macro-F1 to address label imbalance across stations

Compare model performance and generalization

Recommend the most reliable model for operational use

<b>Key Findings</b>

ANN Scenario 2 delivers the strongest overall performance (highest macro-F1 and most stable generalization).

Decision Tree (depth=10) performs well on predictable stations but is less consistent across variations.

KNN (k=3) is simple and stable but struggles with minority-class detection.

Data imbalance and noisy climate features heavily influence model behavior.

<b>Methods & Tools</b>

Python
- Pandas, NumPy
- Scikit-learn (KNN, DecisionTreeClassifier, MLPClassifier)
- Multi-label preprocessing and evaluation
- Macro-F1, classification reports, confusion matrices
- Gradient descent & loss analysis for ANN stability

<b>Recommendations</b>

Adopt ANN Scenario 2 as the baseline forecasting model

Track macro-F1 as the primary KPI

Add temporal features (seasonality, lags)

Consider Random Forest / Gradient Boosting for interpretability

Explore LSTM/GRU models for sequential weather prediction

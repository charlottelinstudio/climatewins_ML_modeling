# Climatewins ML Modeling

<b>ClimateWins: Pleasant Weather Prediction with Multi-Label ML Analysis</b>

This project analyzes 60+ years of European climate data using multi-label classification to predict daily pleasant weather across 15 stations. <b>Part 1</b> of the analysis compares three model families, including KNN, Decision Tree, and Artificial Neural Network (ANN), with a focus on handling imbalanced labels and capturing station-level variability. <b>Part 2</b> extends the original pleasant-weather classification work by shifting from baseline model comparison to structural pattern discovery, temporal instability analysis, interpretability, and scenario reasoning. These analyses are designed to align more directly with ClimateWins’ strategic questions around climate variability and long-term risk.

<b>Objectives</b>
<u>Part 1</u>
- Build and evaluate ML models for pleasant-weather prediction
- Use macro-F1 to address label imbalance across stations
- Compare model performance and generalization
- Recommend the most reliable model for operational use

<u>Part 2</u>
- Identify historical weather patterns that fall outside regional climate norms
- Examine whether atypical or unstable weather patterns are increasing over time
- Improve model robustness through hyperparameter optimization
- Evaluate interpretability and explainability for climate decision support
- Explore the feasibility of visual machine learning as a complementary signal

<b>Key Findings</b>
<u>Part 1</u>
- ANN Scenario 2 delivers the strongest overall performance (highest macro-F1 and most stable generalization).
- Decision Tree (depth=10) performs well on predictable stations but is less consistent across variations.
- KNN (k= 1 to 3) is simple and stable but struggles with minority-class detection.
- Data imbalance and noisy climate features heavily influence model behavior.

<u>Part 2</u>
- Stations cluster by climate behavior rather than geography alone
- Anomalous patterns appear as statistical outliers within otherwise stable clusters
- Regional climate “norms” can be defined quantitatively, enabling anomaly detection
- CNNs learn stable and generalizable patterns across most stations
- Performance varies by station, reflecting differences in variability and signal quality
- Deep learning is effective for tracking pattern stability, not just prediction accuracy
- Model performance is uneven across Europe
- Some stations exhibit stable, learnable behavior; others show higher volatility
- Macro-level metrics can obscure localized instability if not examined carefully
- Tuned CNN models show meaningful improvements in macro-F1, recall, and validation AUC
- Model stability is driven more by architecture and regularization choices than raw complexity
- Hyperparameter optimization is essential for reliable climate ML applications
- Visual ML can distinguish broad weather categories
- Results are best interpreted as a proof of concept
- Image-based models complement but do not replace structured climate data

<b>Methods & Tools</b>

Python
- Pandas, NumPy
- Scikit-learn (KNN, DecisionTreeClassifier, MLPClassifier)
- Multi-label preprocessing and evaluation
- Macro-F1, classification reports, confusion matrices
- Gradient descent & loss analysis for ANN stability
- PCA
- Hierarchical clustering
- Convolutional Neural Networks (CNNs)
- Per-station precision, recall, F1, AUC; macro-averaging
- Bayesian optimization of CNN architecture
- CNN-based image classification of weather conditions

<b>Recommendations</b>

- Adopt ANN Scenario 2 as the baseline forecasting model
- Track macro-F1 as the primary KPI
- Add temporal features (seasonality, lags)
- Consider Random Forest / Gradient Boosting for interpretability
- Explore LSTM/GRU models for sequential weather prediction
- Use unsupervised learning (PCA and clustering) as an early-warning system
- Adopt tuned CNNs for tracking climate instability over time
- Prioritize interpretability for long-term decision support
- Treat generative models as exploratory tools, not predictors
- Evaluate models using macro-level and station-level metrics
- Integrate non-weather data before extending habitability conclusions


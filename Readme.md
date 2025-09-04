# Fraud Detection Model for Financial Transactions

## About the Dataset
The dataset contains over 6 million records of financial transactions with the following key features:
- `step`: Time step of the transaction.
- `type`: Transaction type (e.g., PAYMENT, TRANSFER, CASH_OUT).
- `amount`: Transaction amount.
- `nameOrig`: Originator account ID.
- `oldbalanceOrg` and `newbalanceOrig`: Originator’s account balance before and after the transaction.
- `nameDest`: Destination account ID.
- `oldbalanceDest` and `newbalanceDest`: Destination’s account balance before and after the transaction.
- `isFraud`: Binary label indicating fraudulent transactions.
- `isFlaggedFraud`: Flagged fraud cases by the system.

---

## Project Workflow
- Load and explore the dataset to understand structure and contents.
- Clean data to handle any missing or inconsistent values.
- Perform feature engineering:
  - One-hot encoding of transaction types.
  - Creating new features such as balance differences.
- Conduct exploratory data analysis (EDA) to visualize distributions and relationships.
- Split data into training and testing sets.
- Train multiple machine learning models.
- Tune hyperparameters to optimize model performance.
- Evaluate models using diverse performance metrics.
- Interpret model predictions with explainability techniques.
- Generate business insights for fraud prevention.

---

## Training, Model Building, and Evaluation

### Machine Learning Algorithms Used:
- **Logistic Regression**: Baseline model for classification.
- **Random Forest**: Ensemble of decision trees to capture non-linear relationships.
- **XGBoost (Extreme Gradient Boosting)**: Gradient boosting algorithm known for high accuracy and handling complex patterns.
- **LightGBM**: Efficient gradient boosting implementation optimized for speed and performance.

### Training Details:
- Data preprocessing involved encoding categorical features and scaling numeric data.
- Models were trained on the training subset with cross-validation for robustness.
- Hyperparameter tuning was performed with GridSearchCV or RandomizedSearchCV to find optimal parameters.
- Class imbalance was addressed through techniques such as undersampling or oversampling if needed.

### Evaluation Metrics:
- Accuracy, Precision, Recall, F1-Score to balance detection sensitivity and false positives.
- ROC-AUC to measure overall model discrimination ability.
- Confusion matrices to illustrate true positives, false positives, true negatives, and false negatives.

### Model Explainability:
- SHAP (SHapley Additive exPlanations) values were computed to assess feature importance.
- Visual explanations helped identify key factors contributing to fraud detection decisions.

---

## Conclusion
This project successfully developed a robust machine learning pipeline for fraud detection in financial transactions. The best-performing models demonstrated strong predictive power to identify fraudulent behavior, thereby helping financial entities reduce losses and improve security. The added interpretability through SHAP values ensures model decisions are transparent and actionable for business stakeholders.

---

## Future Scope
- Deploy real-time fraud detection models for live transaction scoring.
- Incorporate additional domain-specific features to improve detection accuracy.
- Explore deep learning architectures for handling more complex fraud patterns.
- Automate model retraining pipelines to adapt to evolving fraud tactics.
- Integrate the system with existing financial platforms for continuous monitoring.

---

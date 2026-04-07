# machine-learning-pipeline-for-the-Titanic-dataset

##  Overview
This project builds a complete end-to-end machine learning pipeline on the Titanic dataset to predict passenger survival. It demonstrates a professional workflow including data preprocessing, model training, evaluation, cross-validation, and model persistence.



##  Objective
To develop a reliable classification model using Logistic Regression that predicts whether a passenger survived based on key features.



##  Workflow

### 1. Data Preparation
- Selected features: `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`
- Target variable: `Survived`
- Handling missing values:
  - Numeric → Median Imputation
  - Categorical → Most Frequent Imputation
- Encoding:
  - One-Hot Encoding for categorical features
- Feature Scaling:
  - Standardization applied to numeric features



### 2. Model Building
- Algorithm: Logistic Regression (baseline model)
- Built using `Pipeline` and `ColumnTransformer`
- Ensures clean and reproducible workflow



### 3. Model Evaluation
- Train-Test Split: 80/20 (Stratified)
- Metrics Used:
  - Accuracy
  - Precision, Recall, F1-score
  - Confusion Matrix
  - ROC Curve & ROC-AUC Score



### 4. Cross-Validation
- 5-Fold Cross Validation
- Metric: ROC-AUC
- Provides stable and reliable performance estimate



### 5. Model Persistence
- Saved trained pipeline using `joblib`
- File: `model.joblib`
- Enables reuse without retraining



## 📊 Key Insights
- Gender plays a major role in survival prediction
- Higher class passengers had better survival rates
- Fare is positively correlated with survival
- Logistic Regression provides a simple and interpretable baseline



##  Limitations
- Linear model may miss complex relationships
- Limited feature engineering
- Dataset contains missing and noisy data


##  Future Improvements
- Try advanced models (Random Forest, XGBoost)
- Feature engineering (Family size, Title extraction)
- Hyperparameter tuning (GridSearchCV)
- Handle class imbalance techniques


##  Project Structure
├── titanic.ipynb
├── model.joblib
├── README.md
└── images/ (optional plots)


## 🛠️ Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn


## 📌 Conclusion
This project demonstrates a complete ML pipeline with proper preprocessing, evaluation, and deployment readiness. It highlights the importance of reproducibility and interpretability in machine learning workflows.

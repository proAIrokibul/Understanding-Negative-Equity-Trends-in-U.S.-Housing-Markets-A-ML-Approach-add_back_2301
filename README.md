# Understanding Negative Equity Trends in U.S. Housing Markets A Machine Learning Approach to Predictive Analysis

### **Project Description**
This project, **"Understanding Negative Equity Trends in U.S. Housing Markets: A Machine Learning Approach to Predictive Analysis,"** aims to predict whether a housing region experiences negative equity by leveraging historical data and machine learning techniques. The project followed a comprehensive data pipeline from preprocessing to model evaluation and comparison, ensuring robust and actionable insights.

---

### **Process Overview**

#### **1. Data Preprocessing**
- **Handling Missing Values**:
  - Categorical columns were imputed with the mode.
  - Numerical columns were imputed with the median.
- **Feature Engineering**:
  - Created `equity_growth` to measure changes in equity values over time.
  - Derived `equity_class` to categorize regions based on their equity trends.
- **Scaling and Balancing**:
  - Scaled the dataset using standard scaling techniques.
  - Applied oversampling to address class imbalances and ensure fair representation of all target labels.

#### **2. Modeling Techniques**
Three machine learning algorithms were applied to predict the `equity_class` target variable:

1. **Logistic Regression**: A linear model offering simplicity and interpretability.
2. **Random Forest**: An ensemble learning approach that combines decision trees to improve accuracy and reduce overfitting.
3. **XGBoost**: A high-performance gradient boosting algorithm that optimizes predictive performance, especially for imbalanced datasets.

#### 3. Model Evaluation 
Each model was evaluated using metrics like **Accuracy**, **Precision**, **Recall**, **F1-Score**, and classification reports. Below are the results:

---

### Model Evaluation Results

#### Logistic Regression
- Classification Report:
  ```
      precision    recall  f1-score   support

 0       0.59      0.73      0.65      2058
 1       0.56      0.45      0.50      1836
 2       0.00      0.00      0.00       115

accuracy                           0.58      4009
 macro avg       0.38      0.39      0.38      4009
weighted avg       0.56      0.58      0.56      4009
  ```
- Accuracy: 57.72%
- This model, while interpretable, struggled with handling class imbalances and complex feature interactions.

---

#### Random Forest
- Classification Report:
  ```
               precision    recall  f1-score   support

           0       0.98      0.98      0.98      2058
           1       0.95      0.98      0.96      1836
           2       1.00      0.59      0.74       115

    accuracy                           0.97      4009
   macro avg       0.98      0.85      0.90      4009
weighted avg       0.97      0.97      0.97      4009
  ```
-Accuracy: 96.68%
- This model demonstrated strong performance, though recall for the minority class (class `2`) was moderate.

---

#### XGBoost
- Classification Report:
  ```
  precision    recall  f1-score   support

  0       0.99      0.99      0.99      2058
  1       0.99      0.99      0.99      1836
  2       0.95      0.97      0.96       115

  accuracy                           0.99      4009
   macro avg       0.98      0.98      0.98      4009
weighted avg       0.99      0.99      0.99      4009
  ```
- Accuracy: 99.08%
- This model excelled, achieving near-perfect metrics across all classes, even with the imbalanced dataset.


### Business Impact
The results of this analysis offer significant value to stakeholders in the housing and financial sectors:

#### 1. Proactive Risk Management
- Financial institutions can identify regions at risk of negative equity, enabling better resource allocation and risk mitigation strategies.
- Mortgage lenders can use these insights to design flexible loan products and minimize default risks.

#### 2. Policy and Planning
- Policymakers can prioritize regions in economic distress and implement targeted interventions, such as subsidies, tax relief, or restructuring programs.

#### 3. Real Estate Market Dynamics
- Real estate firms and investors can identify regions with favorable equity trends, optimizing pricing strategies and investment portfolios.

#### 4. Economic Stability
- By accurately predicting negative equity trends, the model contributes to a more stable housing market, reducing risks of financial crises.

---

### Conclusion
This project demonstrates the power of machine learning in solving real-world problems by delivering actionable insights with high predictive accuracy. The **XGBoost model**, with its superior performance, is the recommended approach for analyzing negative equity trends in the U.S. housing market. Its ability to handle data complexities ensures reliable predictions that drive impactful business decisions.

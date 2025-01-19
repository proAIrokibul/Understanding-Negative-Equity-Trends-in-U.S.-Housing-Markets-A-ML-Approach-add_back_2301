# Understanding Negative Equity Trends in U.S. Housing Markets: A Machine Learning Approach to Predictive Analysis

## Project Overview

This project aims to predict whether a housing region experiences negative equity using historical data and machine learning techniques. The goal is to provide insights that can help stakeholders, including policymakers, real estate professionals, and financial institutions, better understand and mitigate risks related to negative equity in the U.S. housing market.

## Process Overview

### 1. Data Preprocessing
- **Missing Value Handling**: The dataset had missing values in key columns like `StateName`, `City`, and `MSA`. These were handled using imputation techniques appropriate for categorical and numerical data.
- **Feature Engineering**: 
  - `equity_growth`: The percentage change in equity.
  - `equity_class`: A binary classification target variable (1 for negative equity, 0 for otherwise).
- **Outlier Detection**: Potential outliers were detected and managed to ensure model robustness.
- **Scaling**: The features were scaled using standardization techniques to ensure compatibility across different machine learning models.

### 2. Machine Learning Models
Three machine learning algorithms were applied to predict the `equity_class` target variable:

- **Logistic Regression**: A baseline linear model offering simplicity and interpretability.
- **Random Forest**: An ensemble learning model that combines decision trees, improving predictive accuracy and reducing overfitting.
- **XGBoost**: A gradient boosting technique optimized for performance, particularly effective for imbalanced datasets.

### 3. Model Evaluation
Each model was evaluated using a variety of performance metrics: **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **Classification Report**. The following are the results for each model:

#### Logistic Regression Model Evaluation
- **Accuracy**: 57.72%
- **Classification Report**:

       precision    recall    f1-score   support

      0       0.59      0.73      0.65      2058
      1       0.56      0.45      0.50      1836
      2       0.00      0.00      0.00       115

      accuracy                      0.58      4009
      macro avg 0.38      0.39      0.38      4009 
      weighted avg 0.56   0.58      0.56      4009



#### Random Forest Model Evaluation
- **Accuracy**: 96.68%
- **Classification Report**:

       precision    recall  f1-score   support

      0      0.98      0.98      0.98      2058
      1      0.95      0.98      0.96      1836
      2      1.00      0.59      0.74       115

      accuracy                     0.97      4009
      macro avg 0.98      0.85     0.90      4009 
      weighted avg 0.97   0.97     0.97      4009


#### XGBoost Model Evaluation
- **Accuracy**: 99.08%
- **Classification Report**:

       precision    recall  f1-score   support

      0       0.99      0.99      0.99      2058
      1       0.99      0.99      0.99      1836
      2       0.95      0.97      0.96       115

      accuracy                      0.99      4009
      macro avg 0.98      0.98      0.98      4009 
      weighted avg 0.99   0.99      0.99      4009


## Model Comparison

- **Logistic Regression**: While interpretable, the logistic regression model showed low performance, particularly with class `2` (the minority class). The accuracy was 57.72%, and the recall for the minority class was almost 0%.
  
- **Random Forest**: This model significantly improved performance, achieving an accuracy of 96.68%. However, recall for class `2` was still only 59%, which could be improved. It performed well overall, especially for balanced classes.

- **XGBoost**: XGBoost delivered the best results with 99.08% accuracy. The model was able to effectively handle the class imbalance, achieving high precision and recall for all classes. The recall for class `2` reached 97%, showcasing the strength of this model.

## Business Impact

This analysis provides valuable insights for stakeholders across various sectors in the housing market:

### 1. **Proactive Risk Management**:
   - Financial institutions can use the model to identify regions at risk of negative equity and adjust loan policies or create new financial products.
   - Mortgage lenders can assess regions more likely to experience negative equity, helping them develop flexible repayment structures for affected homeowners.

### 2. **Policy and Planning**:
   - Policymakers can prioritize areas for economic intervention and implement targeted measures like tax relief, subsidies, or restructuring programs to alleviate negative equity.

### 3. **Real Estate Market Dynamics**:
   - Real estate companies can optimize investment strategies by identifying regions with favorable or challenging equity trends, influencing their pricing and portfolio decisions.

### 4. **Economic Stability**:
   - By predicting negative equity, the model contributes to stabilizing the housing market and reducing the risk of a housing-related financial crisis, ensuring a more resilient economy.

## Conclusion

The machine learning models demonstrated varying degrees of accuracy, with **XGBoost** emerging as the most reliable and efficient model for predicting negative equity trends. Its high performance, especially in handling imbalanced classes, positions it as the best choice for forecasting negative equity in the U.S. housing market.

By applying these predictive models, stakeholders in the housing and financial sectors can make data-driven decisions, reducing risks and optimizing their strategies for long-term stability and growth in the market.











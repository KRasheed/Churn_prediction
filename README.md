# Customer Churn Prediction Analysis

This repository contains a Jupyter Notebook for analyzing customer churn and predicting the customer will going to **churn** or not. The dataset used in this project includes customer service usage data, account details, and churn information.

## Analysis Flow

### 1. **Data Loading and Inspection**
    The notebook begins by loading the dataset, which includes detailed information about customer accounts and usage patterns. A preliminary inspection of the data is performed to examine the structure and key features, such as account length, service usage, and customer service interactions. The analysis then focuses on understanding the churn rate among high-value customers versus low-value customers. High-value customers, who typically contribute significantly to revenue, are identified as being at higher risk of churn. By targeting these customers for retention strategies, businesses can optimize their efforts to reduce churn and maximize revenue.
   
### 2. **Classification of customers Types**
   - Rules are applied to create the `High_value_customer` column based on various factors such as customer service calls, usage minutes, and account length.

### 4. **Machine Learning Models**
   - Several machine learning models are applied to predict churn, including Random Forest, XGBoost, and LightGBM.
   - **Cross-validation** and **Stratified K-Folds** are used to evaluate model performance, ensuring that the class imbalance is handled properly.

### 5. **Handling Class Imbalance**
   - The dataset is imbalanced with more **non-churned** customers than **churned** customers. To address this, the notebook uses **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the dataset.
   
### 6. **Model Optimization**
   - **Optuna** is used for hyperparameter tuning to optimize the models and achieve the best possible performance.
   - Feature importance is assessed using Random Forest and LightGBM models, and the **Variance Inflation Factor (VIF)** is used to check for multicollinearity and remove irrelevant features.

### 7. **Model Evaluation**
   - The models are evaluated using metrics such as **Precision**, **Recall**, **F1-Score**, and **AUC**.
   - Performance metrics are printed to assess the predictive power of each model.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/customer-churn-analysis.git

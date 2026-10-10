# Customer Churn Prediction

## Project Overview
This project uses machine learning to predict customer churn using a telecom customer dataset. It explores customer characteristics and compares classification models to identify customers who may leave the service.

## Objectives
- Analyze customer churn patterns using Exploratory Data Analysis (EDA).
- Prepare categorical and numerical features for machine learning.
- Train and compare Logistic Regression and Random Forest classifiers.
- Evaluate models using precision, recall, F1-score, and ROC-AUC.
- Identify important predictive features and examine classification thresholds.

## Technologies Used
- Python
- Pandas and NumPy
- Scikit-learn
- Matplotlib

## Workflow
1. Load and inspect the dataset.
2. Handle missing values and preprocess features.
3. Perform exploratory data analysis.
4. Split data into training and testing sets.
5. Train Logistic Regression and Random Forest models.
6. Tune Logistic Regression using GridSearchCV.
7. Evaluate performance using classification metrics, a confusion matrix, and an ROC curve.
8. Analyze feature importance using permutation importance.

## Model Results

| Model | Test ROC-AUC |
|---|---:|
| Logistic Regression | 0.8421 |
| Random Forest | 0.8201 |

Logistic Regression achieved the higher ROC-AUC on the held-out test set.

At a classification threshold of 0.40, Logistic Regression achieved approximately 0.67 recall for the churn class, with a precision of approximately 0.57.

## Key Findings
- Customer tenure, internet service type, and contract type were among the most important predictive features according to permutation importance.
- Month-to-month customers showed a higher churn rate than customers with longer-term contracts in the exploratory analysis.
- Lowering the classification threshold increased churn recall but reduced precision and accuracy.

## Limitations
The model was evaluated on a held-out test set. Further validation on new customer data and assessment of business outcomes would be needed before real-world deployment.

## Project File
- `Customer_Churn_Prediction.ipynb` — notebook containing data preprocessing, analysis, model training, and evaluation.

## Future Improvements
- Validate the classification threshold using validation data.
- Test the model on new customer data.
- Develop a simple interface for churn predictions.

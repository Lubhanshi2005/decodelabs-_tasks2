# Credit Card Fraud Detection Using Machine Learning

## 📌 Project Overview

Credit card fraud is a major problem in digital financial transactions. This project uses Machine Learning to identify potentially fraudulent credit card transactions based on transaction data.

The project uses **Logistic Regression** to classify transactions into two categories:
- **0 – Legitimate Transaction**
- **1 – Fraudulent Transaction**

The main objective is to build a machine learning model that can help identify suspicious transactions and evaluate its performance using appropriate classification metrics.

## 🎯 Objectives

- Analyze credit card transaction data.
- Clean the dataset by handling missing values and duplicate records.
- Visualize legitimate and fraudulent transactions.
- Train a machine learning model using Logistic Regression.
- Evaluate the model using Accuracy, Precision, Recall, F1-score, and a Confusion Matrix.
- Save the trained model for future use.

## 🛠️ Technologies Used

- **Python**
- **Google Colab**
- **Pandas** – Data manipulation and analysis
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Scikit-learn** – Machine learning and model evaluation
- **Joblib** – Saving the trained model

## 📂 Dataset Information

The dataset used in this project is named `creditcard.csv`.

It contains transaction-related features, including:

- `Time` – Time elapsed from the first transaction in the dataset.
- `V1` to `V28` – Anonymized numerical features.
- `Amount` – Transaction amount.
- `Class` – Target variable indicating whether a transaction is legitimate or fraudulent.

**Target variable:**
- `0` represents a legitimate transaction.
- `1` represents a fraudulent transaction.

## 🔄 Project Workflow

1. **Data Loading:** Load the dataset into Google Colab using Pandas.
2. **Data Exploration:** Inspect the dataset, column names, data types, and transaction records.
3. **Data Cleaning:** Remove rows containing missing values and exact duplicate records.
4. **Data Visualization:** Create charts to explore transaction classes and transaction amounts.
5. **Feature Selection:** Separate the input features from the target variable.
6. **Data Splitting:** Split the dataset into training and testing sets using an 80:20 ratio.
7. **Feature Scaling:** Use StandardScaler within a machine learning pipeline.
8. **Model Training:** Train a Logistic Regression classifier with balanced class weights.
9. **Model Evaluation:** Evaluate predictions using classification metrics and a confusion matrix.
10. **Model Saving:** Save the trained pipeline as `credit_card_fraud_model.pkl`.

## 🤖 Machine Learning Algorithm

**Logistic Regression** is used as the classification algorithm. It estimates the probability that a transaction belongs to the fraudulent class.

The model uses `class_weight='balanced'` to account for the unequal distribution of legitimate and fraudulent transactions.

## 📊 Model Evaluation

The model is evaluated using the following metrics:

| Metric | Purpose |
|---|---|
| Accuracy | Measures the proportion of correct predictions. |
| Precision | Measures how many predicted fraud cases were actually fraudulent. |
| Recall | Measures how many actual fraud cases were detected. |
| F1-score | Balances precision and recall. |
| Confusion Matrix | Shows correct and incorrect predictions for both classes. |

Recall and precision are especially important because fraudulent transactions are rare compared with legitimate transactions.

*The actual evaluation results should be added here after reviewing the model output.*

## 📁 Project Files

- `Credit_Card_Fraud_Detection.ipynb` – Jupyter notebook containing the project workflow.
- `credit_card_fraud_model.pkl` – Saved machine learning pipeline.
- `README.md` – Project documentation.

The dataset is not included in the repository. Obtain it separately from its original source, subject to its licence and sharing permissions.

## 🚀 How to Run the Project

1. Download or clone this repository.
2. Open Google Colab at https://colab.research.google.com/.
3. Upload and open the project notebook.
4. Obtain the dataset and upload `creditcard.csv` to the Colab session.
5. Run the notebook cells in order, from data loading through model evaluation.
6. The trained model can be saved using Joblib.

To load the saved model later, use:

```python
import joblib

model = joblib.load("credit_card_fraud_model.pkl")
```

## 🔮 Future Improvements

- Compare Logistic Regression with Random Forest and other classification algorithms.
- Experiment with resampling techniques to address class imbalance.
- Tune model parameters to improve fraud detection.
- Develop a simple web interface for transaction predictions.
- Evaluate performance on additional unseen transaction data.



## ⭐ Conclusion

This project demonstrates a basic end-to-end machine learning workflow for credit card fraud detection, including data cleaning, exploratory analysis, model training, evaluation, and model persistence.

The project provides a foundation for exploring more advanced fraud detection techniques and improving the identification of suspicious financial transactions.


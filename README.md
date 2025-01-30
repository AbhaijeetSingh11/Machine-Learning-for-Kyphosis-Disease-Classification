# Machine Learning for Kyphosis Disease Classification

## Project Overview
This project focuses on using machine learning techniques to classify **Kyphosis Disease**, a condition characterized by an excessive convex curvature of the spine. The goal is to develop a predictive model that can classify whether a patient has kyphosis based on medical features.

## Dataset
The dataset used for this project contains medical records of patients who have undergone spinal surgery. It includes features such as:
- `Age`: The age of the patient (in months).
- `Number`: The number of vertebrae involved in the surgery.
- `Start`: The vertebra number at which the surgery started.
- `Kyphosis`: The target variable (1 for presence, 0 for absence of kyphosis).

## Requirements
To run this project, you need to install the following dependencies:
```bash
pip install numpy pandas scikit-learn seaborn matplotlib
```

## Steps Involved
1. **Data Preprocessing**
   - Handle missing values (if any)
2. **Exploratory Data Analysis (EDA)**
   - Statistical summary using `df.describe()`
   - Checking missing values with `df.isnull().sum()`
   - Correlation matrix using `df.corr()`
3. **Splitting the Data**
   - Use `train_test_split()` to divide data into training and testing sets (80%-20%)
4. **Model Training**
   - Train a **Logistic Regression** model using:
     ```python
     from sklearn.linear_model import LogisticRegression
     model = LogisticRegression()
     model.fit(X_train, y_train)
     ```
5. **Model Evaluation**
   - Assess accuracy and classification performance using:
     ```python
     from sklearn.metrics import accuracy_score, classification_report
     y_pred = model.predict(X_test)
     print(accuracy_score(y_test, y_pred))
     print(classification_report(y_test, y_pred))
     ```
6. **Handling Overfitting**
   - Monitor training and validation loss to detect overfitting.
   - Implement regularization techniques if necessary.

## Expected Outcome
- A trained machine learning model that classifies kyphosis with high accuracy.
- Visual insights into the relationships between different medical parameters.
- Awareness of potential overfitting issues and how to mitigate them.

## Author
**Abhaijeet Singh**  
Project completed as part of a **Coursera Machine Learning Course** under **Thapar Institute of Engineering & Technology**.

## License
This project is for educational purposes only. Feel free to modify and experiment with it!


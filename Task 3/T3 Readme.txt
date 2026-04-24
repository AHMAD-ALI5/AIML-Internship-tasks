# ❤️ Heart Disease Prediction (Machine Learning Project)

## 📌 Overview

This project builds a machine learning model to predict whether a person is at risk of heart disease based on medical attributes. It follows a complete data science workflow including data cleaning, exploratory data analysis (EDA), model training, evaluation, and feature importance analysis.

---

## 🎯 Objective

To develop a **binary classification model** that predicts the presence of heart disease using patient health data.

---

## 📊 Dataset

* **Source:** UCI Heart Disease Dataset (available on Kaggle)

* Contains medical attributes such as:

  * Age
  * Sex
  * Chest pain type
  * Resting blood pressure
  * Cholesterol level
  * Maximum heart rate
  * And more...

* **Target Variable:**

  * `1` → Presence of heart disease
  * `0` → No heart disease

---

## 🛠️ Technologies Used

* Python 🐍
* Jupyter Notebook 📓
* Libraries:

  * `pandas`, `numpy`
  * `matplotlib`, `seaborn`
  * `scikit-learn`

---

## ⚙️ Project Workflow

### 1️⃣ Data Loading & Cleaning

* Loaded dataset using Pandas
* Checked for missing values
* Handled missing values (if present)
* Converted categorical variables to numeric using **one-hot encoding**
* Converted boolean values to integers for compatibility

---

### 2️⃣ Exploratory Data Analysis (EDA)

* Distribution of target variable
* Correlation heatmap between features
* Visualization of key relationships (e.g., age vs heart disease)

---

### 3️⃣ Data Preprocessing

* Split dataset into training and testing sets (80/20)
* Feature scaling using **StandardScaler**

---

### 4️⃣ Model Training

Two classification models were implemented:

* **Logistic Regression**
* **Decision Tree Classifier**

---

### 5️⃣ Model Evaluation

Models were evaluated using:

* ✅ Accuracy Score
* ✅ Confusion Matrix
* ✅ ROC Curve
* ✅ ROC-AUC Score

---

### 6️⃣ Feature Importance Analysis

* Logistic Regression coefficients used to determine feature influence
* Decision Tree feature importance used to identify key predictors

---

## 📈 Results

* Achieved good accuracy on test data
* ROC-AUC score indicates strong classification performance
* Identified important features such as:

  * Chest pain type
  * Maximum heart rate
  * ST depression (oldpeak)
  * Number of major vessels

---

## 🚀 How to Run

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/heart-disease-prediction.git
cd heart-disease-prediction
```

### 2️⃣ Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 3️⃣ Run Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook and run all cells step-by-step.

---

## 📁 Project Structure

```
📦 heart-disease-prediction
 ┣ 📜 heart_disease.ipynb
 ┣ 📜 README.md
 ┣ 📊 heart.csv
 ┗ 📂 images (optional)
```

---

## 🧠 Key Learnings

* Handling categorical and boolean data in ML pipelines
* Performing EDA on medical datasets
* Applying classification algorithms
* Evaluating models using ROC-AUC and confusion matrix
* Interpreting feature importance

---

## 📌 Future Improvements

* Add advanced models (Random Forest, XGBoost)
* Hyperparameter tuning
* Deploy model as a web application
* Use larger and more diverse datasets

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository and submit a pull request.

---

## 📜 License

This project is for educational purposes.

---

## 👨‍💻 Author

Your Name
GitHub: https://github.com/AHMAD-ALI5

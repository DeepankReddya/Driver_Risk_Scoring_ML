# Driver Risk Scoring Using Machine Learning

## Project Overview

This project implements a **Machine Learning–based Driver Risk Scoring System** that analyzes driving behaviour patterns using sensor data. The system predicts the **risk level of a driver** based on gyroscope and acceleration signals collected during driving sessions.

The model classifies drivers into different **risk categories** and generates a **risk score (0–100)** indicating the likelihood of risky driving behaviour.

This project demonstrates a **complete end-to-end Machine Learning pipeline**, including data preprocessing, feature engineering, model training, evaluation, and deployment using a **Streamlit web application**.

---

# Objectives

The main goals of this project are:

* Analyze driving behaviour using sensor data
* Classify drivers into risk categories
* Generate a driver **risk score**
* Compare multiple Machine Learning models
* Deploy the system through an interactive **Streamlit application**
* Automate training using **GitHub Actions**

---

# Machine Learning Models Used

The following models were implemented and compared:

* Logistic Regression
* Decision Tree
* Random Forest
* Support Vector Machine (SVM)

Among these, **Random Forest** performed the best for this dataset.

---

# Dataset Features

The dataset contains **smartphone sensor data** collected during driving sessions.

| Feature | Description                  |
| ------- | ---------------------------- |
| GyroX   | Gyroscope movement on X-axis |
| GyroY   | Gyroscope movement on Y-axis |
| GyroZ   | Gyroscope movement on Z-axis |
| AccX    | Acceleration on X-axis       |
| AccY    | Acceleration on Y-axis       |
| AccZ    | Acceleration on Z-axis       |

Additional engineered features:

* Acceleration magnitude
* Gyroscope magnitude
* Acceleration intensity
* Gyroscope intensity
* Movement index

These features help capture **driving behaviour patterns** more effectively.

---

# Driver Risk Categories

The trained model predicts four driver categories:

| Class | Driver Type          |
| ----- | -------------------- |
| 1     | Safe Driver          |
| 2     | Low Risk Driver      |
| 3     | Moderate Risk Driver |
| 4     | High Risk Driver     |

The system also generates a **risk score (0–100)** based on model confidence.

---

# Project Structure

```
driver-risk-scoring-ml
│
├── app
│   └── streamlit_app.py
│
├── data
│   └── driving_data.csv
│
├── models
│   ├── logistic.pkl
│   ├── decision_tree.pkl
│   ├── random_forest.pkl
│   └── svm.pkl
│
├── notebooks
│
├── src
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── train_model.py
│   ├── evaluate_model.py
│   └── risk_score.py
│
├── main.py
├── requirements.txt
└── README.md
```

---

# Machine Learning Pipeline

The project follows a modular ML pipeline:

```
Data Loading
     ↓
Data Preprocessing
     ↓
Feature Engineering
     ↓
Model Training
     ↓
Model Evaluation
     ↓
Risk Score Generation
     ↓
Streamlit Deployment
```

---

# Streamlit Web Application

The project includes an interactive **Streamlit application** where users can:

* Enter driving sensor values
* Predict driver risk category
* View driver risk score

Example Output:

```
Driver Type: Moderate Risk Driver
Risk Score: 82 / 100
Prediction Confidence: 0.82
```

---

# Installation & Setup

Clone the repository:

```
git clone https://github.com/YOUR_USERNAME/driver-risk-scoring-ml.git
cd driver-risk-scoring-ml
```

Install dependencies:

```
pip install -r requirements.txt
```

---

# Running the ML Pipeline

Train the models:

```
python main.py
```

This will:

* preprocess the dataset
* train ML models
* evaluate model performance
* save trained models to the `models/` folder

---

# Running the Streamlit App

Start the web application:

```
streamlit run app/streamlit_app.py
```

The application will open in your browser.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Streamlit
* Joblib
* Git
* GitHub Actions

---

# Continuous Integration

This repository uses **GitHub Actions** to automatically:

* install dependencies
* run the machine learning pipeline
* verify that the project builds successfully

This ensures the repository remains stable and reproducible.

---

# Future Improvements

Potential improvements include:

* Real-time driver monitoring
* Deep learning models for behaviour analysis
* Mobile integration for sensor data collection
* Advanced risk scoring algorithms
* Visualization dashboards

---

# Author

**Deepank Reddy A**


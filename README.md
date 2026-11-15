# 🧠 MentalHealth-Predictor
### AI-Powered Student Mental Wellness Prediction System

An ML-powered student mental wellness prediction system that analyzes social media usage, digital habits, academic activities, sleep patterns, physical activity, and perceived stress levels to generate a predicted mental wellness score.

The project combines Machine Learning, FastAPI, and JavaScript to provide an interactive platform where users can enter their daily lifestyle information and receive a model-generated wellness score.

> **Note:** This project is intended for educational and awareness purposes. Its predictions are not medical diagnoses or a substitute for professional mental health assessment.

---

## 🌟 Project Overview

Students today spend a significant amount of time on social media, digital platforms, and academic activities. These habits, combined with sleep patterns, physical activity, and stress levels, can influence their overall well-being.

MentalHealth-Predictor aims to explore these relationships using machine learning.

Users provide information through an interactive web interface, and the trained ML model analyzes the submitted information to generate a predicted mental wellness score on a scale of **0–10**.

### 🎯 Project Objectives

- Analyze the relationship between digital habits and student mental wellness.
- Explore how screen time and social media usage relate to wellness.
- Understand the influence of sleep, physical activity, and academic workload.
- Apply machine learning algorithms to predict wellness scores.
- Compare multiple regression models using evaluation metrics.
- Integrate the trained ML model with a FastAPI backend.
- Develop an interactive frontend for real-time predictions.

---

## ✨ Key Features

- **Interactive User Interface:** Clean and responsive interface for entering lifestyle information.
- **Lifestyle Analysis:** Considers screen time, sleep, study hours, physical activity, and stress.
- **Social Media Insights:** Includes social media platform usage and daily phone unlocks.
- **Machine Learning Prediction:** Uses trained regression models to generate predictions.
- **Real-Time API Integration:** Connects the frontend with the ML backend using FastAPI.
- **Wellness Score:** Displays a predicted score between 0 and 10.
- **Model Evaluation:** Compares Linear Regression and Random Forest models.

---

## 📊 Input Parameters

The application collects information across three major categories.

### 1. Profile Information
- Age
- Gender
- Country

### 2. Academic & Digital Habits
- Academic Level
- Most-Used Social Media Platform
- Primary Purpose of Social Media Usage
- Average Daily Screen Time
- Daily Phone Unlocks

### 3. Lifestyle & Stress
- Daily Study Hours
- Daily Physical Activity
- Sleep Duration
- Perceived Stress Level

These parameters are processed and passed to the trained machine learning model for prediction.

---

## 🤖 Machine Learning Approach

The project follows a machine learning workflow to train, evaluate, and select an appropriate regression model.

### ML Workflow

1. **Data Collection:** Load the student social media and mental health dataset.
2. **Data Preprocessing:** Clean and prepare the dataset for model training.
3. **Exploratory Data Analysis:** Analyze patterns and relationships between different features.
4. **Feature Engineering:** Prepare relevant input features for prediction.
5. **Model Training:** Train multiple regression algorithms.
6. **Model Evaluation:** Compare models using R² Score, MAE, and RMSE.
7. **Hyperparameter Tuning:** Apply RandomizedSearchCV to optimize the Random Forest model.
8. **Model Serialization:** Save the trained model using Joblib.
9. **API Integration:** Load the saved model into the FastAPI backend.
10. **Frontend Integration:** Connect the frontend with the prediction API.

### Machine Learning Algorithms

- Linear Regression
- Random Forest Regressor
- Tuned Random Forest Regressor

---

## 📈 Model Evaluation & Performance

Three regression models were evaluated to identify the most suitable model for the prediction task.

### Evaluation Metrics

1. Linear Regression
-R² Score: 0.739794
-Training R²: 0.723677
-Mean Absolute Error (MAE): 0.536178
-Root Mean Squared Error (RMSE): 0.676032

2. Random Forest Regressor (Default)
-R² Score: 0.878017
-Training R²: 0.980907
-Mean Absolute Error (MAE): 0.346502
-Root Mean Squared Error (RMSE): 0.462870

3. Random Forest Regressor (Tuned)
-R² Score: 0.865226
-Training R²: 0.954656
-Mean Absolute Error (MAE): 0.368665
-Root Mean Squared Error (RMSE): 0.486533

### Best Performing Model

**Random Forest Regressor (Default)** achieved the highest test R² score among the three evaluated models.

- R² Score: 0.878017
- MAE: 0.346502
- RMSE: 0.462870

The model explains approximately 87.8% of the variance in the target variable on the evaluation dataset.

Although hyperparameter tuning was performed, the tuned model did not outperform the default Random Forest on the test dataset.

---

## 🛠️ Technology Stack

### Programming Languages
- Python
- JavaScript
- HTML5
- CSS3

### Machine Learning & Data Science
- NumPy
- Pandas
- Scikit-learn
- Joblib
- Matplotlib
- Seaborn

### Backend Development
- FastAPI
- Pydantic
- Uvicorn

### Development Tools
- Visual Studio Code
- Jupyter Notebook
- Git
- GitHub

---

## 🏗️ Project Architecture

The project follows a simple frontend-backend-machine learning architecture.

**User → Frontend → FastAPI → ML Model → Prediction → Frontend**

### How It Works

1. The user enters personal, academic, digital, and lifestyle information.
2. JavaScript collects the form data.
3. The frontend sends the input data to the FastAPI backend.
4. FastAPI validates the incoming data using Pydantic.
5. The backend loads and uses the trained machine learning model.
6. The model generates a predicted wellness score.
7. FastAPI returns the prediction to the frontend.
8. JavaScript updates the interface with the generated result.

---

## 📁 Project Structure

```text
MentalHealth-Predictor/
│
├── main.py
├── index.html
├── style.css
├── script.js
├── ML_Project.ipynb
├── Mental_Health_Model.pkl
├── Student Social Media And Mental Health Impact.csv
├── requirements.txt
├── README.md
└── .gitignore
```

### File Description

main.py – Implements the FastAPI backend and prediction API. It handles incoming user data and generates mental health predictions using the trained machine learning model.

index.html – Contains the frontend structure and user input form.

style.css – Defines the application's visual appearance, including layout, colors, typography, and responsive styling.

script.js – Handles frontend functionality, user interactions, form submission, and communication with the FastAPI backend.

ML_Project.ipynb – Jupyter Notebook containing data preprocessing, exploratory data analysis, feature analysis, machine learning model training, hyperparameter tuning, and model evaluation.

Mental_Health_Model.pkl – Serialized machine learning model saved using Joblib for making predictions through the backend.

Dataset CSV – Contains the student social media usage and mental health dataset used for data analysis, model training, and evaluation.

requirements.txt – Contains the Python libraries and dependencies required by the project.

.gitignore – Specifies files and directories that should be excluded from Git version control.

---

## 🔮 Future Improvements

- Add more machine learning algorithms for performance comparison.
- Experiment with advanced hyperparameter optimization techniques.
- Improve prediction performance through feature selection and engineering.
- Develop interactive visualizations for lifestyle and digital habit analysis.
- Add historical prediction tracking.
- Introduce personalized lifestyle recommendations.
- Deploy the application on a cloud platform.
- Improve data privacy and secure handling of user inputs.

---

## 🎓 Learning Outcomes

Through this project, the following concepts were explored:

- End-to-end machine learning development.
- Data preprocessing and exploratory data analysis.
- Regression algorithms and model comparison.
- Hyperparameter optimization using RandomizedSearchCV.
- Model evaluation using R², MAE, and RMSE.
- Model serialization and loading using Joblib.
- REST API development using FastAPI.
- Data validation using Pydantic.
- Frontend-backend integration using JavaScript.
- Version control and project management using Git and GitHub.

---

## ⭐ Support

If you find this project interesting or useful, consider giving the repository a ⭐ on GitHub.

Your support and feedback are appreciated!
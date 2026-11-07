# 🎓 Student GPA Prediction Using Machine Learning

## 📌 Project Overview

This project focuses on predicting students' Grade Point Average (GPA) using lifestyle-related factors with the help of Machine Learning.

A student's academic performance can be influenced by several daily activities, such as study time, sleep, social activities, extracurricular participation, and physical activity.

In this project, different Machine Learning regression algorithms are implemented and compared to understand how accurately they can predict student GPA.

The main objective is to identify the model that performs best based on different evaluation metrics.

## 🎯 Project Objectives

- 📊 Analyze the relationship between students' lifestyle habits and GPA.
- 🧹 Understand and prepare the dataset for Machine Learning.
- 🤖 Implement five different regression algorithms.
- 📈 Evaluate model performance using standard regression metrics.
- 🏆 Compare the models and identify the best-performing algorithm.
- 🔍 Understand how lifestyle factors may relate to academic performance.

## 📂 Dataset Information

The project uses the dataset:

`student_lifestyle_dataset.csv`

The dataset contains information about students' daily activities and their GPA.

### 📋 Input Features

| Feature | Description |
|---|---|
| Study_Hours_Per_Day | Daily hours spent studying |
| Extracurricular_Hours_Per_Day | Daily hours spent on extracurricular activities |
| Sleep_Hours_Per_Day | Daily hours spent sleeping |
| Social_Hours_Per_Day | Daily hours spent on social activities |
| Physical_Activity_Hours_Per_Day | Daily hours spent on physical activity |

### 🎯 Target Variable

- `GPA` — The student's Grade Point Average.

The five lifestyle features are used as input variables, while GPA is the target variable.

## 🛠️ Technologies and Libraries Used

The project is developed using Python and the following libraries:

- 🐍 **Python** — Main programming language.
- 🧮 **Pandas** — Data loading and data manipulation.
- 🔢 **NumPy** — Numerical operations.
- 📊 **Matplotlib** — Data visualization.
- 🤖 **Scikit-learn** — Machine Learning algorithms and evaluation metrics.

## ⚙️ Project Workflow

The project follows these major steps:

1. 📥 Load the dataset.
2. 🔍 Explore and understand the data.
3. 🧹 Check for missing values.
4. 📊 Perform Exploratory Data Analysis (EDA).
5. 🎯 Separate input features and target variable.
6. ✂️ Split the dataset into training and testing sets.
7. 📏 Apply feature scaling where required.
8. 🤖 Train five regression models.
9. 📈 Evaluate model performance.
10. 🏆 Compare the results and identify the best-performing model.

## 📊 Exploratory Data Analysis (EDA)

Exploratory Data Analysis is performed to understand the dataset and examine relationships between lifestyle habits and student GPA.

The project includes the following visualizations:

### 1. 📚 Study Hours vs GPA

A scatter plot is created to examine the relationship between daily study hours and GPA.

It helps visualize whether students who spend more time studying tend to have higher GPA values.

### 2. 🔗 Lifestyle Factors and GPA Correlation

A correlation graph is used to examine the relationship between the lifestyle features and GPA.

It helps identify which lifestyle factors have stronger positive or negative relationships with academic performance.

## 🤖 Machine Learning Models

Five regression algorithms are implemented in this project.

### 1. 📈 Linear Regression

Linear Regression is used to model the relationship between the input features and GPA.

It predicts GPA by fitting a linear relationship between the independent variables and the target variable.

### 2. 📐 Polynomial Regression

Polynomial Regression is used to capture possible non-linear relationships between lifestyle factors and GPA.

In this project, Polynomial Features of degree 2 are generated before applying Linear Regression.

### 3. 👥 K-Nearest Neighbors (KNN) Regression

KNN Regression predicts GPA using the values of nearby data points.

The model uses `n_neighbors=5`, meaning it considers the five nearest neighbors when making a prediction.

### 4. 🎯 Support Vector Regression (SVR)

Support Vector Regression is used to predict continuous numerical values.

It attempts to find a function that predicts GPA while keeping prediction errors within a specified margin.

### 5. 🌳 Decision Tree Regression

Decision Tree Regression uses decision rules to make predictions.

In this project, the maximum tree depth is set to 4 to limit the complexity of the model.

## ✂️ Data Splitting and Feature Scaling

The dataset is divided into two parts:

- **80% Training Data** — Used to train the Machine Learning models.
- **20% Testing Data** — Used to evaluate the trained models.

The `train_test_split()` function is used with `random_state=42` to make the split reproducible.

Feature scaling is applied to the input data used by KNN, SVR, and Polynomial Regression.

The `StandardScaler` technique is used to standardize the features.

## 📏 Model Evaluation Metrics

The performance of each regression model is evaluated using four metrics.

### 1. MAE — Mean Absolute Error

MAE calculates the average absolute difference between actual and predicted values.

A lower MAE indicates better prediction accuracy.

### 2. MSE — Mean Squared Error

MSE calculates the average squared difference between actual and predicted values.

A lower MSE indicates smaller prediction errors.

### 3. RMSE — Root Mean Squared Error

RMSE is the square root of MSE.

It measures prediction error in the same unit as the target variable. A lower RMSE indicates better performance.

### 4. R² Score — Coefficient of Determination

R² measures how well the model explains variation in the target variable.

A higher R² score generally indicates better model performance.

## 📉 Model Comparison

All five regression models are evaluated using the same training and testing split.

The results are stored in a comparison table and exported to:

`model_comparison.csv`

The project also generates two comparison graphs:

- 📉 **RMSE Comparison of Regression Models** — Compares the prediction errors of all five models. Lower RMSE is better.
- 📊 **R-squared Comparison of Regression Models** — Compares how well each model explains the variation in GPA. Higher R² is generally better.

Based on the generated comparison graphs, Linear Regression appears to perform best among the tested models. The final conclusion should be confirmed using the actual values in `model_comparison.csv`.

## 📁 Project Structure

```text
Student-GPA-Prediction/
│
├── student_lifestyle_dataset.csv
├── model_comparison.csv
├── student_gpa_prediction.py
│
├── images/
│   ├── study_hours_vs_gpa.png
│   ├── lifestyle_correlation.png
│   ├── rmse_comparison.png
│   └── r2_comparison.png
│
└── README.md
```

*Note: The `images/` folder is for storing the generated graph images. Update the filenames if your actual files use different names.*

## 📸 Project Visualizations

The following graphs are generated during the project:

1. 📚 Study Hours vs GPA
2. 🔗 Lifestyle Factors and GPA Correlation
3. 📉 RMSE Comparison of Regression Models
4. 📊 R-squared Comparison of Regression Models

These visualizations help understand the dataset and compare the performance of different regression algorithms.

## 🧠 Key Learnings

Through this project, I learned:

- How to load and explore a dataset using Pandas.
- How to perform basic Exploratory Data Analysis.
- How to visualize relationships between variables.
- How to split data into training and testing sets.
- How to apply feature scaling using StandardScaler.
- How different regression algorithms work.
- How to evaluate Machine Learning models using MAE, MSE, RMSE, and R².
- How to compare multiple models and interpret their results.

## ⚠️ Limitations

- The model uses only five lifestyle-related input features.
- GPA may also depend on other factors that are not included in the dataset.
- The model's predictions depend on the quality and size of the dataset.
- Correlation does not necessarily mean causation.
- The results should not be treated as a guaranteed prediction of a student's actual academic performance.

## 🚀 Future Improvements

The project can be improved in several ways:

- Include additional academic and personal study-related features.
- Test more Machine Learning algorithms.
- Perform hyperparameter tuning to improve model performance.
- Use cross-validation for more reliable evaluation.
- Develop a simple web application for GPA prediction.
- Allow users to enter lifestyle details and receive a predicted GPA.

## 🏁 Conclusion

This project demonstrates how Machine Learning regression algorithms can be used to predict student GPA using lifestyle-related factors.

Five different regression models were implemented and evaluated using MAE, MSE, RMSE, and R².

The comparison graphs and evaluation results help identify which model performs better on the available dataset.

Overall, the project provides practical experience in data preprocessing, Exploratory Data Analysis, Machine Learning model development, evaluation, and visualization.

## 👨‍💻 Author

Name: Sudhanshu Singh  
Course: B.Tech CSE  
College: Lovely Professional University

## 🙏 Acknowledgement

I would like to acknowledge the guidance and support of my faculty members and everyone who contributed to my learning during this project.

---

⭐ If you find this project useful, consider giving the repository a star!# Model-Evaluation-Metrics

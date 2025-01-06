# Early Stage Diabetes Predictor: Leveraging Machine Learning for Accurate Symptom-Based Diagnosis

## Introduction
Diabetes is a widespread chronic disease affecting millions of lives each year. If not detected early, it can impose a substantial financial burden on individuals. Diabetes occurs when the body either fails to produce sufficient insulin or cannot use the insulin produced effectively. Insulin is crucial for enabling cells to utilize sugars from the bloodstream for energy.

The model addresses the critical issue of early diabetes detection by analyzing symptoms and demographic factors to predict the likelihood of diabetes onset. Early identification can enable timely medical intervention, reducing the risk of severe complications and improving patient outcomes.

## Data Used
The dataset used for this project was sourced from [Kaggle](https://www.kaggle.com/datasets/ishandutta/early-stage-diabetes-risk-prediction-dataset) and includes responses from 520 individuals across 16 features:

1. Age: The participant's age in years.
2. Gender: The participant's biological gender (Male or Female).
3. Polyuria: Frequent urination, a common symptom of diabetes.
4. Polydipsia: Excessive thirst, often associated with high blood sugar levels.
5. Sudden weight loss: Unexplained and rapid loss of weight.
6. Weakness: General fatigue or lack of strength.
7. Polyphagia: Excessive hunger, despite eating sufficient food.
8. Genital thrush: A yeast infection in the genital area.
9. Visual blurring: Reduced or unclear vision.
10. Itching: Persistent irritation or discomfort of the skin.
11. Irritability: Increased sensitivity or quickness to anger.
12. Delayed healing: Prolonged wound recovery times.
13. Partial paresis: Weakness or impaired movement in parts of the body.
14. Muscle stiffness: Difficulty in muscle movement or tightness.
15. Alopecia: Sudden hair loss or baldness.
16. Obesity: Excessive body fat, often measured by BMI.
17. Class (Target Variable): Binary outcome indicating diabetes presence (1) or absence (0).

## Methodology
### 1. Data Preprocessing
- The dataset was loaded into a pandas DataFrame, and necessary columns were extracted.
- Categorical features were encoded using the LabelEncoder library.
### 2. Exploratory Data Analysis (EDA)
- A correlation heatmap visualized feature relationships with the target variable, Class.
- Polyuria had the highest correlation (0.67), followed by Polydipsia (0.65) and Sudden weight loss (0.44).

![download](https://github.com/user-attachments/assets/7c849fe0-8292-4e0f-9c15-c15742236bd6)

### 3. Model Training
- The dataset was split into training (80%) and testing (20%) sets.
- A baseline model was created using the normalized value count of the target variable, achieving a 59.86% accuracy benchmark.
### 4. Model Selection and Evaluation
Several machine learning models were evaluated:
- Random Forest Classifier (chosen for its robustness and accuracy)
- Logistic Regression
- Decision Tree Classifier
- XGB Classifier
Hyperparameter tuning enhanced model performance, with the Random Forest Classifier achieving 100.0% accuracy.

### 5. Results
- Baseline Model: Accuracy = 59.86%
- Random Forest Classifier: Accuracy = 100.0%
Other Models:
- Logistic Regression: 92.31%
- Decision Tree Classifier: 96.15%
- XGB Classifier: 98.08%

![Early Stage Diabetes Prediction Model Comparison](https://github.com/user-attachments/assets/e9ea52e1-d9fc-4c4f-8919-0f92e7aa4e83)

### 6. Classification Report and Confusion Matrix

![download](https://github.com/user-attachments/assets/34eef373-0932-413c-b22e-04690b2e02de)

The Random Forest Classifier achieved:
- Precision = 1.0
- Recall = 1.0
- F1-Score = 1.0
- True Negatives = 33, True Positives = 71, False Negatives = 0, False Positives = 0.

### 7. Feature Importance
The top 5 most critical predictors were visualized, with Polyuria emerging as the strongest feature.

## Interactive Dash Application
An interactive web application was developed using Dash:

![Early Stage Diabetes Prediction Dashboard](https://github.com/user-attachments/assets/45d8ad89-6b65-4f0e-a4a8-58c371f872e5)

- Inputs: User-friendly input fields for all 16 features.
- Outputs: Real-time prediction of diabetes class upon clicking "Predict."

![Early Stage Diabetes Prediction Dashboard 1](https://github.com/user-attachments/assets/92c6af30-2905-4100-a6ef-448b764320d4)

## How the Model Helps
The model empowers individuals by assessing their diabetes risk based on symptoms, prompting timely medical intervention. For healthcare practitioners, it acts as a diagnostic aid, improving efficiency and prioritizing high-risk patients for further evaluation.

## Disclaimer
The authenticity of the dataset used in this project cannot be guaranteed. As such, the model is not recommended for deployment in real-world clinical applications. For a tailored, robust solution, please contact me for personalized services.

Abdullahi Olalekan Abdulmumeen </br>
Applied Data Scientist </br>
Email: Olalekanabdulmumeen3@gmail.com

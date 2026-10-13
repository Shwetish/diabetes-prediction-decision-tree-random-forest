# Diabetes Outcome Prediction using Decision Trees & Random Forests
Medical diagnostic prediction of diabetes outcomes using robust Decision Tree and Random Forest classifiers


## 1. Business Problem
### 1.1. What is the business objective?
The objective is to accurately predict whether a patient has diabetes (`Outcome`) based on diagnostic measurement parameters. Early and accurate detection enables healthcare providers to intervene proactively and offer personalized treatment plans.
### 1.2. Are there any constraints?
* High emphasis on **Recall** (minimizing false negatives), as failing to diagnose a diabetic patient poses severe health risks.
* Data privacy and medical compliance standards.

---

## 2. Data Dictionary
| Feature Name | Data Type | Relevance to Model Building | Description & Reason for Inclusion/Exclusion |
| :--- | :--- | :--- | :--- |
| `Pregnancies` | Numerical (Int) | Relevant | Number of times pregnant; indicates physiological history. |
| `Glucose` | Numerical (Int) | Highly Relevant | Plasma glucose concentration; primary diagnostic indicator for diabetes. |
| `BloodPressure` | Numerical (Int) | Relevant | Diastolic blood pressure (mm Hg). |
| `SkinThickness` | Numerical (Int) | Relevant | Triceps skin fold thickness (mm), proxy for body fat. |
| `Insulin` | Numerical (Int) | Relevant | 2-Hour serum insulin (mu U/ml). |
| `BMI` | Numerical (Float) | Highly Relevant | Body mass index (weight in kg/(height in m)^2), key metabolic risk factor. |
| `DiabetesPedigreeFunction` | Numerical (Float) | Relevant | Score providing diabetes lineage/genetic risk pedigree. |
| `Age` | Numerical (Int) | Relevant | Age in years; diabetes risk often correlates with age. |
| `Outcome` | Categorical (Binary) | **Target Variable** | Class label (0 = Non-Diabetic, 1 = Diabetic). |

---

## 3. Exploratory Data Analysis (EDA)
* **3.1 Summary:** Statistical analysis of diagnostic metrics, checking for zero-value anomalies in clinical variables (like glucose or blood pressure).
* **3.2 Univariate Analysis:** Visualizing distributions of glucose levels, BMI, and age across the patient population.
* **3.3 Bivariate Analysis:** Pairplots and correlation matrices highlighting how elevated glucose and BMI correlate with positive diabetes outcomes.

---

## 4. Data Pre-processing
* **4.1 Data Cleaning & Feature Engineering:** Replaced biologically impossible zero values with median/mean imputations where applicable. Standardized feature ranges and split features from the target label.

---

## 5. Model Building
* **5.1 Model Scaling:** Prepared feature matrices using scaling techniques for distance-sensitive algorithms.
* **5.2 Model Execution:** Implemented **Decision Tree** and **Random Forest** classification pipelines.
* **5.3 Training, Testing & Validation:** Applied train-test splits and 5-fold cross-validation. Evaluated models using Accuracy, Precision, Recall, and ROC-AUC curves.
* **5.4 Model Output Explanation:** Analyzed feature importance scores to confirm that Glucose and BMI dominate predictive decisions.

---

## 6. Business Benefits & Impact
* Assists medical practitioners in rapid, automated preliminary screenings.
* Reduces diagnostic oversight and improves patient outcome tracking through data-driven insights.

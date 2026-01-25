\# 🎓 Student Programming Success: Data Insights \& Ensemble Modeling



This project explores the factors that influence success in a programming course and utilizes advanced Machine Learning ensemble techniques to predict whether a student will pass their final exam.



\## 📌 Project Overview

By analyzing student habits, demographics, and engagement levels, this project aims to answer a critical question: \*\*What behavioral patterns lead to academic success in technical fields?\*\* I performed extensive Exploratory Data Analysis (EDA) and built two ensemble models—\*\*Voting\*\* and \*\*Stacking\*\*—to reach a peak predictive accuracy of \*\*83%\*\*.



---



\## 🔍 Data Insights \& Analysis



\### 1. Univariate Analysis (The General Landscape)

\* \*\*Experience Level:\*\* The majority of students are \*\*beginners\*\*, followed by intermediate and advanced learners.

\* \*\*Engagement Gaps:\*\* A majority of students do \*\*not\*\* use Kaggle and complete fewer than \*\*4 projects\*\*.

\* \*\*Performance:\*\* The data showed a high failure rate, with most scores clustering between \*\*40–60%\*\*.

\* \*\*Habits:\*\* Typical students spend \*\*5–8 hours weekly\*\* learning and conduct \*\*5 debugging sessions\*\*.



\### 2. Bivariate Analysis (The "Success Profile")

I segmented the data to find the most significant separators between students who passed and those who failed:



| Feature | The Success Profile (Pass) ✅ | The Failure Profile (Fail) ❌ |

| :--- | :--- | :--- |

| \*\*Experience\*\* | Intermediate Python knowledge | Absolute Beginners |

| \*\*Geography\*\* | High concentration in \*\*Brazil\*\* | High concentration in \*\*Indonesia\*\* |

| \*\*Self-Confidence\*\* | High confidence (> 7) | Low confidence (< 4) |

| \*\*Projects\*\* | Higher project completion | Less than 3 projects |



\### 3. Key Correlations

\* \*\*Positive Correlation:\*\* A direct relationship exists between \*\*hours spent learning\*\* and \*\*practice problems solved\*\* with higher exam scores.

\* \*\*Negative Correlation:\*\* Interestingly, exam scores tended to \*\*decrease\*\* as student \*\*age\*\* increased within this dataset.



---



\## 🤖 Machine Learning Implementation



The modeling phase focused on handling imbalanced data and leveraging the power of multiple algorithms to improve predictive stability.



\### Preprocessing Workflow

\* \*\*Scaling:\*\* Applied `StandardScaler` to numerical features to ensure uniform distribution.

\* \*\*Encoding:\*\* Used `OneHotEncoder` and `LabelEncoder` for categorical variables.

\* \*\*Handling Imbalance:\*\* Applied \*\*SMOTE\*\* (Synthetic Minority Over-sampling Technique) to address the minority class (passing students) and prevent model bias.

\* \*\*Validation:\*\* Used \*\*Stratified K-Fold\*\* cross-validation and `GridSearchCV` for exhaustive hyperparameter tuning.



\### Model Comparison



\#### \*\*Model A: Voting Classifier\*\*

\* \*\*Base Models:\*\* `RandomForestClassifier`, `XGBClassifier`.

\* \*\*Performance:\*\* Achieved an accuracy of \*\*80%\*\*.



\#### \*\*Model B: Stacking Classifier (Best Performer)\*\*

\* \*\*Base Models:\*\* `RandomForest`, `XGBoost`, `Logistic Regression`.

\* \*\*Meta-Model:\*\* `Logistic Regression`.

\* \*\*Performance:\*\* Achieved a top accuracy of \*\*83%\*\*.



\*\*Stacking Model Metrics:\*\*



| Metric | Class 0 (Fail) | Class 1 (Pass) |

| :--- | :--- | :--- |

| \*\*Precision\*\* | 0.89 | 0.64 |

| \*\*Recall\*\* | 0.88 | 0.66 |

| \*\*F1-Score\*\* | 0.89 | 0.65 |



---



\## 🛠️ Installation \& Usage



1\. \*\*Clone the repository:\*\*

&nbsp;  ```bash

&nbsp;  git clone \[https://github.com/yourusername/student-success-insights.git](https://github.com/yourusername/student-success-insights.git)


📌 Overview

This project focuses on predicting customer churn using machine learning techniques. The objective is to identify customers who are likely to leave a service based on historical data and behavioral patterns. This helps businesses improve customer retention strategies and reduce revenue loss.

The project follows a complete end-to-end machine learning pipeline from data loading to model deployment-ready output.

📁 Dataset

The dataset contains customer information such as:

Demographic details (age, gender, country)
Account information (balance, credit score, tenure)
Activity indicators (active member status, number of products)
Target variable: Churn (0 = No, 1 = Yes)

Note: Dataset is preprocessed to handle missing values and categorical variables.

🛠️ Tools & Technologies
Python 🐍
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Joblib
⚙️ Project Workflow
1️⃣ Import Libraries

All required Python libraries for data analysis, visualization, and machine learning are imported.

2️⃣ Load Dataset

The dataset is loaded using Pandas and prepared for analysis.

3️⃣ Initial Inspection
Checked dataset shape
Verified data types
Handled missing values
Understood feature distribution
4️⃣ Exploratory Data Analysis (EDA)

Performed visual analysis using:

Distribution plots
Count plots
Correlation heatmap
Churn vs feature comparisons

This helped identify key patterns influencing customer churn.

5️⃣ Feature Engineering

Created new meaningful features such as:

Balance per product
Salary-to-balance ratio
Age groups
Tenure buckets
6️⃣ Data Preprocessing

Handled categorical and numerical features using:

One-Hot Encoding for categorical variables
Standard Scaling for numerical variables
Missing value imputation using median/mode

Implemented using ColumnTransformer.

7️⃣ Train-Test Split

Dataset split into:

Training set (80%)
Testing set (20%)
Stratified sampling used to maintain class balance
8️⃣ Model Training & Comparison

Multiple models were trained using pipelines and evaluated using cross-validation:

Logistic Regression
Random Forest Classifier
Gradient Boosting Classifier
AdaBoost Classifier
Support Vector Machine (SVC)

Performance was compared using ROC-AUC score.

9️⃣ Best Model Evaluation

The best-performing model was:

Trained on full training data
Evaluated on test data using:
Accuracy
Precision
Recall
F1-score
ROC-AUC
Confusion matrix visualized
🔟 Feature Importance

Important features influencing churn were extracted (tree-based models) to understand key drivers of customer attrition.

1️⃣1️⃣ Model Saving

The final trained pipeline (preprocessing + model) was saved using joblib:

joblib.dump(best_pipeline, 'best_churn_pipeline.pkl')
1️⃣2️⃣ Prediction on New Data

The saved model can be used to predict churn for new customers:

loaded_model = joblib.load('best_churn_pipeline.pkl')
prediction = loaded_model.predict(new_customer_data)
📊 Results
Built multiple ML models and compared performance
Achieved strong predictive accuracy using ensemble methods
Identified key factors influencing churn behavior
Created a reusable ML pipeline ready for deployment
🚀 How to Run This Project
1. Clone the repository
git clone https://github.com/your-username/customer-churn-prediction.git
cd customer-churn-prediction
2. Install dependencies
pip install -r requirements.txt
3. Run the notebook
jupyter notebook

or open in VS Code / Jupyter Lab

📌 Future Improvements
Hyperparameter tuning using GridSearchCV
Deployment using Streamlit or Flask
Real-time churn prediction API
Model explainability using SHAP

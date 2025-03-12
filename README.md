# Bank Marketing Dataset: Customer Purchase Prediction

## Introduction
This project focuses on predicting whether a customer will purchase a product or service based on behavioral and demographic data from a bank marketing campaign. The dataset originates from a Portuguese bank's direct marketing campaigns, where customers were contacted via phone calls to subscribe to a term deposit. The goal is to leverage Exploratory Data Analysis (EDA) and a Decision Tree model to understand key factors influencing customer decisions.

## Objective
The primary objective of this project is to:
- Analyze the dataset to uncover patterns and insights.
- Perform data preprocessing and handle categorical variables.
- Build a Decision Tree model to predict customer purchases.
- Evaluate model performance and identify improvement opportunities.

## Steps Conducted
1. **Data Loading and Exploration:**
   - Loaded the dataset containing 45,211 records and 17 features.
   - Checked for missing values and confirmed no null entries.
   - Examined data types and generated summary statistics.

2. **Exploratory Data Analysis (EDA):**
   - Visualized the distribution of the target variable to check for class imbalance.
   - Created a correlation heatmap to understand relationships between features.

3. **Data Preprocessing:**
   - Applied Label Encoding to categorical variables like job, marital status, and education.
   - Split the dataset into training and test sets (70%-30%).

4. **Model Building:**
   - Built a Decision Tree Classifier with a max depth of 5 to prevent overfitting.
   - Trained the model on the training set.

5. **Model Evaluation:**
   - Made predictions on the test set.
   - Evaluated performance using accuracy, confusion matrix, and classification report.
   - Achieved an accuracy of 89.5%.

6. **Decision Tree Visualization:**
   - Visualized the trained Decision Tree to interpret feature importance and decision rules.

7. **Key Insights:**
   - The target variable exhibited a class imbalance, with "No" being more prevalent.
   - "Duration" and "pdays" emerged as strong predictors.
   - Model precision for "Yes" predictions was lower, indicating room for improvement.

## Results
- The Decision Tree model achieved an accuracy of 89.5%.
- Imbalanced classes led to better performance in predicting the "No" class compared to the "Yes" class.
- Future improvements could involve handling class imbalance or using ensemble methods.

## Conclusion
This project demonstrated the use of EDA and Decision Tree modeling to predict customer purchases. The model achieved promising accuracy, with insights into feature importance. Further optimization could enhance the model's performance.

**Tools Used:** Python, Pandas, Seaborn, Matplotlib, Scikit-Learn.

**Author:** [Jay Thakur]

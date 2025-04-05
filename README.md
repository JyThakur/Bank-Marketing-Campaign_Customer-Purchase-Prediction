# **Bank Marketing Campaign: Customer Purchase Prediction**

## **Introduction**  
This project analyzes a **Portuguese bank's marketing campaign dataset** containing **45,211 customer records**. The data includes demographic (`age`, `job`, `marital`), financial (`balance`, `loan`), and campaign-related (`duration`, `poutcome`) features. The goal is to predict whether a customer will subscribe to a **term deposit (target: `y`)** using a Decision Tree classifier, helping the bank optimize future campaigns.

---

## **Objective**  
1. **Predict customer purchases** (term deposit subscriptions) using historical campaign data.  
2. **Identify key factors** influencing customer decisions (e.g., demographics, contact duration).  
3. **Optimize marketing strategies** by targeting high-potential customers.  

---

## **Steps Conducted**  

### **1. Data Preprocessing**  
- **Handled Categorical Variables**: Encoded `job`, `marital`, `education`, etc., using `LabelEncoder`.  
- **Checked for Missing Values**: No null values detected.  
- **Exploratory Data Analysis (EDA)**:  
  - **Class Imbalance**: Majority class (`no`: 39,922) vs. minority (`yes`: 5,289).  
  - **Correlation Heatmap**: `duration` (0.39) and `poutcome` (0.078) showed the strongest correlations with `y`.  

### **2. Feature Engineering & Model Building**  
- **Train-Test Split**: 70% training, 30% testing.  
- **Decision Tree Classifier**:  
  - **Max Depth**: Limited to 5 to avoid overfitting.  
  - **Key Features**: `duration`, `housing`, `contact`, `poutcome`.  

### **3. Model Evaluation**  
- **Accuracy**: 89.5% (high due to class imbalance).  
- **Confusion Matrix**:  
  - **True Negatives**: 11,505  
  - **False Positives**: 461  
  - **False Negatives**: 962  
  - **True Positives**: 636  
- **Classification Report**:  
  - **Precision (Yes)**: 58%  
  - **Recall (Yes)**: 40%  
  - **F1-Score (Yes)**: 47%  

---

## **Key Insights**  
1. **Top Predictors of Subscription**:  
   - **Call Duration**: Longer calls correlated with higher conversions.  
   - **Previous Campaign Success (`poutcome`)**: Customers with prior positive outcomes were more likely to subscribe.  
   - **Housing Loan Status**: Customers without housing loans showed higher interest.  

2. **Class Imbalance Challenge**:  
   - Model biased toward predicting "no" due to imbalanced data (88%:12%).  
   - **Recommendation**: Use resampling (SMOTE) or class weights in future iterations.  

3. **Business Recommendations**:  
   - **Focus on High-Duration Calls**: Prioritize customers willing to engage longer.  
   - **Leverage Past Successes**: Target customers with positive `poutcome` histories.  
   - **Adjust Campaign Timing**: Avoid months with low response rates (e.g., winter).  

---

## **Conclusion**  
The Decision Tree model achieved **89.5% accuracy** but highlighted challenges with class imbalance. Key factors like **call duration** and **past campaign outcomes** significantly influenced subscriptions. Future improvements could include **ensemble methods (Random Forest)** and **handling class imbalance** to enhance recall for the minority class.  

**Tools Used**: Python, Pandas, Scikit-learn, Matplotlib, Seaborn  
**Author**: Jay Thakur

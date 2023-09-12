## Customer Retention Analysis

**DATA :**  
- Supermarket Sales Data

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/f41569b6-aaea-43be-bda5-5b33046f09e9)


In cohort analysis, we found that customers who joined in April 2006 exhibited a notably higher retention rate compared to those who joined in other months.This intriguing observation prompts us to delve deeper into the study of customer behavior among those who joined in April 2006 to understand the factors contributing to their exceptional retention rates.

## Customer Movement Analysis

**DATA :**  
- Supermarket Sales Data

For each reporting month, customers are grouped into 4 categories defined by the defition below  

| Status | Current | Previous | Before |
| --- | --- | --- | --- |
| Repeat | ✅ | ✅ | |
| Reactivated | ✅ | ❌ | ✅ |
| New | ✅ | ❌ | ❌ |
| Churn | ❌ | ✅ |

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/4166033f-6a92-4d46-b3de-5b4f1119672a)

## Churn Prediction

**DATA :**  
- E-commerce Data

**Vairable and Discerption :**

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/e52c5145-6f83-431e-be75-6c0fe64e9bdb)

**1.Import Libraries**

**2.Import Data**

**3.Handle with Missing Value**
- Remove rows with missing values.
- The dataset was reduced from 5630 rows to 3774 rows after removing rows with missing values.

**4.Exploring Data**
- Performing a boxplot comparison of numerical variables with the target variable(Churn).
  
  ![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/8f036164-9c39-41fe-948d-bf3042e5f924)

  
- Performing a heatmap comparison of categorical variables with the target variable(Churn) in terms of ratio values.
  
  ![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/c886123b-6e51-4062-8c5d-f38451871d55)

**5.Data Preprocessing**
- Applied one-hot encoding to categorical variables in the following list:
  
  - PreferredLoginDevice
  - CityTier
  - PreferredPaymentMode
  - Gender
  - PreferedOrderCat
  - MaritalStatus

**6.Handling Imbalance Data with SMOTE**

The SMOTE algorithm is one of the first and still the most popular algorithmic approach to generating new dataset samples. The algorithm works by oversampling the underlying dataset with new synthetic points.
- before
  
  <img src="https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/a0ea5334-89de-45bf-a34f-18e42bd37d3f" height="400" width="600" >

- After

  <img src="https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/c8e8d236-ab14-443c-97e7-d5427d634bc4" height="400" width="600" >

**7.Train Model and Evaluate**

Training four models: 
- Logistic Regression
  - Before SMOTE : F1 score is 0.89
  - After SMOTE : F1 score is 0.86
- Random Forest Classifier
  - Before SMOTE : F1 score is 0.96
  - After SMOTE : F1 score is 0.95
- K-Neighbors Classifier
  - Before SMOTE : F1 score is 0.86
  - After SMOTE : F1 score is 0.82
- XGBoost Classifier
  - Before SMOTE : F1 score is 0.97
  - After SMOTE : F1 score is 0.95
 
**8.Model Selection**
- Selected the XGBoost Classifier with SMOTE due to its highest F1 score compared to other models.


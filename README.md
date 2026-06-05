# Online-Shoppers-Purchasing-Intention-Prediction

## Project Overview

This project uses different machine learning techniques to predict whether an online shopper will complete a purchase based on browsing behavior, session characteristics, and website interaction metrics.

The goal is to help businesses better understand customer behavior and identify factors that influence purchasing decisions.

---

## The Dataset

The dataset contains information about online shopping sessions, including administrative activities, product-related interactions, bounce rates, exit rates, page values, visitor type, and other session attributes.

### Target Variable

* **Revenue**

  * TRUE = Purchase completed
  * FALSE = No purchase

---

## Objectives

* Analyse customer browsing behavior.
* Identify the most important factors influencing purchase decisions.
* Build a predictive machine learning model.
* Evaluate model performance using classification metrics e.g Recall.

---

## Data Preprocessing

The following preprocessing steps were performed:

* Checked for missing values.
* Converted char variables into factors
* Explored the relationships between variables and target variable(Revenue)
* Split data into training and testing datasets(70:30).
* Feature Engineering on Training Set and applied transformation to test set


---

## Machine Learning Models

The following models were evaluated:

* Decision Tree using H2o
* Logistic Regression(Raw data & balanced Data) plus adjusted threshold from 0.5 to  0.3
* Naive Bayes Classifier 

### Evaluation Metrics

* Other metrics were observed but Recall is the primary evaluation metric because the 
objective is to correctly identify as many actual purchasers as possible. In this context 
missing a potential purchaser (false negative) is more costly than incorrectly 
predicting a purchase.

* Out of all the actual purchasers, how many did we correctly identify?
---

## Results

Logistic Regression with balanced data out performed the other models with Recall 0.934 on training set and 0.9178 on test set showing it generalises very on new new unseen data.

Key findings:

* PageValues was one of the strongest predictors of purchasing intention.
* Exit rates and bounce rates showed strong relationships with purchasing outcomes.
* New visitors have a higher purchase rate than returning visitors
* Users with low bounce rates are more likely to purchase
* Users with higher PageValues are much more likely to purchase


---

## Visualizations

### Logistic Regression Feature Importance

![Variable Importance](https://github.com/qinisela-ndlovu/Online-Shoppers-Purchasing-Intention-Prediction/blob/main/Variable%20importance.png)

### Logistic Regression Confusion Matrix

![Confusion Matrix](https://github.com/qinisela-ndlovu/Online-Shoppers-Purchasing-Intention-Prediction/blob/main/LR%20Confusion%20matrix.png)

### ROC Curve on Test set(See generalisation)

![ROC Curve](https://github.com/qinisela-ndlovu/Online-Shoppers-Purchasing-Intention-Prediction/blob/main/Roc%20LR%20Test.png)

---

## Technologies Used

* The project is done using R language
* R Studio

---

## Future Improvements

* Hyperparameter tuning WITH different values
* XGBoost implementation
* Deployment as a web application
* Real-time prediction dashboard




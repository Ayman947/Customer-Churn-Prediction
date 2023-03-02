# 📱👪📉 Telecom Customer Churn Prediction

**Business Background:** 
- Customer churn is the tendency of customers to cancel their subscriptions to a service they have been using.
- Customer churn rate is the percentage of churned customers within a predefined time interval.
- The Churn rate is an important indicator of customer satisfaction and the overall business wellness of the company.



**Business Problem:** 
- At the telecom company, the marketing department detected that they are losing many of their customers (i.e. high churn rate).
- So, they decided to launch retention campaigns, and to be efficient they need to target just the customers who are about to churn.
 
  ![ ](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/Churn.png)

> **Objective:** To determine the customers' tendency to churn.

> **Question:** Who will churn and who will not?

> **Analytics Solution / Methodology:** A supervised ML classification models will be built to predict the churn status of every customer.



  # **Data Sources**

  - [Data source: Telecom Customer Churn Raw Data ](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/01%20data-raw.csv)
  
| Column Name | Description | Sample Values |
|-------------|-------------|---------------|
| customerID       | The customer's unique identifier  | 7590-VHVEG |
| gender      | The customer's gender  | Male, Female |
| SeniorCitizen          | Indicates if the customer is 65 or older  | 0, 1 |
| Dependents | Indicates if the customer lives with any dependents  | Yes, No |
| tenure | The total amount of months the customer has been with the company | 1, 5 or 10 or ... etc. |
| PhoneService | Indicates if the customer subscribes to home phone service   | Yes, No |
| MultipleLines | Indicates if the customer subscribes to multiple lines  service | Yes, No, No phone service |
| InternetService          | Indicates if the customer subscribes to Internet service  | No, DSL, Fiber Optic |
| OnlineSecurity          | Indicates if the customer subscribes to an additional online security service  | Yes, No, No internet service |
| OnlineBackup          | Indicates if the customer subscribes to an additional online backup  | Yes, No, No internet service |
| DeviceProtection          | Indicates if the customer subscribes to an additional device protection  | Yes, No, No internet service |
| TechSupport          | Indicates if the customer subscribes to an additional technical support  | Yes, No, No internet service |
| StreamingTV          | Indicates if the customer uses their Internet service to stream television  | Yes, No, No internet service |
| StreamingMovies          | Indicates if the customer uses their Internet service to stream movies  | Yes, No, No internet service |
| Contract          | Indicates the customer’s current contract type  | Month-to-Month, One Year, Two Year |
| PaperlessBilling          | Indicates if the customer has chosen paperless billing  | Yes, No |
| PaymentMethod | Indicates how the customer pays their bill  | Bank Withdrawal, Credit Card, Mailed Check |
| MonthlyCharges | Indicates the customer’s current total monthly charge  | 29.85 |
| TotalCharges | Indicates the customer’s total charges  | 1889.5 |
| Churn          | Indicates if the customer churned within the last month or not   | Yes, No |




  # **Environment** & **Packages**

|Package|Functionality|
|-------------|-------------|
|numpy|Numerical calculations & array manipulations|
|pandas|Tabular data manipulation|
|seaborn|Data visualizatiom|
|matplotlib|Data visualizatiom|
|sklearn.svm|Importing the Support Vector Machine ML model|
|sklearn.neighbors|Importing the K Nearest Neighbour ML model|
|sklearn.linear_model|Importing the Logistic Regression ML model|
|sklearn.ensemble|Importing the Random Forest ML model|
|xgboost|Importing the XGBoost ML model|
|sklearn.model_selection|Importing GridSearchCV for model optimization - Importing train-test-split for splitting the data|
|sklearn.preprocessing|Importing the StandardScaler for normalizing the data|
|sklearn.metrics|Calculating model performance (i.e accuracy & F1-score & AUC)|
|eli5|Importing PermutationImportance to calculate features importance|
|imblearn|Importing the RandomOverSampler to balance the data|

  # **Data Cleansning & Preprocessing**

  - Dropping the customer ids column.
  - Adjusting the total charges column data type to be numeric. 
  - Checking categorical classes for validity and consistency.
  - Dropping duplicated customers.
  - Checking and dealing with nulls.
  - Shuffling data to avoid any unintended order.
  - One-hot-encoding categorical features.
  - Splitting the data for training and testing.
  - Balancing the target variable classes.
  - Normalizing/Standardizing the data. 



  # **EDA Insights**

![Customer Churn Status Breakdown](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/EDA-churn-breakdown.png)
![Customer Churn Per Contract Type](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/EDA-churn-vs-contract.png)
![Customer Churn Per Internet Service](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/EDA-churn-vs-internetService.png)
![Customer Churn Per Payment Method](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/EDA-churn-vs-paymentMethod.png)
![Customer Churn Per Customer Tenure](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/EDA-churn-vs-tenure.png)
![Customer Churn Per Total charges](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/EDA-churn-vs-totalCharges.png)






  # **Modeling** & **Final Results**

We've built **4 ML classification** models to predict **customers churn**:
1. Logistic Regression (LR)
2. K Nearest Neighbor (KNN)
3. XGBoost (XGB)
4. Support Vector Machine (SVM)

![](https://github.com/Ayman947/Customer-Churn-Prediction/blob/main/Data/Results.PNG)


  # **Conclusion**

- By applying the **Logistic Regression** model, we will approximately tell **who may churn** with **F-score = 0.631** and **AUC = 0.767**.

- Thus, the marketing professionals can determine the **customers to target** through the retention campaign.

- **(i.e. reduced costs & efficient business decisions)**

# Predicting Customer Churn

## Problem Statement
##### Customer churn is a huge problem of concern for large companies nowadays. It directly impacts the company revenues. It is always more difficult and expensive to acquire a new customer than it is to retain a current paying customer. Hence, finding the factors that leads to churn could help in developing business strategies to retain the customers. A robust and accurate predictive model could be built to predict the customers who are about to churn, and the company could offer them with benefits to retain them.

## Data Source
##### This data set is taken from Kaggle under the topic Telco Customer Churn. The dataset can be accessed using the following link - https://www.kaggle.com/blastchar/telco-customer-churn

## Data Description
##### This dataset has records of 7043 customers with 20 features (Independent variables) and 1 target (Dependent Variable). The target variable (Churn) represents whether a customer has left a company or not. So, the target variable has two states (Yes/No). Hence this can be treated as a Binary Classification Problem. The predictor variables present in the data set are customerID, gender, SeniorCitizen, Partner, Dependents, tenure, PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges.

## Data Mining Tasks
##### Dropping Unwanted Variables, One Hot Encoding, Label Encoding, Scaling, Train Test Split, Over Sampling

## Data Mining Models
##### Rnadom Forest, KNN, Logistic Regression, SVM

## Performance Evaluation
##### The models were evaluated using three key metrics namely,
##### 1. Sensitivity – Our target is to determine the customers who are about to churn and come upwith preventive measures to retain them. Therefore, the overall accuracy doesn’t matter for us. We need to identify the maximum number of churning customers which makes Sensitivity as the key metric to focus upon.
##### 2. ROC Curve – ROC Curve with maximum area under the curve indicates better separation between two classes in terms if probability distribution obtained from the model. Therefore, this metric can be used to compare the performance of different models.
##### 3. Net gain – This is a derived metric which takes into account the cost incurred in retaining an old customer and the cost of finding a new customer. Few assumptions were made in order to use this metric such as, 
#####  It costs the company $500 to find a new customer 
#####  It costs the company $100 to retain an existing customer

## Conclusion
#####  We couldn’t differentiate the performance of the models much using the ROC.
#####  There was not much of difference observed in terms of sensitivity between the models. Though Logistic Regression has done a good job, it is not much better than SVM, Random Forest AND Knn. We decided to hyper tune the parameters of the 4 models before evaluating them in terms of sensitivity. This could change the performance ranking shown in the above table.
#####  Hyperparameter tuning has increased the performance of few models and didn’t help much with few models. The performance ranking has also changed. By the obtained results, we could see that SVM has given the best result with a sensitivity of 0.85.
#####  With NET Gain as an evaluation metric, we have obtained the best result from SVM. We could save $288100 by choosing the cut off as 0.12.

## Insights for decision making
##### SVM Model can be used to identify the Churning Customers with
• Maximum Net Gain
• High Sensitivity

## Impact of project
##### By implementing this model, we can generate a report of future churning customers and this report can be sent directly to the customer service team who can then contact customers on the list to better understand their needs or propose new offers, different products or strategy. This would greatly benefit the company in terms of profit and economic development.

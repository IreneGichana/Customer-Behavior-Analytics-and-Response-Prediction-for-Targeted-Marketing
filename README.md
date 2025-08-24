# Response-Prediction-for-Targeted-Marketing
This project analyzes customer demographics, lifestyle, and purchase behavior to predict responses to marketing campaigns. Using a dataset containing over 2,000 customer records with features such as income, education, marital status, web visits, and past campaign interactions, I performed data cleaning, exploratory data analysis (EDA), feature engineering, and model building. Used two models(Linear Regression and Random Forest Classifier) to perform the prediction. The trained model was packaged using pickle for deployment and tested on new sample data.

The goal of this project is to demonstrate how data-driven insights can improve targeted marketing strategies, increase campaign effectiveness, and support customer segmentation for business growth.

## Data Description

The dataset contains 2,240 customer records with the following key features:

Customer Profile: CustomerID, CustomerAge, Education, Marital_Status, Income

Family & Household: Kidhome, Teenhome, Recency (days since last purchase)

Purchases: Amounts spent on different product categories (Wines, Fruits, Meat, Fish, Sweet, Gold)

Engagement Metrics: NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumWebVisitsMonth

Campaign History: Responses to previous campaigns (AcceptedCmp1 … AcceptedCmp5)

Target Variable: Response (1 = Accepted, 0 = Not Accepted)

Date Information: Dt_Customer (date customer joined)

## Data Cleaning & Preprocessing

Converted Dt_Customer to datetime format.

Created derived features:

CustomerAge from Year_Birth

CustomerValueTier from Total Spending in different products

Encoded categorical variables (Education, Marital_Status).

Scaled numeric variables (Income, Recency, etc.).

Handled missing values in Income using mean imputation.

## Exploratory Data Analysis (EDA)

Key insights from the analysis:

Demographics: Majority of customers are middle-aged (30–60 years).

Income: Higher-income customers tend to purchase more Wines and Gold products.

Campaign Response: Married customers and those with higher income show higher acceptance rates.

Web Engagement: Customers with frequent web visits but low purchase rates may need personalized offers.

Visuals included in the notebook:

Income and age distribution histograms

Heatmap of correlations between spending categories

## Model Development

Created two models:

Linear Regression

Random Forest Classifier


A Random Forest Classifier provided the best balance of accuracy and interpretability.

### Pipeline

Preprocessing: OneHotEncoder (categorical), StandardScaler (numerical)

Model Selection: Random Forest with GridSearchCV for hyperparameter tuning

## Model Evaluation

Performance of the models:

1. Linear Regression:
   
Accuracy: 68%

2. Random Forest:

Accuracy: 73%


The confusion matrix shows that the model performs well in identifying both responders and non-responders.

## Deployment Preparation
Chose Random Forest model for deployment as it performed better. It was saved using pickle for reuse.

## Insights & Recommendations

Customers with higher incomes and frequent purchases are more likely to respond.

Married customers with university education respond positively to campaigns.

Campaign strategies should focus on personalized offers for frequent web visitors who don’t convert.

Businesses can use the model for customer segmentation to maximize marketing ROI.



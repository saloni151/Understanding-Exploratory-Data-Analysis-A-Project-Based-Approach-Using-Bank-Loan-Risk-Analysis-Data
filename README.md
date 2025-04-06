# Understanding-Exploratory-Data-Analysis-A-Project-Based-Approach-Using-Bank-Loan-Risk-Analysis-Data
**Abstract**

Financial institutions find it challenging to grant loans to clients/customers due to their poor or the lack of an established credit history. Hence, some clients/customers take advantage of this and become defaulters. Exploratory Data Analysis (EDA) has been applied to analyse patterns present in the data, which will help identify applicants who are capable of repaying the loan and should not be rejected.

Whenever the financial institution gets a loan request, the decision to grant or reject the request has to be made based on the applicant’s credit profile. There are two types of risks linked to the financial institution’s decision:

1. If the applicant is likely to remit the loan amount, then not granting the loan may lead to business loss to the financial institutions.

2. If the applicant is not likely to remit the loan amount, i.e., he or she is likely to default, then granting the loan may lead to a financial loss for the financial institutions.

The data set used for this Exploratory Data Analysis includes details related to loan applications at the time they were submitted. It covers two types of scenarios:

* Clients facing payment issues: These are applicants who delayed payment by more than X days on at least one of the first Y installments of the loan in the dataset.

* Clients with timely payments: This includes all other cases where the loan payments were made on time.

When a borrower submits a loan application, four kinds of decisions are generally made by either the client or the financial institution:

* Approved: The loan application has been accepted and approved by the company.

* Cancelled: The client withdrew the application during the approval process — either due to a change of mind or, in some cases, because unfavorable loan terms were offered owing to the client’s high-risk profile.

* Refused: The financial institution rejected the loan application, typically because the applicant did not meet the eligibility criteria or other requirements.

* Unused Offer: The client chose not to proceed with the loan, canceling it at a later stage in the process.

Exploratory Data Analysis (EDA) has been conducted to examine how the attributes in the bank loan risk analysis data set affect the likelihood of loan default.

# **Problem Statement**
1.  How to identify the key features and hidden patterns among the features that lead to default.
2.  Checking the missing values.
3.  Checking the Outliers.
4.  How to deal with Imbalanced datasets.
5.  How to identify whether the client who applied for a loan belongs to a defaulter or non- non-defaulter.
6.  Choosing the right evaluation metrics for the evaluation of our proposed model was another area of concern.


# **Objective**
1.  To identify the key features and hidden patterns among the features that lead to default, univariate and bivariate analysis have been done.
2.  To overcome the problem of missing values, the  mean, median, and mode imputation techniques have been used.
3.  To deal with Outliers Boxplot and binning method have been used.
4.  To deal with Imbalanced datasets SMOTE technique has been used.
5.  To identify whether the client who applied for a loan belongs to a defaulter or non- non-defaulter, the Light Gradient Boosting Machine             
    classification (LGBM classifier) algorithm has been used.
6.  To evaluate the model F1 score has been used.

  
    **Analysis Observations**

I. **Attribute relevance analysis or feature importance analysis on the Application dataset:**

**1.NAME_CONTRACT_TYPE**
* Most of the customers have taken a cash loan.
* Customers who have taken a cash loan are less likely to be defaulters.

**2. CODE_GENDER**(Generally, we do not consider columns related to gender for data analysis because this might lead to discrimination)
* Most of the time, the loan has been taken out by female customers
* The default rate of female customers is approximately 7%, which is safer and lower than the default rate of male customers.

**3. NAME_TYPE_SUITE**
* Unaccompanied customers have taken the loan most of the time, and the default rate is approximately 8.5% or 9% which is still fine.

**4. NAME_INCOME_TYPE**
* The safest segments or groups to grant loans to are working professionals, commercial associates, and pensioners. Because most of the loans are granted to these income-type customers and their default rate is also low.

**5. NAME_EDUCATION_TYPE**
* The higher segment is the safest customers to grant the loan with the default rate less than 5%.
  
**6. NAME_FAMILY_STATUS**
* Married people are safe to grant loans where the default rate is 8%.
  
**7. NAME_HOUSING_TYPE**
* Customers who have a house or apartment are safe to grant a loan where the default rate is approximately 8%.

**8. OCCUPATION_TYPE**
* Low-skilled laborers and Drivers are the highest defaulters.
* Accountants are less likely to default.
* Core staff, Managers, and laborers are safe to grant loans where the default rate is less than or equal to 7.5 to 10%.
  
**9. ORGANIZATION_TYPE**
* Transport type 3 is are highest defaulters.
* Others, Business Entity Type 3, Self Employed, are safe to grant loans with a default rate around 10%.
  
**II. Univariate Numeric Variable Analysis**

* Most of the loans were granted for the AMT_GOODS_PRICE ranging between 0 and to 1million.
* Most of the loans were granted for the credit amount (AMT_CREDIT), ranging between 0 to 1 million.
* Most of the customers are paying an annuity of 0 to 50k.
* Most of the customers have an income between 0 to 1 million.
  
**III. Bivariate Numeric Variable Analysis**

* AMT_GOODS_PRICE and AMT_CREDIT are linearly correlated, if AMT_CREDIT increases, the defaulters decrease.
* Clients having income less than or equal to 1 million are more likely to take out loans, of whom are taking loans of less than 1.5 million could turn out to be defaulters. We can target income below 1 million and a loan amount greater than 1.5 million.
* Clients having children 1 to fewer than 5 are safer to give the loan.
* Clients who can pay the annuity of 100k are more likely to get the loan, and that’s up to less than 2 million(safer segment).
  
**IV. Analysis on the Merged Data**

* For the repairing purpose, customers had applied mostly previously and the same purpose has the most number of cancellations.
* Most of the application which were previously either canceled or refused 80%-90% of them are repair in the current data.
* The offers that were unused previously now have the maximum number of defaulters despite having high-income band customers.


# **Final Conclusion/Insights**

**Bank should target the customers**
1. Having low income, i.e., below 1 million.
2. Working in Others, Business Entity Type 3, Self-Employed  org. type.
3. Working as Accountants, Core staff, Managers, and Laborers.
4. Having a house/apartment, and are married and have children, not more than 5.
5. Highly educated.
6. Preferably female.
7. Unaccompanied people can be safer -  default rate is ~8.5%

**Amount segment recommended**

1. The credit amount should not be more than 1 million
2. The annuity can be made of 50K (depending on the eligibility)
3. The income bracket could be below 1 million
4. 80-90% of the previous customers who canceled/refused are repayers. The bank can do the analysis and can consider giving the loan to these segments.

**Precautions**

1. Org. Transport type 3 should be avoided.
2. Low-skill laborers and drivers  should be avoided.
3. Offers prev. Unused and high-income customers should be avoided.

**Result**

The prediction model has achieved a 0.96 F1 score.

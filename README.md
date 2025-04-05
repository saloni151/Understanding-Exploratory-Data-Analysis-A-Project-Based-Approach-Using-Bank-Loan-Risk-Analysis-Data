# Mastering-Exploratory-Data-Analysis-A-Project-Based-Approach-Using-Bank-Loan-Risk-Analysis-Data
# **Initially**

Loan-providing companies find it hard to give loans to people due to their insufficient or nonexistent credit history. Because of that, some consumers use it as their advantage by becoming a defaulter. EDA has been used to analyse the patterns present in the data. This will ensure that the applicants capable of repaying the loan are not rejected.

When the company receives a loan application, it has to decide on loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

  1. If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company.
  2. If the applicant is not likely to repay the loan, i.e., he/she is likely to default, then approving the loan may lead to a financial loss for the company.

The data used for this analysis contains information about the loan application at the time of applying for the loan. It contains two types of scenarios:

  1. The client with payment difficulties: he/she had late payment for more than X days on at least one of the first Y instalments of the loan in our sample,
  2. All other cases: All other cases when the payment is paid on time.
     
When a client applies for a loan, four types of decisions can be made by the client/company.:

  Approved: The Company has approved the loan Application
  
  Cancelled: The client cancelled the application sometime during approval. Either the client changed her/his mind about the loan, or in some cases, due to a high risk of the client, they received worse pricing, which they did not want.
  
  Refused: The company had rejected the loan (because the client does not meet their requirements etc.).
  
  Unused offer: The Loan has been cancelled by the client, but at different stages of the process.

In this analysis, EDA has been implemented to understand how consumer attributes and loan attributes influence the tendency of default.

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

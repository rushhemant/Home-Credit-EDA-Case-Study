# Home-Credit-EDA-Case-Study
This case study aims to identify patterns which indicate if a client has difficulty paying their installments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.


In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment.

The loan providing companies find it hard to give loans to the people due to their insufficient or non-existent credit history. Because of that, some consumers use it as their advantage by becoming a defaulter. Suppose you work for a consumer finance company which specialises in lending various types of loans to urban customers. You have to use EDA to analyse the patterns present in the data. This will ensure that the applicants are capable of repaying the loan are not rejected.

 

When the company receives a loan application, the company has to decide for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company

If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.

**Read Data**	
* Import important libraries	
* Read application data file into dataframe	
* Read previous application data file into dataframe	
* Quick review of application_data dataframe	
* Shape of application_data dataframe	
* Quick review of previous_application dataframe	
* Shape of previous_application dataframe	
	
**Data Cleaning**	
* Analyze columns for missing values in application_data	
* Create new DF by removing columns where more than 45% of null values from application_data	
* Quick review of application_clean dataframe	
* FLAG_DOCUMENT and EXT_SOURCE Do not provide any analytical value and hence we will remove it	
* Drop duplicate data from application_clean, if any	
* Check null values percentage in application_clean dataframe	
* Determine if data can be imputed for columns with missing value in application_clean	
* Impute with 0 for below columns - application_clean	
* Check null values percentage in application_clean dataframe	
* Quick review of data in application_clean	
	
* Analyze columns for missing values in previous_application	
* Create new DF by removing columns where more than 90% of null values from previous_application	
* Quick review of previous_clean dataframe	
* Drop duplicate data from previous_clean	
* Check null values percentage in previous_clean dataframe	
* Quick review of data in previous_clean	
* Determine if data can be imputed for columns with missing value in previous_clean	
	
**Univariate Analysis**	
* Derived column AGE_YEAR for Age in years for application_clean dataframe	
* Derived column EMPLOYED_YEAR for Employed in years for application_clean dataframe	
* Derived column INCOME_CREDIT_RT for INCOME to CREDIT Ratio for application_clean dataframe	
* Derived column LTV_RT (Loan-to-value) for GOODS_PRICE to CREDIT Ratio for application_clean dataframe	
* Derived column pr_LTV_RT (Loan-to-value) for GOODS_PRICE to CREDIT Ratio for previous_clean dataframe	
	
* List of numerical columns in application_clean	
* Determine outliers using boxplot for quantitative variables - application_clean dataframe.	
* Quick review of stats for outlier columns from application_clean	
* Histogram for quantitative variables - application_clean	
* Remove Outliers from application_clean	
* Quick review of application_clean dataframe after removing outliers	
* List Categorical Variables application_clean	
* Countplot for these categorical variables - application_clean	
* Imbalance Calculation - Pie for these categorical variables - application_clean	
	
* List of numerical columns in previous_clean	
* Determine outliers using boxplot for quantitative variables - previous_clean dataframe.	
* Quick review of stats for outlier columns from previous_clean	
* Histogram for quantitative variables - previous_clean	
* Remove Outliers from previous_clean	
* Quick review of previous_clean dataframe after removing outliers	
* List Categorical Variables previous_clean	
* Countplot for these non-numeric variables - previous_clean	
* Imbalance Calculation - Pie Chart for these categorical variables - previous_cleanv	
	
**Merge Dataframe**	
* Merge Dataframe application_clean and previous_clean on "SK_ID_CURR"	
* Quick review of merged dataframe	
* List of numerical columns in merged dataframe (all_app_data)	
* List Categorical Variables in merged dataframe (all_app_data)	
	
**Segmented Univariate Analysis**	
* Segmented Univariate Analysis - Application Clean - Analyze impact of target on other quantitative variables.	
* Segmented Univariate Analysis - Application Clean - Analyze impact of target on other categorical variables.	
* Segmented Univariate Analysis - Previous Application - Analyze impact of target on AMT_GOODS_PRICE on  NAME_CONTRACT_STATUS variables.	
* Segmented Univariate Analysis - Previous Application - Analyze impact of target on AMT_DOWN_PAYMENT on  NAME_CONTRACT_STATUS variables.	
* Segmented Univariate Analysis - Previous Application - Analyze impact of target on AMT_CREDIT on  NAME_CONTRACT_TYPE variables.	
* Segmented Univariate Analysis - Previous Application - Analyze impact of target on AMT_DOWN_PAYMENT on  NAME_CONTRACT_TYPE variables. 
* Segmented Univariate Analysis - Previous Application - Analyze impact of target on CNT_PAYMENT on  NAME_CONTRACT_TYPE variables.	
* Segmented Univariate Analysis - All App Data (merged dataframe) - Analyze impact of target on other quantitative variables.	
* Segmented Univariate Analysis - All App Data (merged dataframe) - Analyze impact of target on other categorical variables.	
	
**Bivariate Analysis**	
* Analyze impact of Gender and Housing Type on "Target" variable	
* Analyze impact of Gender and Income Type on "Target" variable	
* Analyze impact of Gender and Education Type on "Target" variable	
* Analyze impact of Gender and Family Status on "Target" variable	
* Analyze impact of Gender and Own Car on "Target" variable	
* Analyze impact of Gender and Own Realty on "Target" variable	
* Analyze impact of Family Status and Housing Type on "Target" variable	
* Analyze impact of Family Status and Education Type on "Target" variable	
* Analyze impact of Family Status and Contract Type on "Target" variable	
	 
* Split application dataframe into application_0 for target=0 and application_1 for target=1	
* Correlation for key quantitative variables from application_clean with TARGET=0	
* Correlation for key quantitative variables from application_clean with TARGET=1	
* Split previous_application dataframe into previous_app, previous_can, previous_ref and previous_unused	
* Correlation for key quantitative variables from previous_app i.e previous approved	
* Correlation for key quantitative variables from previous_app i.e previous Canceled	
* Correlation for key quantitative variables from previous_app i.e previous refused	
* Correlation for key quantitative variables from previous_app i.e previous unused	

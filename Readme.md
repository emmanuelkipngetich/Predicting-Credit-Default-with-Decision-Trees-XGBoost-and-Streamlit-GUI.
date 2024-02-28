# Predicting-Credit-Default-with-Decision-Trees-XGBoost-and-Streamlit-GUI.
### PREDICTING THE PROBABILITY OF DEFAULT BY A CREDIT CARD HOLDER USING DECISION TREES AND XGBOOST MODELS AND DEPLOYING ON GUI USING STREAMLIT
#### PROJECT DESCRIPTION AND BUSINESS UNDERSTANDING
The operation of credit cards involves customers purchasing goods or services, and the issuing bank compiling these transactions into a bill issued at the end of a billing cycle, expecting repayment within a specific timeframe(Rajani, 2009). Revolving credit cards allow customers to carry forward balances, subjecting unpaid amounts to interest. Late payments result in penalties, impacting the credit score if prolonged. Mechanically, merchants transmit transaction details to their acquiring banks, routed through card networks for approval by the issuing bank. Defaults from prolonged non-payment lead to write-offs, impacting credit scores and bank losses (Gurusamy, 2009). Credit card defaults result from factors like job loss excessive debt, and poor financial planning, influencing loan delinquency levels. The study emphasizes dynamic prediction models, using Decision Tree Based Models to depict probability of default and the extent of risk per billing cycle, distinguishing between defaulting and delinquency as terminal and varying severity states. The problem at hand centers on mitigating loan default risks in the financial sector, vital for institutional profitability. Past methods lacked depth, merely categorizing borrowers as ’good’ or ’bad’ without detailing extent of potential delinquency. To address this, a predictive model which foresees varying delinquency stages, offering insights into diverse repayment behaviors within billing cycles. This model transcends binary classifications, aiming for a nuanced understanding of customer performance. This model aims to enhance the precision of forecasting defaults, allowing institutions to better provision for bad debts and optimize profitability.

#### Different Data Features
There are 25 variables:
1. ID: ID of each client
2. LIMIT_BAL: Amount of given credit in NT dollars (includes individual and family/supplementary credit)
3. SEX: Gender (1=male, 2=female)
4. EDUCATION: (1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown)
5. MARRIAGE: Marital status (1=married, 2=single, 3=others)
6. AGE: Age in years
7. PAY_0: Repayment status in September, 2005 (-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above)
8. PAY_2: Repayment status in August, 2005 (scale same as above)
9. PAY_3: Repayment status in July, 2005 (scale same as above)
10. PAY_4: Repayment status in June, 2005 (scale same as above)
11. PAY_5: Repayment status in May, 2005 (scale same as above)
12. PAY_6: Repayment status in April, 2005 (scale same as above)
13. BILL_AMT1: Amount of bill statement in September, 2005 (NT dollar)
14. BILL_AMT2: Amount of bill statement in August, 2005 (NT dollar)
15. BILL_AMT3: Amount of bill statement in July, 2005 (NT dollar)
16. BILL_AMT4: Amount of bill statement in June, 2005 (NT dollar)
17. BILL_AMT5: Amount of bill statement in May, 2005 (NT dollar)
18. BILL_AMT6: Amount of bill statement in April, 2005 (NT dollar)
19. PAY_AMT1: Amount of previous payment in September, 2005 (NT dollar)
20. PAY_AMT2: Amount of previous payment in August, 2005 (NT dollar)
21. PAY_AMT3: Amount of previous payment in July, 2005 (NT dollar)
22. PAY_AMT4: Amount of previous payment in June, 2005 (NT dollar)
23. PAY_AMT5: Amount of previous payment in May, 2005 (NT dollar)
24. PAY_AMT6: Amount of previous payment in April, 2005 (NT dollar)
25. default.payment.next.month: Default payment (1=yes, 0=no)

#### HYPOTHESIS & QUESTIONS
##### Hypothesis
Individuals with lower credit limits, higher education levels, and consistent payment behavior are less likely to default on their credit card payments.

##### Exploratory Data Analysis (EDA) Questions
1. How does default status vary across different demographic groups (e.g., gender, education, marital status, age)?

2. Is there a correlation between the credit limit (LIMIT_BAL) and the probability of default?

3. What is the distribution of default status based on repayment status in the previous months (PAY_0 to PAY_6)?

4. How do the billing amounts (BILL_AMT1 to BILL_AMT6) relate to the likelihood of default?
   
5. How do the previous payment amounts (PAY_AMT1 to PAY_AMT6) influence the probability of default?

These questions aim to explore the relationships between various features and the target variable (default.payment.next.month). They will help uncover patterns, trends, and potential factors influencing the probability of default in the dataset, guiding further analysis and model development.
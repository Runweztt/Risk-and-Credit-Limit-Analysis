# Risk-and-Credit-Limit-Analysis

 
# Introduction


In today's financial landscape, understanding customer credit behavior is crucial for financial institutions to assess risk and make informed lending decisions. One of the key factors influencing a customer’s financial risk profile is their credit utilization ratio, which measures how much credit a customer is using relative to their credit limit. Additionally, analyzing payment behaviors such as full payments, minimum payments, or partial payments can provide valuable insights into potential defaults.
In this analysis, we dive deep into the relationship between credit utilization, payment patterns, and default risk among a group of customers. By identifying high-risk individuals based on these financial indicators, we aim to help financial institutions proactively manage credit risk and maintain portfolio stability. Specifically, we’ll be looking at how factors like high credit utilization and missed payments correlate with elevated risk categories.
This kind of analysis is essential in ensuring that financial services can identify early warning signs and take appropriate action to mitigate losses while ensuring customers can continue managing their credit effectively.


# Project Overview: 

This project aims to evaluate customer behavior concerning their credit limits and risk of default. By analyzing factors such as credit utilization ratios, payment patterns, and balances, we can draw insights about customers who might be at financial risk and propose strategies to mitigate those risks.
Tools Used

#Python:

Python was employed for advanced data manipulation, analysis, and visualization:
Data Cleaning and Preprocessing:
Libraries Used: Pandas, NumPy
Python was used to clean the dataset by handling missing values, detecting outliers, and ensuring data consistency for analysis.

# Statistical Analysis:
Descriptive Statistics: Python was used to calculate key statistical measures such as the mean, standard deviation, and percentiles, providing insights into credit utilization and payment behavior.

# Data Visualization:

Libraries Used: Matplotlib, Seaborn
Python created visualizations like scatter plots and histograms to explore relationships between credit limit, balance, and other variables, making patterns easier to interpret.

# Excel:

Excel was used for basic exploratory analysis, particularly to understand data patterns and missing values:
Data Exploration:
Excel helped in quickly identifying patterns in the dataset, such as missing values and outliers, before more detailed analysis in Python.

# Data Cleaning Steps

#Step 1: Identify Missing Data
I started by checking for missing values and found out that when the "Payments" column   row has  0 input . the "Minimum Payment" row next to it  had missing values 
Step 2: Choose an Imputation Strategy
Since missing "Minimum Payment" values were mostly tied to 0 payments, I decided to fill those missing values with 0.
Step 3: Apply the Imputation
I filled all the NaN values in the "Minimum Payment" column with 0 to ensure consistency.
Step 4: Remove Remaining Missing Values
There was one missing value in the "Credit Limit" column, so I dropped that row from the dataset.
Step 5: Review the Cleaned Data
After these steps, I checked the data to ensure everything was cleaned and ready for analysis.


                     #1. Credit Limit Analysis

a. Determine Credit Utilization

Steps: 
Calculate Credit Utilization Ratio: This measures the percentage of credit customers use relative to their credit limit.
Analyze Utilization Across Customers: We explore how credit utilization varies among different customer segments.

Questions:
· What is the average credit utilization ratio across all customers?
· Are there any customers with unusually high or low credit utilization?
· How does credit utilization vary across different customer segments?

1.a Credit Limit Analysis
Summary Statistics Explained:
 
Count (8949):
 This indicates that there are 8,949 observations (customers) in the dataset used to calculate the credit utilization ratio. It represents the total number of data points.
 
Mean (0.388926):
 The average credit utilization ratio across all customers is approximately 0.39, or 39%. This means that, on average, customers are utilizing about 39% of their available credit.
 
Standard Deviation (0.389722):
 The standard deviation is about 0.39, indicating how spread out the credit utilization ratios are from the mean. A larger standard deviation suggests that there are significant variations in how different customers use their credit.
 
Minimum (0.000000):
The minimum credit utilization ratio is 0.0, meaning some customers have a balance of $0 compared to their credit limit, indicating they are not using their credit at all.

25th Percentile (0.041527):
 Also known as Q1, this value indicates that 25% of customers have a credit utilization ratio of 4.15% or lower. This shows that a significant portion of customers maintains very low utilization levels.
 
Median (50th Percentile) (0.302870):
The median credit utilization ratio is approximately 30.29%. This is the midpoint of the data, meaning half of the customers have a utilization ratio below this value and half above. This indicates that while the average is around 39%, many customers are using significantly less credit.

75th Percentile (0.717582):
 Also known as Q3, this value indicates that 75% of customers have a credit utilization ratio of 71.76% or lower. This suggests that a large segment of customers is using a moderate to high portion of their available credit.
 
Maximum (15.909951): 
 The maximum credit utilization ratio is approximately 15.91, which is unusually high. This indicates that there are some customers with balances that significantly exceed their credit limits, suggesting possible overextension or mismanagement of credit.
 
# Insights from the Statistics:

· General Usage: On average, customers are utilizing a moderate amount of their available credit, but the wide standard deviation suggests varied behavior among customers.
· Risk Consideration: The presence of a maximum ratio above 15 indicates that there may be customers at risk of default or mismanagement of their credit.
· Low Utilizers: A significant portion of customers maintains low credit utilization, as indicated by the low 25th percentile, which could reflect cautious financial behavior or underutilization of available credit.
· High Utilizers: The high 75th percentile indicates a segment of customers using a large portion of their credit, which could be a potential area of concern for risk management.

#Average Credit Utilization Ratio: 0.39

· The average credit utilization ratio of 0.39 means that, across all customers in the dataset, customers are using about 39% of their available credit. This indicates a moderate level of credit usage overall.

Customers with High Credit Utilization

·  In this context, "high credit utilization" typically refers to customers with a utilization ratio greater than 1.0, meaning they owe more than their credit limit.
Examples:
o Customers like C10006 (1.01), C10011 (1.08), and C10015 (0.92) have ratios indicating they are either over-utilizing their credit or close to their limits. This behavior could suggest financial strain or overextension.
· 
#Implications:
· 
o Risk Management: High credit utilization ratios can be a red flag for potential default risk. Customers consistently using more than their limit may struggle to make payments.
o Customer Support: Identifying these customers could lead to proactive outreach or financial counseling to help them manage their credit better.
· 
#Data Sample: The output mentions that there are 1,812 customers identified with high credit utilization, indicating a significant segment of the customer base that may need attention.


# Customers with Low Credit Utilization· 

 Low credit utilization typically refers to customers with a ratio significantly below the average, often under 0.2 or 20%.
Examples:
o Customers like C10001 (0.04), C10007 (0.05), and C10009 (0.14) have low ratios, suggesting they are using a small fraction of their available credit.
Implications:
o Financial Health: Low utilization can indicate a conservative approach to credit usage or financial stability. These customers may be good candidates for credit limit increases, as they are not utilizing their available credit fully.
o Marketing Opportunities: They could be targeted for offers encouraging more active use of credit, such as rewards programs or promotional offers.
Data Sample: There are 4,948 customers identified with low credit utilization, indicating another substantial segment that represents different financial behaviors.
· 

# Overall Insights
· 
Diversity in Customer Behavior: The dataset reveals a diverse range of credit utilization behaviors. While the average is 0.39, there's a significant difference between those who overutilize credit and those who underutilize it. 

Targeted Strategies:· 
o For High Utilizers: Risk assessment strategies might be needed, including monitoring account activity and offering financial education.
o For Low Utilizers: Opportunities for engagement to encourage responsible credit usage can help deepen the relationship and possibly increase 
revenue through usage-based fees or interest.



                    #2. Assess Credit Limit Adequacy


Steps:
Compare Balance to Credit Limit: Analyze the distribution of balances relative to credit limits to understand if credit limits are generally adequate or excessive.
Identify High Risk Customers: Determine which customers are close to or exceeding their credit limit.

Questions:
Are there customers who are frequently near or at their credit limit?
Is there a correlation between credit limit size and customer balance?

 b. Assess Credit Limit Adequacy

#Analysis Breakdown:

C10006 has a balance of 1,809.83 against a credit limit of 1,800.00, meaning they have exceeded their credit limit by a small margin (ratio of 1.005).

C10011 has a balance of 1,293.12 on a limit of 1,200.00, with a ratio of 1.078, meaning they are 7.8% over their limit.

C10015 is slightly below the limit with a ratio of 0.924, meaning they have used 92.4% of their available credit.

Interpretation:
Customers with a balance-to-credit ratio greater than or equal to 1 are considered at high risk since they have already maxed out or exceeded their credit limits.

Even those with ratios close to 1 (like 0.92 or 0.95) are also concerning because they are nearing their credit limits and may face issues if they need more credit.
This could be a signal for financial institutions to review their credit terms or consider additional risk management strategies for these customers.


                                    # 3.Risk Analysis


a. Identify Risk Indicators
Steps:
Analyze Payment Behavior: Compare PAYMENTS with MINIMUM_PAYMENTS to see if customers are consistently meeting or exceeding the minimum payment requirement.
Assess Full Payment Ratio: Review PRC_FULL_PAYMENT to determine how many customers are making full payments versus partial or minimum payments.
Questions:
What percentage of customers make full payments versus partial payments?
How does the risk of default correlate with payment behavior?

# Analysis Breakdown

Percentage of Customers Meeting or Exceeding Minimum Payments: 70.08%

 Approximately 70% of customers are making payments that meet or exceed the minimum required payment. This indicates a relatively healthy payment behavior among the majority of the customer base. However, it also suggests that around 30% of customers are not meeting the minimum payments, which could be a potential risk factor.

# Percentage of Customers Making Full Payments: 5.45%

: Only about 5.45% of customers are paying off their full balance each month. This low percentage could signal that most customers are either struggling financially or are choosing not to pay their balances in full, which may lead to increased interest charges and potential debt accumulation.

Percentage of Customers Making Partial Payments: 94.55%

 A staggering 94.55% of customers are making partial payments. This high percentage indicates that most customers are not managing to pay off their balances fully, which can increase their financial risk and may lead to a higher likelihood of defaults.
Implications

#Risk Indicators: 

The combination of a low percentage of full payments and a high percentage of partial payments suggests a potential risk for the lender. Customers consistently making partial payments might accumulate more debt over time, which could lead to defaults, especially if they also struggle to meet minimum payments.

Financial Health: The relatively high percentage of customers meeting minimum payments is encouraging, but the overall payment behavior raises concerns about long-term financial health. With such a high rate of partial payments, it may be worth exploring strategies to encourage customers to make full payments.

Customer Support: The company may need to assess its customer support strategies. It might be beneficial to implement educational programs about credit management or offer flexible payment plans to help customers transition to making full payments.
Next Steps
Explore Customer Segmentation: Identify which segments of customers are making partial payments versus those who are close to meeting the minimum payments. This may help target specific interventions.

Investigate Customer Feedback: Conduct surveys or gather feedback to understand the reasons behind the low full payment percentage. Are customers facing financial difficulties, or are they not incentivized to pay off their balances?

Monitor Payment Trends: Continue to track these metrics over time to observe trends. Are customers improving their payment habits, or is there a growing risk of default?
Insights


#High-Risk Indicators:

CUST_ID C10006 and CUST_ID C10011 both have a BALANCE_TO_CREDIT_RATIO greater than 1 (1.0055 and 1.0776, respectively). This indicates that these customers are exceeding their credit limits, making them high-risk borrowers. Exceeding the credit limit can lead to penalties and increased interest rates, heightening the risk of default.

CUST_ID C10021 also has a ratio just above 1 (1.0083), indicating they are very close to their credit limit as well.

Potentially Manageable Risk:

CUST_ID C10015 and CUST_ID C10027 have ratios below 1 (0.9243 and 0.9506, respectively), indicating they are within their credit limits. However, they are close to their limits, suggesting they should be monitored closely to prevent crossing over into high-risk territory.
Recommendations
Monitor High-Risk Customers: Since customers C10006 and C10011 are exceeding their credit limits, it is crucial to monitor their payment behaviors closely. Consider reaching out to them to offer assistance or advice on managing their debt.

Credit Limit Review: For customers like C10015 and C10027, consider reviewing their credit limits to ensure they are appropriate based on their spending habits and repayment history. They are at risk of becoming high-risk if their balances increase.

Financial Education: Offering financial education resources or workshops to help customers understand the importance of staying within their credit limits and the consequences of exceeding them may be beneficial.

Personalized Communication: Engaging with customers who are at risk of exceeding their credit limits with personalized communication could help prevent potential defaults.


# Analysis of Payment Behavior and Risk Indicators


1. Payment Behavior Insights:
The bar chart shows the distribution of full versus partial payments made by customers. The data reveals the following:
Percentage of Full Payments: Only 5.45% of customers make full payments.
Percentage of Partial Payments: A staggering 94.55% of customers are making partial payments.

This significant difference highlights a concerning trend, suggesting that the majority of customers are not paying off their balances in full, which can increase their risk of falling into debt and potentially defaulting.

2. Correlation Between Meeting Minimum Payments and High Risk:
The correlation coefficient of -0.36 indicates a moderate negative correlation between customers meeting their minimum payments and the risk of default. This suggests that:
As the likelihood of meeting or exceeding minimum payments increases, the risk of default decreases. Conversely, if customers are regularly not meeting their minimum payments, their risk of default increases.

# Insights on High-Risk Customers:

High risk customers, who often do not meet their minimum payments or only make partial payments, are in a precarious financial situation. This behavior can lead to accumulating debt and higher chances of default.
Recommendations:
Engagement Strategies: Implement targeted communication strategies for customers who frequently make partial payments, providing resources on financial management and the benefits of making full payments.

Monitoring and Alerts: Set up systems to monitor payment behavior closely. Customers who consistently fail to meet minimum payments could receive alerts or be contacted by financial advisors.

Incentives for Full Payments: Consider offering incentives, such as reduced interest rates or rewards points, for customers who make full payments regularly.
Financial Education: Increase awareness through workshops or resources aimed at educating customers about the implications of partial payments and the importance of maintaining good payment behavior to avoid high-risk situations

                              # 4 Evaluate Default Risk
 
Steps:
Calculate the Risk of Default: Identify patterns and indicators that suggest a higher likelihood of default or late payments.
Use Payment Patterns and Credit Utilization: Combine factors such as credit utilization, payment patterns, and balances to build a risk profile.
Questions:
Are there specific factors (e.g., high credit utilization, low payments) that are strongly associated with a higher risk of default?
Which customers are at the highest risk of default based on current data?

  Evaluate Default Risk
Insights on Average Credit Utilization Ratio
Interpretation of 0.39:
An average credit utilization of 39% means that, on average, customers are using 39% of their available credit limits. This level is generally considered acceptable in many financial contexts since it indicates that customers are not over leveraged.

Risk Assessment:

Moderate Utilization: A ratio below 50% typically suggests that customers are managing their credit responsibly. High utilization (usually above 80%) is a red flag for potential defaults, while low utilization (below 30%) can indicate underuse of credit.

Opportunity for Growth: If customers maintain a healthy credit utilization ratio, it can lead to increased credit limit offers, which may benefit customer satisfaction and loyalty.
High Credit Utilization Customers
The data shows that there are 1,812 customers with a credit utilization ratio greater than 0.8. This is a critical indicator, as it implies that these customers are using more than 80% of their available credit, which may suggest higher financial strain and an increased risk of default.
Key Considerations:
Potential Default Risk: Customers with a credit utilization ratio over 1 (100%) are already exceeding their credit limits, indicating a heightened risk of late payments or defaults.

Payment Behavior: Analyzing the payment patterns of these customers can provide insights into whether they are meeting minimum payment obligations, which is crucial for assessing their risk profiles.
Low Credit Utilization Customers
Conversely, the output reveals numerous customers (with utilization ratios ranging from about 0.02 to 0.15) classified as low credit utilization, suggesting they are using only a small fraction of their available credit.
Key Considerations:
Financial Stability: Generally, low credit utilization can indicate better financial health and lower default risk. However, extremely low usage could also imply that these customers are not effectively managing their credit, potentially leading to negative credit scores over time if they are not utilizing their accounts.

Assessment of Payment Behavior: Investigating how these customers are making payments can reveal if they are consistently paying their balances or if they are maintaining their credit cards without sufficient use.
High-Risk Customer Analysis
Customer Identification:
Each row corresponds to a customer, identified by CUST_ID.
Key Metrics:

Balance: The current outstanding balance on the customer's account.

Credit Limit: The maximum amount of credit that the customer has been authorized to use.

Credit Utilization: This is calculated as the ratio of the current balance to the credit limit. Values over 1.0 indicate that the customer is exceeding their credit limit, which is a significant risk indicator.

Payments: The total amount paid by the customer within the analysis period.

Minimum Payments: The minimum payment required for the customer to avoid late fees.
Insights from the Data
Credit Utilization:

Customers with high credit utilization ratios (greater than 1.0) are particularly concerning as they may be living beyond their means. For example, customers like C10001 with a utilization of 0.04 are in a safer zone, while C10004 has a balance that suggests they may not be able to meet payment obligations given their low payment amount.

Payment Behavior:
Customers who have made no payments (like C10004 with a payment of 0.00) are at a higher risk of default. This is especially critical if their balances are high relative to their credit limits.


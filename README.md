## Telco Customer Churn Analysis Using Python

# 1. Project Overview

This project is about understanding why customers leave a telecommunications company. I explored customer information and service details to identify patterns that may be related to customers leaving or staying with the company.

The main idea was to understand customer behavior through data and charts instead of making decisions based on guesses.

# 2. Project Objective

The main objectives of this project were:

- Understand how many customers left the company and how many stayed.

- Identify customer groups with higher churn.

- Explore how customer age group, service duration, contract type, payment method, and subscribed services relate to churn.

- Find useful insights that could help a business improve customer retention.

- Customer churn means customers stop using a company's services.

# 3. Dataset Understanding

- I used a dataset named Customer Churn.csv.

- Total records: 7,043 customers.

- Total columns: 21.

- customerID: Unique identification number for each customer.

- gender, SeniorCitizen, Partner, Dependents: Customer details.

- tenure: Number of months a customer has used the service.

- Service columns: PhoneService, InternetService, OnlineSecurity, OnlineBackup, TechSupport, and others describe the services customers use.

- Contract: The type of contract selected by a customer.

- Payment Method: How a customer pays the bill.

- MonthlyCharges and TotalCharges: Monthly and total charges.

- Churn: Shows whether a customer left the company (Yes) or stayed (No).

# 4. Data Cleaning and Preparation

I performed the following checks and changes before analyzing the data:

Loaded the dataset: Used Pandas to read the CSV file into a DataFrame.

Checked the data structure: Used df.info(), df.shape, and df.describe() to understand the columns, data types, number of records, and numerical values.

Checked missing values: Used df.isnull().sum(). The output showed zero missing values in every column.

Checked duplicate records: Used df.duplicated().sum(). No duplicate rows were found.

Checked duplicate customer IDs: No duplicate customer ID values were found.

Prepared TotalCharges: Replaced blank strings with "0" and tried converting the column to a numeric type. However, the converted result was not saved back to the DataFrame, so this step needs correction before using the column for further calculations.

Changed SeniorCitizen: Converted numeric values (1 and 0) into readable categories (Yes and No).

These steps helped me understand the data and make some columns easier to analyze.

# 5. Exploratory Data Analysis (EDA)

EDA means exploring data using calculations and charts to understand what is happening. I used Seaborn and Matplotlib to create count plots, a pie chart, a histogram, and a stacked percentage bar chart.

These charts helped me compare customer groups, understand the distribution of churn, and identify patterns between customer characteristics and churn.

# 6. Step-by-Step Analysis

# Step 1: Overall Customer Churn
I created a count plot and a pie chart for Churn to understand the overall distribution of customers who left and stayed. The charts showed the distribution of both groups, but the notebook did not record the exact counts or percentages in its written findings.

# Step 2: Churn by Gender
I compared male and female customers using a count plot, with separate bars for churn status. This helped me check whether churn patterns differed by gender. However, no specific conclusion was recorded in the notebook.

# Step 3: Churn by Senior Citizen Status
I created a count plot and a stacked percentage bar chart for senior citizens and non-senior citizens. The notebook records that a greater percentage of senior citizens had churned than non-senior citizens.

# Step 4: Churn by Customer Tenure
I created a histogram showing customer tenure, separated by churn status, to understand whether the length of time customers had used the service was related to churn. The notebook notes that customers who had used the service for a long time generally stayed, while customers who had used it for only one or two months were more likely to leave.

# Step 5: Churn by Contract Type
I compared churn counts for different contract types to understand whether customers with different contract commitments behaved differently. The notebook notes that customers with month-to-month contracts were more likely to churn than those with one-year or two-year contracts.

# Step 6: Churn Across Different Services
I created nine count plots for Phone Service, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, and Streaming Movies. These charts helped compare churn counts across different service categories. The notebook did not record exact churn rates for these categories, so further calculations are needed to identify which groups have the highest risk.

# Step 7: Churn by Payment Method
I created a count plot comparing churn across payment methods to understand whether the way customers paid was associated with churn. The notebook records that customers using electronic checks were more likely to churn. Churn rates should be calculated to confirm the size of this difference.

# 7. Key Findings

- A greater percentage of senior citizens churned than non-senior citizens.

- Customers with shorter tenure appeared more likely to leave.

- Month-to-month contract customers were more likely to churn than customers with longer contracts.

- Electronic-check users were identified as a group worth investigating.

- The service-related charts revealed differences in churn counts across customer groups.

- The dataset contained 7,043 records and 21 columns, with no missing values reported by the null-value check and no duplicate rows or customer IDs.

# 8. Business Insights

- These findings can help a telecommunications company decide where to investigate customer loss.

- New customers: Improve onboarding and provide support during the first few months.

- Month-to-month customers: Understand their concerns and consider suitable contract options.

- Senior citizens: Investigate whether their needs or service experiences differ from those of other customers.

- Electronic-check users: Examine payment experiences and customer feedback to understand why churn is higher.

- Service-related groups: Calculate churn rates for individual services before deciding which customers need attention.

- These are possible actions based on the observed patterns. The analysis does not prove why customers leave or whether these actions will reduce churn.

# 9. Tools and Technologies

- Python: Used to perform the analysis.

- Pandas: Loaded, inspected, and prepared the dataset.

- Seaborn: Created count plots and the tenure histogram.

- Matplotlib: Created charts, labels, the pie chart, and subplot layouts.

- Jupyter Notebook: Provided the environment for writing and running the analysis.

# 10. Final Conclusion

This project helped me understand how customer data can be used to investigate churn and identify patterns in customer behavior. I learned how to inspect a dataset, check data quality, prepare columns, create visualizations, and compare customer groups.

The analysis highlighted customer tenure, contract type, senior-citizen status, and payment method as useful areas for further investigation. It also taught me that counting customers is only the first step. Calculating churn percentages and investigating the reasons behind these patterns are important next steps before making business decisions.

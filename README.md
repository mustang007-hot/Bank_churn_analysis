# Bank Churn Analysis

## Table Of Content

- [Project Overview](#project-overview)

- [Data Source](#data-source)

- [Tools](#tools)

- [Analytical Questions Asked During the EDA](#analytical-questions-asked-during-the-eda)

- [Key Steps And Insights Gained](#key-steps-and-insights-gained)

- [Recommendations Based On Bank Churn EDA](#recommendations-based-on-bank-churn-eda)

- [References](#references)

### Project Overview
---

This repository contains a comprehensive data science project focused on predicting and understanding customer churn within a retail bank's customer base. The primary goals were to build a reliable machine learning model to flag at-risk customers and, crucially, to uncover the underlying factors that drive customer attrition.

The dataset includes customer demographics, Estimated Salary, Credit Score, Age and Card-type.

### Data Source 
Bank Churn Data : Download from [Kaggle](www.kaggle.com)

### Tools
- <b>EXCEL</b> - Data Cleaning, Pivot tables, Visualization, Power Query, Excel Charts


#### Analytical Questions Asked During the EDA
---
-Data Quality: What is the structure of the dataset, and does it contain any critical data quality issues (e.g., missing values, incorrect data types) that need cleaning before modeling?

-Target Imbalance: What is the distribution of the target variable (Exited), and how significant is the class imbalance (churn vs. non-churn)?

-Geographic Drivers: Does the customer churn rate differ significantly by country, and is there a specific region driving higher attrition?

-Financial Impact: How do financial variables like Balance and Credit Score correlate with the likelihood of a customer leaving the bank?

-Age and Churn: Is customer Age a significant factor in attrition, and which age bracket exhibits the highest churn risk?

-Product Stickiness: How does the Number of Products a customer holds affect their propensity to churn (e.g., are customers with fewer products more likely to leave)?

-Tenure Effect: Is there a linear relationship between customer Tenure (years with the bank) and the probability of churn?

-Feature Distribution: Do continuous features (Age, Balance, EstimatedSalary) exhibit normal distributions, and are there significant outliers that could impact model training?

#### Key Steps and Insights Gained
---

1. Data Structure and Quality Assessment

- Initial Review: Inspected data types, checked for missing values (nulls), and assessed the cardinality of categorical features. The dataset was found to be exceptionally clean, with no significant missing data, allowing us to focus immediately on statistical relationships.

2. Univariate and Bivariate Analysis
We analyzed how individual and pairs of features relate to the target variable (Exited):


- Geographic Analysis: This produced the project's most significant finding, illustrating a stark difference in churn rates across countries. Germany showed a much higher rate of attrition compared to France and Spain, suggesting an external or regional factor at play.

- Financial Features: Examined the relationship between churn and monetary variables:

- Balance: Customers with very low or very high balances were less likely to churn, while those in the middle range showed the highest risk.

- Credit Score: A slight trend showed that customers with extremely low credit scores were more likely to churn, though the effect was not linear.

<b>Demographic & Behavioral Features:</b>

- Age: Churn risk significantly increases for customers older than 40, peaking in the 50-60 age bracket.

- Tenure: No strong linear relationship was found between the number of years a customer has been with the bank and their likelihood of leaving.

- Number of Products: Customers holding only one product showed a very high risk of exiting, potentially due to a "pain point" that a single service couldn't solve.

3. Outlier and Distribution Checks

- Visualized the distributions of continuous features (e.g., Age, Balance, EstimatedSalary) using histograms and box plots. This helped identify potential outliers and confirm that most features are relatively well-behaved, minimizing the need for extensive transformation before modeling.

The insights gained from this EDA directly fueled the creation of new features (like age-group bins and interaction terms) and guided the selection of Gradient Boosting as the final model, ensuring we addressed the complexities and imbalance found in the data.

#### Recommendations Based on Bank Churn EDA

---
The Exploratory Data Analysis revealed several critical segments and features that drive customer attrition. These recommendations focus on maximizing retention efforts where the risk is highest.

1. Geographical Remediation (Highest Priority)

Insight: Germany showed a significantly higher churn rate compared to other countries.

<b>Recommendation:</b>

Targeted Investigation: Immediately launch a task force to investigate the specific issues driving churn in the German market. This could involve exit interviews, competitor analysis, or local branch service audits.

Local Intervention: Implement pilot retention programs specifically for high-risk German customers, such as dedicated local support channels or loyalty bonuses.

2. Age-Based Retention Programs

Insight: Churn risk significantly increases for customers older than 40, peaking in the 50-60 age bracket.

<b>Recommendation:</b>

Proactive Engagement: Develop targeted communication campaigns for customers entering the 40-50 age range. Messages should focus on stability, retirement planning, and long-term financial security.

Product Fit: Review product offerings for this demographic. Are current products meeting their needs, or are they being underserved compared to younger customers?

3. Product Diversification and Pain Point Removal

Insight: Customers holding only one product showed a very high risk of exiting, indicating low 'stickiness.'

<b/>Recommendation:</b>

Cross-Sell Incentives: Introduce attractive incentives (e.g., fee waivers, promotional rates) to encourage single-product customers to adopt a second product within the first year.

"Product Check-up" Campaign: Proactively contact single-product customers to perform a "financial health check" to ensure their current product is meeting their needs and subtly introduce other relevant services.

4. Balance Risk Segmentation

Insight: Customers in the middle balance range showed the highest churn risk, while those with very low or very high balances were more stable.

<b>Recommendation:</b>

Value Proposition Review: Analyze the value proposition for the mid-tier balance customers. They are stable enough to have significant funds but not high-value enough to be receiving personalized relationship management.

Tiered Service: Introduce a new service tier or rewards program designed to reward and stabilize customers whose balances fall into the identified high-risk range.

By focusing retention resources on these segments—especially German customers aged 40+ with single products and mid-range balances—the bank can achieve the most immediate and significant impact on reducing customer attrition.
Geographic Impact: The analysis revealed a disproportionately high churn rate in the Germany segment, accounting for 39.33% of all customer exits in the dataset. This finding suggests an urgent need for targeted retention strategies and deeper local investigation in that region.

#### References
---
- [kaggle](www.kaggle.com)
- <b>EXCEL</b>

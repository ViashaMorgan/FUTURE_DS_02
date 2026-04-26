# FUTURE_DS_02

# Customer Retention And Churn Analysis

## 1.) Objective

To simulate a real-world SaaS analytics workflow by analyzing churn, retention, and customer lifetime trends, and translating findings into actionable business recommendations.

## 2.) Datasets
Source: Kaggle (https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)

This project uses five separate datasets to analyze different aspects of business performance:

🔹 ravenstack_accounts
  
  Contains customer-level information such as account details, industry, country, and signup date.

🔹 ravenstack_subscriptions
  
  Tracks subscription data including plan tier, pricing (MRR), billing cycles, and subscription status.

🔹 ravenstack_churn_events
  
  Records churn occurrences, including churn dates and associated reasons where available.

🔹 ravenstack_feature_usage
  
  Captures product engagement metrics such as features used, usage frequency, duration, and error counts.

🔹 ravenstack_support_tickets

  Includes customer support interactions, enabling analysis of support volume, issues, and their relationship to churn.



## 3.) Analysis Performed

3.1) Data Cleaning & Feature Engineering:

   🔹 Handled missing values and duplicates
  
   🔹 Created key variables such as churn flags, tenure, and engagement indicators

3.2) Customer Behavior Aggregation

  🔹 Transformed raw usage logs into customer-level metrics: Usage, Duration, Errors, Feature adoption

3.3) KPI Analysis

 🔹  Evaluated core business metrics: Churn rate, Customer count, Average customer lifetime

3.4) Churn Segmentation

  🔹 Analyzed churn rates across: Plan tiers, Geographic regions

3.5) Customer Lifetime Analysis

  🔹 Examined tenure distributions
  
  🔹 Compared churned vs retained customers

3.6) Cohort Retention Analysis

  🔹 Built cohort models based on signup month
  
  🔹 Tracked retention trends over time

3.7)  Retention Driver Analysis

  🔹 Identified relationships between churn and: Product usage, Error rates, Feature adoption

3.8) Advanced Retention Modeling

   🔹 Explored interactions between: Feature usage, Retention rates, Revenue (MRR) across customer segments

## 4.) Tech Stack


| Tool | Purpose |
|------|--------|
| Google Colab | Python development environment used to run notebooks and perform data analysis |
| Python | Core programming language used for data cleaning, manipulation, and analysis |
| Pandas | Data handling and preprocessing (cleaning, grouping, aggregation) |
| NumPy | Numerical computations and array-based operations |
| Matplotlib / Seaborn | Data visualisation in Python for exploratory analysis |
| Power BI | Building interactive dashboards and final business visualisations |
| Jupyter/Colab Notebook | Organising and documenting the analytical workflow |
| GitHub | Version control and project hosting |

*Minor discrepancies between Python and Power BI visual outputs arise from differences in default aggregation behaviour, data type handling, and filtering order within each tool. These variations do not affect the overall analytical conclusions, as both pipelines are derived from the same cleaned dataset and show consistent directional trends*

## 5.) Key Insights
<details>
  <summary> Churn Patterns</summary>
  <img width="556" height="512" alt="image" src="https://github.com/user-attachments/assets/94cdce94-ba00-4d93-a351-5333e74608b0" />

  * Enterprise churn is highest because these customers have higher expectations, more complex use cases, and lower tolerance for performance gaps or missing features.
    
  * They are also more price-sensitive at scale, so any perceived drop in ROI leads to cancellations more quickly than lower-tier users.
    
  * Pro sits in the middle with moderate expectations and cost, while Basic users churn less due to lower commitment and simpler needs.


 <img width="564" height="435" alt="image" src="https://github.com/user-attachments/assets/aa0e6b37-ca54-4339-8753-ea94c8751efb" />

* These countries are largely located in highly developed, saturated SaaS markets (North America, Europe, and parts of APAC), where competition is intense.

* Customers in these regions have many alternatives and higher expectations, making them more likely to switch providers.
  
* This combination of market maturity and choice drives higher observed churn rates.

  




</details>

<details>
  <summary> Customer Lifetime Trends</summary>

  <img width="552" height="435" alt="image" src="https://github.com/user-attachments/assets/f27b300b-0cf4-4b5c-bd24-13b632262cdb" />

  * The distribution is heavily right-skewed, showing most customers have relatively short lifetimes with a sharp peak around the mid-range.
    
  * There’s a noticeable drop-off as lifetime increases, indicating fewer long-term customers and gradual attrition over time. 
    
  * The small spike near very low lifetimes suggests early churn (customers leaving shortly after joining).

  * Towards the middle, there is a “critical churn window” where users reassess value after a few billing cycles.



</details>

<details>
  <summary> Cohort Retention Analysis</summary>


</details>









## 6.) Dashboard Preview
> Link to the dashboard: https://app.powerbi.com/links/s8iPDCh_7r?ctid=4b1b908c-5582-4377-ba07-a36d65e34934&pbi_source=linkShare

<img width="1046" height="1052" alt="image" src="https://github.com/user-attachments/assets/12d416e3-c4b9-4c9f-acb0-836da6c1ff2b" />



## 7.) Business Recommendations

## 8.) Outcome



## 👤 Author

Viasha Morgan

E-mail: viashamorgan7@gmail.com

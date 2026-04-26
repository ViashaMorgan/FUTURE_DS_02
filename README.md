# FUTURE_DS_02

# Customer Retention And Churn Analysis

## 1.) Objective

To simulate a real-world SaaS analytics workflow by analyzing churn, retention, and customer lifetime trends, and translating findings into actionable business recommendations.

## 2.) Datasets
Source: Kaggle (https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)

This project uses five separate datasets to analyze different aspects of business performance:

- ravenstack_accounts
  
  Contains customer-level information such as account details, industry, country, and signup date.

- ravenstack_subscriptions
  
  Tracks subscription data including plan tier, pricing (MRR), billing cycles, and subscription status.

- ravenstack_churn_events
  
  Records churn occurrences, including churn dates and associated reasons where available.

- ravenstack_feature_usage
  
  Captures product engagement metrics such as features used, usage frequency, duration, and error counts.

- ravenstack_support_tickets

  Includes customer support interactions, enabling analysis of support volume, issues, and their relationship to churn.



## 3.) Analysis Performed

🔹 Data Cleaning & Feature Engineering:

   Handled missing values and duplicates
  
   Created key variables such as churn flags, tenure, and engagement indicators

🔹 Customer Behavior Aggregation

   Transformed raw usage logs into customer-level metrics: Usage, Duration, Errors, Feature adoption

🔹 KPI Analysis

   Evaluated core business metrics: Churn rate, Customer count, Average customer lifetime

🔹 Churn Segmentation

   Analyzed churn rates across: Plan tiers, Geographic regions

🔹 Customer Lifetime Analysis

   Examined tenure distributions
   Compared churned vs retained customers

🔹 Cohort Retention Analysis

   Built cohort models based on signup month
   Tracked retention trends over time

🔹 Retention Driver Analysis

   Identified relationships between churn and: Product usage, Error rates, Feature adoption

🔹 Advanced Retention Modeling

   Explored interactions between: Feature usage, Retention rates, Revenue (MRR) across customer segments

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

  


  




</details>

<details>
  <summary> Customer Lifetime Trends</summary>

</details>

<details>
  <summary>🏷 Cohort Retention Analysis</summary>


</details>

<details>
  <summary> Retention Drivers: Why Customers Churn</summary>
  


</details>







## 6.) Dashboard Preview
> Link to the dashboard: https://app.powerbi.com/links/s8iPDCh_7r?ctid=4b1b908c-5582-4377-ba07-a36d65e34934&pbi_source=linkShare

<img width="1046" height="1052" alt="image" src="https://github.com/user-attachments/assets/12d416e3-c4b9-4c9f-acb0-836da6c1ff2b" />



## 7.) Business Recommendations
Based on the analysis, a business should prioritize strengthening its presence in the United Kingdom, which generates the vast majority of revenue, while simultaneously reducing geographic risk by expanding into underperforming but promising markets such as Germany and France. A dual product strategy is recommended: maintain consistent availability of high-demand, low-cost items (such as office supplies) to sustain sales volume, while actively promoting high-value products like technology and equipment to maximize revenue. Additionally, the business should focus on retaining and nurturing high-frequency, high-spending customers through targeted marketing and loyalty initiatives, as these customers contribute disproportionately to total revenue. Finally, underperforming categories should be reviewed and optimized through pricing, bundling, or promotional strategies to improve overall profitability and ensure balanced growth.

## 8.) Outcome

This project successfully transformed raw sales and transaction data into meaningful business insights through structured analysis and visualization. Key revenue drivers, high-performing products, and dominant markets were identified, along with clear patterns in customer purchasing behavior. The analysis highlights opportunities for revenue growth, improved customer targeting, and better product strategy. Overall, the project demonstrates how data analytics can be effectively applied to support informed decision-making and drive business performance in a real-world context.

## 👤 Author

Viasha Morgan

E-mail: viashamorgan7@gmail.com

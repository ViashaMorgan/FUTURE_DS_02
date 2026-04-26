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
    

<img width="580" height="432" alt="image" src="https://github.com/user-attachments/assets/169ed70f-3a0c-4eab-97b6-5e2bbef3dda9" />


* Non-churned customers (0) have significantly higher tenure days, with a higher median and wider distribution.
  
* Churned customers (1) tend to have very low tenure, indicating they leave early in their lifecycle.
  
* Overall, there is a strong inverse relationship between tenure and churn: the longer a customer stays, the less likely they are to churn.


</details>

<details>
  <summary> Cohort Retention Analysis</summary>

<img width="1313" height="790" alt="image" src="https://github.com/user-attachments/assets/e3cedb9c-267e-40be-b563-335a2bbc4833" />

* Activity is concentrated early: most cohorts show their highest values in months 0–3, meaning user engagement is strongest right after signup.
  
* Mid-to-late spikes cluster in specific cohorts: e.g., 2024-04 (month 9), 2024-06 (month 7), 2024-08 (month 5), 2024-09 (month 4), and 2024-10 (month 3), suggesting re-engagement or campaign-driven returns at those points.
  
* Newer cohorts (late 2024) concentrate heavily in the first 1–2 months, indicating strong initial traction but limited long-term data yet.



<img width="1030" height="547" alt="image" src="https://github.com/user-attachments/assets/b29e3553-b07b-470e-bbcb-7d612d9ebec5" />


* Retention generally increases as the number of features used goes up, though the relationship isn’t perfectly linear.
  
* Enterprise customers (larger bubbles) tend to use more features and show slightly higher retention than Basic/Pro users.

* Driving feature adoption—especially among higher-value customers—likely improves retention, so focus on onboarding and feature discovery.


<img width="1288" height="339" alt="image" src="https://github.com/user-attachments/assets/7f418957-9ed9-42c4-9abb-2a6b1b31c4b6" />


* Users who churn (1) show slightly higher errors and more variability, but the distributions largely overlap with non-churners (0).
  
* Total usage is fairly similar between both groups, with no strong separation—suggesting usage alone isn’t a clear churn driver.
  
* Feature usage is slightly lower for churned users, hinting that less engagement with features may be linked to higher churn.





  
</details>





## 6.) Dashboard Preview
> Link to the dashboard: https://app.powerbi.com/links/ZYNsIljxdx?ctid=4b1b908c-5582-4377-ba07-a36d65e34934&pbi_source=linkShare

<img width="1242" height="1042" alt="image" src="https://github.com/user-attachments/assets/4c51b07b-a60f-4acc-b517-fffec1cf5fba" />


## 7.) Business Recommendations

High-risk customers (especially lower-tier plans and certain regions) should be identified early and supported through stronger onboarding and regular check-ins in the first 30–60 days. Low engagement and limited feature use are major drivers of churn, so improving onboarding, adding simple in-app guidance, and encouraging feature exploration can help increase retention. Customers experiencing more errors or frequent support interactions are more likely to leave, so fixing bugs, improving system stability, and strengthening self-service support are important. Early-stage drop-off is particularly significant, meaning structured onboarding and clear “first value” milestones are critical in the first 90 days. Overall, customers who use more features tend to stay longer, so encouraging deeper product usage and aligning plan value with user needs can further reduce churn.


## 8.) Outcome

Good — then your **Outcome** should not repeat *what to do*. It should focus on **what you discovered and what the analysis achieved**.

Here’s a clean, short version that is clearly distinct from recommendations:

---

## 📊 Outcome

This analysis revealed clear behavioural patterns behind customer churn, with early-stage users, lower-tier plans, and low-engagement customers showing the highest likelihood to churn. Cohort and segmentation analysis confirmed that retention is strongest among users with deeper and more consistent product usage. The project successfully transformed raw customer and usage data into actionable insights, highlighting key risk segments and measurable differences in retention behaviour across plans, regions, and usage levels.


## 👤 Author

Viasha Morgan

E-mail: viashamorgan7@gmail.com

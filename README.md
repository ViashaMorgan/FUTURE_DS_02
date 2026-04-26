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

  > Handled missing values and duplicates
  
  > Created key variables such as churn flags, tenure, and engagement indicators

🔹 Customer Behavior Aggregation

  > Transformed raw usage logs into customer-level metrics: Usage, Duration, Errors, Feature adoption

🔹 KPI Analysis

  > Evaluated core business metrics: Churn rate, Customer count, Average customer lifetime

🔹 Churn Segmentation

  > Analyzed churn rates across: Plan tiers, Geographic regions

🔹 Customer Lifetime Analysis

  > Examined tenure distributions
  > Compared churned vs retained customers

🔹 Cohort Retention Analysis

  > Built cohort models based on signup month
  > Tracked retention trends over time

🔹 Retention Driver Analysis

  > Identified relationships between churn and: Product usage, Error rates, Feature adoption

🔹 Advanced Retention Modeling

  > Explored interactions between: Feature usage, Retention rates, Revenue (MRR) across customer segments

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
  <summary>💰 Revenue Trends</summary>
  <img width="1189" height="590" alt="image" src="https://github.com/user-attachments/assets/49218366-d000-40fe-832f-c59bbdeadc4a" />

* Revenue fluctuates moderately in the first half of the year, with no clear upward trend.
* From around August, there is a strong and consistent increase, peaking sharply in November.
* December shows a significant drop, likely indicating seasonality 

  
<img width="1188" height="590" alt="image" src="https://github.com/user-attachments/assets/84c16316-edf2-4ac0-aefb-748041333e77" />

* After the peak at year-end, revenue typically drops sharply, creating low spikes in the following months.
* This is due to reduced consumer spending after heavy holiday purchases and tighter budgets in January.
* Retail activity slows as demand normalizes and fewer promotions are offered.
* These low spikes reflect a post-holiday correction before sales gradually stabilize again.
* Revenue shows an overall upward trend from 2014 to 2018, indicating growth over time.
* The highest sales occur toward late 2017, showing peak performance in the most recent period.


</details>

<details>
  <summary>🌍 Regional Performance</summary>
<img width="636" height="659" alt="image" src="https://github.com/user-attachments/assets/14cd1943-2ade-4188-a93b-271959fafb50" />
  
* We can see that the UK generates the most revenue
* The top revenue-generating countries are all located in Western Europe, indicating a strong regional concentration.
* These markets are high-income and well-developed, leading to higher consumer spending and consistent demand.
* Their close proximity and strong logistics networks also support efficient distribution and higher sales volumes.

</details>

<details>
  <summary>🏷 Category Performance</summary>
<img width="578" height="522" alt="image" src="https://github.com/user-attachments/assets/2868b45b-aa09-4fb0-9e67-912bc4509414" />
  
* We have indicated the high-value categories
* Technology leads in both sales and profit, making it the most financially rewarding category overall.
* Furniture has strong sales but extremely low profit, suggesting high costs or heavy discounting that significantly eats into margins.
* Office Supplies performs solidly and has a healthier profit relative to its sales, making it the most efficient category.
* Across all three categories, the gap between sales and profit is very large, indicating high operating or product costs that the business should look to address.

</details>

<details>
  <summary>🛍 Product Performance</summary>
  <img width="629" height="470" alt="image" src="https://github.com/user-attachments/assets/b6eb50b1-531c-4443-a3eb-e235cf73dc76" />

* Office supplies are the top quantity of items sold  
* Higher quantity sold relates to more popular products
* More popular products don't automatically correlate to higher profits

<img width="839" height="838" alt="image" src="https://github.com/user-attachments/assets/55937b93-8803-4b83-8c83-19804d3d0e8b" />

* The Canon ImageCLASS 2200 Advanced Copier dominates sales at ~62,000 units, nearly double the second-highest product (Fellowes PB500 at ~28,000), suggesting it's a flagship or heavily promoted item.
* Products 3–10 form a tightly clustered mid-tier ranging from ~17,000–23,000 units, indicating relatively uniform demand across the remaining office equipment categories.
* The steep drop-off after the top two products reveals a classic long-tail distribution, meaning the business relies heavily on a small number of high-performing specific products to drive overall revenue.
* Copiers and printers are the most in-demand product category, likely because they are essential, high-use machines in most office environments.

<img width="839" height="838" alt="image" src="https://github.com/user-attachments/assets/672db723-6a27-4c2f-b326-620ed1eeb2bf" />

* The Canon imageCLASS 2200 Advanced Copier dominates profit, showing that high-end office technology is the strongest profit driver in this set.
* There’s a noticeable drop after the top product, but mid-tier tech like binding machines, laser printers, and inkjet printers still generate solid profits (~4K–8K), indicating steady demand for essential office equipment.
* Lower-profit items are still mostly technology products (shredders, label printers, headsets) , suggesting the business relies heavily on a broad range of office tech, even if individual profits are smaller.


</details>

<details>
  <summary>👥 Customer Behavior</summary>
<img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/d0d77972-6f80-4699-914a-1c196290e9e4" />
  
* Most customers generate relatively low revenue while a small number contribute very high amounts.
* The majority of customers fall within the lower revenue range (roughly under 5,000), indicating a large base of low-to-mid spenders.
* There are a few extreme high-value customers (outliers) reaching up to ~25,000, suggesting the presence of key high-revenue contributors.

<img width="540" height="374" alt="image" src="https://github.com/user-attachments/assets/1f4607d0-21fa-4da8-a4dc-985ffe92f9c7" />

* Repeat customers significantly outnumber one-time customers, with nearly 800 compared to around 200–300 for the latter.  
* This suggests strong customer loyalty or effective retention strategies, as the majority of purchases come from returning buyers.
* To further grow revenue, consider focusing on converting the existing one-time customers into repeat buyers through targeted engagement or loyalty programs.

</details>

<details>
  <summary>🔁 Purchase Behavior</summary>
<img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/2df09323-0330-4edc-b2f0-eb7785cec5f9" />
  
* Most customers make only 4-7 purchases and very few reaching 8 or more.
* This indicates a large base of low-frequency buyers, which aligns with the earlier finding that repeat customers exist but don't purchase often.
* To increase customer lifetime value, consider implementing engagement tactics like loyalty rewards or personalized offers to encourage more frequent purchases.

  <img width="713" height="470" alt="image" src="https://github.com/user-attachments/assets/6581e9af-00bd-4cd0-bcc0-c0ee11f9c726" />
  
* This scatter plot likely shows a positive correlation, where customers with more orders tend to generate higher revenue, supporting the value of retaining frequent buyers.
* Any outliers, such as high revenue with low orders or low revenue with high orders could reveal unique customer segments like bulk purchasers or discount-driven shoppers.
* Adding a trend line or correlation coefficient would help quantify the strength of the relationship and guide strategies for increasing order frequency.


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

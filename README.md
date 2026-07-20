 # Bright Coffee Sales Analytics Agent
 
 
## 1. Introduction & Objective

### Introduction
Businesses generate large amounts of sales data every day, making it difficult to manually identify trends and make informed decisions. Artificial Intelligence (AI) agents can simplify this process by analysing data, answering business questions, and presenting insights in an easy-to-understand format.
This project involved developing an AI-powered sales analysis agent in Databricks using the Bright Coffee sales dataset. The agent was designed to answer business-related questions accurately and provide insights that support data-driven decision-making.

### Objective
The objectives of this project were to:
- Build a Bright Coffee Sales Analytics Agent using Databricks.
- Configure the agent with clear instructions to analyse the Bright Coffee dataset.
- Test the agent using business-related questions.
- Validate the accuracy of the agent's responses against the source data.
- Generate business insights and recommendations based on the analysis.

## 2. Dataset Description
The project uses the Bright Coffee retail sales dataset, which contains transaction-level information for sales made across multiple store locations.

- transaction_id:	Unique identifier for each sales transaction.
- transaction_date: Date on which the transaction occurred.
- transaction_time: Time when the transaction was completed.
- transaction_qty	: Number of units purchased in the transaction.
- store_id: Unique identifier for the store where the transaction occurred.
- store_location: Name or location of the store where the sale took place.
- product_id: Unique identifier for the product sold.
- unit_price: Price of a single unit of the product (converted to numeric during analysis).
- product_category: Category to which the product belongs 
- product_type: Product type or subcategory.
- product_detail: Detailed name or description of the product.

## 3. Agent Instructions

### Role
You are the Bright Coffee Sales Analysis Agent, an AI assistant that helps users understand and analyze sales performance using the Bright Coffee dataset. Your purpose is to transform raw sales data into clear, accurate, and actionable business insights that support better decision-making.

### Users
You assist:
- Business owners
- Store managers
- Operations managers
- Sales managers
- Marketing managers
- Executives and decision-makers
- Data analysts who need quick business insights

Assume users may not have technical or data analysis knowledge. Explain findings in simple business language.

### Dataset
Use only the Bright Coffee dataset when answering questions.

The dataset includes information such as:
- Transaction ID
- Transaction Date
- Transaction Time
- Quantity Sold
- Store ID
- Store Location
- Product ID
- Unit Price
- Product Category
- Product Type
- Product Detail

the data does a revenue column use unit price*quantity sold As revenue

### Answer questions related to:
- Sales Performance
- Total sales
- Revenue
- Number of transactions
- Sales growth
- Daily, weekly, monthly, or yearly performance
- Customer Purchasing Patterns
- Busy hours
- Peak days
- Seasonal purchasing trends
- Average transaction size
- Product Performance
- Best-selling products
- Lowest-selling products
- Product categories
- Quantity sold
- Revenue by product
- Store Performance
- Store comparisons
- Best-performing locations
- Sales by store
- Revenue differences between stores
- Business Trends
- Sales trends over time
- Growth and decline
- Peak periods
- Slow periods
- Product popularity changes
- Explaining Insights

Always present insights in a clear and professional way.

For every answer:
- Start with a direct summary.
- Support the summary with numbers from the dataset.
- Explain why the result matters for the business.
- Keep explanations concise unless the user asks for more detail.

Use:
- Exact values
- Percentages
- Comparisons
- Rankings
- Trends

Avoid unnecessary technical or statistical terminology.

Example structure:
- Summary
State the main finding.

- Evidence
Include the relevant figures from the Bright Coffee dataset.

- Business Insight
Explain what the numbers suggest.

### Handling Ambiguous Questions
If a user's question is unclear:
- Ask a clarifying question before answering.
- Do not guess what the user means.

Examples:
- Which store are you referring to?
- Which time period would you like to analyze?
- Which product category do you mean?

If the dataset does not contain the requested information:
- Clearly state that the information is unavailable.
- Explain what data is available instead.
- Offer related analyses when appropriate.
- Accuracy and Data Integrity

Only report information that exists in the Bright Coffee dataset.

### Never:
- Invent numbers
- Estimate missing values
- Create products or categories that do not exist
- Assume causes for trends without evidence

If the dataset cannot answer the question, clearly say so.

### Recommendations
Provide recommendations only when the available data supports them.

Recommendations should:
- Be based on observed trends.
- Clearly reference the supporting data.
- Be practical and business-focused.

Examples:
- Increase stock for consistently high-selling products.
- Schedule more staff during peak sales hours.
- Promote slower-selling products if sales remain consistently low.

Do not recommend actions when:
- There is insufficient evidence.
- The user only asks for factual information.
- The data does not support a conclusion.

Separate recommendations from factual findings by using a Recommendations section.

### Response Style
Your responses should be:
- Accurate
- Professional
- Clear
- Objective
- Business-focused
- Easy to understand

Always prioritize facts from the Bright Coffee dataset over assumptions or opinions. When uncertainty exists, state it explicitly rather than guessing.

## 4. Validation of Agent Responses
Three responses were independently validated using pandas data aggregations and visualisations to verify the accuracy of the agent.

### Validation 1

Question 1
- What is the total revenue generated by Bright Coffee during the entire period covered by the dataset?

Agent Answer 
- 698,812.33

Validation Method
- Calculated the sum of the revenue column using pandas.

Result
- The calculated total revenue was 698,812.33, matching the agent's answer exactly.

Verdict: Correct

### Validation 2

Question 2
- Which product category generated the highest total sales revenue, and what percentage of overall revenue did it contribute?

Agent Answer
- Coffee generated 269,952.45 in revenue and contributed 38.63% of the total revenue.

Validation Method
- Grouped the data by product category, calculated total revenue for each category, and confirmed the results using a bar chart.

Result
- Both the calculations and the chart confirmed that Coffee was the highest-performing category, contributing 38.63% of total revenue.

Verdict: Correct

### Validation 3

Question 3
- Which store location had the highest sales revenue, and how does it compare with the lowest-performing store?

Agent Answer
- Hell's Kitchen generated the highest revenue (236,511.17), while Lower Manhattan generated the lowest (230,057.25), a difference of 6,453.92 (2.81%).

Validation Method:
- Grouped revenue by store location and compared the results using a bar chart.

Result
- The grouped calculations and chart matched the agent's response exactly.

Verdict: Correct

## 5. Key Insights
The Bright Coffee Sales Analysis Agent identified several important business insights.
Bright Coffee generated a total revenue of 698,812.33 during the analysed period. Coffee was the highest-performing product category, contributing 38.63% of total revenue, while Tea contributed 28.11%. Together, these two categories accounted for over two-thirds of total sales.

The lowest-performing product categories were Packaged Chocolate, Flavours, Loose Tea, and Branded merchandise, indicating opportunities for promotional campaigns or product improvements.Hell's Kitchen generated the highest overall revenue; however, all three stores performed similarly, showing consistent operations across locations.Lower Manhattan achieved the highest average transaction value despite having the lowest total revenue, suggesting customers spend more per visit but visit less frequently.

Monthly revenue increased steadily from February to June, indicating strong business growth driven primarily by increased customer traffic rather than higher spending.Sales activity was highest during the morning hours (approximately 6 AM–11 AM), highlighting the importance of staffing and inventory planning during peak periods.Revenue remained relatively consistent across weekdays, suggesting that hourly demand has a greater impact on sales than differences between days of the week.

## 6. Business Recommendations
Based on the analysis, the following recommendations are proposed:
- Continue prioritising Coffee and Tea, as they generate the majority of total revenue.
- Increase staffing and inventory during morning peak hours to improve customer service and reduce waiting times.
- Investigate the factors contributing to Lower Manhattan's higher average transaction value and apply successful practices to other stores.
- Introduce promotions or bundled offers to improve sales of underperforming categories such as Packaged Chocolate, Flavours, Loose Tea, and Branded merchandise.
- Focus marketing efforts on increasing customer traffic rather than increasing prices, as business growth is currently driven by higher transaction volumes.
- Monitor monthly sales trends to identify seasonal patterns and plan inventory and staffing accordingly.

## 7. Conclusion
This project successfully demonstrated how an AI agent can be developed in Databricks to analyse retail sales data and provide accurate business insights. The Bright Coffee Sales Analysis Agent consistently answered business questions using the dataset and produced reliable, data-driven results.Independent validation confirmed that the agent's responses were accurate, demonstrating that the instructions effectively prevented unsupported conclusions or fabricated information. One challenge encountered during the project was ensuring that the dataset was correctly prepared, particularly converting data types and creating the revenue column before analysis.If this project were extended, additional features such as customer segmentation, sales forecasting, and interactive dashboards could further improve the agent's analytical capabilities and business value.




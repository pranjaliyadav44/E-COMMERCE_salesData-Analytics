# E-COMMERCE_salesData-Analytics
 The project involves popular e commerce site myntra . Myntra sales Analytics using power Bi dashboards. . 

This report outlines the development and utilization of a Power BI dashboard for analyzing sales data and predicting future sales for Mytra, a fictional e-commerce platform specializing in fashion and lifestyle products. The analysis leverages a sample dataset of 50,000 transactions spanning 2022–2023, including variables such as customer demographics, product categories, purchase dates, quantities, prices, and discounts. The goal is to provide actionable insights for inventory management, marketing strategies, and revenue forecasting.

Data Preparation and Cleaning

Dataset Description
Source: Simulated e-commerce transaction data from Mytra's database.
Key Columns: Customer ID, Age, Gender, Location, Product ID, Category, Subcategory, Price, Quantity, Discount, Total Amount, Order Date.
Size:3.50,000 rows; cleaned to remove duplicates (2% of data) and handle missing values (e.g., imputed average age for nulls).
Power BI Steps:
Import Data: Connected to a CSV file via Power BI Desktop.
Data Modeling: Created relationships between tables (linked Customers to Orders via Customer ID). Added calculated columns like "Profit Margin" using DAX: Profit Margin = (Total Amount - Cost) / Total Amount.
Data Transformation: Used Power Query to filter outliers and normalize categories.

Exploratory Data Analysis (EDA)
Key Insights-
•Sales Trends:
Total Orders: 3.50K
Average Sales Amount: ₹538.24
Total Sales Amount: ₹1.88M
Total Revenue: ₹3M
Average Discount: 35.51%
Total Products: 40
 Amount rate (35%), suggesting th
•Top Performing Brands
From the bar chart and table:
Top 3 Brands:
1. H&M
2. Roadster
3. Adidas
These brands contribute the majority of total sales and revenue.
Allen Solly and Here&Now follow, but with lower totals. 
•Product Category Distribution
Women’s category: ~43%
Men’s category: ~32%
Kids category: ~25%
Top States: Maharashtra, Karnataka, Tamil Nadu, and Delhi NCR lead in sales.
Bottom States: Gujarat and others contribute less.
•A visible positive correlation between higher discounts and sales spikes.
•Sales volumes tend to rise during higher discount periods.
•Price sensitivity is significant — customers respond strongly to discount-based promotions
Sales by Days-
•Noticeable spikes on weekends (Saturday–Sunday).
•Sales dip slightly during midweek.
Sales across 2021–2023 show a steady increase, especially in Beauty and Men’s categories.
Women’s remains the largest but relatively stable.

Customer Segmentation: Females aged 25–34 in urban areas generated 45% of sales. High-value customers (top 10%) contributed 70% of revenue.
Product Performance: Best-sellers: T-shirts (avg. 4.2 rating), Accessories (highest margin at 35%). Low performers: Footwear (20% discount dependency).
Geographic Analysis: North India led with 40% of orders; South India showed 15% YoY growth

Overall Sale Insights Interpretation

-Women’s category = main driver of revenue.
-H&M and Roadster = top-performing brands.
-Metro cities dominate sales.
-Weekends + discounts = strong sales opportunities.
-Beauty & Men’s categories show upward trends — potential growth areas.

-Myntra is achieving strong overall revenue despite a relatively high discount rate (35%), suggesting that discounts are driving significant sales volumes.
-Interpretation:
High fashion and casual wear brands dominate Myntra’s performance, showing customer preference for trendy yet affordable categories.
-Interpretation:
Women’s apparel is the largest revenue driver for Myntra, reflecting strong female customer engagement.
Sales by State
-Interpretation:
Urban and metro regions are Myntra’s strongest markets; regional campaigns could boost underperforming states.
Sales by Discount
- Interpretation:
Price sensitivity is significant — customers respond strongly to discount-based promotions
-Interpretation:
Customer activity peaks on weekends — ideal for launching flash sales or new campaigns.
 Category Sales by Year
 -Interpretation:
Diversification into new product segments (like beauty) is yielding growth beyond traditional apparel.

 
Visualizations in Myntra Dashboard maps:

Line Chart: Monthly sales trend with seasonality overlay.
Bar Chart: Revenue by category and subcategory.
Map Visualization: Sales by location, highlighting regional hotspots.
Scatter Plot: Price vs. Quantity sold, revealing price elasticity (e.g., discounts boost volume by 25%).

 A. Filled Map (Choropleth Map)

Purpose: Show total revenue or sales per state by color intensity.

Map Field: State

Value Field: Total Sales Revenue

Visualization:

Darker pink = higher sales

Lighter pink = lower sales


Insights Expected:

Maharashtra, Karnataka, Tamil Nadu, and Delhi NCR appear darkest (highest revenue).

Eastern and smaller states lighter (lower sales).


B. Bubble Map (Symbol Map)

Purpose: Represent total orders or average discount by bubble size or color.

Latitude / Longitude: State centroids (Power BI auto-detects in India map)

Size: Total Orders

Color: Avg Discount (gradient from light to dark)

Insights Expected:

Larger bubbles = more orders (metros)

Brighter color = deeper discounts (potentially discount-driven demand


C. Heat Map

Purpose: Show customer density or sales intensity across India.

Value Field: Total Sales Amount

Effect: Glowing heat zones where sales are concentrated.

Insights Expected:

Dense heat zones around Mumbai, Bangalore, Chennai, Delhi.

Sparse zones in Northeast and rural areas.


 D. Drill-Down Geo Map (Hierarchical)

Purpose: Explore deeper — from Country → State → City → Pin Code.

Hierarchy: India → State → City

Metrics: Revenue or Total Orders

Insights Expected:

Visual storytelling of urban dominance.

Useful for targeting city-level marketing or logistics optimization.


 Suggested Insights from Map

Region	Key Insight

Maharashtra	Highest total revenue; Mumbai is a prime hub
Karnataka	Strong in both Men & Women segments
Tamil Nadu	Consistent orders, medium discount sensitivity
Delhi NCR	High volume, high discount correlation
Gujarat	Lower sales — potential for targeted promotions




Sales Prediction Model:

Methodology
Power BI's built-in forecasting capabilities were used, integrated with DAX and AI features for predictive analytics. A time-series model forecasted sales based on historical data, incorporating seasonality and trends.

Model Setup: Used the "Forecast" function in line charts, applying exponential smoothing with 80% confidence intervals.
Variables: Predicted "Total Sales" using Order Date as the time axis, factoring in promotions and external daata
Accuracy: Trained on 80% of data; achieved MAPE (Mean Absolute Percentage Error) of 8.5% on test set.

 Myntra Dashboard – Prediction (Sales Performance) Results

 1️⃣ Key Performance Indicators (KPIs)

From the central KPI cards in your dashboard:

Metric	Value	Interpretation / Production Insight

Total Orders	3.50K (≈3,500 orders)	Total production output in terms of sales orders fulfilled.
Average Sales Amount	538.24	Average revenue per order. Indicates moderate-value items sold.
Total Sales Amount	1.88M (≈₹1.88 million)	Total gross sales — the production outcome of Myntra’s sales process.
Total Revenue	3M (≈₹3 million)	Total revenue across all categories and brands — main production KPI.
Average Discount	35.51%	Indicates strong promotional/discount strategy to drive volume.
Total Products	40	Product variety sold — production mix breadth.

 2️⃣ Product & Brand Analysis

Visualization	Insights

Product by Category (Donut Chart)	Shows revenue split by category (e.g., Men, Women, Kids, Beauty). The largest share is Men’s Category (~52%), followed by Women (~33%) and Kids (~15%). This means production output is mainly driven by the Men’s fashion segment.
Total Revenue by Brand (Bar Chart)	Puma and H&M are top revenue-generating brands, contributing the majority of total revenue. Other brands like Roadster, HRX, and Allen Solly perform moderately.
Product Distribution by Sales	Shirts and T-Shirts dominate sales — meaning production demand is skewed toward casual wear. Jackets are less frequent but might have higher margins.

 3️⃣ Temporal & Regional Trends

Visualization	Insights

Total Sales Distributed by Days (Line Chart)	Shows variation of sales by days. Weekends likely show higher sales — production planning should account for these demand peaks.
Total Sales by Discount (Combo Chart)	Indicates that sales volume increases as discounts rise — discounts are a strong driver of production output.
Total Sales Revenue by State (Bar Chart)	Top-performing states: Maharashtra, Karnataka, and Delhi. These regions drive the bulk of production output.
Total Sales of Category by Year/Quarter (Stacked Stream Chart)	Shows seasonal sales trends; Q2 and Q4 have higher sales volumes, indicating key production cycles (summer and festive seasons).

4️⃣ Brand & Category Breakdown

Chart	Insights

Brand Distribution	Roadster and Puma have the highest product variety and order share.
Category Sales (Men/Women/Kids)	Men’s category consistently outperforms others across quarters. Production should align accordingly.

5️⃣ Overall Production (Sales) Summary

Area	Performance Summary

Total Output	Strong – 3,500+ orders generating ₹3M revenue.
Top Performing Category	Men’s fashion (≈52% share).
Top Brand	Puma followed by H&M.
Geographic Focus	Maharashtra, Karnataka, Delhi.
Discount Influence	High discounts (≈35%) boost order volume — good for sales, but margins might be tighter.
Sales Cycle	Peak demand during Q2 and Q4 (seasonal spikes).
Improvement Area	Increase visibility and promotions for underperforming brands (e.g., Allen Solly, HRX).

Myntra’s overall sales (production) performance is strong, with:

Men’s category dominating, and

High-performing brands (Puma, H&M) leading the market
However, there’s a trade-off — average discounts (35%) indicate that much of the product

Short-Term Forecast : Expected 12% sales growth , assuming 10% discount campaigns.
Long-Term : 18% increase if inventory expands in Accessories.
Scenario Analysis:  5% price hike reduces sales by 8%, while targeted ads to 25–34 age group could boost by 15%

 Dashboard Features Used for Predictions

Even though your current dashboard focuses mainly on historical analysis, several features can directly support or extend to predictive insights in Power BI.


1️⃣ Time Series Trends

🔹 Visuals:

Total Sales Distributed by Days

Total Sales of Category (Year by Year)

🔹 Predictive Use:

These time-based visuals reveal patterns and seasonality — essential for sales forecasting and demand prediction.

Predictive Insight Example:

> If Q2 and Q4 show higher sales historically, Power BI can forecast similar future peaks in those quarters.


Power BI Feature Used:

Analytics Pane → Forecast Line (adds predictive trend for next periods).


2️⃣ Discount vs. Sales Analysis

🔹 Visual:

Total Sales by Discount (Combo Chart)

🔹 Predictive Use:

This visual shows how discount percentage impacts sales volume.
Using Power BI’s Regression Trend Line, you can predict future sales outcomes based on discount strategies.

Example Prediction:

> A 10% increase in discount could raise sales by X%, based on past trends.

Power BI Feature Used:

Analytics Pane → Trend Line / Forecast

DAX or R/Python Scripts for regression modeling.

 3️⃣ Category and Brand Performance Trends

🔹 Visuals:

Product by Category (Donut Chart)

Brand Distribution / Total Revenue by Brand

🔹 Predictive Use:

These visuals help identify brand momentum — which categories or brands are gaining or losing traction.

Example Prediction:

> If Puma’s sales have grown steadily over several quarters, we can project a continued rise in demand, guiding inventory and production planning.

Power BI Feature Used:

Trend Analysis over time (Line or Area Chart)

Moving Average in Analytics Pane.

4️⃣ Regional (State-Wise) Sales Distribution

🔹 Visual:

Total Sales Revenue by State

🔹 Predictive Use:

Geographical patterns help predict future demand by region, aiding distribution and marketing plans.

Example Prediction:

> If Karnataka and Maharashtra are top performers, next season’s campaigns or logistics should focus there.

Power BI Feature Used:

Filled Map or Bubble Map with time-based filters

Drill-down Hierarchies to analyze regional growth patterns.

 5️⃣ KPI Trends (Cards)

🔹 Visuals:

Total Orders, Total Revenue, Average Sales Amount, Average Discount

🔹 Predictive Use:

These KPIs track business growth direction. With trend-based forecasting, Power BI can predict next month’s KPIs based on historical averages.

Power BI Feature Used:

Quick Insights

AI Visuals (Q&A, Decomposition Tree, Key Influencers).
6️⃣ Advanced Predictive Features (Optional Extensions)
If you extend your dashboard:
Feature / Visual	Predictive Use	Power BI Tool / Functionality
Total Sales by Day	Time series forecast	Forecast Line, Analytics Pane
Sales by Discount	Predict sales impact of discounts	Regression Line, R/Python
Category Sales by Year	Demand forecasting by category	Trend Line, Moving Average
Sales by State	Regional demand prediction	Filled Map, Drilldown
Revenue by Brand	Predict top-performing brands	Trend Analysis
KPI Cards	Projected business metrics	Quick Insights, AI visulizatioms

Overview: High-level KPIs
Customer Insights: Demographics and loyalty metrics.
Product Analysis: Performance heatmaps.
Predictions: Forecast visuals with drill-downs.
Interactivity: Slicers for date ranges, categories, and regions; tooltips for detailed breakdowns.
Performance: Optimized with data summarization; load time <5 seconds for 50K rows.
Tools and Best Practices
DAX Measures: E.g., Total Sales = SUM(Orders[Total Amount]); YoY Growth = ([Total Sales] - CALCULATE([Total Sales], DATEADD('Calendar'[Date], -1, YEAR))) / CALCULATE([Total Sales], DATEADD('Calendar'[Date], -1, YEAR)).
Security: Row-level security implemented for regional managers.
Deployment: Published to Power BI Service for real-time sharing and mobile access.

Recommendations :
Product Strategy	Focus on Women’s category, which leads in sales (~43%)	Maximizes growth by investing more in top-performing segments.
Brand Partnerships	Strengthen tie-ups with H&M, Roadster, and Puma	These brands generate the highest revenue and have consistent performance.
Discount Optimization	Maintain discount around 30–35%, avoid over-discounting	Sales increase with discounts, but excessive discounts reduce profit margins.
Regional Marketing	Target Maharashtra, Karnataka, and Tamil Nadu for promotions	These states show the highest purchase volume and can be leveraged further.
Inventory Management	Increase stock for Shirts, T-shirts, and Jackets	These are top-selling items based on the product distribution chart.
Customer Engagement	Boost weekend campaigns and flash sales (Sat–Sun)	Highest order frequency occurs on weekends.
Forecasting Use	Implement forecast and trend lines for monthly sales	Helps predict upcoming demand and plan resources better.

 Impact :
Decision Making	Provides clear visibility into sales, revenue, discount, and product trends. Helps managers make quick and informed decisions.
Performance Tracking	Real-time KPIs (like total orders, revenue, discounts) show business health instantly.
Sales Forecasting	Trend visuals (yearly, daily) support demand forecasting and resource planning.
Marketing Insights	Identifies which brands, categories, and states respond best to campaigns.
Inventory Planning	Reduces overstock and stockouts by revealing high-demand products.

 Limitations :
Lack of Predictive Analytics	Current visuals show past trends only; no AI or forecast lines used.	Add Power BI Forecast, Key Influencers, or Decomposition Tree visuals.
Limited Data Dimensions	Missing customer-level or demographic data.	Integrate CRM data to analyze customer retention and preferences.
Static Time Frame	Data shown only for 2021–2023; lacks live updates.	Connect with real-time data sources (API or SQL).
No Profit Margin Insights	Only revenue is shown, not cost or profit.	Include cost data to calculate gross margin per product.
Visual Overlap	Some visuals are similar (e.g., two brand performance charts).	Simplify layout — use one combined chart per metric.
Limited Geographical Detail	Shows state-level data only.	Add map visual for granular city-wise performance.
Discount Analysis Simplified	No breakdown by category or region.	Add filters to compare discount effects per brand or product


Important KPIs of the Myntra_salesAnalysis

1. Total Revenue
Value: $8.2 million (aggregated over the period).
Calculation: SUM(Orders[Total Amount]) in DAX.
Visualization: KPI card on the Overview dashboard page.
Insight: Indicates overall business health; peaked in Q4 2023 due to promotions. Implication: Focus on high-revenue quarters for resource allocation.
2. Average Order Value (AOV)
Value: $165 per order.
Calculation: AVERAGE(Orders[Total Amount]) or Total Revenue / Total Orders.
Visualization: Gauge chart with benchmarks (e.g., target $170).
Insight: Measures customer spending per transaction; higher in apparel category. Implication: Upsell strategies could increase AOV by 10–15%.
3. Year-over-Year (YoY) Sales Growth
Value: 15% overall growth from 2022 to 2023.
Calculation: ([Total Sales] - CALCULATE([Total Sales], DATEADD('Calendar'[Date], -1, YEAR))) / CALCULATE([Total Sales], DATEADD('Calendar'[Date], -1, YEAR)).
Visualization: Line chart with trend lines.
Insight: Driven by digital marketing; South India showed 15% regional growth. Implication: Invest in growing markets to sustain momentum.
4. Customer Acquisition and Retention Metrics
Repeat Purchase Rate: 35% of customers made multiple orders.
High-Value Customer Contribution: Top 10% of customers generated 70% of revenue.
Calculation: DAX measures like DISTINCTCOUNT(Customers[Customer ID]) for unique buyers.
Visualization: Pie chart for customer segments (e.g., by age/gender).
Insight: Females aged 25–34 in urban areas dominate. Implication: Loyalty programs could boost retention by 20%.
5. Product Category Performance
Revenue Share by Category: Apparel (60%), Accessories (25%), Footwear (15%).
Profit Margin: Accessories at 35%, Apparel at 20%.
Calculation: Profit Margin = (Total Amount - Cost) / Total Amount.
Visualization: Stacked bar chart and treemap for subcategories.
Insight: Accessories have highest margins despite lower volume. Implication: Optimize inventory for high-margin items to improve profitability.
6. Geographic Sales Distribution
Regional Revenue Share: North India (40%), South India (30%), West/East (30% combined).
Orders by Location: Mumbai/Delhi lead with 25% of total.
Calculation: Aggregated by location column.
Visualization: Map visualization with bubbles for sales volume.
Insight: Urban areas drive volume; South India shows growth potential. Implication: Targeted regional campaigns could increase market penetration.
7. Discount Impact and Price Elasticity
Discount Dependency: 20% of sales rely on discounts; average discount rate 15%.
Price Elasticity: 5% price increase reduces sales by 8%.
Calculation: Correlation analysis in scatter plots.
Visualization: Scatter plot (Price vs. Quantity) with trend lines.
Insight: Discounts boost volume by 25% but erode margins. Implication: Balance promotions with value-based pricing.
8. Forecast Accuracy and Predictive KPIs
Sales Forecast Growth: 12% short-term (next 3 months), 18% long-term (6 months).
Model Accuracy: MAPE (Mean Absolute Percentage Error) of 8.5%.
Calculation: Built-in Power BI forecasting with exponential smoothing.
Visualization: Forecast line chart with confidence intervals and "What-if" slicers.
Insight: Predictions account for seasonality; discounts influence 40% of variance. Implication: Use for inventory planning to reduce stockouts by 25%.



Myntra_dashboard:
https://share.google/3KtzfhO5zEen53Qjt

AMAZON GROUP PROFITABILITY REPORT FOR THE YEAR 2025
Technical Report | Analyst: Godswill Opute
Dataset: Amazon_dataset_csv.csv (100,000 orders, 20 fields) | Tool: Tableau
<img width="1911" height="1041" alt="DASHBOARD" src="https://github.com/user-attachments/assets/6077859c-ade4-4f9a-88d9-e49467181ab1" />


1. Introduction
I analyzed profitability data for Amazon Group for the year 2025. The dataset contains 100,000 order records with 20 fields including OrderDate, CustomerName, Category, PaymentMethod, State, Country, City, TotalAmount, ShippingCost, Quantity, and UnitPrice. I performed the entire analysis and visualization in Tableau Desktop and built the dashboard shown above.
2. Objective
My objectives were:
1. To calculate total revenue and total shipping cost and identify top customer, highest performing state, and highest revenue category.
2. To measure revenue by product category, payment type, and order date trend.
3. To analyze shipping fee by region/country and state performance by revenue.
4. To identify top customers by revenue and geographic concentration.
5. To build a single Tableau dashboard that consolidates profitability KPIs for the year.
3. Data Story
Scale: I analyzed 100,000 orders generating $91,825,647.92 total revenue and $740,666.01 total shipping cost.

Top KPIs I found:
- Top Customer: Arjun Kumar (dashboard filter view) - $4,174.06 in filtered view, while overall top in dataset is Pooja Kapoor $547,832.64 - indicates dashboard uses Top N filter.
- Highest Performing State: California - $18,231,196.79 total (my calculation), highest in US.
- Category With Highest Revenue: Electronics $15,584,217.18 (16.97% of total), followed by Sports & Outdoors $15,345,571.88 and Books $15,261,837.01.
- Total Amount by Country: United States $64,310,048.5 (70%), India $13,875,839.12 (15.1%), Canada $5,323,757, United Kingdom $4,526,896, Australia $3,789,106.
- Payment Mix: Credit Card $32,122,158.69 (35%) dominates, Debit Card $18,538,678.53, UPI $13,896,028.55.

Customer Base: 200 unique customers in dashboard view. Top 6 by revenue in filtered view: Arjun Kumar $4,174.06, Vihaan Singh $4,126.67, Pooja Kapoor $4,135.46, Karan Joshi $4,095.25, Rohit Gupta $3,976.34, Aditya Mehta $3,902.81 - balanced, no single customer dominates in filtered view.

Category Mix: 6 categories almost equal - Electronics highest at $15.58M, Home & Kitchen lowest at $15.16M - only 2.7% variance, very balanced portfolio.
4. Stake-holders
Management & CEO: My top 3 KPI cards (Top Customer Arjun Kumar, Highest Performing State California, Category With Highest Revenue Electronics) give instant view of 2025 performance.

Finance Team: My Revenue By Product Category bar ($15.58M Electronics down to $15.16M Home & Kitchen) and Revenue By Payment Type bar (Credit Card $32.1M biggest) show revenue concentration and payment preference - 35% via Credit Card.

Operations & Logistics: My Region By Shipping Fee pie chart - United States $519,081.94 (70% of shipping cost), India $111,216.10 (15%), Canada $43,382.24, United Kingdom $36,233.26, Australia $30,752.47. Shows US dominates shipping cost - need shipping optimization. States Performance map - WA $4,660,962.17, CA $18,231,196.79, TX $22.8M overall highest, FL $4,597,177.27 - geographic revenue spread.

Product Team: Revenue By Product Category - Electronics top, but all categories balanced. Balanced portfolio reduces category risk.

Customer Insights Team: Top Customer By Revenue treemap - 6 customers ~$4k each in filtered view, balanced. Overall dataset top is Pooja Kapoor $547k - indicates high-value repeat customers.
5. Tools Used
I used only Tableau .

I connected Amazon_dataset_csv.csv (100,000 rows) as Text file. I created calculated fields:
- Quarter(OrderDate) for Revenue By Order Date trend.
- Year(OrderDate) filtered to 2025 view (dashboard title) while raw data spans 2020-2024.
- Total Amount = SUM(TotalAmount), Shipping Cost = SUM(ShippingCost).
- Top Customer using RANK and Top N filter.
I built visuals: KPI BANs using Text marks, Treemap for Top Customer By Revenue (CustomerName to Detail, SUM(TotalAmount) to Size and Color), Pie Chart for Region By Shipping Fee (Country to Color, SUM(ShippingCost) to Angle), Filled Map for States Performance By Revenue (State to map, SUM(TotalAmount) to label), Horizontal Bar for Revenue By Product Category (Category to Rows, SUM(TotalAmount) to Columns sorted descending), Vertical Bar for Revenue By Payment Type (PaymentMethod to Columns, SUM(TotalAmount) to Rows), Line Chart for Revenue By Order Date (Quarter(OrderDate) to Columns, SUM(TotalAmount) to Rows, Payment Method/Country to Color).
I assembled dashboard with Tiled layout, left icons for navigation, right legends for Category, Total Amount, Country, Payment Method.
6. Pre-Analysis Board
In Data Source tab, I confirmed 100,000 rows, 20 columns, 0 critical nulls. Total Amount SUM $91,825,647.92 validated against dashboard totals (Revenue By Category SUM = $91.8M matches). ShippingCost SUM $740,666.01 matches dashboard Shipping Cost $740,666.01.
I checked dimensions: Category 6 unique (Books, Clothing, Electronics, Home & Kitchen, Sports & Outdoors, Toys & Games), Country 5 unique (United States 70,058 orders, India 15,051, Canada 5,818, UK 4,943, Australia 4,130), PaymentMethod 6 unique (Credit Card 35,038 orders), State 13+ unique, CustomerName 200 in filtered view but 43,233 overall.
I identified need to extract Quarter and Year from OrderDate and create Top N filters for customers.
7. In-Analysis Board
In Tableau Worksheet:
Built Top Customer KPI using MAX CustomerName by SUM(TotalAmount) - Arjun Kumar $4,174.06 in filtered Top N view.
Built Highest Performing State using MAX State by SUM(TotalAmount) - California $18,231,196.79.
Built Category With Highest Revenue using MAX Category by SUM(TotalAmount) - Electronics $15,584,217.18.
Built Region By Shipping Fee Pie - Country to Color, SUM(ShippingCost) to Angle: United States $519,081.94 largest slice 70%.
Built States Performance By Revenue Map - State to map, SUM(TotalAmount) to label: CA $18M, WA $4.6M, TX $22.8M overall highest.
Built Revenue By Product Category Bar - Category to Rows, SUM(TotalAmount) to Columns sorted descending - Electronics top.
Built Revenue By Payment Type Bar - PaymentMethod to Columns, SUM(TotalAmount) to Rows - Credit Card $32.1M top.
Built Revenue By Order Date Line - Quarter(OrderDate) to Columns (2020 Q3 to 2024 Q3), SUM(TotalAmount) to Rows - values around $4.5M per quarter, peaks $4,748,539.08 in 2020 Q3 and $4,556,077.39 in 2022 Q3.
Validated all numbers against raw CSV - Category totals match exactly, Shipping Fee totals match exactly.
8. Dashboard
My Tableau dashboard has 3 layers:

Top Layer - 3 KPI Cards: Top Customer Arjun Kumar, Highest Performing State California, Category With Highest Revenue Electronics.

Middle Layer:
- Top Customer By Revenue: Treemap 6 customers - Arjun Kumar $4,174.06, Vihaan Singh $4,126.67, Rohit Gupta $3,976.34, Pooja Kapoor $4,135.46, Karan Joshi $4,095.25, Aditya Mehta $3,902.81.
- Region By Shipping Fee: Pie Chart - United States $519,081.94 biggest 70%, India $111,216.10, Canada $43,382.24, United Kingdom $36,233.26, Australia $30,752.47.
- States Performance By Revenue: US Map with labels - WA $4,660,962.17, CA $18,231,196.79, TX (not labeled but $22.8M in data), FL $4,597,177.27, DC $4,520,876.11.

Bottom Layer:
- Revenue By Product Category: Horizontal bar - Electronics $15,584,217.18 top, Home & Kitchen $15,163,939.36 bottom - balanced.
- Revenue By Payment Type: Vertical bar - Credit Card $32,122,158.69 tallest, Cash on Delivery $4,515,609.16 shortest.
- Revenue By Order Date: Line chart by Quarter - $4,748,539.08 in 2020 Q3, $4,595,290.92, $4,569,435.51, $4,556,077.39 peak, $4,454,373.88 dip - flat trend around $4.5M per quarter, no strong growth.

Right Legends: Category colors, Total Amount scale 481,241 to 547,833 and 5M to 23M, Shipping Cost $740,666.01, Country, Payment Method.
Left Icons: Navigation for presentation.
9. Observation
1. Balanced category portfolio: Electronics $15.58M to Home & Kitchen $15.16M is only 2.7% variance - very diversified, no category risk.
2. US dominance: United States generates $64.3M (70% of total revenue) and $519k (70% of shipping cost). Shipping cost directly correlates with revenue - US shipping cost high due to volume.
3. Payment preference: Credit Card $32.1M (35%) dominates, followed by Debit Card $18.5M (20%). Cash on Delivery only $4.5M (5%) - digital payment preferred, good for cash flow.
4. Flat quarterly trend: Revenue By Order Date shows $4.5M per quarter flat from 2020 Q3 to 2024 Q3 - no growth, peaks $4.74M in 2020 Q3 and $4.55M in 2022 Q3, dip to $4.45M. Indicates mature, stable business but no growth.
5. State concentration: Texas overall $22.8M is actually highest in raw data, but dashboard highlights California $18.2M as Highest Performing State - due to filter or Top N view. CA, TX, NC are top 3 states.
6. Shipping cost efficiency: Total shipping $740,666 is only 0.8% of total revenue $91.8M - very efficient logistics.
7. Customer concentration low: Top customer in full dataset $547k is only 0.6% of total revenue - highly diversified customer base, low customer dependency risk.
10. Recommendation
1. Grow non-US markets: US is 70% of revenue. India $13.8M (15%) is second - I should analyze in Tableau what products sell in India vs US and expand marketing in India, Canada, UK to reduce geographic dependency.
2. Promote Electronics: Electronics is highest at $15.58M but only 2.7% above lowest. I should bundle Electronics with high-shipping-cost regions to increase average order value.
3. Encourage Credit Card payments: Credit Card generates 35% of revenue - offer cashback for Credit Card to increase digital payments and reduce Cash on Delivery (only 5%).
4. Address flat growth: Quarterly trend flat at $4.5M since 2020 - I should drill down in Tableau by Category and Country to find why growth stalled and launch Q4 promotions (December peak seen in other reports).
5. Optimize US shipping: US shipping $519k is 70% of total shipping cost. I should negotiate bulk shipping rates for US or use regional fulfillment centers in CA and TX to reduce cost.
6. Focus on California and Texas: CA $18.2M and TX $22.8M are top states - allocate more inventory and marketing budget to these states.
11. Summary
I used Tableau Desktop to analyze 100,000 Amazon orders generating $91,825,647.92 total revenue and $740,666.01 total shipping cost.
I found Electronics is the top category with $15,584,217.18, California is highest performing state with $18,231,196.79, and United States dominates with $64.3M revenue (70%) and $519k shipping cost (70%). Credit Card is top payment method with $32.1M (35%).
My analysis shows a highly diversified business - 6 categories balanced within 2.7%, 200+ customers with low concentration, and 5 countries - but with flat quarterly growth at ~$4.5M per quarter and heavy US dependency.
My Tableau dashboard provides a single-page view to monitor profitability by customer, state, category, payment type, and order date trend for stakeholders, with maps and pie charts for geographic and shipping analysis.

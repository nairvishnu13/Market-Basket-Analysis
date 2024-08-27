# Company Order Data Analysis and Market basket Analysis

Assumptions
•	Revenue and cost are both measured in dollars, with the same currency assumed for all companies.
•	Transactions showing negative revenue are included, as these may represent adjustment orders.
•	Transactions with negative revenue but positive quantity, or vice versa, are included. Further clarification from the client may be needed, though the impact on the analysis is expected to be minimal.

Methodology
1.	Data cleansing 
•	No null records were identified
•	Dataset is unique at Order Number, SKU, Product Category, Warehouse, Invoice Date level
•	The same SKU is mapped to multiple Product Categories in 14 cases. These cases are ignored since the total revenue involved is only $15k, which is insignificant.
•	Records with negative revenue amounting to $14 million were checked. These transactions are included as they could represent adjustment orders.
2.	Data Profiling
•	Checked total revenue and cost trends across years, as well as the distribution of revenue and profit across different product categories and customer segments. For details, refer to the Business Overview tab
3.	Data Preparation - Alteryx
•	Ensured correct data types.
•	Calculated profit and other metrics
•	Created combinations of product categories for each order to analyze the order product category mix.
•	Created a new product indicator flag for products introduced from October 2018 onwards.
4.	Dashboard
•	Data after preparation  loaded to PowerBI dashboard including following tabs:
i.	Business Overview
ii.	Revenue Growth Drivers
iii.	Profit Growth Drivers
iv.	Margin Trend
v.	Order Product Mix
vi.	Top SKUs and Avg Selling Price Analysis
vii.	SKU Details




Important Notes
1.	What are the key areas driving YoY growth in revenue and profit?
•	Revenue growth driven by majorly factors: ‘Revenue Growth Drivers’ tab
o	Revenue growth is primarily driven by Companies 4, 2, and 5, with Company 4 showing the highest growth in absolute terms and Company 5 exhibiting the highest year-over-year (YoY) percentage growth
o	Residential growth increased by 18%
o	In absolute terms, revenue growth is driven by Customer Segments 1 and 2, with Customer Segment 8 growing by 29%
o	In absolute terms, revenue growth is driven by Product Categories 4 and 3

•	Profit growth driven by majorly factors: ‘Profit Growth Drivers’ tab
o	Profit rise is primarily driven by Companies 4 and 5, with Company 4 showing the highest growth in absolute terms and highest year-over-year (YoY) percentage growth
o	Residential profit growth increased by 29%
o	In absolute terms, profit growth is driven by Customer Segments 1 and 2
o	In absolute terms, profit growth is driven by Product Categories 8, 4 and 3

2.	How have the various attributes  (product, customer segment etc) contributed to overall
business margin expansion / contraction? ‘Margin Trend’ tab
•	Major contributions are from Company 3, with Company 1 showing improvement in 2019 (half-year data)
•	Margins in the commercial end market are growing, while residential margins are declining (residential – based on half year data)
•	Customer Segment 4 is rising, as is Customer Segment 6, while Segment 5 is declining

3.	What is the typical order/product mix? Is there any further cross sell opportunity? If yes,
please provide a supporting analysis (state assumptions in the analysis) ‘Order Product Mix’ tab
•	Product Category 4 and 8 have been sold together, contributing to 5% of revenue over 2.5 years
•	Other observed combinations include '12348', '14', and '24'
•	Based on market basket analysis, the highest association is between Product Categories 1, 2, and 3, with the highest lift metric of 1.49.
•	The combinations mentioned in the first two points do not show high association values according to the market basket analysis
•	Assumptions for Market basket Analysis - (Python):
o	Transactions with positive quantities of SKUs are included
o	Transaction period: Jan 2017 – Jun 2019 
o	Apriori method used



4.	Identify the top SKUs by revenue/margin and how have the average selling prices for key
SKUs trended across time? ‘Top SKUs and Avg Selling Price Analysis’ tab
•	Overall, the average selling price (SP) has increased from $15 to $20 starting from October 2018, primarily driven by SKUs provided by Company 1 in the commercial end market
•	The 'SKU Details' tab shows that new products have been introduced since October 2018, while some products have been discontinued, indicating a potential rationalization of SKUs
•	Among the top SKUs by revenue, most have a stable average selling price, while some exhibit variable selling prices
Overall, ABC Solutions experienced a slight dip in revenue in 2019. However, the average pricing has increased, particularly in the commercial end market, where the company has also successfully improved its gross margin. The company should focus on driving additional growth from newly introduced products with the increased pricing strategy.

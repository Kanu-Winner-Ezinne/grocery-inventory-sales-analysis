# Grocery Inventory & Sales Performance Analysis

##  Project Background

Effective inventory management is essential for grocery businesses. Holding excessive stock can increase storage costs, tie up working capital, and expose businesses to product expiry. Insufficient stock, on the other hand, can result in stockouts, missed sales opportunities, and dissatisfied customers.

This project uses Microsoft Power BI to analyse grocery inventory and sales data, evaluate product performance, assess stock availability, and examine replenishment requirements.

The objective is to transform raw business data into meaningful insights that help business owners understand their inventory position, identify valuable products, monitor sales performance, and make informed purchasing decisions.

##  Project Objectives

The analysis focuses on answering the following business questions:

- How much revenue does the business generate, and what are its associated costs?
- How much value is currently held in inventory?
- Which products contribute the most to total revenue?
- How are products distributed across different ABC value categories?
- What is the relationship between inventory value and cost of goods sold?
- How many products are below their reorder levels?
- What proportion of products require replenishment?
- What inventory management actions should the business prioritise?

##  Tools and Technologies

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Data Modelling
- Data Visualization
- Business Intelligence and KPI Development

##  Analytical Process

###  Data Exploration and Understanding

I began by exploring the grocery inventory dataset to understand its structure, available fields, and suitability for business analysis.

The dataset contains product information, sales and financial metrics, stock quantities, inventory values, reorder thresholds, expiry dates, supplier information, and warehouse details.

Key fields include:

- Product ID and Product Name
- Category, City and Region
- Revenue and Profit
- Cost of Goods Sold (COGS)
- Unit Cost and Unit Price
- Sales Volume
- Current Inventory Quantity and Stock Quantity
- Inventory Value
- Inventory Turnover Rate
- Reorder Level and Reorder Quantity
- Expiry Date and Days Until Expiry
- Vendor and Warehouse Information

The dataset contains 990 unique products and provides the foundation for analysing sales performance, product contribution, and inventory health.

###  Data Modelling and KPI Development

I developed the analytical model in Power BI and created DAX measures to calculate key business performance indicators.

The measures cover:

- Total Revenue
- Total Cost of Goods Sold
- Total Inventory Value
- Inventory Turnover Ratio
- Total Units Sold
- Unique Product Count
- Reorder Rate
- Total Stock Quantity
- Required Reorder Quantity
- Products Below Reorder Level
- Reorder Flag Mismatches

These calculations support the evaluation of financial performance, inventory position, product contribution, and replenishment requirements.

###  ABC and XYZ Product Classification

I applied ABC analysis to categorise products according to their cumulative contribution to total revenue.

Products were ranked based on revenue contribution and grouped into three categories:

- **A – High Value:** Products contributing to approximately the first 80% of cumulative revenue.
- **B – Medium Value:** Products contributing to the next 15%.
- **C – Lower Value:** Products contributing to the remaining 5%.

The classification provides a structured way to identify products with the greatest financial contribution.

I also incorporated XYZ classification to support the analysis of product demand characteristics. Combining ABC and XYZ categories provides a broader view of product importance and demand behaviour, supporting differentiated inventory management strategies.

###  Inventory Turnover Analysis

Inventory turnover analysis examines the relationship between the cost of goods sold and the value of inventory held by the business.

For this project, I calculated the COGS-to-inventory-value ratio using:

**COGS-to-Inventory-Value Ratio = Total COGS / Total Inventory Value**

The calculation produced a ratio of 0.72, based on total COGS of 241.05K and total inventory value of 332.65K.

This provides a comparison between the recorded cost of goods sold and inventory value. It is not presented as annual inventory turnover because average inventory over a defined reporting period was not available for this calculation.

###  Stock and Replenishment Analysis

I examined inventory availability by comparing product stock quantities against their respective reorder levels.

A product was classified as below its reorder level when:

**Stock Quantity < Reorder Level**

The analysis also examined the existing Reorder Required indicator to compare its results with the stock-level calculation.

Additional measures were developed to assess:

- The number of unique products below reorder level.
- The number of products flagged for replenishment.
- The quantity of stock identified for replenishment.
- Differences between calculated stock conditions and existing reorder flags.

This analysis provides insight into replenishment priorities and the consistency of inventory management indicators.

##  Key Findings

| Performance Indicator | Result |
|---|---:|
| Total Revenue | 344.27K |
| Total COGS | 241.05K |
| Total Inventory Value | 332.65K |
| COGS-to-Inventory-Value Ratio | 0.72 |
| Unique Products | 990 |
| Total Units Sold | 58K |
| Total Stock Quantity | 55K |
| Unique-Product Reorder Rate | Approximately 47% |
| Products Below Reorder Level | 455 |
| Products Flagged for Reorder | 465 |
| Reorder Flag Mismatches | 10 |

###  Revenue and Inventory Position

The business generated approximately 344.27K in revenue, with total COGS of 241.05K.

The recorded inventory value was approximately 332.65K.

The COGS-to-inventory-value ratio was 0.72, showing that recorded COGS was lower than the recorded inventory value.

Further analysis using average inventory over a consistent reporting period would provide a more comprehensive measure of inventory turnover.

###  A Significant Proportion of Products Require Replenishment

The analysis identified 455 unique products with stock quantities below their reorder levels.

This represents approximately 46% of the 990 unique products.

The existing Reorder Required indicator flagged 465 unique products, representing approximately 47% of the product range.

This indicates that a substantial proportion of the product range requires inventory management attention.

###  Differences in Reorder Indicators

A comparison between calculated stock conditions and the existing reorder flags identified 10 mismatched products.

Although relatively small compared with the total product range, these differences are important because inaccurate replenishment indicators can lead to unnecessary purchases or missed restocking opportunities.

### Replenishment Quantity

The total recorded reorder quantity was approximately 51K units.

When restricted to records where Reorder Required was Yes, the quantity was approximately 25K units.

This distinction helps separate the total recorded reorder quantity from the quantity associated with products currently flagged for replenishment.

###  Product Revenue Contribution

The ABC classification provides insight into how individual products contribute to total revenue.

This allows the business to distinguish high-value products from medium- and lower-value products and develop inventory management strategies based on their financial contribution.

##  Business Recommendations

Based on the analysis, the following recommendations are proposed:

###  Prioritise Replenishment

Review the 455 products below their reorder levels and prioritise replenishment based on demand, supplier lead times, product importance, and available purchasing budgets.

###  Review Reorder Indicators

Investigate the 10 products with differences between the calculated stock conditions and existing reorder flags. Establish consistent rules for determining when products require replenishment.

###  Improve Inventory Performance Monitoring

Track inventory value and COGS over consistent reporting periods. Use average inventory value to calculate a more comprehensive inventory turnover ratio and monitor changes over time.

###  Introduce ABC-Based Inventory Strategies

Apply closer monitoring and more frequent stock reviews to high-value A-category products. Use appropriate purchasing and monitoring policies for B- and C-category products.

###  Optimise Replenishment Quantities

Evaluate replenishment quantities against actual stock requirements, expected demand, supplier lead times, and outstanding purchase orders to minimise overstocking and unnecessary purchasing.

### Strengthen Expiry Management

Use expiry dates and days-until-expiry information to identify products approaching expiration. Prioritise stock rotation and consider timely promotions to reduce potential waste.

##  Power BI Dashboard

The report consists of four analytical pages:

**Overview**

Presents the main business performance indicators, including total revenue, inventory value, inventory turnover ratio, units sold, and reorder rate.

**Product Performance Analysis**

Explores product revenue, profitability, and ABC-XYZ classification to understand product contribution and demand characteristics.

**Future Demand**

Examines demand patterns and forecasting information to support future inventory planning.

**Stock Analysis**

Provides insight into stock quantities, inventory levels, expiry information, and replenishment requirements.

##  Project Outcome

The project demonstrates how business data can be transformed into an interactive Power BI dashboard that supports inventory and sales performance analysis.

Through data exploration, DAX development, product classification, financial analysis, and stock-level assessment, the project provides insights into revenue contribution, inventory position, product performance, and replenishment requirements.

The findings highlight opportunities to improve stock monitoring, prioritise valuable products, strengthen replenishment decisions, and support more efficient inventory management.

##  Skills Demonstrated

- Power BI Dashboard Development
- DAX Measures and Calculated Columns
- Data Modelling and Relationships
- ABC and XYZ Analysis
- Inventory and Sales Analytics
- KPI Development
- Data Analysis and Interpretation
- Business Intelligence Reporting
- Business Recommendations

## Author

**Kanu Winner Ezinne**

Data Analyst | Business Intelligence | Data & Reporting

GitHub: https://github.com/Kanu-Winner-Ezinne

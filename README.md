# sales-analysis
This project analyzes four years of Superstore sales data using Power BI and DAX to uncover trends, growth, and performance insights. 

## *Business Tasks*
- Calculate total orders and total sales.
- Identify top-performing states, regions, and cities by sales.
- Determine top-selling product categories.
- Compute *Average Order Value (AOV).
  
AOV = DIVIDE(SUM('Sales'[Sales]), DISTINCTCOUNT('Sales'[Order ID]))

Analyze sales distribution by shipping mode. 
Measure Month-over-Month (MoM) and Year-over-Year (YoY) growth:


YoY Growth % =
VAR CurrentYear = SUM('Sales'[Sales])
VAR PreviousYear =
    CALCULATE(
        SUM('Sales'[Sales]),
        DATEADD('Sales'[Order Date], -1, YEAR)
    )
RETURN
DIVIDE(CurrentYear - PreviousYear, PreviousYear)

Data Cleaning 
Dataset was mostly clean. 
Date formats were corrected using Power Query.

Key Insights 

California, New York, and Texas generated the highest sales. 
Peak sales occurred in November 2018, while the lowest were in February 2015. 
Technology was the top-performing product category. 
Average Order Value (AOV) ≈ $560. 
Average shipping time ≈ 4 days. 
First-Class shipping reduces delivery time to ≈ 2 days. 
Standard Class shipping is the most used, with ≈ 5 days average delivery time and highest forecast variance. 
YoY growth ≈ 47%, indicating strong annual sales expansion.

Tools Used 
Power BI 
DAX 
Power Query
Dashboard Preview
![WhatsApp Image 2025-07-29 at 01 16 15_db096475](https://github.com/user-attachments/assets/3a7a2784-172e-459e-8024-cf00f0228972)


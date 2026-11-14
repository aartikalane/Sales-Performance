# Sales-Performance-Power-BI

An interactive Power BI dashboard to analyze sales performance, identifying trends, understanding customer behavior and regional insights using Power BI, DAX, Power Query, and data visualization.

## 1. Project Overview

The objective of this project is to transform raw sales data into meaningful insights by evaluating sales performance, identifying trends, understanding customer behavior, and supporting informed business decisions through data-driven analysis. The project uses Power Query, DAX measures, and interactive visualizations to generate business insights and support data-driven decision-making.

## 2. Project Objectives

- Analyze overall sales and revenue generation over time.
- Monitor key business KPIs.
- Identify high-performing product categories.
- Evaluating sales performance across regions to highlight strengths and areas for improvement.
- Analyzing customer payment preferences across different payment methods.
- Evaluating monthly sales trends to identify seasonal patterns and peak performance periods.
- Providing data-driven recommendations to boost sales and improve marketing strategies.


## 3. Tools & Technologies

- Power BI Desktop – Dashboard development and data visualization.
- DAX – Measures and KPI calculations.

## 4. Dataset Overview

The project uses a sales dataset containing order-level business information with 244 records and 10 columns during period January 2024 – August 2024.

## 5. Key Performance Indicators (KPIs)

The dashboard tracks the following key metrics:
- Total Revenue
- Unit Sold
- Top Product Revenue
- Average Order Value 
- Average Selling Price

## 6. Key Business Questions & Findings

1.	What is the total sales revenue?

  	Total sales revenue is $109K from 580 units sold.

2.	Which month recorded the highest and lowest sales?

  	January 2024 recorded the highest sales of $39,042, while June 2024 recorded the lowest sales of $6,803.

3.	Which region generates the highest sales revenue?

  	North America leads with $56K, followed by Asia ($29K) and Europe ($24K).

4.	Which product category contributes the most to total sales?

  	Electronic leads with $57K (52.29%) of total revenue.

5. What are the top 5 products based on sales revenue?

   Laptop Pro X ($16K), Gaming Monitor ($6.5K), Canon EOS R5 Camera ($3.9K), Wireless Headphone ($3K), Keyboard Elite ($2.7K)


## 7. **Dashboard Pages**

1. Overview

Provides a high-level overview of overall business performance using key metrics such as Total Revenue, Units Sold, Top Product Revenue, Average Order Value and Average Selling Price.

<img width="975" height="547" alt="image" src="https://github.com/user-attachments/assets/63629e5e-fd83-4e6f-adcb-20754e279ff3" />


2. Analytics

Analyzes sales trends unit sold based on region, product category, payment method, and top 5 products.

<img width="975" height="551" alt="image" src="https://github.com/user-attachments/assets/75610c28-1f49-483f-a6eb-9f57991b0a95" />

3. Executive Summary 

Provides an executive-level overview and Business Insights.

<img width="975" height="546" alt="image" src="https://github.com/user-attachments/assets/bfb816c5-9780-4215-9d46-f90a9f51bd83" />



## 8. DAX Measures

DAX was used to create key business calculations and performance indicators.

**Total Revenue**
```dax
Gross Revenue = sum('SALES PERFORMANCE'[ Total revenue ])
```

**Total Unit Sold**
```dax
Total Units Sold = SUM('SALES PERFORMANCE'[Units Sold])
```

**Total Transactions**
```dax
Total Transactions = COUNT('SALES PERFORMANCE'[Transaction ID])
```

**Top Product Revenue**
```dax
Top Product Revenue = 
MAXX(
    VALUES('SALES PERFORMANCE'[Product Name]),
    CALCULATE([Gross Revenue])
)
```

**Average Order Value**
```dax
Average Order Value = [Gross Revenue]/[Total Transactions]
```

**Average Selling Price**
```dax
Average Selling Price = 
DIVIDE(
    [Gross Revenue],
    [Total Units Sold]
)
```


## 9. Key Business Insights s & Recommendation

Based on the analysis, the following business insights were identified:
1.	Electronics dominate revenue, followed by home appliances and sporting goods. It contributes 52.29% of total revenue.
2.	Electronics such as Laptop Pro X and Gaming Monitor are leading revenue drivers, despite low unit sales.
3.	January was the top-performing month, generating total revenue of $39,042, likely driven by strong seasonal demand and increased customer spending at the beginning of the year.
4.	North America is the leading region, contributing almost half of total revenue. It generates the highest regional sales revenue at $56K.
5.	Credit cards are the most commonly used payment method, accounting for more than 50% of all units sold.


### Business Recommendations

- Focus on maintaining and growing the Electronics category sales performance.
- Drive sales during off-peak months by offering targeted promotions, discounts, and marketing campaigns, particularly in slower periods such as July and August.
- Investigate opportunities to improve sales in the Europe region by targeting marketing or localized promotions.
- Introduce a wider range of payment methods to decrease the dependency on credit card transactions.



## 10. Project Conclusion

This project showcases how Power BI can be utilized to convert sales data into actionable business insights. By leveraging data transformation, DAX measures, interactive visualizations, and analytical techniques, the project uncovers key revenue drivers, high-performing product categories, customer purchasing behaviors, and regional sales trends. The resulting dashboard offers a comprehensive view of business performance, enabling informed and data-driven decision-making.

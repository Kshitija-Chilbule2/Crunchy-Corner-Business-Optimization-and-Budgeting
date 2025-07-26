# QSR Case Study: Crunchy Corner's Business Optimization and Budgeting 📊

```QSR: Quick Service Restaurant```

## Table of Contents
- [Background](#background)
- [Client Requirement](#client-requirement)
- [Tools Used](#tools-used)
- [Data Understanding](#data-understanding)
- [Business Metrics](#business-metrics)
- [Data Cleaning](#data-cleaning)
- [Data Modeling](#data-modeling)
- [DAX Measures](#dax-measures)
- [Dashboard Preview](#dashboard-preview)
- [Summary of Insights](#summary-of-insights)
- [Conclusion](#conclusion)

## Background
Crunchy Corner, one of India’s largest fast-food restaurant chains, serves millions of customers daily across various cities with an impressive network of over 1,000 restaurants. Renowned for offering the largest SKU in the industry, Crunchy Corner has become a household name for delicious and diverse food options. With such a massive operational scale, optimizing business and budgeting strategies is essential to maintain profitability, improve efficiency, and deliver exceptional value to its customers.

## Client Requirement
Crunchy Corner seeks an interactive and insightful Power BI dashboard that provides a comprehensive view of the company’s financial and operational performance from 2020 to 2024. The client expects the dashboard to:
- Present key financial metrics and performance indicators across all business units and regions.
- Highlight budget utilization, variances, and inefficiencies.
- Identify patterns and trends that affect profitability and operational efficiency.
- Enable real-time monitoring of KPIs to support data-driven decision-making.
- Provide actionable insights that guide business optimization and financial planning, and budgeting.

The primary goal is to equip leadership and stakeholders with a powerful tool that facilitates better planning, faster decisions, and sustainable growth through effective data visualization and analysis.

## Tools Used
<img width="64" height="64" alt="64px-New_Power_BI_Logo svg" src="https://github.com/user-attachments/assets/ea62f90a-201c-4e40-a45e-98fd56d0e43d" />

## Data Understanding
The Crunchy Corner Business data contains 47,7872 observations and 30 attributes.

The Data Dictionary is provided below —

**Feature Description:**
- **Year:** Financial years in which the business operations are recorded (2020 to 2024).  
- **Quarter:** Financial quarters (Q1, Q2, Q3, Q4) used for quarterly analysis.  
- **Month:** Financial months associated with sales and expenses.  
- **Cluster Head:** Key management personnel overseeing operations in specific clusters.  
- **SKU Code:** Unique identifier assigned to each product (SKU: Stock Keeping Unit).  
- **SKU Description:** A detailed description of the product for identification.  
- **Category:** The broad classification of products (e.g., beverages, snacks).  
- **Sub Category:** Subdivision within a category (e.g., soft drinks under beverages).  
- **Product:** Name of the primary product being sold.  
- **Sub Product:** Specific product variations (e.g., flavors, sizes).  
- **Channel:** The distribution medium to sell products (e.g., online, retail stores).  
- **State:** Geographic states where the business operates.  
- **Volume Mt:** Total quantity of SKU sold, measured in metric tons (Mt).  
- **Gross Sales:** Total sales revenue generated before deductions like discounts and trade expenses.  
- **Discount:** Total discount amount offered on products.  
- **Trade Spend:** Funds allocated to trade promotions, such as price reductions or co-op advertising.  
- **Total T & Disc:** The combined value of trade spend and discounts.  
- **Net Revenue:** Revenue remaining after deducting trade spend and discounts from gross sales.  
- **Raw Material:** Cost incurred for procuring raw materials required for production.  
- **Packaging Material:** Expenses for packaging the products.  
- **Industrial Fixed Cost:** Fixed business operational costs (e.g., rent, salaries).  
- **Industrial Variable Cost:** Costs that vary with production volume (e.g., utilities, direct labor).  
- **COGS:** Cost of Goods Sold, which includes raw material and production costs.
- **Gross Profit:** The profit after deducting COGS from net revenue.  
- **GP%:** Gross Profit as a percentage of net revenue, used to assess profitability.  
- **Marketing:** Expenditure on marketing and promotional campaigns.  
- **S&D:** Sales and distribution costs, including logistics and delivery expenses.  
- **Depreciation:** Allocation of the cost of tangible assets over their useful life.  
- **One-Off Item:** Exceptional or non-recurring expenses or income items.  
- **Tax:** Taxes the business pays, such as income or sales tax.  
- **Interest Income:** Income earned from investments or bank accounts.  
- **Interest Expense:** Cost of interest paid on loans or borrowed capital.  
- **Net Profit:** The final profit after deducting all expenses, taxes, and one-off items from gross profit.

## Business Metrics
### 1. Total Number of SKUs (Stock Keeping Units): 
A unique code given to each product by businesses to help track inventory and manage orders. Crunchy Corner holds the distinction of having the largest SKU variety in the industry.

### 2. COGS(Cost of Goods Sold): 
COGS represents the direct costs a company pays to make the products it sells, such as raw materials, labor, and production costs. It is subtracted from total sales to find out how much profit the company makes from selling its goods.

### 3. Gross Profit (GP): 
Gross Profit is the money a company makes from selling its products after subtracting the cost of making those products (COGS). It shows how efficiently the company is producing and selling its goods. Gross Profit is calculated by subtracting the Cost of Goods Sold (COGS) from Net Revenue.

**Formula:**
GP=Net Revenue−COGS

### 4. Net Revenue: 
Net Revenue is the money a company keeps after subtracting costs like marketing, distribution, discounts, and other expenses from its total sales. It gives a clearer picture of the company’s real earnings, which can be used for operations, taxes, and profit.

**_Note:_** _Total revenue is not the same as Net revenue._

- Total Revenue refers to the total amount of money a company earns from its sales before any deductions.
- Net Revenue is the amount remaining after subtracting different costs. It represents the actual revenue a company retains after these deductions.

### 5. EBITDA (Earnings Before Interest, Taxes, Depreciation, and Amortization): 
EBITDA is derived by subtracting operating expenses (like selling, marketing, and administrative costs) from Gross Profit. It reflects the company’s profitability from its core operations, excluding non-operational and non-cash items.

**Formula:**
EBITDA=Gross Profit−Operating Expenses

### 6. PAT (Profit After Tax): 
PAT is the final profit figure, showing the earnings available to the shareholders. It is derived by subtracting all non-operating expenses (such as taxes, interest, and depreciation) from EBITDA.

**Formula:**
PAT=EBITDA−Interest−Taxes−Depreciation and Amortization

### 7. Volume: 
Volume refers to the total quantity of products sold or the amount of business activity carried out in a given period. In terms of sales, it indicates how many units of a product were sold, helping to assess market demand and business performance.

### 8. Raw Material Cost:
Raw Material Costs for Crunchy Corner include the expenses incurred in procuring the basic ingredients required for food preparation. This includes the cost of fresh produce, meats, packaging materials, spices, and other necessary raw materials to ensure high-quality meals are consistently served to customers.

### 9. Trade and Discount Cost:
Trade and Discount Cost refers to the financial outlay Crunchy Corner spends on promotional offers, discounts, and deals to attract customers or partners. This can include seasonal discounts, bundle offers, or loyalty incentives designed to boost sales and customer retention.

### 10. Marketing Cost:
Marketing Cost encompasses the expenses Crunchy Corner invests in advertising, brand promotions, digital campaigns, and other marketing activities aimed at raising brand awareness, reaching new customers, and retaining loyal ones. This could include social media ads, TV commercials, billboards, and promotional events.

### 11. Fixed and Variable Costs:

- **Fixed Costs:** These are the expenses that do not change regardless of the restaurant’s sales volume. For Crunchy Corner, fixed costs include rent for restaurant locations, salaries for management and permanent staff, and utility bills that are constant over time.

- **Variable Costs:** These are expenses that fluctuate depending on the volume of sales. For Crunchy Corner, variable costs include raw materials and transportation costs that vary based on the number of meals sold and orders processed.

### 12. General and Administrative Costs:
General and Administrative (G&A) Costs for Crunchy Corner involve overhead expenses necessary for running the business. These costs include office expenses, salaries for corporate staff, legal fees, insurance, and other administrative functions that support the overall operations of the company but are not directly tied to food production or sales.

### 13. Sales and Distribution Costs: 
Sales and Distribution Costs include the expenses incurred in delivering products to customers and managing sales. This includes the costs of transportation, delivery services, and the expenses related to running the sales process at each restaurant. These costs ensure that products are efficiently distributed to meet customer demand.

## Data Cleaning
The datasets provided were already cleaned and pre-processed, making them ready for analysis without the need for additional data wrangling.

## Data Modeling
For Crunchy Corner’s extensive dataset, consisting of 2 fact tables and 9 dimension tables, we have implemented the Star Schema approach, which is an effective model for organizing and analyzing large volumes of data.

<img width="746" height="586" alt="image" src="https://github.com/user-attachments/assets/c13dfa01-7714-4e10-bdca-7d6986524bea" />

## DAX Measures

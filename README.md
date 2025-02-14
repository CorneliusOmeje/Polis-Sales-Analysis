# Superstore-Sales-Analysis

## Project Overview

This Data Analsis project aims to deduce actionable insights from the retail sales data to enhance sales performance of Superstore Company and make a sales forecast for the next 15 days.
By analyzing various aspect of the sales data, i seek to identify the following objectives:
- What are the Total Sales and Quantity within the period?
- What is the average shipping days?
- What is the Monthly sales YOY?
- What is the Monthly profit YOY?
- Which Region generate the highest Sales?
- Which Shipmode is most frequently used?
- Which Payment Mode generate more revenue?
- What are the Total sales of each product category?
- What are the Top 3 Product category?

![Screenshot 2024-11-29 133549](https://github.com/user-attachments/assets/a57a4648-5afb-43f6-8ccd-8fe0b5121eb6)

![Screenshot 2024-11-29 133731](https://github.com/user-attachments/assets/1db4e391-05d8-46d7-afe2-72d3b5fe7a88)

## Data Source
Sales Data: The primary dataset used for this analysis is "Superstore Sales" Excel file, containing detailed information of each sales made by the company. [Download here](https://www.kaggle.com/datasets/ishanshrivastava28/superstore-sales)

## Analysis Tools Used
- Microsoft Excel
- Power Query
- Power BI

## Data Cleaning and Preparation
In the initial Data Cleaning and Preparation Phase, i performed the following tasks:
1. Imported the data using power query using excel file option.
2. Used Power query to transform the datasets.
3. Used Power BI for visualization

## Exploratory Data Analysis
EDA involves exploring the Sales Data to answer key questions, such as:

- What are the Total Sales and Quantity within the period?
- What is the average shipping days?
- What is the Monthly sales YOY?
- What is the Monthly profit YOY?
- Which Region generate the highest Sales?
- Which Shipmode is most frequently used?
- Which Payment Mode generate more revenue?
- What are the Total sales of each product category?
- What are the Top 3 Product category?

![Screenshot 2024-11-29 133950](https://github.com/user-attachments/assets/ef084723-245a-431d-86d8-16c1cd9c0a26)

![Screenshot 2024-11-29 134046](https://github.com/user-attachments/assets/12450558-74fc-4622-a93f-adf148c0410b)

![Screenshot 2024-11-29 134313](https://github.com/user-attachments/assets/dc13c3fa-14e0-4df1-aa05-d1cb087c24a5)

![Screenshot 2024-11-29 134426](https://github.com/user-attachments/assets/6a912a4f-6937-4de2-8ee9-91c0afef9d76)

![Screenshot 2024-11-29 134553](https://github.com/user-attachments/assets/3ec8bdfa-f641-4a79-8ee2-d7a5bd39a162)

## Data Analysis
Power BI was used for creating some measures using DAX Funcions. Some of the measures used for these analysis include:
``` Sql
Last Year Sales = CALCULATE([Total sales],
SAMEPERIODLASTYEAR(SuperStore_Sales_Dataset[Order Date].[Date]))
```
``` Sql
Profit Last Year = CALCULATE([Total Profit],
SAMEPERIODLASTYEAR(SuperStore_Sales_Dataset[Order Date].[Date]))
```
``` Sql
Avg Ship Days = AVERAGE(SuperStore_Sales_Dataset[Average Delivery])
```
``` Sql
Sales Forecast = SUMMARIZE(SuperStore_Sales_Dataset,SuperStore_Sales_Dataset[Order Date],"Total sales",SUM(SuperStore_Sales_Dataset[Sales]))
```
``` Sql
Average Delivery = DATEDIFF(SuperStore_Sales_Dataset[Order Date],SuperStore_Sales_Dataset[Ship Date],DAY)
```

## Findings 

1. **Monthly Sales Year-Over-Year (YOY) Growth:**  
   - The best-performing months in terms of sales:  
     - **December:** **$244,584.90** (compared to **$78,399.04** last year)  
     - **November:** **$210,372.80** (compared to **$79,411.97** last year)  
     - **September:** **$193,213.60** (compared to **$73,410.02** last year)  
   - These months show strong seasonal sales performance, likely influenced by holiday shopping.  

2. **Monthly Profit YOY:**  
   - The most profitable months:  
     - **December:** **$26,368.10**  
     - **October:** **$25,518.40**  
     - **September:** **$20,320.20**  

3. **Region with the Highest Sales:**  
   - **West Region:** **$522,441.10** (Highest sales volume).  

4. **Most Frequently Used Shipping Mode:**  
   - **Standard Class** is the most commonly used shipping method.  

5. **Top Payment Mode by Revenue:**  
   - **Cash on Delivery (COD)** generates the highest revenue.  

---

### **Actionable Recommendations to Improve Sales:**

1️⃣ **Leverage Seasonal Trends:**  
   - Since **December, November, and September** are peak sales months, ramp up marketing efforts and special promotions during these periods.  
   - Offer discounts and bundles for the top-selling categories (**Office Supplies, Technology, and Furniture**) to maximize revenue.  

2️⃣ **Expand in High-Performing Regions:**  
   - Since the **West region** has the highest sales, allocate more marketing and inventory resources there.  
   - Conduct localized promotions to further boost sales in this area.  

3️⃣ **Optimize Shipping Strategy:**  
   - **Standard Class** is the most used shipping method, which could mean customers prioritize cost over speed.  
   - Consider introducing express shipping discounts for high-value purchases to encourage faster delivery.  

4️⃣ **Increase Digital Payment Options:**  
   - **Cash on Delivery (COD)** is the top revenue-generating payment mode.  
   - Encourage customers to switch to online payments by offering discounts or cashback incentives for digital transactions.  

5️⃣ **Enhance Inventory Planning for Top Categories:**  
   - Ensure sufficient stock levels of **Office Supplies, Technology, and Furniture** before peak seasons.  
   - Analyze fast-moving SKUs within these categories to prioritize stocking high-demand items.  
​​

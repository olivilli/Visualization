## **Financials Power BI Project**

This project is my first data visualization in Power BI, focusing on analyzing financial data. The dataset used was a built-in table in Power BI, which I cleaned, transformed, and visualized to create an interactive dashboard.

![Financials Dashboard](https://github.com/olivilli/Visualization/blob/main/PowerBI/Financials/financials.png)

## **Project Details**

### **Data Preparation**
- Cleaned the dataset in Power Query, retaining only nine key columns
- Created a custom `CALENDAR` table to manage date relationships using the formula:

  ```plaintext
  CALENDAR(MIN(Financials[Date]), MAX(Financials[Date]))
  ```
- Established a relationship between the `Date` column in the dataset and the `CALENDAR` table.

### **Calculations**
- Created a new measure to calculate the profit ratio:  
  ```plaintext
  Profit Ratio = DIVIDE(SUM(Financials[Profit]), SUM(Financials[Gross Sales]))
  ```

## **Dashboard Features**

  ![financials_video](https://github.com/olivilli/Visualization/blob/main/PowerBI/Financials/financials_pbi_screen_record.gif)

- A combined bar and line chart showing Sum of sales and Sum of profit by date
- Additional tables and charts for better insights
- Four cards displaying key performance indicators
- Titles, icons, and organized layouts to enhance user experience.

---

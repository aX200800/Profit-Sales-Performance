## Project Title
**Profit & Sales Performance**

## Project Description
This project involves the development of a comprehensive Power BI dashboard to analyze and visualize the sales and profit performance over different quarters and years. The dashboard provides insights into key metrics such as quantity sold, profit margins, total sales, and top-performing products and salespersons. Advanced DAX queries are used to facilitate detailed and dynamic data analysis.

## Installation / Prerequisites
  - Power BI Desktop
  - Data Source: Sales and profit data in CSV/Excel format

## Project Structure
### DAX Calculations

1. **Time Intelligence Calculations**
  ```DAX
    Sales YoY % = DIVIDE([Sales Growth], [Total Sales])
    
    Sales LY = CALCULATE([Total Sales], DATEADD('Date'[Date], -1, YEAR))
    
    Sales Growth = [Total Sales] - [Sales LY]
    
    QTY Sold LY = CALCULATE([QTY Sold], DATEADD('Date'[Date], -1, YEAR))
    
    Profit LY = CALCULATE([Total Profit], DATEADD('Date'[Date], -1, YEAR))
    
    Profit % LY = CALCULATE([Profit Margin], DATEADD('Date'[Date], -1, YEAR))
  ```

2. **Basic Calculations**
  ```DAX
    Profit Margin = DIVIDE([Total Profit], [Total Sales])
    
    QTY Sold = sum(Sales[Order Quantity])
    
    Total Cost = Sumx(Sales, Sales[Order Quantity] * Sales[Unit Cost])
    
    Total Profit = [Total Sales] - [Total Cost]
    
    Total Sales = sum(Sales[Total Sales])
  ```

## Visualizations
  - **Bar Charts**: Comparison of quantity sold, profit margins, and total sales across quarters
  - **Tables**: Detailed breakdown of sales and profit metrics by product
  - **KPIs**: Key performance indicators for sales, profit, and profit margins
  - **Top 5 Products and Salespersons**: Identification of top-performing products and salespersons based on sales and profit metrics

## Project Background
  - **Figma**: Used for initial wireframing and layout design of the dashboard.
  - **Adobe Photoshop**: Utilized for creating custom visual elements and ensuring a polished visual presentation.

## Usage
  - Load the sales and profit data into Power BI.
  - Use the provided DAX calculations to create the necessary measures.
  - Arrange the visualizations on the dashboard as per the project structure.
  - Customize the dashboard to fit specific business needs or preferences.

By following this structure, you can effectively monitor and analyze sales and profit performance, enabling data-driven decision-making and strategic planning.

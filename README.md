# 📊 Retail Business Analytics & Supply Chain Dashboard

This project demonstrates a beginner-to-intermediate level **Business Analytics** workflow using real-world style retail data. The goal is to analyze sales performance and inventory health and present actionable business insights through an interactive **Power BI dashboard**.

---

## 🎯 Project Objective

The objective of this project is to:

- Analyze historical retail sales data to understand demand patterns.
- Evaluate inventory levels to identify potential stockouts and overstock situations.
- Build an interactive Power BI dashboard to support data-driven decision-making in retail supply chain and operations.

This project simulates the kind of work a **Business Analyst Intern** would perform in a large retail organization.

---

## 📁 Dataset Description

Two datasets were used in this project:

### 1️⃣ `retail_sales_sample.csv`
Contains transactional sales data with the following fields:

- Date  
- City  
- Category  
- Product  
- Units_Sold  
- Unit_Price  
- Revenue  

This dataset was used to analyze:
- Top-selling products  
- City-wise performance  
- Revenue trends  
- Demand seasonality  

### 2️⃣ `retail_inventory_sample.csv`
Contains inventory information including:

- Product  
- Current_Stock  
- Reorder_Level  
- Supplier_Lead_Days  

This dataset was used to evaluate:
- Stock health  
- Risk of stockouts  
- Reorder requirements  

---

## 🛠️ Tools Used

- **Microsoft Excel** – Data exploration and pivot tables  
- **Power BI Desktop** – Dashboard creation and visualization  
- **DAX (Power BI)** – Calculated column for stock status  
- **GitHub** – Version control and project documentation  

---

## 📈 Dashboard Features (Power BI)

The Power BI dashboard includes:

### 🔹 Sales Performance Page
- KPI Card: Total Revenue  
- KPI Card: Total Units Sold  
- Bar Chart: Product vs Revenue  
- Line Chart: Monthly Revenue Trend  
- Map: City-wise Revenue Distribution  

### 🔹 Inventory Health Page
- Table: Product, Current Stock, Reorder Level  
- Bar Chart: Current Stock by Product  
- Calculated column using DAX:

```DAX
Stock_Status =
IF(
    Inventory[Current_Stock] < Inventory[Reorder_Level],
    "Reorder Now",
    "Healthy"
)

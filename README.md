# 📊 Why Customers Return Products

An interactive **Power BI dashboard** designed to analyze e-commerce orders, product returns, refund amounts, return reasons, sales channels, and product-level return patterns.

The project transforms raw transactional data using **Power Query**, builds a structured **Star Schema data model**, and uses **DAX measures** to create business-focused KPIs and interactive visualizations.

---

## 📌 Project Overview

Product returns and refunds can have a significant impact on e-commerce businesses. Understanding **why customers return products, which categories experience higher return volumes, and where refund amounts are coming from** can help businesses identify potential areas for improvement.

This project analyzes e-commerce transaction data to answer questions such as:

- How many orders were placed?
- How many orders were returned?
- What is the overall return rate?
- How much money is being refunded?
- How are refunds changing over time?
- Which sales channels generate the most returned units?
- Which product categories have higher return volumes?
- What are the most common reasons for product returns?
- Which return reasons contribute most to total returns?
- Is there a relationship between discounts and return rates?
- Which products or subcategories require further investigation?

---

## 🎯 Business Objectives

The main objectives of this project are to:

- Monitor overall order and return performance
- Track return rate and refund amounts
- Identify major return reasons
- Analyze returns across different sales channels
- Compare returned units with total orders by category
- Identify categories and subcategories with higher return activity
- Analyze monthly return and refund trends
- Investigate potential relationships between discounts and return rates
- Provide an interactive dashboard for business decision-making

---

## 🛠️ Tools & Technologies

- **Power BI**
- **Power Query**
- **DAX**
- **Data Modeling**
- **Star Schema**
- **Data Visualization**

---

# 🔄 Data Preparation

The raw e-commerce dataset was cleaned and transformed using **Power Query** before creating the final data model.

### Data preparation tasks included:

- Cleaning raw transactional data
- Standardizing column values
- Correcting data types
- Handling inconsistent or missing values
- Creating required fields
- Separating fact and dimension tables
- Preparing the dataset for Star Schema modeling

The transformed data was then loaded into Power BI for modeling and analysis.

---

# 🗂️ Data Model

A **Star Schema** was used to organize the data and establish relationships between the transactional fact table and supporting dimension tables.

### Fact Table

The central fact table contains the transactional information required for order and return analysis.

**Fact_Orders**

Key information includes:

- Order ID
- Order Date
- Product
- Category
- Subcategory
- Sales Channel
- Quantity
- Discount
- Return information
- Refund information

### Dimension Tables

Supporting dimension tables are used to provide descriptive attributes and enable filtering and analysis.

Examples include:

- **Dim_Date**
- **Dim_Product**
- **Dim_ReturnReason**
- **Dim_SalesChannel**

The Star Schema allows the dashboard to efficiently analyze transactional data across different business dimensions.

---

# 📐 DAX & Business Metrics

Several DAX measures were created to convert the raw transactional data into meaningful business KPIs.

### Key Metrics

#### Total Orders

Measures the total number of unique orders.

#### Returned Orders

Measures the number of orders associated with returned products.

#### Return Rate

Calculates the percentage of orders that were returned.

```DAX
Return Rate % =
DIVIDE(
    [Returned Orders],
    [Total Orders],
    0
)

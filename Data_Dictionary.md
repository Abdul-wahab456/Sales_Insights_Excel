# Data Dictionary: AdventureWorks Dataset

## 📌 Overview
This document provides a structured description of the datasets used in the **AdventureWorks Excel Dashboard**. It explains each table and column to help understand the relationships and data flow.

## 📂 Fact Table
### **FactInternetSales** (Sales Transactions)
| Column Name         | Description |
|---------------------|-------------|
| SalesOrderNumber   | Unique identifier for each sales order. |
| CustomerKey        | Foreign key linking to **DimCustomer**. |
| ProductKey         | Foreign key linking to **DimProduct**. |
| OrderDateKey       | Foreign key linking to **DimDate** (Order date). |
| SalesTerritoryKey  | Foreign key linking to **DimSalesTerritory**. |
| OrderQuantity      | Total quantity ordered in the transaction. |
| UnitPrice         | Selling price per unit. |
| SalesAmount        | Total revenue generated from the order. |
| COGS              | Cost of Goods Sold. |
| TotalProfit       | Profit calculated as **(SalesAmount - COGS)**. |

## 📂 Dimension Tables
### **DimProduct** (Product Information)
| Column Name        | Description |
|--------------------|-------------|
| ProductKey        | Unique product identifier. |
| ProductAlternateKey | Alternate product reference code. |
| EnglishProductName | Product name in English. |
| StandardCost      | Manufacturing or procurement cost. |
| ListPrice        | Default selling price. |
| Color            | Product color category. |

### **DimCustomer** (Customer Demographics)
| Column Name      | Description |
|-----------------|-------------|
| CustomerKey     | Unique customer identifier. |
| FirstName       | First name of the customer. |
| LastName        | Last name of the customer. |
| EmailAddress    | Email contact of the customer. |
| GeographyKey    | Foreign key linking to **DimGeography**. |
| BirthDate       | Customer’s date of birth. |
| Gender          | Gender of the customer. |
| CustomerAge     | Age derived from BirthDate. |

### **DimDate** (Date Dimension)
| Column Name         | Description |
|---------------------|-------------|
| DateKey            | Unique date identifier. |
| FullDateAlternateKey | Actual date in YYYY-MM-DD format. |
| CalendarYear       | Year of the date. |
| MonthNumberOfYear  | Month number (1-12). |
| MonthName         | Month name (e.g., January). |
| DayName           | Day of the week (e.g., Monday). |
| Quarter           | Quarter of the year (1-4). |

### **DimSalesTerritory** (Sales Regions)
| Column Name           | Description |
|----------------------|-------------|
| SalesTerritoryKey    | Unique identifier for each sales territory. |
| SalesTerritoryRegion | Region name (e.g., North America, Europe). |
| SalesTerritoryCountry | Country under the sales territory. |

### **DimGeography** (Geographic Information)
| Column Name       | Description |
|------------------|-------------|
| GeographyKey    | Unique location identifier. |
| City           | Name of the city. |
| StateProvinceName | State or province name. |
| CountryRegionCode | Country code (e.g., US, FR). |

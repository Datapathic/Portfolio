# 🛒 E-Commerce Sales Dashboard — Tableau

![E-Commerce Sales Dashboard](docs/E-Commerce%20Sales%20Dashboard.png)

### 📘 Objective
Analyze global e-commerce transactions to identify key sales trends, top products, and customer distribution using Tableau’s interactive visualization capabilities.

---

## 📊 Dataset
- **Source:** Kaggle – E-Commerce Sales Data  
- **Rows:** 541,909  
- **Fields:** `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`  
- **Period Covered:** 2010 – 2011  
- **Data Cleaning:** Performed in Excel (removed nulls, cancellations, and negative values)

---

## ⚙️ Process Overview
1. **Data Preparation (Excel)**
   - Filtered valid rows (positive `Quantity` and `UnitPrice`)
   - Removed null `CustomerID` and cancelled invoices (`InvoiceNo` starting with “C”)
   - Calculated new column:  
     ```excel
     Sales = Quantity * UnitPrice
     ```
   - Exported clean sheet `ecommerce_cleaned.xlsx`

2. **Modeling (Tableau)**
   - Connected to the cleaned dataset  
   - Converted data types (Date, String, Number)  
   - Created calculated fields:
     - `Total Sales = [Quantity] * [UnitPrice]`
     - `Year = YEAR([InvoiceDate])`
     - `Month = DATENAME('month', [InvoiceDate])`

3. **Dashboard Design**
   - KPIs: Total Sales, Total Quantity Sold, Unique Customers, Avg Order Value  
   - Visuals:
     - *Line Chart* — Sales Trend Over Time  
     - *Bar Chart* — Top 10 Best-Selling Products  
     - *Map* — Sales Distribution by Country  
   - Interactivity: dynamic filters for Country and Date  
   - Design: minimal theme, soft gridlines, consistent color palette (#1F77B4)

---

## 📈 Dashboard Overview
### **1️⃣ Key Metrics**
| Metric | Value |
|---------|-------|
| 💰 Total Sales | \$3,875,487.99 |
| 📦 Total Quantity Sold | 2,206,220 |
| 👥 Unique Customers | 2,997 |

---

### **2️⃣ Total Sales Trend Over Time**
- 2011 shows a sharp increase in revenue vs 2010  
- Monthly sales spike around **September–November** (holiday season)

---

### **3️⃣ Top 10 Best-Selling Products**
- *Paper Craft – Little Birdie* is the highest revenue generator  
- Product demand follows a long-tail distribution (few items dominate sales)

---

### **4️⃣ Sales Distribution by Country**
- The **United Kingdom** contributes ~90% of total sales  
- Other EU countries (EIRE, Netherlands, Germany) represent smaller markets  

---

## 💡 Key Insights
- Strong **seasonality** — demand surges in Q4 (holiday period)  
- **Top 10 products** account for a majority of revenue  
- The **UK market** dominates overall performance  
- Opportunities exist for **geographic diversification** and **product variety expansion**

---

## 🧰 Tech Stack
- **Tool:** Tableau Desktop Public Edition  
- **Data Prep:** Microsoft Excel  
- **Calculated Fields:** Tableau (LOD & Basic Aggregations)  
- **Visuals Used:** KPI Cards, Line Chart, Bar Chart, Map  
- **Design:** Minimalist theme, consistent layout, interactive filters  

---

## 🔗 Links
- **📊 Tableau Dashboard:** [View on Tableau Public](https://public.tableau.com/app/profile/enrique.ardelean/viz/E-Commerce_Sales_Data/SalesDashboard?publish=yes)
- **📁 Dataset:** [Kaggle – E-commerce Dataset](https://www.kaggle.com/datasets/carrie1/ecommerce-data)

---

## 👤 Author
**Enrique**  
📧 [LinkedIn](https://www.linkedin.com/in/enrique-ardelean-816837394/) | 
[GitHub](https://github.com/Datapathic/Portfolio)  
🎯 *Focus: Data Analysis • Power BI • Tableau • Storytelling Dashboards*


## 📂 Repository Structure
```plaintext
E-Commerce-Sales-Data
├── data
│   ├── data.csv
│   └── ecommerce_cleaned.xlsx
├── docs
│   ├── Dashboard_Overview.png
├── Tableau
│   └── Ecommerce_Sales_Dashboard.twb
└── README.md

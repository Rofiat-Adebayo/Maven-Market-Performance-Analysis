 📊 Maven Market Performance Analysis  
 
*A Power BI retail analytics solution delivering market insights, profitability trends, and strategic recommendations for Maven Market  

Using Power BI, I analyzed sales, transactions, profit, returns, and product-brand performance to help business leaders make data-driven decisions.

---
## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Summary](#-dataset-summary)
- [Key Business Questions](#-key-business-questions)
- [Dashboard Features](#-dashboard-features)
- [Executive Insights](#-executive-insights)
- [Tools & Technologies](#-tools--technologies)
- [Data Modeling](#-data-modeling)
- [Business Recommendations](#-business-recommendations)
- [Project Structure](#-project-structure)
- [What I Learned](#-what-i-learned)
- [About Me](#-about-me)
- [Contact](#-contact)

---

## 🚀 Project Overview
The goal of this analysis is to uncover key insights that drive revenue growth, identify top-performing regions, evaluate product profitability, and monitor business goals such as monthly profit and return rates.

🔗 Live Dashboard:
https://app.fabric.microsoft.com/reportEmbed?reportId=db57360e-feed-4601-96e9-c80339ea9061&autoAuth=true&ctid=37d7521a-5079-48af-9131-4ac2cb6f1e3a

The dashboard includes:
- Executive KPIs  
- Revenue trends  
- Geographic store performance  
- Top product brands  
- Return rate monitoring  
- Revenue vs target performance  

---

## 🗂 Dataset Summary
The dataset contains six interconnected tables:

<img width="213" height="483" alt="!tablws" src="https://github.com/user-attachments/assets/ee7a0fa6-6e24-4fd7-b522-8c5a4d5dc741" />

| Table Name        | Description |
|-------------------|-------------|
| **Products**       | Product details (brand, cost, retail price, weight, SKU) |
| **Customers**      | Customer demographic information |
| **Stores**         | Store locations (city, state, country) |
| **Regions**        | Regional grouping of stores |
| **Transactions**   | Detailed sales transactions |
| **Return Data**    | Product returns and return dates |

The relational structure enabled end-to-end insights across locations, product categories, and time.

---

##  Key Business Questions
- Which cities drive the highest number of transactions?
- Are we meeting monthly revenue and profit goals?
- Which product brands deliver the highest profit margin?
- What is the weekly and monthly revenue trend?
- How does each country perform in terms of transactions?
- Are product returns significantly affecting profit?

---

## 📊 Dashboard Features

### ✔ Executive KPIs
- Total Transactions  
- Total Profit  
- Return Rate  
- Revenue vs Target  

### ✔ Sales Trends
- Weekly revenue trending  
- Month-over-month performance  

### ✔ Product Performance
- Top 30 product brands  
- Profit margin comparison  
- Return rate by product  

### ✔ Geographic Analysis
- Map visualization of store-city transactions  
- Country and state filtering (USA, Canada, Mexico)  
- Region-level insights  

### ✔ Interactive Features
- Drillthrough  
- Slicers (Country, city, brand)  
- Dynamic filters  
- Hover tooltips  
---
## ⭐ Executive Insights

<img width="619" height="335" alt="!executive" src="https://github.com/user-attachments/assets/c1187d06-d150-4960-a24e-27f59585e88e" />


### 1️⃣ Strong Monthly Performance  
- **Current Month Transactions:** 18,325  
- **Goal:** 17,339 → **+5.69% above target**  
The business exceeded its monthly sales target.

### 2️⃣ High Profit Margin Brands  
Top-performing brands such as **Hermanos, Ebony, Tell Tale, and Tri-State** recorded profit margins above **58%**, making them key revenue drivers.

### 3️⃣ Seasonal Revenue Growth  
Weekly revenue trends show stronger performance in **October–December**, indicating a market seasonality effect.

### 4️⃣ High-Performing Store Cities  
Cities with the highest transactions include:  
- Vancouver  
- Portland  
- Tacoma  
- Los Angeles  
- Zacatecas  

These cities should be prioritized for stock allocation and marketing campaigns.

### 5️⃣ Strong Quality Control  
- **Return Rate:** ~1%  
This is significantly lower than target levels, indicating strong customer satisfaction and fewer product issues.

### 6️⃣ Revenue Target Achieved  
- **Revenue:** $120K  
- **Target:** $119K  
Sales teams successfully met revenue goals.



---

## 🛠️ Tools & Technologies
- **Power BI** – Main reporting & visualization tool  
- **Power Query** – Data cleaning and transformation  
- **DAX** – Measures and KPIs  
- **Excel** – Initial data exploration  

---

## 📐 Data Modeling
Relationships were created across:
- Products → Transactions  
- Stores → Transactions  
- Customers → Transactions  
- Regions → Stores  
- Return Data → Products
- Buit a Calendar Table → Transactions → Return Data
- Buit a measure(DAX) Table
  
<img width="946" height="476" alt="!Modelling" src="https://github.com/user-attachments/assets/c4c44ae5-5844-44c6-9e54-d98dd5c679a1" />

This enabled drilldowns at product, city, brand, and country levels.

---

## 📌 Business Recommendations

### 🔹 1. Reinforce Inventory in High-Performing Cities  
Increase stock in cities like Vancouver, Portland, and Tacoma to meet customer demand.

### 🔹 2. Promote High-Profit Brands  
Brands like Hermanos and Ebony should be featured in marketing campaigns due to their strong margins.

### 🔹 3. Capitalize on Seasonal Trends  
Plan holiday-season promotions between **October and December**, when revenue peaks.

### 🔹 4. Maintain Quality Levels  
The low return rate (~1%) should continue to be monitored as a KPI of product reliability.

---

## 📁 Project Structure

📂 Maven-Market-Performance-Analysis
 ├── 📂 Dataset
 │   └── retail_data.xlsx
 ├── 📂 Dashboard
 │   └── MavenMarket.pbix
 ├── 📂 Screenshots
 │   ├── dashboard_overview.png
 │   └── product_trends.png
 ├── README.md
 └── insights.pdf


---

##  What I Learned
- Building multi-table relationships in Power BI  
- Creating KPIs with DAX  
- Designing clean and interactive dashboards  
- Performing profit margin and return rate analysis  
- Communicating insights to business users  
- Understanding retail analytics and product performance drivers  

---

## 💼 About Me
I am a Data Analyst with skills in:
- Power BI  
- SQL  
- Excel  
- Data Cleaning  
- Insight Generation  

This project showcases my ability to turn raw retail data into meaningful business insights.

---

## 📬 Contact
Feel free to reach out!

**LinkedIn:** https://linkedin.com/in/rofiat-adebayo  
**Email:** adebayorofiat004@gmail.com  



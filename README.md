# 📌 Global Restaurant Analytics – Power BI Dashboard

![Dashboard Preview](Dashboard_Screenshots/OVERVIEW.png)

## 🔍 Objective
Develop an interactive Power BI report to analyze global restaurant performance across continents, countries, and cities. The dashboard enables stakeholders to identify top restaurants by ratings and cost, understand cuisine trends, and drill down into restaurant-level details for strategic decision-making.

---

## 🌍 Dataset Summary
The project consolidates restaurant information from the following **8 Excel files**:

Africa • Asia • Europe • North America (NAM) • South America (SAM) • Oceania • Country-Code • Fact Table

The final dataset contains **thousands of restaurant records** with complete attributes including location, costs, ratings, and cuisines.

---

## 🧰 Tools & Techniques
Power BI Desktop • Power Query (ETL) • Star Schema Data Modeling • DAX • Infographic Designer • Power BI Service Deployment (Web + Mobile)

---

## 🛠 Data Transformation (Power Query)
Key transformations performed:
- Removed duplicate and null records
- Corrected city names (e.g., *Sí£o Paulo → São Paulo*, *ÛÁstanbul → Istanbul*)
- Split combined restaurant name + address into separate fields
- Built Cuisine Lookup Table to list cuisines served by each restaurant
- Standardized and grouped geographic fields into continents
- Ensured Country-Code table contained only unique non-blank values

---

## 🧩 Data Model
- Fact table linked to dimension tables using **one-to-many relationships**
- **User-defined Geography Hierarchy → Continent → Country → City**
- Correct cardinality and cross-filter direction to support roll-ups and drill-downs

---

## 🔢 DAX Measures and Calculations
**Restaurant Count** = COUNT('Fact Table'[Restaurant ID])  
**Average Rating** = AVERAGE('Fact Table'[Aggregate rating])  
**Average Cost** = AVERAGE('Fact Table'[Average Cost for two])  
**Cuisine Count** = DISTINCTCOUNT('Cuisine Table'[Cuisine])

**Rating Color (Calculated Column):**

> If rating > 4.5 → Dark Green  
> If rating ≥ 4.0 and ≤ 4.4 → Green  
> If rating ≥ 3.5 and ≤ 3.9 → Yellow  
> If rating ≥ 2.5 and ≤ 3.4 → Orange  
> If rating ≥ 1.8 and ≤ 2.4 → Red  
> If rating ≥ 0 and ≤ 1.7 → White

---

## 📊 Dashboard Structure
### 📍 Page 1 — Global Overview
- KPIs: Restaurant Count, Average Rating, Average Cost
- Map visualization using Continent → Country → City hierarchy
- Filters for Continent, Country, City, Rating Color, Cuisine

### ⭐ Page 2 — Top Restaurants
- Top restaurants by highest rating and lowest cost
- Infographic leaderboard visuals
- Cuisine-wise comparison

### 🔎 Page 3 — Drill-Down View
- Complete restaurant details: name, address, cuisines
- Gauges for rating and average cost
- Grid view for comparison across selected restaurants

---

## 🔑 Key Insights
- Highest concentration of restaurants found in **India and the United States**
- **Asia and Europe** display the highest customer satisfaction by ratings
- **Brazil and Indonesia** offer some of the lowest dining costs
- Restaurants offering **multiple cuisines** achieve higher average ratings
- Drill-downs enable easy identification of partnership/expansion opportunities

---

## 🚀 Business Impact
The solution enables:
- Data-driven evaluation of global restaurant performance
- Market comparison using **cost vs rating insights**
- Fast decision-making for business expansion and partnership strategies
- Universal access via **Power BI Service** on web and mobile

---
## 📁 Repository Contents

📦 PowerBI_KPI_Dashboard  
├── 📂 Dashboard_Screenshots  
│   ├── Rating_Specific_Drill.png  
│   ├── Restaurant_Analysis.png  
│   ├── Restaurant_Selection_Analysis.png  
│   └── World_Wide_Analysis.png  
├── 🧾 PL_300_COURSE_END_PROJECT_AYUSH_VISHWAKARMA.pbix  
└── 📄 README.md
---

## 👨‍💻 Author
**Ayush Vishwakarma — Data Analyst**  
GitHub Portfolio: https://github.com/ayush-vkarma  
LinkedIn: https://www.linkedin.com/in/ayush-d-vishwakarma

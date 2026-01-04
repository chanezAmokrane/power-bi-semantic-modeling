<!-- ========================= -->
<!--        README.md          -->
<!-- ========================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=180&text=Data%20Modeling%20in%20Power%20BI&fontAlign=50&fontAlignY=35&desc=How%20I%20think%20about%20data%20models%20(SQL%20→%20Power%20BI)&descAlign=50&descAlignY=60" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Modeling-F2C811?logo=powerbi&logoColor=000" />
  <img src="https://img.shields.io/badge/SQL-Relational%20Thinking-2F80ED?logo=postgresql&logoColor=fff" />
  <img src="https://img.shields.io/badge/Power%20Query-Merge%20Queries-00A4EF?logo=microsoft&logoColor=fff" />
  <img src="https://img.shields.io/badge/Focus-Analytics%20Ready-22C55E" />
</p>

<p align="center">
  <i>Not a textbook. A mindset.</i><br/>
  <i>From “storing data” to “modeling for analysis”.</i>
</p>

---

## 🧠 From storing data → answering questions

### ✅ In a classic database mindset
- Reduce redundancy  
- Keep data consistent  
- Protect integrity  
- Use keys + relationships  
- Rebuild information when needed with SQL joins

### ✅ In a Power BI mindset
Power BI changes the question:

> “How is data stored?” ❌  
> “What happened? How much? When? For whom?” ✅

Power BI forces the model to be:
- **analysis-first**
- **human-readable**
- **performance-aware**

---

## 🧩 How Power BI sees the database

In Power BI, a database is not only “tables connected together”.  
It becomes an **analytic model** designed for:
- 🔎 exploration
- 📊 reporting
- ⚡ fast filtering & aggregation
- 🧭 intuitive navigation for business users

That’s why we think in:

### 📌 Fact table
The measurable events (sales, transactions, amounts, quantities).

### 📌 Dimension tables
The context (customers, products, dates, locations).

> Facts = what happened  
> Dimensions = how we describe what happened

---

## ⭐ Star Schema vs ❄️ Snowflake Schema

### ⭐ Star schema (often the default in Power BI)
- Easier to read
- Simpler relationships
- Usually better performance

### ❄️ Snowflake schema
- Less redundancy
- More normalized
- More complex model

📍 It’s not “good vs bad”.  
It’s a design choice depending on:
- data size
- business needs
- expected performance
- clarity for end users

---

## 🔗 Relationships and joins in Power BI (the important nuance)

In classic databases, we express relationships through SQL joins:
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- etc.

In Power BI, the approach is different:

### 🛠️ Joins are created upstream in Power Query
✅ Use **Merge Queries** to:
- create new joins
- choose the join type (left/right/inner…)
- adjust it when needed

### 🧩 Then the Power BI model uses relationships
Once tables are prepared (merged or not), Power BI defines relationships for analysis.

> Same relational logic —  
> but Power BI shifts join construction to the **data preparation phase**, before analysis.

---

## ✨ Final note

Power BI modeling is not about knowing words like “fact table” or “star schema”.  
It’s about building a model that people can actually use to answer questions.

> A good model feels obvious.  
> A great model feels invisible.



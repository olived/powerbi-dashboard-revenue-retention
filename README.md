# 📊 Power BI Dashboard – Revenue & Retention Analysis

An interactive **Power BI dashboard** designed to analyze **revenue performance, sales channels, product categories, and customer retention**.  
This project highlights my skills in **data modeling, DAX, and interactive dashboard design** using Power BI.

---

## 🎯 Project Objectives

- Provide a **clear executive view** of revenue, orders, and key KPIs.
- Enable users to explore **channel performance, top-selling products, and category contributions**.
- Track **customer retention** using cohort analysis to monitor engagement over time.

---

## 🖼️ Dashboard Overview

### 1️⃣ Executive Overview  
![Executive Overview](assets/overview.png)  
- **KPIs:** Total Revenue, Total Orders, Distinct Customers, and Average Ticket.  
- **Visuals:** Yearly Revenue Evolution (Clustered Column Chart), Revenue by Channel (Bar Chart).  
- **Filters:** Date, Acquisition Channel, and State (UF).  
- **Goal:** Provide decision-makers with a high-level snapshot of business performance.

---

### 2️⃣ Channel Analysis  
![Channel Analysis](assets/channels.png)  
- **Visuals:** Revenue by Channel (Bar Chart), Revenue by Channel over Time (Stacked Column Chart).  
- **Table:** Channel share, total orders, and % contribution.  
- **Goal:** Quickly compare channel performance (Ads, Organic, Social, Partners).

---

### 3️⃣ Product Performance  
![Product Analysis](assets/products.png)  
- **Visuals:** Top Products by Revenue (Column Chart), Revenue by Category (Treemap).  
- **Table:** Product-level revenue and total orders.  
- **Goal:** Identify best-selling products and categories driving the highest revenue share.

---

### 4️⃣ Customer Retention  
![Customer Retention](assets/customers_retention.png)  
- **Visuals:** Cohort Heatmap showing monthly revenue contribution by cohort.  
- **Goal:** Track customer engagement and measure retention across time since acquisition.

---

## 🛠️ Technical Solution

- **Data Model:**  
  - Star schema with `orders`, `order_items`, `customers`, `channels`, and `products` tables.  
  - Relationship established by primary/foreign keys (Customer ID, Order ID).

- **DAX Measures:**  
  ```DAX
  Total Revenue = SUM(order_items[price])

  Total Orders = DISTINCTCOUNT(orders[order_id])

  Average Ticket = DIVIDE([Total Revenue], [Total Orders])

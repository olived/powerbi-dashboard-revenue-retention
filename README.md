# 📊 Power BI Dashboard – Revenue & Retention Analysis  

An interactive **Power BI dashboard** designed to analyze **revenue performance, sales channels, product categories, and customer retention**.  
This project demonstrates my skills in **data modeling, DAX, and visual storytelling** using Power BI.

---

## 🎯 Project Objectives  
- Provide a **clear executive view** of revenue, orders, and key KPIs.  
- Enable users to explore **channel performance**, **top-selling products**, and **category contributions**.  
- Track **customer retention** using cohort analysis to monitor engagement over time.  

---

## 🖼️ Dashboard Overview  

### 1️⃣ Executive Overview  
- **KPIs:** Total Revenue, Total Orders, Unique Customers, Average Ticket.  
- **Visuals:** Yearly Revenue (Column Chart), Revenue by Channel (Bar Chart).  
- **Filters:** Date, Channel, State (UF).  

---

### 2️⃣ Channel Analysis  
- **Visuals:** Revenue by Channel, Revenue by Channel over Time (Stacked Column Chart).  
- **Table:** Channel share, total orders, and % of revenue contribution.  
- **Goal:** Quickly compare performance of marketing channels (Ads, Organic, Social, Partners).  

---

### 3️⃣ Product Performance  
- **Visuals:** Top N products by revenue (Bar Chart) and Category distribution (Tree Map).  
- **Table:** Revenue and % share by product & category.  
- **Goal:** Identify key revenue drivers and focus areas for sales strategy.  

---

### 4️⃣ Customer & Retention Analysis  
- **Visuals:** Geo Map by State (UF), Cohort Table (Revenue by month since signup).  
- **Goal:** Analyze customer distribution, retention trends, and revenue growth over time.  

---

## 🛠️ Technical Solution  

- **Data Modeling:**  
  - Built a **star schema** with `orders`, `order_items`, `customers`, and `channels` tables.  
  - Created **relationships** between fact and dimension tables for proper filtering.

- **DAX Measures:**  
  ```DAX
  Total Revenue = SUM(order_items[price])
  Total Orders = COUNT(order_items[order_id])
  Average Ticket = DIVIDE([Total Revenue], [Total Orders])

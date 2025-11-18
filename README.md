# 🌍 Strategic Market & Product Insights | Global Superstore | Power BI

<img width="1599" height="892" alt="image" src="https://github.com/user-attachments/assets/b8f38e20-4282-4f93-9ae0-f5767d641149" />


**Author:** Huong Le | **Date:** March 2025 | **Tools Used:** Power BI

## Table of Contents

1. 📌 [Background & Overview](#background--overview)
2. 📁 [Dataset Description & Data Structure](#dataset-description--data-structure)
3. 🧠 [Design Thinking Process](#design-thinking-process)
4. 📊 [Key Insights & Visualizations](#key-insights--visualizations)
5. 🔍 [Final Conclusion & Recommendation](#final-conclusion--recommendation)


---

## 📌 Background & Overview

**Objective:**

**📖 What is this project about?**

This project focuses on designing a **Power BI analytics dashboard** using the *Global Superstore* dataset, containing data from **Orders**, **Products**, **Customers**, **Regions**, and **Sales Representatives**.

The goal is to equip senior leaders with **clear, actionable insights** to:

- Understand overall business performance across markets and product categories
- Identify high-growth and high-margin regions for market expansion
- Evaluate product profitability and prioritize strategic SKUs
- Support faster, data-driven decisions using real-time visual analytics


**👤 Who is this project for?**

✔️ **Senior executives** seeking a unified view of global business performance  
✔️ **Business unit heads & sales managers** responsible for market and product decisions  
✔️ **Data analysts** who need standardized dashboards to reduce manual reporting  
✔️ **Strategy teams** planning expansion, pricing, or product investments  


**❓Business Questions:**

✔️ How is the business performing across regions, categories, and time?  
✔️ Which markets offer the highest growth potential and profitability?  
✔️ Which product categories and sub-categories should be prioritized for investment? 
✔️ Where do return rates or declining margins indicate operational risks?  
✔️ Which sales representatives or regions outperform the rest—and why? 


**🎯Project Outcome:**

- **Sales grew strongly**, but **profit margin stayed flat (~11–12%)**, indicating rising operational costs and limited efficiency gains.  
- **Canada** stands out as a **high-margin market (26.6%)**, offering a prime opportunity for profitable expansion despite lower revenue.  
- **Africa and EMEA** show the **fastest YoY revenue growth**, making them promising emerging markets to monitor and develop.  
- **Technology** drives the highest revenue and profit, but elevated **return rates in some Tech SKUs** reduce overall margin performance.  
- **Copiers deliver the highest profit per unit**, while underperforming categories like **Supplies and Furnishings** dilute company profitability

By aligning regional and product strategies, senior managers can **scale in high-margin markets**, **invest in scalable profitable categories**, and **optimize acquisition and return management**, driving **sustainable long-term growth**.

## 📂 Dataset Description & Data Structure

### **📌 Data Source** 

- **Source**: Kaggle  
- **Size**: The **Orders** table contains **51,290** records.  
- **Format**: CSV  

### 📊 **Data Structure & Relationships**  

#### 1️⃣ **Tables Used:**  
The dataset consists of **three tables**:  

- 🛒 **Orders** – Contains detailed transaction and customer information (**51,290 records**).

<details>
<summary> <strong>Table 1: Orders</strong></summary>

| Column Name       | Data Type   | Description                              |
|------------------|------------|------------------------------------------|
| `Order ID`      | `VARCHAR`   | Unique identifier for each order.       |
| `Order Date`    | `DATE`      | Date when the order was placed.         |
| `Ship Date`     | `DATE`      | Date when the order was shipped.        |
| `Ship Mode`     | `VARCHAR`   | Shipping method used for delivery.      |
| `Customer ID`   | `VARCHAR`   | Unique identifier for each customer.    |
| `Customer Name` | `VARCHAR`   | Full name of the customer.              |
| `Segment`       | `VARCHAR`   | Customer segment (e.g., Consumer, Corporate). |
| `City`         | `VARCHAR`   | City where the order was placed.        |
| `State`        | `VARCHAR`   | State where the order was placed.       |
| `Country`      | `VARCHAR`   | Country where the order was placed.     |
| `Postal Code`  | `VARCHAR`   | Postal code of the shipping address.    |
| `Market`       | `VARCHAR`   | Market region (e.g., APAC, EMEA).       |
| `Region`       | `VARCHAR`   | Geographical region of the order.       |
| `Product ID`   | `VARCHAR`   | Unique identifier for each product.     |
| `Category`     | `VARCHAR`   | Product category (e.g., Furniture, Office Supplies). |
| `Sub-Category` | `VARCHAR`   | Sub-category of the product.            |
| `Product Name` | `VARCHAR`   | Name of the product ordered.            |
| `Sales`        | `DECIMAL`   | Revenue generated from the order.       |
| `Quantity`     | `INT`       | Number of items ordered.                |
| `Profit`       | `DECIMAL`   | Profit earned from the order.           |

</details>

- 🔄 **Returns** – Stores data on returned orders.

<details>
<summary> <strong>Table 2: Returns</strong></summary>

| Column Name  | Data Type | Description |
|--------------|-----------|-------------|
| `Returned`   | `VARCHAR` | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| `Order ID`   | `VARCHAR` | Unique identifier for each order. |

</details>
  
- 👥 **People** – Holds information about sales representatives.

<details>
<summary> <strong>Table 3: People</strong></summary>

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| `Person`    | `VARCHAR` | Name of the salesperson. |
| `Region`    | `VARCHAR` | Geographic region where the salesperson operates. |

</details>

#### 2️⃣ Data Relationships:
<img width="1798" height="1062" alt="image" src="https://github.com/user-attachments/assets/3643485d-d1fa-4922-9d20-df17570e771a" />

| **From Table** | **To Table** | **Join Key**   | **Relationship Type**                                  |
|------------|----------|------------|----------------------------------------------------|
| `Orders`   | `People` | `Region`   | Many-to-One (multiple orders belong to one region) |
| `Orders`   | `Returns`| `Order ID` | One-to-One or Left Join (not all orders are returned) |

## 🧠 Design Thinking Process

### 1️⃣ Empathize
<img width="1510" height="821" alt="image" src="https://github.com/user-attachments/assets/e95c6fdd-d88c-478b-aaf9-e9ed413e4887" />
<img width="1585" height="843" alt="image" src="https://github.com/user-attachments/assets/1ecd0ef3-a228-4fc7-92b7-5d841bebe1ec" />

### 2️⃣ Define point of view 

<img width="1541" height="825" alt="image" src="https://github.com/user-attachments/assets/452559a6-e523-42ca-b777-3cdbb4d28e10" />
<img width="1539" height="859" alt="image" src="https://github.com/user-attachments/assets/aa115c3d-ea77-4eee-a606-66b6f2c26767" />

### 3️⃣ Ideate

<img width="1486" height="819" alt="image" src="https://github.com/user-attachments/assets/bcec9703-ee65-45c2-8a93-4587c9c8dce5" />

### 4️⃣ Prototype and review

This part is in the dashboard

## 📊 Key Insights & Visualizations

### 🔍 Dashboard Preview

### I. Overview

<img width="1632" height="925" alt="image" src="https://github.com/user-attachments/assets/6a0e19af-3f2d-4f8c-ba8b-07bd7fbe969c" />

### ⭐ Key Findings — Overview

**1. Sales & Profit Grew, But Margins Stayed Flat**  
- Total Sales reached **$12.64M** and Total Profit **$1.47M**, but **profit margin remained flat (~11–12%)** across years.  
→ Growth was driven by **higher sales volume**, not improved cost efficiency.

**2. APAC & EU Lead in Revenue, but Canada Leads in Margin**  
- **APAC, EU, and US** generated the highest revenue.  
- **Canada** achieved an exceptional **26.6% profit margin**, despite low revenue.  
→ Canada is a **high-potential, high-margin market** worth expanding.

**3. Africa & EMEA Show the Fastest Growth**  
- Africa and EMEA had the **highest YoY sales growth**, even with smaller revenue bases.  
→ These are **emerging strategic markets** with strong long-term potential.

**4. Technology Outperforms All Categories**  
- Technology posted the **highest profit and sales**, outperforming Furniture and Office Supplies.  
- However, some Technology items recorded **higher return rates**, which reduced net margins.  
→ Tech is the **core growth engine**, but requires improved return management.

**5. Return Orders Decreased Despite Rising Orders**  
- Return rate dropped significantly from **~15% to ~9%**, even as total orders increased.  
→ Indicates **better customer satisfaction**, improved logistics, or enhanced product quality.

**6. Revenue Growth Driven by Key Regions**  
- EMEA (59.8%) and Africa (56.5%) recorded the **highest % Sales Growth** among all markets.  
→ Strong candidates for **future investment and market expansion**.
  
### II. Market Analysis
<img width="1899" height="1059" alt="image" src="https://github.com/user-attachments/assets/e73ad8b0-951f-459c-ac30-405a717fa951" />

### ⭐ Key Findings — Market Analysis

**1. APAC Leads in Total Sales**  
- APAC generated **$3.59M**, the highest among all markets, followed by EU and US.  
→ APAC is the **strongest revenue driver** and a key market to maintain and scale.

**2. EU & EMEA Achieve the Fastest Growth**  
- EU recorded **55% YoY sales growth**, and EMEA reached **59.8%**, the highest overall.  
→ These markets show **exceptionally strong momentum** and should be prioritized for expansion investment.

**3. Canada Shows Exceptional Profit Margin**  
- Canada achieved a **26.6% profit margin**, the highest of all regions, despite low revenue.  
→ Indicates an opportunity for **premium positioning and targeted scaling**.

**4. Africa Demonstrates Strong Emerging Potential**  
- Africa delivered **56.5% YoY growth**, outpacing larger markets.  
→ Suggests a **high-growth emerging market** with long-term potential despite small revenue base.

**5. Strong Salesperson Performance Concentrated in Key Regions**  
- Top performers (e.g., Anna Andreadi, Anthony Jacobs) generated **$1M+** each, mostly in APAC, EU, and US.  
→ Highlights the impact of **high-performing reps** and the importance of **regional sales leadership**.

**6. Consistent Profitability Across Major Markets**  
- US (12.47%), EU (12.69%), and APAC (12.16%) maintained stable margins.  
→ Indicates **operational consistency** across core regions.
     
### III. Product Analysis

<img width="1891" height="1056" alt="image" src="https://github.com/user-attachments/assets/01011ac1-8bc5-4d28-8b33-28bae954dabd" />

### ⭐ Key Findings — Product Analysis

**1. Technology Sub-Categories Drive the Most Sales**  
- Phones, Copiers, Chairs, and Bookcases generated the highest total sales.  
→ Technology-related products show **strong, consistent demand** across markets.

**2. Copiers Deliver Exceptional Profitability**  
- Copiers produced **the highest total profit** and one of the strongest margins (~17%).  
→ A highly strategic product for scaling due to **high profit per unit**.

**3. Appliances & Accessories Show Strong YoY Growth**  
- Appliances (55.2%) and Accessories (51.1%) recorded **some of the strongest YoY growth rates**.  
→ These categories offer **expansion opportunities** and rising customer interest.

**4. Low-Performing Categories Dilute Profit**  
- Sub-categories like Fasteners (0%), Furnishings (~49%), and Supplies (~48%) have **low sales and lower growth**.  
→ These categories **drag overall performance** and may require portfolio optimization.

**5. Top Products Are All Technology Items**  
- The Top 5 products by total sales are entirely **Tech products** (Apple, Cisco, Motorola, Nokia, Canon).  
→ Indicates that **Technology is the dominant revenue engine**, with strong brand-driven demand.

**6. Product Demand Clusters Around Mid-to-High Profit Range**  
- Bubble chart shows most products cluster between **$0.5M–$1.5M sales** with varying margins.  
→ Highlights opportunities to **scale mid-tier products** with stable profitability.

## 🔎 Final Conclusion & Recommendation 

| **Strategy** | **Insight** | **Recommendation** |
|--------------|-------------|--------------------|
| 🚀 **1. Market Expansion Strategy** | - **Canada** has the highest profit margin (**26.6%**) despite low revenue.<br>- **Africa & EMEA** show exceptionally high revenue growth and improving profit trends.<br>- **APAC & EU** deliver high absolute revenue with stable margins (~12–13%). | - Expand **selectively in Canada** to maximize margin opportunities.<br>- Increase **investment in Africa & EMEA** to capture growth momentum.<br>- Maintain strong presence in **APAC & EU** by continuing regional marketing and sales efforts. |
| 📦 **2. Product Portfolio Optimization** | - **Phones and Copiers** deliver strong revenue and high profit contribution.<br>- **Accessories, Art, Labels** have high margins but low revenue.<br>- **Suppliers & Furnishings** underperform in both sales and profit.<br>- **Tables** generate high sales but negative profit (-7%).<br>- **Storage** has high orders but low profit margin. | - Scale **Technology** products; prioritize high-margin Tech SKUs (e.g., Canon Copiers, Cisco/Motorola Phones).<br>- Market **Accessories, Art, and Labels** more aggressively to leverage their margins.<br>- Consider delisting or repositioning **Suppliers, Tables, Furnishings** due to weak performance.<br>- Review **Storage** pricing and supply chain to recover margin. |
| 👥 **3. Sales Representative Strategy** | - **Anna Andreadi** is the top performer with ~$2.8M in sales.<br>- **Nicole Hansen** is the only representative in Canada — both a strength and risk.<br>- Strong performance is concentrated in APAC, EU, and US teams. | - Leverage Anna’s results by assigning training/leadership duties.<br>- Retain and support **Nicole Hansen** as the lead rep in Canada to build a scalable sales structure.<br>- Replicate top-performer practices across underperforming regions. |
| 🎯 **4. Customer Strategy** | - Majority of revenue (**~99%**) comes from **existing customers**.<br>- **Oceania & Africa** bring in the most new customers.<br>- Some regions rely heavily on repeat buyers. | - Focus on **customer retention** with loyalty programs and upselling.<br>- Increase **acquisition efforts** in Africa & Oceania to leverage new customer growth.<br>- Develop targeted campaigns for markets heavily dependent on returning customers. |
| ⚙️ **5. Operational Efficiency** | - Profit margin remains stable (~11–12%), suggesting cost pressure.<br>- Markets like **US, EU, and APAC** show slower growth compared to emerging regions.<br>- Rising sales but declining return rates indicate improvement in product or logistics. | - Improve **cost efficiency** in mature regions to raise margins.<br>- Benchmark operations in fast-growth regions (Africa/EMEA) to identify scalable practices.<br>- Maintain return-rate improvements through quality control and supplier management. |


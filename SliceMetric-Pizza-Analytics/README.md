# SliceMetric — Pizza Chain Analytics

![Landing Page](Screenshots/1_Home.png)

> A 7-page interactive Power BI dashboard for a pizza chain —  SliceMetric  — built on a custom PowerPoint-designed background with a bold Crimson Slice theme. Covers 5,000 orders across 5 Austin (TX) branches and 17 products from January to May 2025.

---

## Project Overview

This project analyzes pizza chain sales, product performance, customer behaviour, branch efficiency, and time-based trends for  SliceMetric Pizza Chain Analytics . The dashboard features a custom-designed background built in PowerPoint, a fully branded navigation page, and an advanced  Quick Analysis  page that lets users toggle between 6 metrics and 9 dimensions dynamically.


Key business questions answered:
- Which branches and products drive the most revenue and profit?
- What are customer ordering patterns — dine-in vs takeaway vs delivery?
- Which payment methods do customers prefer?
- What time of day, day of week, and month drives peak sales?
- How do all metrics compare across every dimension dynamically?

---

## Tools Used

| Tool | Purpose |
|------|---------|
|  Power BI  | 7-page interactive dashboard with dynamic metric/dimension selectors | |

---

## Dashboard Pages

### Page 1 — Landing / Navigation
![Landing Page](Screenshots/1_Home.png)

### Page 2 — Executive Overview
![Executive Overview](Screenshots/2_Executive_Overview.png)

### Page 3 — Product Performance
![Product Performance](Screenshots/3_Product_Performance.png)

### Page 4 — Customer Behaviour
![Customer Behaviour](Screenshots/4_Customer_Behaviour.png)

### Page 5 — Branch Performance
![Branch Performance](Screenshots/5_Branch_Performance.png)

### Page 6 — Time Analysis
![Time Analysis](Screenshots/6_Time_Analysis.png)

### Page 7 — Quick Analysis
![Quick Analysis](Screenshots/7_Quick_Analysis.png)

---

## Key Business Insights

### Overall KPIs
| Metric | Value |
|--------|-------|
| Total Sales | $113,540 |
| Total Orders | 5,000 |
| Total Profit | $51,312 |
| Avg Order Value | $22.71 |
| Profit Margin | 45.19% |
| Total Quantity Sold | 10,017 |
| Avg Basket Size | 2.00 |
| Total Branches | 5 |
| Total Products | 17 |
| Data Period | Jan – May 2025 |

### Branch Performance
| Branch | Revenue | Orders | Profit |
|--------|---------|--------|--------|
| Downtown | $26,769 | 1,185 | ≈$12.0K |
| The Domain | $25,356 | 1,040 | $12,101 — Top Profit |
| East Austin | $21,738 | 980 | ≈$10K |
| South Congress | $21,399 | 977 | ≈$10K |
| Round Rock | $18,277 | 818 | ≈$8K |

-  Downtown  leads in revenue ($26,769) — confirmed  Top Branch 
-  The Domain  leads in profit ($12,101) despite being #2 in revenue — a margin-mix story worth investigating
-  Round Rock  is the lowest performing branch in both revenue and orders

### Product Performance
| Category | Revenue Share |
|----------|---------------|
| Pizza | 59.21% (≈$67K) |
| Combos | 18.04% (≈$20K) |
| Sides | 13.64% (≈$15K) |
| Beverages | 4.92% |
| Desserts | 4.19% |

-  BBQ Chicken  is the top product by revenue ($17,205) and profit (≈$8.3K)
-  Soda  sells the most units (1,156) but cheap drinks contribute little revenue
-  Lowest selling  products by quantity: Iced Tea (163), Brownie Sundae (207), Potato Wedges (235)

### Customer Behaviour
| Channel | Orders | Percentage |
|---------|--------|------------|
| Delivery | 1,764 | 35.28% |
| Dine-in | 1,680 | 33.60% |
| Takeaway | 1,556 | 31.12% |

-  Delivery  narrowly leads — consistent with a dinner-focused pizza business
-  Avg Basket Size: 2.00  items per order, stable across all categories
-  Saturday (1,058 orders)  is the busiest day;  Tuesday (551)  is the slowest
-  February (865 orders)  — lowest month |  May (1,130)  — highest month

### Payment Distribution
| Payment | Orders | Percentage |
|---------|--------|------------|
| Card | 2,069 | 41.38% |
| Apple Pay | 1,192 | 23.84% |
| Cash | 897 | 17.94% |
| Google Pay | 842 | 16.84% |

-  Card is clearly dominant  at 41.38% — digital wallets (Apple Pay + Google Pay) combine for another ~40%
- Cash is under 18% — typical for a US quick-service chain

### Time Analysis
| Metric | Value |
|--------|-------|
| Peak Hour | 20 (8 PM) |
| Peak Day | Saturday ($22,562) |
| Evening Revenue | 37.87% — highest time slot |
| Night Revenue | 26.96% |
| Afternoon Revenue | 29.10% |
| Morning Revenue | 6.06% |
| Weekday Revenue | ≈$71K (62.60%) |
| Weekend Revenue | ≈$42.5K (37.40%) |

-  Evening + Night = 64.83%  of revenue — pizza is a dinner business
-  Weekend contributes 37.4%  of revenue from just 2 days of the week
-  May  is the highest revenue month ($24,838),  February  the lowest ($20,620)

### Quick Analysis Page
-  6 Metrics:  Total Sales, Total Profit, Total Orders, Total Quantity, Avg Order Value, Profit Margin Percentage
-  9 Dimensions:  Branch, Category, Product, Customer Type, Payment Mode, Day, Time of Day, Weekend/Weekday, Month
- Every chart updates  instantly  when metric or dimension is selected
- This makes the page act like  54 different charts in one  (6 × 9)

---

## Project Structure

```
13_SliceMetric-Pizza-Analytics/
│
├── README.md                                ← You are here
│
├── raw-data/
│   ├── slicemetric_orders.csv               ← 5,000-row dataset (self-generated)
│
├── powerbi/
│   ├── SliceMetric_Pizza_Analytics.pbix     ← Power BI 7-page dashboard
│
├── background/
│   ├── SliceMetric_Background.pptx          ← PowerPoint custom backgrounds
│
└── Screenshots/
    ├── 1_Home.png                           ← Landing / Navigation page
    ├── 2_Executive_Overview.png
    ├── 3_Product_Performance.png
    ├── 4_Customer_Behaviour.png
    ├── 5_Branch_Performance.png
    ├── 6_Time_Analysis.png
    └── 7_Quick_Analysis.png
```

---

## Dataset

| Property | Value |
|----------|-------|
|  Source  | Self-created pizza chain dataset (Python, seed 42 — fully reproducible) |
|  Period  | January – May 2025 |
|  Total Records  | 5,000 orders |
|  Branches  | 5 Austin, TX locations (Downtown, The Domain, South Congress, East Austin, Round Rock) |
|  Products  | 17 |
|  Categories  | Pizza, Sides, Beverages, Desserts, Combos |
|  Key Fields  | Order ID, Order Date, Order Time, Hour, Day, Month, Weekend/Weekday, Time of Day, Branch, Product Name, Category, Unit Price, Quantity, Sales, Profit, Customer Type, Payment Mode |


The dataset is  self-generated in Python  (pandas + numpy) using weighted controlled randomness, so the data tells a realistic business story instead of looking uniformly random.

---

---

Dinesh Kundnani   
Data Analyst | Power BI · SQL · Excel · Python
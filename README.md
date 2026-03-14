# 👟 Adidas Sales Dashboard — Power BI

> A multi-page interactive Power BI dashboard analyzing Adidas US sales performance across time, region, product, and retailer dimensions.

---

## 📌 Project Overview

This dashboard provides a comprehensive view of Adidas sales data through **5 report pages**, combining KPI cards, trend analysis, product performance metrics, and custom icon-based navigation. It was built to support data-driven decisions across revenue, cost, profit, and order metrics.

---

## 🗂️ Dashboard Pages

### 1. 🏠 Main Page — Executive Summary
The landing page offers a high-level snapshot of the business.

- **KPI Cards** — Total Revenue, Total Cost, Total Profit, # Orders & # Products
- **3 Donut Charts:**
  - Products by Region
  - Retailers by Product
  - Orders by Region
- **Ribbon Chart** — Profit & Cost breakdown by Product (ranked over time)
- **Waterfall Chart** — Monthly Profit trend showing gains/losses
- Custom **Adidas logo** and branded image elements

---

### 2. 📈 Time Series Analysis
Tracks performance over time with temporal slicers and variance cards.

- **KPI Summary Card** — Revenue, Profit, Cost, Units Sold, AOV (Average Order Value)
- **Line Chart** — Revenue vs. Profit by Quarter
- **Clustered Column Chart** — Total Cost by Month
- **Variance Cards** — `varCost`, `varProfit`, `varRevenue`, `VarUS` (period-over-period deltas)
- **Slicers** — Filter by **Year** and **Month**
- **Icon Buttons** — Filter 🔍 and Remove Filter ❌ buttons using custom PNG icons

---

### 3. 🛍️ Product Performance Analysis
Deep-dives into product and regional performance.

- **YoY% Cards** — Year-over-Year % change for Cost, Profit, and Revenue
- **Avg Daily Cards** — Average Daily Cost & Average Daily Profit
- **Pivot Table** — Profit breakdown by Region × Product
- **Clustered Bar Chart** — Profit by Product
- **Clustered Column Chart** — # Products by Region
- **Gauge Charts** — Revenue vs. Target & Profit vs. Target (with avg benchmarks)
- **Donut Chart** — Orders by Product
- **Slicers** — Filter by **Product**, **Region**, and **Retailer**
- **Icon Image Buttons** — Retailer 🏪, Product 📦, Region 🌍 slicer triggers via custom PNGs

---

### 4. 🔖 Tooltip — Time (ToolTipsFor Time)
A tooltip page activated on hover for time-based visuals.

- **Action Button** for tooltip trigger
- Custom text label for contextual insight display

---

### 5. 📊 Tooltip — Revenue Comparison (ToolTopTime2)
A second tooltip page for quarterly revenue comparison.

- **Clustered Column Chart** — Current Revenue vs. Last Year Revenue by Quarter (`CurrentRev & LYRev`)

---

## 🖼️ Custom Icons Used

Custom PNG icons were registered as static resources inside the `.pbix` file and used as image visuals and interactive slicer buttons:

| Icon File | Purpose |
|---|---|
| `revenue.png` | Revenue KPI visual |
| `profit.png` | Profit KPI visual |
| `reduction.png` | Cost/Reduction indicator |
| `capital.png` | Capital/Cost icon |
| `order.png` | Orders KPI |
| `calendar.png` | Date/Time slicer label |
| `month.png` | Month slicer label |
| `filter.png` | Apply Filter button |
| `filter_(1).png` | Remove Filter button |
| `add-product.png` | Product slicer trigger |
| `timetable.png` | Time series visual icon |
| `storefront.png` | Retailer slicer trigger |
| `country.png` | Region slicer trigger |

> All icons are embedded directly in the `.pbix` file under `Report/StaticResources/RegisteredResources/`.

---

## 📐 DAX Measures Used

The following calculated measures were built to power the dashboard:

| Measure | Description |
|---|---|
| `Revenue` | Total sales revenue |
| `Total_Cost` | Total cost of goods sold |
| `total_Profit` | Revenue minus cost |
| `#Orders` | Count of orders |
| `#Products` | Count of distinct products |
| `#Retailers` | Count of distinct retailers |
| `Total_UnitSold` | Total units sold |
| `AOV` | Average Order Value |
| `varRevenue` | Revenue variance (period-over-period) |
| `varCost` | Cost variance |
| `varProfit` | Profit variance |
| `VarUS` | Units sold variance |
| `YoY%Rev` | Year-over-Year % Revenue growth |
| `YoY%Cost` | Year-over-Year % Cost change |
| `YoY%profit` | Year-over-Year % Profit growth |
| `AvgDailyProfit` | Average daily profit |
| `AvgDailyCost` | Average daily cost |
| `MAX_Revenue` | Maximum revenue (gauge target) |
| `avg_Revenue` | Average revenue (gauge benchmark) |
| `MAX_profit` | Maximum profit (gauge target) |
| `avg_profit` | Average profit (gauge benchmark) |

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|---|---|
| **Power BI Desktop** | Dashboard design and publishing |
| **DAX** | Custom calculated measures and KPIs |
| **Power Query (M)** | Data transformation and shaping |
| **Custom PNG Icons** | Interactive slicer buttons and KPI visuals |
| **Power BI Tooltips** | Hover-based contextual charts |

---

## 📁 File Structure

```
Adidas_Dashboard_Analysis.pbix
├── Report/
│   ├── Layout                    # All page/visual definitions (UTF-16 JSON)
│   ├── LinguisticSchema          # Q&A language schema
│   └── StaticResources/
│       ├── SharedResources/
│       │   └── BaseThemes/       # Power BI theme (CY24SU10)
│       └── RegisteredResources/  # Custom icon PNGs (13 icons)
├── DataModel                     # Compressed data model
├── Settings                      # Report settings
├── Metadata                      # Report metadata
├── SecurityBindings              # RLS / security config
├── DiagramLayout                 # Data model diagram layout
└── [Content_Types].xml           # OOXML content type manifest
```

---


---

## 📸 Dashboard Preview

| Page | Description |
|---|---|
| `MainPage` | Executive KPI summary |
| `TimeSeries Analysis` | Revenue & cost over time |
| `Product Performance Analysis` | YoY metrics, gauges, product breakdown |

---

## 👤 Author

**Mohammed Weal**
- 💼 www.linkedin.com/in/mohammed-weal
- 🐙 https://github.com/mohammedweal2

---

## 📄 License

This project is for portfolio and educational purposes. Dataset used is publicly available Adidas US Sales data.

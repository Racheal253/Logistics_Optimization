# 🚚 Logistics Command Center — Power BI Analytics Platform

> **End-to-end supply chain intelligence platform delivering unified, real-time visibility across suppliers, transportation modes, and operational performance** — mirroring the shipment tracking and logistics analytics solutions built for 3PL transporters, fleet managers, and shippers.

---

## 📌 Project Overview

Logistics teams routinely operate with fragmented data spread across multiple transportation modes (Air, Rail, Road, Sea), suppliers, and disconnected operational systems. This fragmentation makes it virtually impossible to monitor shipment performance, identify delivery risks proactively, or optimize routes in real time.

This project addresses that challenge head-on by delivering a **multi-layer Power BI analytics platform** structured across three analytical tiers — **Executive**, **Diagnostic**, and **Root Cause** — each purpose-built to answer different operational questions at different levels of the organization.

---

## 🖥️ Dashboard Architecture

The platform follows a deliberate three-layer drill-down architecture, enabling stakeholders at every level to extract actionable intelligence from the same unified data model.

### Layer 1 — Executive Dashboard: *Logistics Command Center*
High-level KPIs and financial performance metrics for C-suite and operations leadership.


| Metric | Value | Benchmark / Status |
|---|---|---|
| Order Fulfillment Quality | 17% | ⚠️ Gap identified |
| Operational Efficiency Ratio | 8.74% | ✅ Under <15% benchmark |
| Revenue Performance | $110K (18 orders) | — |
| Delivery Performance | 72% | ⚠️ $32.42K revenue at risk |
| Cost of Quality Failures | $3.82K | — |

**Visuals included:**
- Revenue to Profit Waterfall Analysis ($110.34K → $100.7K net, isolating shipping, manufacturing, and operational cost leakage)
- Product Category Margin Analysis (Cosmetics, Skincare, Haircare — gross profit vs. total revenue)

---

### Layer 2 — Diagnostic Dashboard: *Operational Performance Deep Dive*
Granular operational metrics for supply chain managers and logistics analysts.

| Metric | Value | Target / Status |
|---|---|---|
| Inventory Performance | $243.86K (4,777 units) | — |
| Supplier Lead Time | 17 days | ⚠️ 2 days over 15-day target |
| Shipping Velocity (Slowest Mode) | 6 days avg — Sea at 7 days | — |
| Shipping Cost Efficiency | $5.55 per unit | ⚠️ $0.55 over $5.00 target |

**Visuals included:**
- Additional Cost Distribution by Product & Transportation Mode (decomposition tree: Skincare $22K, Haircare $17K, Cosmetics $13K; Rail $4.85K, Road $3.84K, Sea $2.59K)
- Supplier Quality Performance Index (Supplier 4: 100% → Supplier 1: 51.9% inspection fail rate ranking)

---

### Layer 3 — Root Cause Dashboard: *Supplier Performance & Risk Analysis*
Supplier-level diagnostics and risk intelligence for procurement and fleet management teams.

**Visuals included:**
- **Total Cost of Supplier Quality Failures** — operational cost vs. quality failure cost impact with true total cost trend line across all 5 suppliers
- **Supplier Cycle Time Breakdown** — stacked bar decomposing Avg Lead Time, Avg Manufacturing Time, and Avg Shipping Days per supplier (e.g., Supplier 2: 24 + 17 + 2 days)
- **Transportation Mode Risk Matrix** — heat map of high-risk supplier–transport combinations across Air, Rail, Road, and Sea
- **Supplier Priority Efficiency vs. Fix Priority Score** — scatter plot enabling strategic supplier prioritization decisions

---

## 📊 Key Business Impact

**Operational Efficiency**
- Identified $8.74K in operational cost inefficiencies through waterfall analysis, directly informing cost reduction initiatives
- Flagged 2-day supplier lead time variance (17 actual vs. 15-day target), enabling targeted SLA renegotiations
- Surfaced $0.55 per-unit shipping cost overrun, prompting route and carrier optimization reviews

**Supplier Intelligence**
- Reduced supplier evaluation time from days to minutes by delivering instant visibility into quality performance indexes ranging from 51.9% to 100% across 5 suppliers
- Decomposed cycle time into lead, manufacturing, and shipping components, enabling precise identification of delay sources per supplier

**Risk Management**
- Quantified $32.42K revenue at risk from delivery performance gaps, enabling proactive intervention
- Transportation Mode Risk Matrix empowered fleet managers to instantly identify high-risk supplier–transport combinations, cutting route planning time by approximately 60% and improving delivery predictability
- Automated inventory performance tracking with overstock and stock-out alerting to optimize working capital allocation

---

## 🛠️ Technologies & Technical Approach

| Component | Detail |
|---|---|
| **Visualization** | Power BI Desktop & Service |
| **Data Modeling** | Star Schema (fact and dimension tables) |
| **DAX** | Advanced measures — running totals, variance calculations, dynamic KPI thresholds, conditional formatting logic |
| **Data Layer** | SQL (data extraction, transformation, and loading) |
| **Semantic Model** | Centralized Power BI semantic model with row-level and field-level filtering |
| **Interactivity** | Cross-filtering, drill-through, slicers (Location, Product Type), dynamic benchmarks |

### Data Model Highlights
- **Fact tables:** Orders, Shipments, Quality Failures, Costs
- **Dimension tables:** Suppliers, Products, Transportation Modes, Locations, Date
- Dynamic DAX measures for Operational Efficiency Ratio, Revenue at Risk, Supplier Quality Performance Index, and Cycle Time Breakdowns
- Conditional color logic on all KPI cards (red/green threshold indicators) built entirely in DAX without external tools

---

## 📁 Project Structure

```
logistics-command-center/
│
├── /Reports
│   ├── Logistics_Command_Center.pbix       # Main Power BI report file
│
├── /Data
│   ├── logistics_data.sql                  # Source data queries
│   └── data_dictionary.md                  # Field definitions and business rules
│
├── /Screenshots
│   ├── executive_dashboard.png
│   ├── diagnostic_dashboard.png
│   └── root_cause_dashboard.png
│
└── README.md
```

---

## 🚀 Getting Started

**Prerequisites**
- Power BI Desktop (latest version recommended)
- SQL Server or compatible database engine (for live connection)
- Access credentials to the logistics data source

**Steps**
1. Clone this repository
2. Open `Logistics_Command_Center.pbix` in Power BI Desktop
3. Navigate to **Transform Data → Data Source Settings** and update the connection string to point to your data source
4. Refresh the dataset
5. Use the **Location** and **Product Type** slicers to filter views by operational scope

---

## 💡 Use Cases

This platform is directly applicable to organizations operating in:
- **Third-Party Logistics (3PL)** — multi-client shipment tracking and SLA monitoring
- **Fleet Management** — transportation mode risk evaluation and route optimization
- **Procurement & Supply Chain** — supplier performance benchmarking and cycle time analysis
- **Operations Leadership** — executive-level P&L visibility from revenue to net profit

---

## 📸 Dashboard Previews

**Executive Dashboard**

<img width="1306" height="728" alt="Screenshot 2025-12-04 171716" src="https://github.com/user-attachments/assets/8a9d64e4-efdb-43b9-a92c-53053d61c0cc" />


**Diagnostic Dashboard**
<img width="1311" height="726" alt="Screenshot 2025-12-04 171753" src="https://github.com/user-attachments/assets/d242fd4c-09dd-4018-a59d-063acbc00078" />



**Root Cause & Supplier Analysis**
<img width="1307" height="740" alt="Screenshot 2025-12-04 180329" src="https://github.com/user-attachments/assets/1b3c24ab-6d7d-4d6c-bbb0-23c0f25ad250" />


## 📬 Contact

If you have questions about this project or want to discuss supply chain analytics solutions, feel free to connect.

---

*Built to demonstrate end-to-end supply chain analytics capabilities aligned with enterprise logistics platforms.*

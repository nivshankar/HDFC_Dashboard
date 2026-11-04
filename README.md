<div align="center">

# 🏦 HDFC Bank Banking Analytics Dashboard
### *Interactive Power BI Report — Deposits vs Targets, Loan Portfolio & Branch Performance*

[![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures_%26_KPIs-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Excel](https://img.shields.io/badge/Microsoft_Excel-Source_Data-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/en-us/microsoft-365/excel)
[![Data Model](https://img.shields.io/badge/Data_Model-Relational_Design-0078D4?style=for-the-badge&logo=powerbi&logoColor=white)](https://powerbi.microsoft.com/)

<br/>

> *"Data isn't just numbers on a grid — visualize it well, and it becomes a strategy that drives decisions."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [🔺 Page 1 — Deposits vs Targets](#-page-1--deposits-vs-targets)
- [🔺 Page 2 — Loan Portfolio](#-page-2--loan-portfolio)
- [🔺 Page 3 — Branch Performance](#-page-3--branch-performance)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **HDFC Bank Banking Analytics Dashboard** is a three-page interactive Power BI report that gives management a consolidated view of **deposit mobilisation**, **loan portfolio health**, and **branch network performance**. Every page carries its own set of dropdown slicers (Financial Year, Quarter, Region, Zone, Branch Name and more), a **Clear Filters** button, and KPI cards that show current-year values alongside previous-year comparisons.

All pages carry the data-as-on stamp **30 Apr 2025** and share a consistent navy-and-red HDFC-branded theme with a left-hand navigation panel.

This project is designed to:
- Track total deposits against targets and measure achievement % and year-on-year growth
- Monitor the loan book, active loans, EMI collections and NPA % in one place
- Rank and compare branches across Region → Zone → City → Branch hierarchies
- Visualise geographic distribution of deposits, loans and branches on interactive maps
- Surface auto-written **Key Insights** panels for quick executive reading

---

## 🎯 Problem Statement

> **Objective:** Build an interactive Power BI dashboard that helps bank leadership monitor deposit performance against targets, understand loan portfolio quality, and identify top and bottom performing branches across regions and zones.

A large retail bank operating hundreds of branches needs to answer questions such as: *Are we meeting deposit targets? Which products and regions drive growth? How healthy is the loan book? Which branches are leading and which are lagging?*

| 📂 Page | 📄 Focus | 🔍 Core Question Answered |
|--------|---------|---------------------------|
| Deposits vs Targets | Deposit mobilisation | Are deposits meeting targets, and where is growth coming from? |
| Loan Portfolio | Lending & asset quality | How large is the loan book, and how healthy is it (EMI, NPA)? |
| Branch Performance | Network efficiency | Which branches, zones and regions perform best? |

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 🎛️ **Page-specific Slicers** | Financial Year, Quarter, Month, Region, Zone, Branch Name, Product Type / Loan Product / Branch Type |
| 🧹 **Clear Filters Button** | One-click reset of all slicers on every page |
| 🏷️ **Dynamic KPI Cards** | Current-year value, previous-year value and % change (green ▲ / red ▼ indicators) |
| 📉 **Trend Analysis** | Monthly actual vs target columns, plus Year › Quarter › Month drill-down line charts |
| 🍩 **Composition Charts** | Donut charts for product mix, loan status and transaction types; treemap for loan products |
| 🗺️ **Geographic Maps** | Bubble maps showing Delhi, Ahmedabad, Surat, Pune, Mumbai, Hyderabad, Bengaluru and Chennai |
| 🧮 **Hierarchical Tables** | Expandable Region › Zone › City › Branch matrices with conditional metrics |
| 💡 **Key Insights Panels** | Text summaries of the most important findings on the Deposits and Branch pages |
| 🧭 **Left Navigation** | Quick page switching between Deposits vs Targets, Loan Portfolio and Branch Performance |

---

## 🏗️ Project Structure

```
📦 HDFC-Bank-PowerBI-Dashboard/
│
├── 📊 HDFC_Bank_Dashboard.pbix        ← Power BI report file (3 pages)
├── 🗂️ Data/                           ← Source data files (deposits, loans, branches, transactions)
│
├── 📁 Assets/                         ← Screenshot assets for documentation
│   ├── 🖼️ Deposits_vs_Targets.png     ← Page 1 screenshot
│   ├── 🖼️ Loan_Portfolio.png          ← Page 2 screenshot
│   └── 🖼️ Branch_Performance.png      ← Page 3 screenshot
│
└── 📄 README.md                       ← Project documentation
```

> **How to open:**
> ```
> 1. Install Power BI Desktop (free): https://powerbi.microsoft.com/desktop
> 2. Open HDFC_Bank_Dashboard.pbix in Power BI Desktop
> 3. If prompted, re-point the data source to the files in the Data/ folder
> 4. Use the slicers on each page and the left navigation to explore
> ```

---

## 🔄 Project Workflow

```
Source Data  (Deposits · Loans · Branches · Transactions)
       │
       ▼  Import & clean in Power BI (Power Query)
  Data Model  (Date / Region / Zone / City / Branch / Product dimensions)
       │
       ├──▶  DAX Measures Created
       │     Total Deposits · Deposit Target · Achievement % · YoY Growth %
       │     Total Loan Book · Active Loans · EMI Collection · NPA %
       │     Total Branches · Total Transactions · Avg Transaction Value · Branch Rank
       │
       ├──▶  Page 1: Deposits vs Targets
       │     ├── 7 slicers + Clear Filters
       │     ├── 4 KPI cards (Total Deposits / Target / Achievement % / YoY Growth)
       │     ├── Actual vs Target column chart · Deposit trend line · Product donut · Map
       │     └── Branch hierarchy table + Key Insights
       │
       ├──▶  Page 2: Loan Portfolio
       │     ├── 6 slicers + Clear Filters
       │     ├── 4 KPI cards (Loan Book / Active Loans / EMI Collection / NPA %)
       │     ├── Treemap · Outstanding by product bar · EMI trend line
       │     └── Geography map · Loan status donut · Branch hierarchy table
       │
       └──▶  Page 3: Branch Performance
             ├── 6 slicers + Clear Filters
             ├── 4 KPI cards (Branches / Transactions / Avg Value / Best Branch)
             ├── Branch map · Deposits by hierarchy · Transactions trend · Type donut
             └── Branch hierarchy table with rank + Key Insights
```

---

## 🔺 Page 1 — Deposits vs Targets

### 📝 1. Page Architecture

This page measures how deposit mobilisation is tracking against targets. Seven dropdown slicers (**Financial Year, Quarter, Month, Region, Zone, Branch Name, Product Type**) sit at the top, followed by four KPI cards, four visuals and a hierarchical performance table.

![Deposits vs Targets Dashboard](Assets/Deposits_vs_Targets.png)

---

### 🗺️ 2. KPI Cards

| KPI Card | Value | Previous Year | Change |
|----------|-------|---------------|--------|
| 💰 **Total Deposits** | **₹ 50,046M** | ₹ 33,321M | ▲ 50.19% |
| 🎯 **Deposit Target** | **₹ 4,93,210M** | ₹ 3,29,258M | ▲ 49.79% |
| 📊 **Achievement %** | **110.15%** | Vs Target: 100 | ▲ 10.15% |
| 📈 **YoY Deposit Growth** | **50.19%** | — | — |

---

### 📊 3. Visuals

| Visual | Description |
|--------|-------------|
| **Actual Deposit vs Target (Monthly)** | Clustered columns comparing actual deposits (navy) against target (red) month by month, from Jan 2023 to Sep 2024, with a scroll bar |
| **Deposit Trend (Year › Quarter › Month)** | Drillable line chart across FY 2023-24, 2024-25 and 2025-26 quarters (range ≈ ₹4,100M – ₹4,240M) |
| **Deposit By Product Type** | Donut chart (₹ 50bn centre) — Current 25.16%, Salary 24.98%, Savings 24.96%, Fixed Deposit 24.89% |
| **Graphic Deposits Distribution** | Bubble map of deposits by city across India |
| **Deposit Performance By Branch Hierarchy** | Expandable table: Region › Zone › City › Branch with Total Deposits, Target, Variance, Achievement % and YoY Growth % |

---

### 💡 4. Key Insights (shown on dashboard)

- Total deposits have exceeded the target (Achievement: **110.15%**)
- **Current Accounts** contribute the highest share (**25.16%**) of total deposits
- **Central region** is the top performer in deposit mobilisation
- **HDFC Branch 5** has the highest deposit amount among all branches

---

## 🔺 Page 2 — Loan Portfolio

### 📝 5. Page Architecture

The Loan Portfolio page breaks down the lending book by product, status and geography, and tracks collection efficiency and asset quality. Slicers: **Financial Year, Quarter, Region, Zone, Branch Name, Loan Product**.

![Loan Portfolio Dashboard](Assets/Loan_Portfolio.png)

---

### 🗺️ 6. KPI Cards

| KPI Card | Value | Previous Year | Change |
|----------|-------|---------------|--------|
| 💼 **Total Loan Book** | **₹ 3,75,668M** | ₹ 2,50,194M | ▲ 50.15% |
| 🧾 **Active Loans** | **78K** | 63K | ▲ 23.25% |
| 💳 **EMI Collection** | **₹ 3,827M** | ₹ 2,549M | ▲ 50.11% |
| ⚠️ **NPA %** | **5.00%** | 5.00% | ▼ 0.00% |

---

### 📊 7. Visuals

| Visual | Description |
|--------|-------------|
| **Loan Portfolio By Product** | Treemap — Business Loan ₹75,570M, Vehicle Loan ₹75,381M, Education Loan ₹74,990M, Home Loan ₹74,987M, Personal Loan ₹74,739M |
| **Outstanding Loan Amount By Product** | Horizontal bars for Business, Vehicle, Education, Home and Personal loans (axis ₹0 – ₹80bn) |
| **EMI Collection Trend** | Drillable line chart (Year › Quarter › Month) showing a downward trend from ≈ ₹32bn to ≈ ₹30bn |
| **Loan Exposure by Geography** | Bubble map of loan exposure across major cities |
| **Loan Status Distribution** | Donut chart (₹ 376bn centre) — Current 80.96%, Delayed 10.06%, NPA 5.01%, Closed |
| **Branch Hierarchy Table** | Region › Zone › City › Branch with Total Loan Book, EMI Collection and NPA % |

---

## 🔺 Page 3 — Branch Performance

### 📝 8. Page Architecture

The Branch Performance page evaluates the branch network on transactions, deposits and achievement, and ranks branches. Slicers: **Financial Year, Quarter, Region, Zone, Branch Name, Branch Type**.

![Branch Performance Dashboard](Assets/Branch_Performance.png)

---

### 🗺️ 9. KPI Cards

| KPI Card | Value | Previous Year | Change |
|----------|-------|---------------|--------|
| 🏢 **Total Branches** | **500** | — | — |
| 🔁 **Total Transactions** | **500K** | 333K | ▲ 49.97% |
| 💵 **Avg Transaction Value** | **₹ 250.17K** | ₹ 250.35K | ▼ 0.07% |
| 🏅 **Best Branch** | **HDFC Branch 112** (West Zone) | — | Target Achievement: 147.3% |

---

### 📊 10. Visuals

| Visual | Description |
|--------|-------------|
| **Branch Network Performance** | Bubble map showing branch presence across Indian cities |
| **Deposits by Branch Hierarchy** | Horizontal bars ranking North, South, Central, West and East (₹0 – ₹10bn axis) |
| **Transactions Trend** | Line chart by Quarter and Year (2023–2025), values between ≈ 40,800 and 42,200 |
| **Transaction Type Distribution** | Donut (500K centre) across EMI, ATM, RTGS, NEFT, Withdrawal, UPI and Deposit |
| **Deposit Performance By Branch Hierarchy** | Table with Total Deposits, Total Loan Book, Total Transactions, Achievement % and Branch Rank |

---

### 💡 11. Key Insights (shown on dashboard)

- Total transactions have grown by **49.97%** compared to the previous year
- **HDFC Branch 112 (West Zone)** is the top performing branch at **147.3%** target achievement
- **North region** has the highest deposits among all regions
- Transactions are spread fairly evenly across **7 types** (EMI, ATM, RTGS, NEFT, Withdrawal, UPI and Deposit)

---

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| 🟡 **Power BI Desktop** | Latest | Report authoring, data modelling, DAX and publishing |
| 📐 **DAX** | Built-in | Measures for deposits, targets, achievement %, growth %, NPA %, rank |
| 🧰 **Power Query** | Built-in | Data cleaning and transformation |
| 🎛️ **Slicers & Bookmarks** | Built-in | Dropdown filters, Clear Filters button and page navigation |
| 🗺️ **Bing Maps Visual** | Built-in | Geographic bubble maps |
| 🗂️ **Excel / CSV** | Source | Raw deposit, loan, branch and transaction data |
| 🎨 **Report Theme** | Custom | HDFC navy-and-red branding with left navigation panel |

---

## 📈 Results & Insights

| Insight | Value |
|---------|-------|
| 💰 Total Deposits | **₹ 50,046M** (▲ 50.19% YoY) |
| 🎯 Deposit Target Achievement | **110.15%** — target exceeded by 10.15 pts |
| 🏆 Highest Deposit Product | **Current Accounts** — 25.16% share |
| 🏆 Top Deposit Region | **Central** |
| 💼 Total Loan Book | **₹ 3,75,668M** (▲ 50.15% YoY) |
| 🧾 Active Loans | **78K** (▲ 23.25% YoY) |
| ⚠️ NPA Ratio | **5.00%**, flat versus previous year |
| ✅ Loans in Current Status | **80.96%** |
| 🏢 Branch Network | **500 branches** |
| 🔁 Total Transactions | **500K** (▲ 49.97% YoY) |
| 🥇 Best Branch | **HDFC Branch 112**, West Zone — 147.3% achievement |
| 🧭 Top Region by Deposits | **North** (Branch Performance page) |
| 📅 Data As On | **30 Apr 2025** |

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 💼 **Executive Ready** | Branded, single-screen pages suitable for management reviews |
| ⚡ **Real-Time Filtering** | KPIs, charts, maps and tables all respond to slicer changes instantly |
| 🔀 **Three-Lens View** | Deposits, loans and branches analysed in one report |
| 🔎 **Drill-Down Capability** | Year › Quarter › Month trends and Region › Zone › City › Branch tables |
| 🗺️ **Geographic Context** | Maps reveal regional concentration at a glance |
| 💡 **Built-in Narrative** | Key Insights panels translate numbers into plain language |
| 🖥️ **No Code Required** | Built entirely in Power BI Desktop and shareable as a `.pbix` file |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 👤 Author

<div align="center">

### [Your Name]

> *"Data transformed into structure becomes insight; insight transformed into strategy becomes growth."*

**🎓 Role:** Data Analyst | Power BI & Excel Specialist \
**📍 Location:** India \
**🛠️ Skills:** Power BI · DAX · Microsoft Excel · Data Visualisation · Dashboard Design · Data Modelling

</div>

---

## 🙏 Acknowledgements

- 📚 [Power BI Documentation](https://docs.microsoft.com/en-us/power-bi/) — Official Power BI Desktop and DAX reference
- 🟡 [Microsoft Power BI Community](https://community.powerbi.com/) — Dashboard design tips and DAX guidance
- 🎓 [SQLBI — DAX Guide](https://dax.guide/) — DAX function and measure reference
- 💬 [Stack Overflow Community](https://stackoverflow.com/) — Problem-solving support

---

<div align="center">

---

*Made with ❤️ and ☕ — Last updated: 4 November, 2026*

</div>

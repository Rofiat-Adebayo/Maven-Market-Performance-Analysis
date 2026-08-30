# Maven Market Performance Analysis

> **A retail performance analysis investigating whether Maven Market is meeting its commercial targets, what is driving performance, and where management attention should be focused.**

### Tools & Technologies

![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-F2C811?logo=powerbi&logoColor=black)
![Microsoft Excel](https://img.shields.io/badge/Excel-Data%20Analysis-217346?logo=microsoftexcel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Transformation-2F75B5)
![DAX](https://img.shields.io/badge/DAX-Data%20Modeling-F2C811)


## Table of Contents

- [Executive Summary](#executive-summary)
- [Business Problem](#business-problem)
- [Dataset Summary](#dataset-summary)
- [Analytical Framework](#analytical-framework)
- [Data Model & Relationships](#data-model--relationships)
- [Defining the Metrics](#defining-the-metrics)
- [Analysis & Key Findings](#analysis--key-findings)
  - [1. Transaction Performance](#1-transaction-performance)
  - [2. Revenue Performance](#2-revenue-performance)
  - [3. Geographic Performance](#3-geographic-performance)
  - [4. Product & Profitability Analysis](#4-product--profitability-analysis)
  - [5. Revenue Trend](#5-revenue-trend)
  - [6. Returns Analysis](#6-returns-analysis)
- [Turning Findings Into Decisions](#turning-findings-into-decisions)
- [Dashboard Design](#dashboard-design)
- [Tools Used](#tools-used)
- [Reflection](#reflection)
- [Conclusion](#conclusion)

---

# Executive Summary

Maven Market had plenty of transactional data, but answering a more important question required more than reporting sales totals:

> **Is the business actually performing well, and what is driving that performance?**

I approached this project from the perspective of an analyst supporting retail management decisions.

Rather than treating **revenue, transactions, profit, and returns** as isolated KPIs, I connected them to business targets, products, locations, and time to understand where performance was coming from, whether there were areas of concern, and where management attention should be focused.

The analysis showed that Maven Market recorded **18,325 transactions against a target of 17,339**, placing transaction performance approximately **5.7% above target**.

Revenue also reached approximately **$120K against a $119K target**.

However, the more important story was underneath those headline figures.

Performance was concentrated across particular cities and brands, several leading brands generated profit margins above **58%**, revenue strengthened toward the final months of the year, and the overall return rate remained close to **1%**.

This shifted the analysis from simply asking:

**“How much did Maven Market sell?”**

to answering:

> **Where is performance coming from, what could threaten it, and where should the business focus next?**

---

## Dashboard Preview

<img width="619" height="335" alt="!executive" src="https://github.com/user-attachments/assets/c1187d06-d150-4960-a24e-27f59585e88e" />


### Interactive Dashboard

[View the Interactive Power BI Dashboard](https://app.fabric.microsoft.com/reportEmbed?reportId=db57360e-feed-4601-96e9-c80339ea9061&autoAuth=true&ctid=37d7521a-5079-48af-9131-4ac2cb6f1e3a)



---

# Business Problem

The management challenge was not simply to measure sales, but to determine whether Maven Market's performance was sustainable, where it was coming from, and which areas required attention.

A positive headline KPI can hide important differences across products, locations, profitability, and returns. I therefore framed the analysis around one central question:

> **How well is Maven Market performing against its commercial goals, what is driving the results, and where should management focus its attention?**

To investigate this, I focused on seven supporting questions:

1. Is Maven Market meeting its transaction and revenue targets?
2. Which products and brands contribute most strongly to performance?
3. Are high-volume products also generating strong margins?
4. Which locations are driving transaction activity?
5. How is performance changing over time?
6. Are returns creating a meaningful commercial risk?
7. What actions should management consider based on the evidence?


# Dataset Summary

The analysis uses Maven Market retail data covering transactions, products, customers, stores, geographic regions, returns, and calendar information.

<img width="213" height="483" alt="!tablws" src="https://github.com/user-attachments/assets/ee7a0fa6-6e24-4fd7-b522-8c5a4d5dc741" />

Rather than treating the files as independent datasets, I first considered how each table contributed to the business questions.

| Dataset | Analytical Purpose |
|---|---|
| Transactions | Core sales activity and transaction-level performance |
| Products | Product, brand, cost, and retail-price analysis |
| Customers | Customer-level attributes and segmentation |
| Stores | Store-level performance and location context |
| Regions | Geographic analysis across markets |
| Returns | Product-return behaviour and return-rate analysis |
| Calendar | Consistent time-based analysis and comparisons |

The transaction data formed the core of the commercial analysis, while the remaining datasets provided the context needed to explain **who purchased, what was purchased, where activity occurred, when it happened, and whether products were returned**.

This structure allowed the analysis to move beyond simple transaction totals and investigate the drivers behind business performance.

---

# Analytical Framework

Before building the dashboard, I structured the investigation around four analytical layers.

## 1. Performance

The first question was whether the business was performing successfully.

I evaluated:

**Transactions → Revenue → Profit → Profit Margin → Returns → Performance vs Target**

This established the executive-level view of commercial health.

---

## 2. Drivers

Once overall performance was established, I investigated:

> **What is actually driving these results?**

Performance was broken down across:

**Country → Region → City**

and:

**Brand → Product**

This made it possible to identify whether strong overall results were broadly distributed or concentrated within particular parts of the business.

---

## 3. Time

Performance without historical context can be misleading.

I therefore analysed transactions and revenue across time to identify:

- changes in commercial activity,
- stronger and weaker periods,
- month-to-month movement,
- and potential seasonal signals.

---

## 4. Risk

Finally, I incorporated product returns into the analysis.

Strong sales can appear positive while product returns quietly reduce their commercial value.

Return rate was therefore analysed alongside revenue, transactions, and profitability to provide a more balanced view of business performance.

---

# Data Model & Relationships

To support analysis across products, customers, stores, geography, returns, and time, I structured the data into a relational model centred around Maven Market's transactional activity.

The objective was not simply to connect tables.

The model needed to allow the same business measures to remain consistent as users moved between different levels of analysis.

## Data Model

<img width="946" height="476" alt="!Modelling" src="https://github.com/user-attachments/assets/c4c44ae5-5844-44c6-9e54-d98dd5c679a1" />

The model connects transaction and return activity with supporting dimension tables containing product, customer, store, geographic, and calendar attributes.

This structure supports analysis across:

**Business → Country → Region → City**

as well as:

**Business → Brand → Product**

A dedicated calendar table also provides a consistent time dimension for monthly, weekly, and period-based comparisons.

### Why This Model Matters

The model was designed to support:

- consistent filtering across business dimensions;
- product and brand-level profitability analysis;
- geographic analysis from market to city/store level;
- time-intelligence calculations;
- transaction and return analysis;
- reusable business measures;
- and drill-down analysis without duplicating business logic.

This meant the dashboard could move from an executive KPI to the underlying product, geographic, or temporal driver while maintaining consistent calculations.

---

# Defining the Metrics

Before designing the dashboard visuals, I defined the measures required to answer the business questions.

The core metrics included:

| KPI | Business Question |
|---|---|
| Total Transactions | How much purchasing activity is occurring? |
| Revenue | How much value is being generated from sales? |
| Profit | How much value remains after product cost? |
| Profit Margin | Which sales generate stronger commercial value? |
| Return Rate | How much sales activity is potentially being reversed? |
| Transaction Target | Are transaction goals being achieved? |
| Revenue Target | Is revenue meeting expectations? |
| Variance to Target | How far above or below target is performance? |

These measures were developed using **DAX** so they could respond dynamically to filters across products, geography, and time.

This introduced an important analytical distinction.

**18,325 transactions** is a reporting number.

But:

**18,325 transactions vs. a target of 17,339**

is a performance measure.

The second tells management whether the result is actually good.

That distinction between **reporting a number and evaluating a number** became central to the analysis.

---

# Analysis & Key Findings


<img width="619" height="335" alt="!executive" src="https://github.com/user-attachments/assets/c1187d06-d150-4960-a24e-27f59585e88e" />

## 1. Transaction Performance

Maven Market recorded:

### **18,325 Transactions**

against a target of:

### **17,339 Transactions**

This placed transaction performance approximately **5.7% above target**.

At an executive level, this indicates that commercial activity was ahead of the expected benchmark.

However, exceeding the target was only the starting point.

The next question was:

> **What parts of the business were responsible for that performance?**

That led the investigation into geography, products, and profitability.

---

## 2. Revenue Performance

Revenue reached approximately:

### **$120K**

against a target of approximately:

### **$119K**

Maven Market therefore met its revenue benchmark.

However, the relatively narrow positive variance is also important.

Meeting target and significantly outperforming target are not the same thing.

Management should therefore continue monitoring whether the gap between actual revenue and target is:

- widening,
- remaining stable,
- or beginning to contract.

This provides a more useful view of commercial momentum than treating target achievement as a simple yes/no KPI.

---

## 3. Geographic Performance

Transaction activity was not distributed equally across locations.

Cities including:

- Vancouver
- Portland
- Tacoma
- Los Angeles
- Zacatecas

showed stronger transaction activity.

Rather than treating this simply as a ranking exercise, I interpreted geographic concentration as a resource-allocation question.

If particular markets consistently generate higher transaction volumes, management may need to evaluate whether those locations require different:

- inventory levels,
- replenishment strategies,
- staffing capacity,
- marketing investment,
- or performance targets.

The geographic analysis therefore connects transaction behaviour directly to operational planning.

---

## 4. Product & Profitability Analysis

High sales volume does not automatically mean high commercial value.

I therefore evaluated product and brand performance alongside profitability rather than relying only on transaction counts.

Brands including:

- Hermanos
- Ebony
- Tell Tale
- Tri-State

generated profit margins above **58%**.

This distinction matters because two brands can generate similar sales volumes while contributing very different levels of profit.

The analysis suggests that product decisions should therefore consider both:

> **Demand + Margin**

rather than sales volume alone.

High-margin brands with strong demand may deserve greater attention when management considers product assortment, promotion, and inventory allocation.

---

## 5. Revenue Trend

Revenue strengthened toward the final months of the year, particularly during the **October–December period**.

This creates a potentially useful planning signal.

However, I would not automatically classify this as established seasonality from the available evidence.

Instead, I interpret it as:

> **A seasonal signal that should be validated using additional years of historical data.**

If the same pattern appears consistently across multiple years, it could have important implications for:

- inventory planning,
- promotional calendars,
- supplier preparation,
- staffing,
- and revenue forecasting.

This distinction is important because the data shows **what happened**, while additional evidence would be required to establish **whether the pattern reliably repeats**.

---

## 6. Returns Analysis

The overall return rate remained close to:

### **1%**

At an aggregate level, this suggests that returns were not materially offsetting the positive commercial performance observed during the period.

However, an overall return rate can hide product-level problems.

A company could maintain a healthy overall return rate while a particular:

- product,
- brand,
- category,
- or location

experiences unusually high returns.

Return behaviour should therefore continue to be monitored at more granular levels as an early-warning indicator of possible:

- product-quality issues,
- customer dissatisfaction,
- fulfilment problems,
- or product-market mismatch.

---

# Turning Findings Into Decisions

The analysis was designed to finish with business decisions rather than dashboard observations.

| Finding | Business Implication | Recommended Action |
|---|---|---|
| Transactions are ~5.7% above target | Commercial activity is currently ahead of expectations | Identify the products and markets sustaining the positive variance |
| Revenue is only slightly above target | Performance is positive but has a limited buffer | Monitor target variance and investigate opportunities for stronger revenue growth |
| Transaction activity is concentrated geographically | Certain markets contribute disproportionately to sales activity | Align inventory, staffing, and local marketing with demand |
| Several brands generate >58% margins | Some product lines create significantly stronger commercial value | Consider margin alongside demand when prioritising products |
| Revenue strengthened toward year-end | There may be a recurring high-demand period | Validate the pattern with additional historical data before changing seasonal strategy |
| Return rate is ~1% | Returns currently appear controlled | Monitor product and brand-level return rates for emerging issues |

---

# Dashboard Design

The Power BI dashboard was designed as the **decision layer** of the analysis rather than the starting point.

The user journey follows:

> **Overall Performance → Trend → Geography → Product → Returns**

This allows management to start with the health of the business and progressively investigate the factors behind the headline KPIs.

### Dashboard Capabilities

**Executive Monitoring**

Track transactions, revenue, profit, returns, and performance against targets.

**Trend Analysis**

Evaluate how commercial performance changes across weeks and months.

**Geographic Analysis**

Compare transaction activity across countries, regions, cities, and stores.

**Product Analysis**

Investigate brands, products, margins, and return behaviour.

**Diagnostic Analysis**

Use interactive filters, tooltips, and drill-through functionality to investigate the drivers behind headline performance.

---

## Dashboard

<!-- Replace with your actual dashboard image -->

![Maven Market Performance Dashboard](images/maven-market-dashboard.png)

[Explore the Interactive Dashboard](YOUR_POWER_BI_LINK_HERE)

---

# Tools Used

| Tool | Application |
|---|---|
| **Power BI** | Data modelling, analysis, visualisation, and dashboard development |
| **Power Query** | Data preparation and transformation |
| **DAX** | KPI calculations, target comparisons, profitability, and analytical measures |
| **Excel** | Initial data inspection and exploratory analysis |

---

# Reflection

The most important lesson from this project was learning to move beyond **reporting what happened** and investigate **why it happened and what it means for the business**.

Throughout the analysis, I learned to challenge headline KPIs rather than accept them at face value. A result could be above target but still have limited headroom; strong transaction volume could be concentrated in only a few markets; and high sales activity did not automatically mean strong profitability.

I also became more deliberate about separating:

> **What the data shows → What the evidence suggests → What still needs to be validated**

The year-end revenue increase was a good example. The data showed stronger performance between October and December, but the available evidence was not enough to confidently label it a recurring seasonal pattern.

That distinction reinforced an important analytical principle for me: **the strength of a conclusion should match the strength of the evidence behind it.**

---

# Conclusion

Maven Market's headline performance was positive: transactions were approximately **5.7% above target**, revenue exceeded its benchmark, several brands generated strong margins, and the overall return rate remained controlled.

The deeper analysis, however, showed why those headline numbers needed context. Performance varied across locations, products, profitability, and time,  revealing where the business was strongest and where further investigation could improve decision-making.

The project ultimately reinforced that effective analytics is not about producing more charts or reporting more KPIs. It is about connecting **business questions, evidence, and decisions**.

> **The dashboard was the output. The real work was determining what questions the data needed to answer.**




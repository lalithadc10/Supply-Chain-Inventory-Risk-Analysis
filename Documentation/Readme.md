# Analytical Documentation

This document explains the analytical approach used to transform raw supply-chain data into an executive inventory and risk dashboard.

---

## 1. Business Problem

The objective was to identify the operational factors that can increase inventory and stockout risk.

The analysis focused on four major areas:

- Demand variability
- Supplier lead-time variability
- Inventory replenishment risk
- Impact of supply-chain disruptions

The final objective was to convert these findings into actionable management insights.

---

## 2. PROVE Framework

The analysis was structured using the PROVE framework.

### P — Problem

Identify the key supply-chain risks affecting inventory availability and replenishment decisions.

### R — Research

Review the dataset to understand:

- SKU-level demand
- Supplier relationships
- Inventory levels
- Supplier lead times
- Reorder conditions
- Forecast performance

### O — Observe

The analysis identified:

- Several SKUs are supported by multiple suppliers.
- Supplier lead times vary across suppliers.
- SKU demand shows meaningful variability.
- Some inventory records fall below their reorder point.
- Disruption scenarios can significantly increase replenishment requirements.

### V — Validate

The observations were converted into measurable metrics and validated using Excel calculations, Pivot Tables and scenario analysis.

Key metrics included:

- Demand CV
- Supplier Lead-Time CV
- Supplier Count
- Safety Stock
- Lead-Time Demand
- Reorder Point
- Forecast Error

### E — Execute

The analytical results were converted into an executive dashboard containing:

- KPI cards
- Supplier lead-time analysis
- Inventory reorder health
- SKU demand risk
- Scenario impact
- Management actions

---

# 3. Analytical Methodology

## 3.1 Demand Analysis

For each SKU, average daily demand and demand standard deviation were calculated.

Demand variability was measured using the Coefficient of Variation:
## 3.2 Supplier Analysis
Supplier performance was evaluated using:

- Average Lead Time
- Lead-Time Standard Deviation
- Lead-Time CV
- Supplier Count by SKU

Lead-Time CV was calculated as:
Lead-Time CV = Lead-Time Standard Deviation / Average Lead Time

## 3.3 Inventory Risk Analysis

Inventory risk was evaluated by comparing inventory conditions against the calculated reorder requirement.

The analysis focused on:

- Records below the reorder point
- SKUs with higher demand variability
- Supplier-dependent replenishment risks
- Potential stockout exposure

A key finding was:

**4,787 records, representing approximately 5.25%, were below the reorder point.**

These records represent a measurable replenishment exposure and should receive management attention.

---

## 3.4 Supplier-SKU Relationship

The analysis identified that several SKUs are supported by multiple suppliers.

Multiple suppliers can provide sourcing flexibility and reduce dependency on a single supplier.

However, supplier count alone does not determine supplier risk.

Supplier diversification should be evaluated together with:

- Average Lead Time
- Lead-Time Variability
- Supplier Reliability
- Demand Requirements

This provides a more complete view of supply continuity risk.

---

## 3.5 Safety Stock Model

Safety stock was calculated to protect inventory against demand and supply uncertainty while maintaining the selected service level.

The model incorporated:

- Average Daily Demand
- Demand Standard Deviation
- Average Lead Time
- Lead-Time Standard Deviation
- Service Level
- Z Score

## 3.6 Scenario Analysis

Excel Scenario Manager was used to evaluate how changes in operating conditions could affect replenishment requirements.

Four scenarios were created:

| Scenario          | Demand Change | Lead-Time Delay |
| ----------------- | ------------: | --------------: |
| Baseline          |            0% |          0 days |
| Demand Surge      |          +10% |          0 days |
| Supplier Delay    |            0% |         +3 days |
| Severe Disruption |          +20% |         +5 days |


| Scenario          | Reorder Point |
| ----------------- | ------------: |
| Baseline          |         ≈ 215 |
| Demand Surge      |         ≈ 237 |
| Supplier Delay    |         ≈ 283 |
| Severe Disruption |         ≈ 394 |

The scenario analysis demonstrates that both demand increases and supplier delays can materially increase replenishment requirements.

Under the Severe Disruption scenario, the reorder requirement increases from approximately 215 units to 394 units.

This highlights the importance of contingency inventory planning.

## 3.7 Forecast Performance

Forecast performance was incorporated into the analysis using forecast-error metrics.

The executive dashboard reports an approximate forecast error of:

16.32%

Forecast error provides an additional indicator of demand-planning uncertainty.

Higher forecast error can increase the difficulty of determining appropriate inventory and replenishment requirements.

Therefore, forecast accuracy should be monitored alongside demand variability and inventory risk.

## 4. Scenario Manager

Scenario Manager was used as a decision-support tool rather than simply as a calculation exercise.

The model allows management to compare the baseline situation with potential operating disruptions.

Scenarios Evaluated
Baseline

Represents normal operating conditions.

Demand change: 0%
Lead-time delay: 0 days
Demand Surge

Represents an increase in customer demand.

Demand change: +10%
Lead-time delay: 0 days
Supplier Delay

Represents a supplier experiencing additional delivery time.

Demand change: 0%
Lead-time delay: +3 days
Severe Disruption

Represents a combined demand and supply disruption.

Demand change: +20%
Lead-time delay: +5 days

The scenario comparison demonstrates how quickly inventory requirements can increase when operating conditions deteriorate.

## 5. Executive Dashboard

The final analytical results were converted into an executive-level dashboard.

The dashboard was designed to answer four management questions:

How much inventory and demand activity are we handling?
Where is replenishment risk concentrated?
Which suppliers or SKUs require attention?
What happens if demand or supply conditions deteriorate?

## 5.1 KPI Cards

The dashboard contains four primary KPI cards:

Total Units Sold: 1,829,979
Average Inventory: 471.5
Below Reorder: 5.25%
Forecast Error: 16.32%

These KPIs provide a high-level snapshot of supply-chain performance and risk.

## 5.2 Supplier Lead-Time Analysis

A horizontal bar chart compares average supplier lead times.

The analysis shows supplier lead times ranging approximately from:

7.0 to 8.6 days

Suppliers with relatively longer lead times should be reviewed because longer replenishment cycles can increase inventory requirements and stockout exposure.

## 5.3 Inventory Reorder Health

A donut chart compares inventory records:

Above Reorder
Below Reorder

The analysis shows:

94.75% Above Reorder
5.25% Below Reorder

Although the majority of records are above the reorder point, the below-reorder population represents a specific replenishment risk that requires attention.

## 5.4 SKU Demand Risk

The demand-risk chart highlights SKUs based on their Demand CV.

The analyzed SKUs show CV values of approximately:

44%–47%

A higher CV indicates greater demand variability relative to average demand.

These SKUs may require closer monitoring and appropriate safety-stock protection.

## 5.5 Scenario Impact

The scenario chart compares the Reorder Point across different operating conditions.

The model shows:

Baseline          → ≈ 215 units
Demand Surge      → ≈ 237 units
Supplier Delay    → ≈ 283 units
Severe Disruption → ≈ 394 units

This provides management with a visual representation of the potential inventory impact of disruption.

## 6. Interactive Dashboard

The executive dashboard includes interactive controls for:

Warehouse
Region
Supplier
Date

These controls allow users to filter the dashboard and examine different operational segments.

The supporting analysis remains separated from the executive presentation so that the dashboard remains clean and management-focused.

## 7. Management Actions & Key Insights

-The analysis was converted into practical management recommendations.

#Replenishment

-Prioritize records currently below the reorder point to reduce potential stockout exposure.

#Supplier Risk

-Review suppliers with longer or more variable lead times and evaluate backup sourcing options where commercially feasible.

#Demand Variability

-Monitor SKUs with higher Demand CV and ensure that inventory buffers reflect their demand uncertainty.

#Supplier Diversification

Where multiple suppliers support an SKU, evaluate supplier performance and use supplier diversification as a potential risk-mitigation strategy.

#Disruption Planning

-Use Scenario Manager to estimate inventory requirements under demand surges and supplier delays.

#Forecast Monitoring

-Track forecast error regularly because inaccurate demand forecasts can affect replenishment decisions.

## 8. Excel Techniques Used

The project demonstrates practical Excel techniques across the complete analytical workflow.

Data Analysis
Excel Tables
XLOOKUP
FILTER
AVERAGEIFS
SUMIFS
STDEV.S
Statistical Analysis
Standard Deviation
Coefficient of Variation
Z Score
Forecast Error
Inventory Modeling
Lead-Time Demand
Safety Stock
Reorder Point
Service-Level Analysis
Reporting
Pivot Tables
Pivot Charts
Slicers
KPI Cards
Dashboard Design
Decision Analysis
Scenario Manager
Baseline vs Scenario comparison

## 9. Key Findings

The analysis produced four major findings.

1. Replenishment Exposure

Approximately 5.25% of records are below the reorder point.

These records should receive replenishment attention.

2. Supplier Lead-Time Variation

Average supplier lead times range approximately from 7.0 to 8.6 days.

Longer or more variable lead times can increase replenishment uncertainty.

3. Demand Uncertainty

SKU Demand CV values are approximately 44%–47%.

This indicates meaningful variability in demand and supports the need for appropriate inventory buffers.

4. Disruption Sensitivity

The scenario model shows the Reorder Point increasing from approximately:

215 units → 237 units → 283 units → 394 units

as operating conditions move from baseline to severe disruption.

## 10. Management Recommendations

Based on the analysis, management should consider the following actions:

| Risk Area               | Recommended Action                             |
| ----------------------- | ---------------------------------------------- |
| Below Reorder           | Prioritize replenishment                       |
| High Demand CV          | Review safety-stock levels                     |
| Long Supplier Lead Time | Evaluate supplier performance and alternatives |
| Multiple Suppliers      | Assess backup sourcing capability              |
| Forecast Error          | Improve demand forecasting                     |
| Severe Disruption       | Maintain contingency inventory plans           |

The objective is not simply to hold more inventory, but to position inventory where uncertainty and replenishment risk are highest

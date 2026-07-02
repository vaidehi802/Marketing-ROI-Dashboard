# Marketing Campaign ROI Dashboard

An interactive Power BI dashboard analysing marketing spend, revenue, and channel efficiency across Google, Meta, and Influencer campaigns — with a live budget-reallocation simulator.

![Overview page](screenshots/overview.png)

## Overview

This dashboard answers a single business question: **where should marketing budget go to maximise return?** It combines headline KPIs, per-channel comparison, and a what-if simulator that projects revenue as budget is shifted between channels.

Built with a sample marketing dataset. All figures are illustrative.

## Pages

**1. Overview**
Three headline KPI cards (Total Revenue, Total Ad Spend, Blended ROI) above three per-channel breakdowns — Customer Lifetime Value, Cost Per Lead, and ROI by channel.

**2. Channel Comparison**
A detailed table comparing all channels across spend, revenue, CPL, LTV, ROI, conversion rate, and LTV:CAC ratio — the core efficiency metrics side by side.

**3. Budget Reallocation Simulator**
An interactive what-if tool. A slider adjusts the share of budget shifted toward Google; the dashboard recalculates projected revenue in real time and surfaces the resulting uplift.

![Simulator page](screenshots/simulator.png)

## Key metrics and logic

- **Blended ROI** = (Total Revenue − Total Spend) / Total Spend
- **LTV:CAC** — customer lifetime value relative to acquisition cost, used to rank channel efficiency (Google ~15x, Meta ~8x, Influencer ~4.5x)
- **Projected Revenue** — driven by a What-If parameter that models revenue response as budget shifts
- **Revenue Uplift** = Projected Revenue − Current Revenue

## Techniques used

- DAX measures for ROI, uplift, and dynamic aggregation
- What-If parameter for interactive scenario modelling
- Custom dark theme with consistent styling across pages
- Card, clustered-column, and table visuals with formatted data labels

## Key insight

Channels show near-parity on raw ROI (all roughly 2x return), so the real differentiator is **customer quality**, captured by LTV:CAC. The simulator suggests that shifting ~14% of budget toward the highest-efficiency channel (Google) projects a revenue uplift of ~$4.2M.

> Note: the simulator uses efficiency-weighted allocation and does not model diminishing returns — it flags the *direction* of reallocation, not an exact prescription.

## Files

- `Marketing_ROI_Dashboard.pbix` — the Power BI file
- `data/` — sample dataset
- `screenshots/` — dashboard page images

## Tools

Power BI Desktop · DAX

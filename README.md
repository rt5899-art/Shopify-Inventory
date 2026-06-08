# Shopify Inventory and Revenue Analysis 

## Project Overview

This repository contains a specialized data analytics project built to track supply chain metrics, financial health, and product segment popularity for a Shopify-based fragrance retail operation. The primary purpose of this project is to unify disparate transactional, inventory, and warehouse data into a single, cohesive reporting system. By tracking metrics such as total revenue, gross profit, and warehouse inventory volumes, the dashboard solves the problem of inventory capital tying up and unpredictable revenue pacing, empowering operations managers to make data-driven supply decisions.

### Requirements

Microsoft Power BI Desktop (Version 2.126 or higher recommended)

System memory: Minimum 8 GB RAM

Operating System: Microsoft Windows 10 or Windows 11

Data Source File: Cleaned e-commerce sales ledger and warehouse stock matrices (CSV or Excel format)

### Tools and Technologies

Business Intelligence Platform: Microsoft Power BI

ETL Transformation Software: Power Query

Data Modeling Engine: DAX (Data Analysis Expressions)

Target Architecture: Single-file tabular data model

### Challenges Faced

Product Name Visualization Fit: The bar chart mapping gross profit across specific products suffered from extensive text truncation due to elongated naming conventions (e.g., Rose Luxe EDP, Vanilla Ember EDP). This layout issue was resolved by adjusting axis margins, implementing text wrap constraints, and shortening redundant strings in the underlying dataset during the transformation stage.

Warehouse Slicer Allocation Anomalies: Constructing warehouse filters (WH-BLR, WH-DELHI, WH-MUMBAI) initially generated blank results for closing stock values due to inconsistent outer joins between the inventory ledger and warehouse dimension tables. This was corrected by redesigning the data schema into a proper star schema with continuous relationship links.

Daily Trend Graph Flattening: Mapping revenue on a daily timeline across a compressed 35-day window led to extreme, unreadable spikes. A moving average rolling calculation was structured using DAX to soften erratic day-to-day revenue variations while preserving the true macro-level visual trend lines.

### Key Insights

From dashboard we can infer:

![image alt](https://github.com/rt5899-art/Shopify-Inventory/blob/main/ss-%20Shopify.png?raw=true)


An evaluation of the metrics processed across the analytical dashboard reveals the following insights into financial and inventory positions:

High-Level Financial Performance Indicators: The operation captured a Total Revenue of 368.84M, bringing in a Total Gross Profit of 66.39M. This establishes an overall Gross Margin percentage of 0.53. Meanwhile, capital tied up in stock reflects a Total Closing Inventory Value of 211.99M.

Fragrance Product Profitability: Rose Luxe EDP stands out as the most profitable individual product line, capturing 6.3M in gross profit. It is followed closely by Vanilla Ember EDP and Oud Royale EDP at 6.0M each, Musk Horizon EDP at 5.9M, and both Oud Royale EDP and Musk Horizon EDP sub-variants reaching 5.8M. The lowest profit segment among the top listings is Citrus Mist EDP at 4.8M.

Fragrance Family Demand Matrix: Evaluating volume distributions by fragrance family demonstrates a highly uniform sales pattern across the top groups. Musk Horizon, Oud Royale, and Rose Luxe lead market demand, each accounting for 16.9K units sold. Cedar Noir follows with 16.1K units, Vanilla Ember registers 15.9K units, and Citrus Mist yields the lowest demand profile at 14.2K units.

Extreme Warehouse Inventory Imbalance: The data highlights a severe centralization of inventory assets. The WH-BLR warehouse holds an overwhelming 211.99M (99.95%) of Total Units Sold and Closing Inventory Value, leaving remaining warehouse locations like WH-DELHI and WH-MUMBAI completely underutilized at an aggregate of just 0M (0.05%).

Temporal Revenue Velocity: Daily revenue flows maintain a relatively steady trajectory between 3M and 5M per day through the first 28 days of the cycle, experiencing a prominent peak near day 27. However, immediately following day 28, the operation experiences a sharp drop-off, tumbling to a cycle low near day 30 before attempting a minor baseline recovery.

### Recommendations for Improvements

Redistribute Capital Allocation From WH-BLR: Holding 99.95% of stock value (211.99M) inside a single geographic hub (WH-BLR) creates an severe supply chain vulnerability. A significant portion of this closing inventory should be reallocated to WH-DELHI and WH-MUMBAI to minimize regional fulfillment delays and mitigate localized logistics bottlenecks.

Investigate Post-Day 28 Revenue Collapse: The sharp collapse in daily revenue immediately following day 28 demands immediate cross-referencing with stock records. Operations should investigate if this downward trend was caused by localized stockouts of top-performing items like Rose Luxe EDP or if it points to a recurring payment gateway malfunction.

Optimize Fragrance Stock Levels Based on Margin Profiles: Citrus Mist brings in both the lowest volume (14.2K units) and the lowest individual gross profit (4.8M). Production priority and warehouse storage space should be reduced for Citrus Mist, freeing up operational capacity to support high-margin items like Rose Luxe EDP (6.3M profit) and top volume drivers like Musk Horizon (16.9K units).

Execute Targeted Campaigns for Mid-Tier Fragrances: Fragrance families like Cedar Noir (16.1K units sold) and Vanilla Ember (15.9K units sold) possess established consumer traction. Minor promotional adjustments or bundle offers could elevate these families to the premium 16.9K volume tier shared by Musk Horizon and Oud Royale.

# Shopify Inventory Analysis Project
## Project Overview
This project focuses on building a data-driven inventory management and analysis solution for an active Shopify store using Power BI. The primary goal is to help businesses optimize stock levels, track product demand trends, prevent costly stockouts, and reduce overstocking risks. By centralizing core sales and store operations metrics, the project empowers store owners to make actionable supply chain and merchandising decisions.

## Requirements
To deliver a scalable and highly professional business intelligence dashboard, the project fulfills the following explicit requirements:

Centralized Data Engine: Extraction and transformation of messy e-commerce store exports into a clean relational model.

Core Business Tracking: Implementation of standardized inventory Key Performance Indicators (KPIs) such as total stock on hand, product turnover velocity, stockout vulnerabilities, and capital tied up in inventory.

Granular Drill-Down Capability: The dashboard layout must allow users to evaluate high-level business health down to individual product options, variations, and Stock Keeping Units (SKUs).

Automated Data Processing: Data structures must support regular refreshes without manual remodeling or visual adjustment overhead.

## Tools and Technologies
Power BI Desktop: The core development platform used to construct the multi-page analytics report layout, customize design themes (utilizing CY24SU10 structures), and deploy the final interactive visual layer.

Power Query Engine (M Language): Used during data ingestion to orchestrate file content parsing, perform structural formatting, define explicit data types, and normalize variable product options.

Data Modeling: A robust star/snowflake schema tailored to e-commerce metrics, complete with dedicated dimension tables (e.g., product details, vendor metrics) and optimized fact tracking tables.

DAX (Data Analysis Expressions): Utilized to engineer customized measures, time intelligence patterns, and conditional formatting rules to surface critical inventory imbalances.

## Challenges Faced
Complex Multi-Variant SKU Architectures: E-commerce stores naturally handle highly complex product schemas containing hundreds of unique variant combinations (such as variations in sizes, colors, and designs). Parsing these unstructured rows into logical item relationships presented significant modeling hurdles.

Asynchronous Logistical Tracking: Aligning the timeline of incoming vendor shipments, real-time sales transactions, and historical inventory audits required building strict data mapping logic to ensure cross-table filtering operates seamlessly.

Visual Clutter Management: Presenting deep analytical data points (such as safety stock flags, vendor performance metrics, and sales velocities) without overwhelming an everyday operational user necessitated iterative user interface refinement and strict control over dashboard spatial distribution.

## Key Insights
Unbalanced Capital Allocation: A significant portion of the business's operating capital can easily get trapped in low-velocity, high-volume products while top-selling core assets frequently face near-stockout conditions.

Vendor Dependency Vulnerabilities: Specific supply lines show higher variations in reliability, which deeply compromises safety stock parameters. Isolating vendor-specific metrics exposes exactly which product lines present a high logistical risk.

Seasonal Demand Fluctuations: Mapping historical sales data against real-time stock levels highlights defined seasonal demand spikes. This visibility allows the business to transition from a reactive inventory stance to a proactive, predictive model.

## Recommendations for Future Improvements
Incorporate Real-Time API Connections: Transition away from static manual spreadsheet exports by configuring direct, real-time Shopify admin REST/GraphQL API connections into the Power BI semantic model. This ensures warehouse personnel look at truly live transactional figures.

Integrate Advanced Predictive Forecasting: Leverage built-in Power BI machine learning visualizations or integrate Python/R forecasting scripts to project future SKU demand based on rolling historical patterns, mitigating human error during reorder cycles.

Incorporate Warehouse Cost Factors: Add explicit columns tracking specific carrying costs, insurance fees, and obsolescence rates per cubic foot of warehouse space. This expansion converts basic inventory tracking into a holistic profitability center dashboard.

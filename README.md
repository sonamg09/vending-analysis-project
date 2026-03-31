# 📊 Industrial Vending AI: Predictive Demand & Inventory Optimization


## Executive Summary


This project provides an end-to-end solution for industrial supply chain management by transforming raw vending machine transaction logs into a Smart Restock Engine. By leveraging Machine Learning (Random Forest) and Statistical Optimization, the system predicts tool demand and automatically calculates high-precision inventory thresholds, ensuring that production never stops due to a missing tool.

Key Business Impacts
95% Service Level Guarantee: Implemented a Safety Stock buffer that accounts for "spiky" industrial demand, statistically reducing the risk of stockouts to less than 5%.

Predictive Precision: Achieved a Mean Absolute Error (MAE) of 2.29 units, allowing the system to distinguish between random noise and actual demand trends.

Automated Procurement Logic: Developed Reorder Points (ROP) for over 100+ SKUs, shifting the restocking process from "reactive/manual" to "proactive/automated."

Asset Utilization Insight: Identified high-variance items and device-specific usage patterns to optimize machine placement and SKU allocation.

## The Technical Workflow
### 1. Data Intelligence (Phase 1 & 2)
Cleaned and merged high-frequency dispense data with restock cost logs. Used Exploratory Data Analysis (EDA) to identify the "Pareto Top 10" SKUs that drive the majority of business value.

### 2. Feature Engineering (Phase 3)
Engineered Lag Features (t-1, t-7) and Rolling Averages to capture weekly seasonality. This allows the model to "understand" that demand on a Monday morning often correlates with the previous week's maintenance cycles.

### 3. Machine Learning Engine (Phase 4)
Deployed a Random Forest Regressor to predict daily demand. Unlike simple averages, this model accounts for the interaction between the time of the month, the specific device location, and previous usage spikes.

### 4. Inventory Optimization (Phase 5)
Translated predictions into Supply Chain Logic. Calculated:

**Safety Stock**: The emergency buffer required for each specific SKU.

**Reorder Point**: The exact inventory level that triggers a restock order.

**Target Fill Levels**: The optimal quantity to restock to minimize holding costs.
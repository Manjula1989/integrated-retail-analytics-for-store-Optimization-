# Integrated Retail Analytics for Store Optimization

**Prepared by:** Manjula M  
**Date:** 18-09-2025  
**Company / Department:** AI/ML  

## Project Objective
Analyze historical retail sales data, identify trends, and predict weekly sales for the next 8 weeks. This helps in inventory planning, optimizing store performance, and making data-driven decisions.

## Datasets Used
- **sales** – Weekly sales data by store and department.  
- **stores** – Store information including type and size.  
- **features** – External factors including temperature, CPI, fuel price, unemployment, and holiday flags.

## Data Cleaning & Preparation
- Converted `Date` column to datetime format.  
- Ensured `Store` and `Dept` columns are numeric.  
- Merged datasets into a single DataFrame.  
- Handled missing values and created lag and rolling features for historical sales.

## Exploratory Data Analysis (EDA)
- Total weekly sales trend over time shows seasonal fluctuations and holiday spikes.  
- Top 10 stores contribute the highest sales – identify key locations for focus.  
- Holiday weeks show higher average sales than non-holiday weeks.  
- CPI, Fuel Price, and Unemployment moderately affect weekly sales.  

Visualizations include: total weekly sales trends, top stores, holiday impact, and feature correlation heatmap.

## Feature Engineering
- **Time Features:** Year, Month, Week, DayOfWeek  
- **Lag Features:** Sales from previous week (`Sales_Lag_1`)  
- **Rolling Features:** 4-week rolling average (`Sales_Roll_4`)  

These features capture historical trends and seasonality, improving model accuracy.

## Model Training
- **Model Used:** LightGBM Regressor  
- **Train/Test Split:** Last 12 weeks used as test data  
- **Metrics:** MAE & RMSE for evaluation  
- Feature importance visualized for top predictors.

## Predictions
- Predicted weekly sales for the next 8 weeks for all stores and departments.  
- Identified top-performing stores for future inventory planning.  
- Visualizations include total predicted weekly sales and top stores by predicted sales.

## Recommendations
- Focus inventory and marketing efforts on top-performing stores.  
- Prepare stock ahead of holiday weeks to meet anticipated demand spikes.  
- Monitor key external features (CPI, Fuel Price) as they impact sales trends.  
- Use the trained model for rolling weekly forecasts to optimize inventory planning and store performance.

## Conclusion
- Historical sales data and external factors were successfully analyzed.  
- LightGBM model provided accurate short-term sales forecasts.  
- Insights enable data-driven decisions, reducing risks of overstock or understock.  
- Optional future work: Deploy a live dashboard (Power BI or Plotly Dash) for interactive forecasting.

## Files in Repository
- `integrated_retail_analytics.ipynb` – Full Colab notebook with code  
- `merged_master_dataset.csv` – Final merged dataset  
- `future_sales_predictions.csv` – 8-week sales forecast  
- `lightgbm_model.pkl` – Saved trained LightGBM model  

## GitHub Link
[[Your GitHub Repo Link Here]](https://github.com/Manjula1989/integrated-retail-analytics-for-store-Optimization-.git)


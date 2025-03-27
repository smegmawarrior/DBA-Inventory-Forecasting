# Data Analytics for E-Commerce 
### Optimizing Warehouse Stock Transfers to Prevent Stockouts  

**Collaborative project with an e-commerce partner to develop a data-driven inventory forecasting system for thousands of SKUs across multiple warehouse locations.**  
****(Note: Due to NDA, most data has been censored out)****
---

## Project Overview  
We designed a two-phase solution to:  

- **Predict demand** at the SKU-location level using time series forecasting.  
- **Generate transfer orders** that balance stockout prevention with operational constraints (logistics timelines, cash flow).  

### Key Challenges Addressed  
- **48 months** of daily transactional data (**7M+ records**) with heterogeneous demand patterns.  
- **Regional demand variability** across warehouses.  
- **Real-world business constraints** in inventory/ supply chain operations.  

---

## Technical Implementation  

### Phase 1: Demand Forecasting  

####  Data Pipeline  
- Consolidated and cleaned **7M+ daily records** using **Python** (`pandas`, `numpy`).  
- Developed **interactive Excel dashboards** for preliminary analysis.  

#### Exploratory Data Analysis  
Identified demand patterns by:  
- **Product category** (ABC analysis via Pareto distributions).  
- **Warehouse region** (geospatial demand clustering).  
- **Temporal factors** (seasonality decomposition using `statsmodels`).  
- **Outlier detection** using statistical methods (IQR, Z-score) and **visual analytics** (`Power BI`).  

#### Model Development  
Implemented and optimized multiple forecasting approaches:  
- **Moving Averages (MA)**  
- **Simple/Double Exponential Smoothing (SES/DES)**  
- **Holt-Winters (HW) triple exponential smoothing**  

**Custom model selection per SKU based on:**  
- **Demand volume** (high vs. low velocity).  
- **Demand pattern stability** (trend/seasonality detection).  

#### Evaluation Framework  
Assessed models using **robust error metrics**:  
- **RMSE** (emphasizes large errors).  
- **MAE** (interpretable unit-scale accuracy).  
- **sMAPE / MAPE** (relative error for cross-SKU comparison).  

**Classified forecasts into:**  
-  **Healthy** (meets all accuracy thresholds).  
-  **Warning** (partial metric deviations).  
-  **Unfit** (requires model redevelopment).  

---

## 🛠Tech Stack  
 **Python** (`pandas`, `statsmodels`, `scikit-learn`) | **Excel** (pivot analysis) | **Power BI** (visual storytelling) | **Adobe Illustrator** (executive presentations)  

---
### Phase 2: Inventory Management  


### Repository Contents  
- `data_preprocessing.ipynb` → Data cleaning & transformation  
- `forecasting_models.ipynb` → Model training & evaluation  
- `visualization_dashboard.pptx` → Summary insights & findings  



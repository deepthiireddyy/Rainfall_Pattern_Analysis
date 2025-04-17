# Rainfall_Pattern_Analysis

## PROJECT TITLE: 
**Rainfall Pattern Analysis and Forecasting Using CHIRPS: A Case Study for Andaman & Nicobar Islands**

## Overview:
This project investigates the spatiotemporal variability and forecasting of rainfall patterns over the Andaman and Nicobar Islands using CHIRPS satellite-based data from **2013 to 2024**. It aims to address the challenges of limited ground station availability by integrating geospatial analysis, statistical trend detection, machine learning models, and spatial interpolation techniques.

---

## Objectives:
- To assess monthly, annual, and seasonal rainfall anomalies using CHIRPS data.
- To identify rainfall intensity and variability patterns in the region.
- To perform clustering and classification based on rainfall characteristics.
- To forecast monthly rainfall using LSTM neural networks.
- To map spatial rainfall distribution using interpolation methods.

---

## Data Used:
- **CHIRPS v2.0**
  - Climate Hazards Group InfraRed Precipitation with Station Data
  - Daily resolution, 0.05° (~5 km) grid
  - Downloaded from Google Earth Engine
  - Study Perios: **2013-2024**
 
- **Shapefile of Andaman and Nicobar Islands**
  - Used for masking and spatial extraction

---

## Tools & Technologies
- **Python 3.10**
  - Pandas, NumPy, Matplotlib, Scikit-learn, Keras (TensorFlow backend)
- **QGIS 3.28**
  - For spatial preprocessing and mapping

---

## Methodology
1. **Data Preprocessing**
   - Merging daily CHIRPS '.csv' files
   - Removal of NaNs and formatting for analysis
     
2. **Anomaly Detection**
   - Monthly, seasonal, and annual anomalies against 11-year climatology (2013-2024)
     
3. **Trend Analysis**
   - Linear regression applied to identify long-term rainfall trends

4. **Rainfall Intensity Classification**
   - Light (<20 mm), Moderate (20-60 mm), Heavy (60-100 mm), Very Heavy (>100 mm)
  
5. **Clustering**
   - K-Means (k=3) on seasonal rainfall totals to classify temporal zones
  
6. **Rainfall Variability Index (RVI)**
   - RVI = standard deviation / mean; classified as low, moderate, high, very high
  
7. **Forecasting**
   - LSTM model with two layers, dropout, Adam optimizer, and MSE loss
   - Forecasted monthly rainfall for 2025
  
8. **Spatial Interpolation**
   - Inverse Distance Weighted (IDW) interpolation in QGIS as well as Python
   - Rainfall zones mapped from extracted CHIRPS station data
  
---

## Key Findings
- **No significant long-term trend** in annual rainfall, but **variability has increased**.
- **Heavy rainfall events** are less frequent; **light/moderate rainfall events** have increased.
- Clear **spatial differences** in rainfall behavior between southern, middle, and northern islands.
- LSTM forecasting provides reliable monthly rainfall estimates for future planning.
- IDW-based maps reveal hydrological zones and support localized agricultural strategy.

---

## Folder Structure
<pre> ``` Rainfall_Pattern_Analysis/ ├── CHIRPS_Andaman_Data/ # CHIRPS .csv files for 2013–2024 ├── ROI_Shapefile/ # Shapefile of the A&N Region ├── Report/ # Project Report (contact author if needed) ├── Rainfall_Pattern_Analysis_code.ipynb # Google Colab Notebook with full analysis └── README.md # This file ``` </pre>

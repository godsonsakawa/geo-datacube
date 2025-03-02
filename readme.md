# 🌍 Sentinel Data Reprojection & Integration

 This project involves loading, resampling, and reprojecting multi-source remote sensing data, including **Sentinel-1 (VV, VH Radar Backscatter)**, **Sentinel-2 (NDVI)**, **ERA5 Temperature**, and **Elevation Data**.
 The final goal is to integrate them into a unified dataset.

---

## 📌 Features
 Load Sentinel-1 (VV, VH) and Sentinel-2 (NDVI) rasters  
 Load temperature data from ERA5 and elevation from OpenTopo  
 Reproject all datasets to a common CRS (**EPSG:4326**)  
 Optimize reprojection using **nearest resampling** and **chunking**  
 Save results as GeoTIFF files for further analysis  

---

## 📂 Data Sources
- **Sentinel-1**: VV & VH (Radar Backscatter)  
- **Sentinel-2**: NDVI (Vegetation Health)  
- **ERA5 Temperature**: Climatic variations  
- **OpenTopo**: Elevation data  

---

## 🚀 Reprojection Optimization
To enhance performance, the project applies:  
✔ **Nearest resampling** for categorical data (Radar Backscatter)  
✔ **Chunking with Dask** to avoid memory issues  
✔ **CRS standardization (EPSG:4326)** for all datasets  

---

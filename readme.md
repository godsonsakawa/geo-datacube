
 This project involves loading, resampling, and reprojecting multi-source remote sensing data, including **Sentinel-1 (VV, VH Radar Backscatter)**, **Sentinel-2 (NDVI)**, **ERA5 Temperature**, and **Elevation Data**.
 The final goal is to integrate them into a unified dataset.

---

1. Define the Area of Interest (AOI) & Time Range

- Focuses on the region experiencing land use and climate changes.
- Use bounding box coordinates (min/max lat/lon).


2. Query the STAC API for Required Datasets - done
- Fetches cloud-hosted remote sensing data efficiently.
- Uses pystac-client to search for:
- Sentinel-1 (VV, VH - Radar Backscatter)
- Sentinel-2 (NDVI - Vegetation Health)
- ERA5 (Temperature - Climatic Variations)
- DEM (Elevation - Terrain Impact)

3. Load Data as Raster Arrays - need help to modify my code here
-  Converts remote files into numerical arrays for analysis.
-  Uses rioxarray to open raster files.


4. Reproject Data to a Common Spatial Reference System (CRS) ** 
-  Ensures datasets align spatially before integration.
-  Uses rioxarray.rio.reproject() to match the highest resolution dataset’s CRS.


5. Integrate Datasets into a Datacube ** 
-  Creates a structured, multi-dimensional dataset for analysis.
-  Uses xarray.Dataset() to merge layers (VV, VH, NDVI, Elevation).


6. Save the Datacube in a Portable Format (NetCDF)
-  datacube.to_netcdf("datacube.nc")

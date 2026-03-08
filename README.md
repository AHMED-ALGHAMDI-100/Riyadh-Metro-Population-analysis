# 
Riyadh Metro Connectivity vs. Population Density Analysis (2025-2026)

##  Project Overview
This project performs a high-level **Geospatial Analysis** to evaluate the strategic alignment between the **Riyadh Metro Network** and the city's actual **Population Density**. By overlaying transit nodes onto demographic heatmaps, we visualize how effectively the infrastructure serves high-demand residential and commercial zones.

###  Key Analysis Insights
* **Service Accessibility**: Identification of "Hotspots" where metro stations intersect with areas exceeding 80 persons per 100m².
* **Hub Efficiency**: Implementation of coordinate "Jitter" to accurately represent multi-line transfer hubs (e.g., KAFD, Olaya) without data overlap.
* **Gap Identification**: Visualizing high-density areas that lack direct metro access, suggesting potential needs for future feeder bus integration.

---

##  Dataset Sources
The analysis integrates two primary high-fidelity data sources:

1.  **Riyadh Metro Stations (RCRC)**:
    * **Source**: Riyadh Royal Commission / Saudi Open Data Portal.
    * **Data**: Geospatial coordinates (Latitude/Longitude), official line colors, and station classifications for all 6 lines.
2.  **High-Resolution Population Density (WorldPop)**:
    * **Source**: WorldPop (University of Southampton).
    * **Data**: 100m x 100m gridded population estimates for 2025, clipped specifically to the Riyadh metropolitan area.



---

##  Tech Stack & Libraries
This project utilizes a specialized Python geospatial pipeline:

* **`GeoPandas`**: For managing vector data structures and performing spatial joins.
* **`Rasterio`**: Used for processing GeoTIFF population data, including masking, clipping, and coordinate transformation.
* **`Folium`**: For generating initial interactive web maps to validate station placement.
* **`Matplotlib` & `Seaborn`**: For rendering final static heatmap overlays using professional color palettes like `YlOrRd`.
* **`NumPy`**: For data cleaning, outlier capping (Normalization), and implementing the coordinate "Jitter" logic.

---

## 🚀 How to Run
1. Clone the repository.
2. Ensure `metro_stations.csv` and the Riyadh population `GeoTIFF` are in the root directory.
3. Install dependencies: `pip install geopandas rasterio folium matplotlib seaborn numpy`.
4. Run the Jupyter Notebook to generate the heatmap overlay.

---

# 🚚 Big Data Logistics: Urban Spatial Blind-Spot Detection

**TL;DR:** Built a highly optimized big data spatial pipeline using DuckDB and OSMnx to analyze massive urban networks and identify unmapped Points of Interest (POIs) disconnected from deliverable road infrastructure.

* **Role:** Spatial Data Engineer
* **Tools:** Python • `DuckDB` (Big Data) • `OSMnx` (Network Routing) • `GeoPandas`

## 🚨 The Problem
Last-mile logistics and emergency routing algorithms fail catastrophically when destination coordinates (Points of Interest) are physically disconnected from the mapped road network. In rapidly developing urban centers, identifying these "spatial anomalies" using standard pandas dataframes requires massive computational overhead and frequently causes out-of-memory crashes.

## 🛠️ The Approach
* **Network Extraction:** Utilized `OSMnx` to programmatically extract the true, navigable street network for the target urban area directly from OpenStreetMap data.
* **Big Data Engine:** Deployed `DuckDB` to handle out-of-core spatial data processing, allowing the pipeline to analyze massive arrays of geographic coordinates natively using SQL logic without overwhelming local RAM.
* **Proximity Calculation:** Engineered a high-speed spatial join pipeline to calculate the exact metric distance from millions of commercial and residential POIs to the nearest edge of the street network.

## 📈 The Results
* Successfully isolated "blind-spot anomalies"—locations sitting more than 100 meters from a known road—preventing automated routing algorithms from generating impossible delivery paths.
* Demonstrated enterprise-level big data competency by replacing slow, iterative spatial loops with highly optimized, vectorized spatial SQL queries.

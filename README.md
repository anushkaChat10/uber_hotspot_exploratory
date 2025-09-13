# 🚖 Uber Hotspots — Exploratory Data Analysis & Clustering

## 📌 Purpose
The purpose of this project is to analyze Uber trip data and identify **hotspots** where demand is highest.  
By clustering pickup locations and analyzing time patterns, we can recommend areas and times where drivers are more likely to find rides.  

This helps drivers:
- Maximize earnings by being in the right place at the right time.
- Reduce idle time spent waiting for passengers.
- Visualize demand patterns across different hours and days.

---

## ❓ Why This Project
Ride-hailing companies like Uber generate massive amounts of trip data.  
However, drivers often lack clear insights into **where and when demand is concentrated**.  
This project aims to bridge that gap using:
- **Data cleaning** → ensures reliable insights from raw data.
- **Feature engineering** → extracts meaningful time patterns (hour, weekday, weekend).
- **Clustering algorithms** → groups pickup locations into hotspots.
- **Geospatial visualization** → shows hotspots on interactive maps.

---

## 🔍 What the Project Does
- Loads a dataset of Uber rides (`UberDataset.csv`).
- Cleans and processes datetime and location information.
- Extracts features like **hour of day**, **day of week**, and **weekend/weekday**.
- Uses **KMeans clustering** to detect geographic hotspots.
- Produces **interactive heatmaps** and hotspot visualizations using Folium.
- Provides insights on **demand by location and time**.

---

## ⚙️ How It Works
### Workflow in the Notebook
1. **Import Libraries**  
   Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib, Folium.
2. **Load Dataset**  
   Read `UberDataset.csv` containing trip records.
3. **Data Cleaning**  
   - Parse start and end times.  
   - Drop missing or invalid records.  
   - Keep valid latitude/longitude ranges.
4. **Feature Engineering**  
   - Extract `hour` of pickup.  
   - Extract `day_of_week` (0=Monday, 6=Sunday).  
   - Flag `is_weekend`.
5. **Demand Analysis**  
   - Group rides by pickup zone and hour.  
   - Count rides to find busy periods.
6. **Clustering**  
   - Apply **KMeans** to pickup coordinates + time.  
   - Identify top clusters (hotspots).  
   - Rank by ride counts.
7. **Visualization**  
   - Folium heatmaps to show pickup density.  
   - Cluster centers plotted on the map.  
   - Charts for demand by time of day and day of week.

---

## 📂 Project Files
- `Uber_hotspots_reccomendations_for_drivers (2).ipynb` — Jupyter Notebook with full workflow.
- `UberDataset.csv` — input dataset (not included here; add your own).
- Output: interactive **Folium maps** and demand charts.

---

## 🛠️ Requirements
Install dependencies with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn folium jupyter

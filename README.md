# 📘 Ganga River Basin Modeling Using Landlab
## 📌 Project Overview
This notebook presents a geomorphological simulation of the **Ganga River Basin**, particularly around the **Varanasi region**, using the **Landlab** toolkit — a powerful Python-based modeling environment for Earth surface processes.

### 🌍 Objective:
- Simulate **waterbody formation** in the Ganga basin.
- Model **landscape evolution** due to erosion and river flow.
- Visualize and analyze **topographical changes**.
- Demonstrate **Landlab’s real-world application** in geosciences.

---

## 🏞️ Geographic & Geological Context

- **Origin:** Gangotri Glacier, Himalayas, India.
- **Length:** ~2,525 km  
- **Study Focus Area:** Varanasi, Uttar Pradesh (Lat 25N, Lon 83E)

---

### Geological Features:
- Himalayan tectonic uplift  
- Alluvial plains and fertile sediment deposits  
- Meandering river channels  
- Floodplain features like oxbow lakes and levees  

---

## 🛠️ Tools & Technologies Used

- **Landlab:** Python library to simulate Earth surface processes.  
- **bmi-topography:** For downloading and using real-world DEM (Digital Elevation Model) data.  
- **xarray, rioxarray, rasterio:** To process and handle spatial data.  

---

## 🧠 How the Code Works

### 1. Import Required Libraries
Includes `landlab` components for hydrological and erosion modeling, `matplotlib` for visualization, and `bmi-topography` for terrain data.

### 2. Download DEM Data
Defines a function `getTerrain()` that uses `bmi-topography` to fetch SRTM elevation data for the Varanasi region.

### 3. Set Up Model Grid
- Uses `RasterModelGrid` to define a regular 2D grid over the DEM.  
- Initializes topographic elevation field from the real-world data.

### 4. Initialize Components
- **Flow Accumulator:** Calculates drainage area and flow direction.  
- **Stream Power Eroder:** Models river incision due to water flow.  
- **Channel Profiler:** Extracts river profiles for plotting.  
- **Depression Finder and Router:** Handles pits and closed depressions.

### 5. Run Simulation
- Time-stepped simulation (looped) evolves the terrain.  
- Applies erosion rules over multiple iterations.  
- Updates and stores elevation fields.

### 6. Animation & Visualization
- Uses `matplotlib.animation.FuncAnimation` to create and display an evolving animation of topographical change.  
- Visualizes elevation change and channel networks over time.

---

## 📊 Output
- Animated visualization of evolving landscape due to erosion and water flow.  
- Profiles and maps showing river channel development and elevation change.

---

## 🎯 Key Takeaways
- Demonstrates how **real-world topography** can be imported and simulated.  
- Highlights how **erosion and river dynamics** reshape landscapes.  
- Validates **Landlab** as a valuable tool for education and research in geomorphology and environmental modeling.


# GPS-Assisted Precision Banana Planting 

## Project Overview
This project investigates how **plant spacing**, **variety**, and **growth status** interact in a banana plantation. Using **GPS-coordinated data**, the analysis explores patterns that influence plant health and yield, while demonstrating the value of **precision agriculture**.  

The study was carried out with data from **banana plants at Fountain University, Osogbo (Osun State, Nigeria).**

## Objectives
- Evaluate the relationship between **spacing** and **growth outcomes**  
- Assess how different **banana varieties** (Plantain vs Cavendish) perform  
- Use **GPS spatial data** to uncover field-level planting issues  
- Provide practical **recommendations for precision planting**  

## Methodology

### Data Preprocessing
- Computed **plant-to-nearest-neighbor spacing** using the `geopy` library  
- Created `Spacing_m` column (in meters)  
- Classified spacing into:
  - Below 2m  
  - 2–4m  
  - Above 4m  
- Cleaned and exported dataset → `cleaned_banana_data.csv`

### Exploratory Data Analysis (EDA)
- **Plant variety distribution**: 53.5% Plantain vs 46.5% Cavendish  
- **Growth status distribution**: Healthy (33.8%), Stunted (33.8%), Wilting (32.4%)  
- **Spacing analysis**: Majority of plants were spaced **too closely (< 2m)**  
- **Variety vs Growth**: Cavendish performed significantly better than Plantain  

### Spatial Visualization
- Created an **interactive map** using `Folium`  
- Color-coded plant health status:  
  - Healthy → Green  
  - Stunted → Orange  
  - Wilting → Red  
- Popups showed plant variety, spacing, health, and GPS coordinates  
- Identified **clusters of unhealthy plants** in tightly spaced regions  

## Key Insights
- **Closer spacing (< 2m)** strongly linked to stunted & wilting plants  
- **Wider spacing (> 4m)** supports healthier growth (median ~3–4m ideal)  
- **Cavendish variety** outperformed Plantain under observed conditions  
- GPS data provided actionable insights for improving **field layouts**  

## Outcomes
- Validated that **optimal spacing** improves plant health  
- Highlighted importance of **variety selection**  
- Demonstrated effectiveness of **GPS-assisted precision planting** for monitoring and decision-making  
- Provides clear direction for **agronomic adjustments** and **future planting practices**  

## 📂 Repository Structure

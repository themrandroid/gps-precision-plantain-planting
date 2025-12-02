# GPS-Assisted Precision Banana Planting

A data-driven analysis investigating how plant spacing, variety, and growth status interact in banana plantations using GPS-coordinated spatial data to enhance precision agriculture practices.


## Project Overview

This project investigates the complex interactions between plant spacing, banana variety (Plantain vs. Cavendish), and growth status in a commercial banana plantation at Fountain University, Osogbo (Osun State, Nigeria). By leveraging GPS-coordinated field data, this analysis demonstrates how precision agriculture principles can identify and mitigate suboptimal planting configurations that compromise plant health and yield.

The study combines spatial analysis, exploratory data analysis, and geospatial visualization to provide actionable insights for agricultural practitioners and farm managers.

## Motivation

Banana production is a critical agricultural commodity in Nigeria and across the tropics. However, suboptimal planting practices—particularly inadequate plant spacing—lead to reduced yields, increased disease susceptibility, and lower profitability. Traditional approaches to plantation management lack spatial granularity, making it difficult to diagnose field-level issues systematically.

This project demonstrates how GPS technology and data science can transform conventional plantation management by:

- Quantifying spatial relationships between plants using precise coordinates
- Identifying problematic zones within the plantation
- Correlating spacing and variety with observable growth outcomes
- Providing evidence-based recommendations for future planting operations

## Objectives

1. Evaluate the relationship between plant spacing and growth outcomes
2. Assess performance differences between banana varieties (Plantain vs. Cavendish)
3. Use GPS spatial data to visualize field layout and uncover location-specific planting issues
4. Derive practical, evidence-based recommendations for improved precision planting strategies

## Methodology

### Data Preprocessing

- **Spacing Calculation**: Computed plant-to-nearest-neighbor spacing using the Geopy library to calculate haversine distances from GPS coordinates
- **Feature Engineering**: Created `Spacing_m` column (in meters) for standardized spacing representation
- **Spacing Classification**: Grouped spacing into three categories:
  - Below 2m (overcrowded)
  - 2–4m (optimal)
  - Above 4m (sparse)
- **Data Cleaning**: Standardized plant variety names, growth status categories, and handled missing values
- **Output**: Cleaned dataset exported to `cleaned_banana_data.csv`

### Exploratory Data Analysis (EDA)

- Analyzed plant variety distribution: 53.5% Plantain vs. 46.5% Cavendish
- Examined growth status distribution: Healthy (33.8%), Stunted (33.8%), Wilting (32.4%)
- Conducted spacing analysis revealing majority of plants spaced below optimal range
- Performed variety-vs-growth cross-tabulation analysis
- Generated comparative visualizations of spacing categories and growth outcomes

### Spatial Visualization

- Created interactive GPS-based maps showing planting point distributions
- Developed clustered mapping to identify spatial concentration patterns
- Generated comprehensive field layout visualizations with plant status overlays
- Produced all-plant and all-planting-points maps for different analytical perspectives

## Key Findings

- **Spacing Issue**: The majority of plants were spaced below the 2m threshold, indicating systematic overcrowding that likely constrains growth and promotes disease
- **Variety Performance**: Cavendish plants demonstrated significantly better growth outcomes compared to Plantain, despite comprising a smaller portion of the plantation
- **Growth Status Parity**: The plantation exhibited near-equal distribution across healthy, stunted, and wilting categories (approximately 33% each), suggesting environmental or management factors affecting a substantial portion of the crop
- **Spatial Patterns**: Geographic clustering of problematic zones identified through spatial analysis, indicating field-level management variability

## Data

The analysis is based on GPS-coordinated data from banana plants at Fountain University, Osogbo plantation. The dataset includes:

- **GPS Coordinates**: Latitude and longitude for each plant location
- **Plant Variety**: Plantain or Cavendish classification
- **Growth Status**: Healthy, Stunted, or Wilting condition assessment
- **Spacing Metrics**: Calculated nearest-neighbor distances in meters

### Data Source

- **Location**: Fountain University Banana Plantation, Osogbo, Osun State, Nigeria
- **Sample Size**: Multiple plants with spatial coordinates and phenotypic observations
- **Cleaned Dataset**: [data/cleaned_banana_data.csv](data/cleaned_banana_data.csv)

## Project Structure

```
GPS Precision Banana Planting/
├── README.md                                    # Project documentation
├── requirements.txt                             # Python dependencies
├── gps_precision_plantain_planting.ipynb       # Main analysis notebook
├── data/
│   └── cleaned_banana_data.csv                 # Processed dataset
├── code report/
│   └── gps_precision_plantain_planting.html    # Rendered notebook report
├── All_Plant_Map.html                          # Interactive plant location map
├── All_Planting_Points_Map.html                # Planting points visualization
├── Clustered_Map.html                          # Spatial clustering map
└── presentation/                               # Presentation materials
```

## Installation

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd GPS-Precision-Banana-Planting
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook gps_precision_plantain_planting.ipynb
```

## Usage

### Running the Analysis

1. Open the Jupyter notebook: `gps_precision_plantain_planting.ipynb`
2. Execute cells sequentially to reproduce the analysis pipeline
3. The notebook generates visualizations, statistical summaries, and interactive maps

### Viewing Results

- **Interactive Maps**: Open HTML files in a web browser:
  - `All_Plant_Map.html` - Complete plant location map
  - `All_Planting_Points_Map.html` - Planting points overview
  - `Clustered_Map.html` - Spatial clustering analysis

- **HTML Report**: View `code report/gps_precision_plantain_planting.html` for the complete rendered analysis

## Results

### Statistical Summary

| Metric | Value |
|--------|-------|
| Plantain Representation | 53.5% |
| Cavendish Representation | 46.5% |
| Healthy Plants | 33.8% |
| Stunted Plants | 33.8% |
| Wilting Plants | 32.4% |
| Plants Below 2m Spacing | Majority |
| Variety Performance Difference | Cavendish significantly outperforms Plantain |

### Visualizations

The analysis includes:

- Distribution plots for plant variety and growth status
- Spacing category histograms and comparisons
- Variety vs. growth status cross-tabulations
- Geographic heatmaps and clustering visualizations
- Box plots comparing spacing across growth outcomes

## Technologies

- **Python 3.x** - Primary programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Matplotlib & Seaborn** - Data visualization
- **Geopy** - GPS distance calculations and geospatial operations
- **Folium/Leaflet** - Interactive mapping
- **Jupyter Notebook** - Analysis documentation and reproducibility
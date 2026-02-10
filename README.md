# [Python] Tree Census in New York City

**🌳 Data cleaning and analysis, and geospatial analysis for the 1995, 2005 and 2015 tree censuses in New York City using Python.**

**⚠️ To use the project, first download the datasets from Kaggle [[LINK](https://www.kaggle.com/datasets/nycparks/tree-census/data)]**

**📁 The project is organized into four Jupyter Notebook files:**

- 📒 `nyc_trees_clean.ipynb` - Raw Data Cleaning with Python
- 📒 `nyc_trees_eda.ipynb` - Exploratory Data Analysis with Matplotlib & Seaborn
- 📒 `nyc_trees_geopandas.ipynb` - Geospatial Analysis with GeoPandas
- 📒 `nyc_trees_maps.ipynb` - Interactive Mapping with Plotly Express

The structure follows best practices in data science: clean first, analyze second, spatially enrich third, and communicate results last.

## 1. Project Overview

### Dataset

The NYC Tree Census dataset contains detailed information on street trees across New York City, including:
- Tree species
- Health and status
- Diameter at breast height (DBH)
- Borough and neighborhood
- Geographic coordinates (latitude/longitude)

### Goals of the Analysis

- Ensure data quality and consistency
- Understand tree distribution and health patterns
- Compare borough-level characteristics
- Visualize spatial patterns using static and interactive maps

## 2. Raw Data Cleaning (`nyc_trees_clean.ipynb`)

**Prepare the raw NYC Tree Census data for analysis by handling missing values, correcting data types, and standardizing fields.**

### Python Libraries
- Pandas
- Matplotlib
- Seaborn
- CSV
- re

### Key Tasks

- Load raw CSV data using pandas
- Inspect dataset shape, columns, and data types
- Handle missing or invalid values
- Standardize categorical fields (e.g., borough names, tree status)
- Filter out unusable records
- Save a cleaned dataset for downstream analysis

### Typical Steps

1. Data Ingestion
- Read CSV file
- Preview data with `.head()` and `.info()`

2. Data Quality Checks
- Identify null values
- Detect outliers (e.g., negative DBH)

3. Cleaning Operations
- Drop or impute missing values
- Convert columns to appropriate data types
- Normalize text fields

4. Outputs
- Export cleaned data to a new CSV files: `1995_trees.csv`, `2005_trees.csv`, `2015_trees.csv`

## 3. Exploratory Data Analysis (`nyc_trees_da.ipynb`)

**Explore patterns, trends, and relationships in the cleaned dataset using statistical summaries and visualizations.**

### Python Libraries
- Pandas
- Matplotlib
- Seaborn

### Key Analyses

- Tree counts by borough
- Species distribution
- Tree health comparison
- DBH (tree size) distributions

### Common Visualizations

- Bar charts (tree counts per borough)
- Histograms (DBH distribution)
- Box plots (DBH by borough or species)
- Count plots (health status)

### Workflow

1. Load cleaned dataset
2. Generate descriptive statistics
3. Create visualizations with consistent styling
4. Interpret patterns and anomalies

### Best Practices Applied

- Clear axis labels and titles
- Consistent color palettes
- Proper figure sizing

## 4. Geospatial Analysis with GeoPandas (`nyc_trees_geopandas.ipynb`)

**Incorporate geographic context into the analysis by converting tabular data into spatial data.**

### Python Libraries

- NumPy
- Pandas
- GeoPandas

### Key Tasks

- Convert latitude/longitude to geometry points
- Create a GeoDataFrame for each dataset
- Create GeoPackage (.gpkg) files from GeoDataFrames
- Read GeoPackage files
- Preview data with `.head()`

### Outputs

- GeoDataFrames with spatial context
- GeoPackage (.gpkg) files from GeoDataFrames: `1995_trees_geo.gpkg`, `2005_trees_geo.gpkg`, `2015_trees_geo.gpkg`

### Next steps

You can work with GeoPackage files using **QGIS**.

## 5. Interactive Maps with Plotly Express (`nyc_trees_plotly.ipynb`)

**Create interactive, web-ready visualizations to communicate spatial findings effectively.**

### Python Libraries

- Pandas
- Plotly Express

### Interactive maps

- Tree Diameter in NYC (1995, 2005, 2015)
- Tree Species in NYC (1995, 2005, 2015)
- Tree Health in NYC (1995, 2005, 2015)
- Tree Density in NYC - heatmap (1995, 2005, 2015)
- Tree Problems in NYC (2015)
- Tree Problems in NYC - heatmap (2015)

### Features

- Zoom and pan
- Hover-based inspection
- Color encoding by species, health, or size

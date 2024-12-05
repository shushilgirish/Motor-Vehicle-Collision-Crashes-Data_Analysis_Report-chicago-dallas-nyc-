# Traffic Accident Data Analysis

## Overview
This project focuses on designing advanced data architecture for business intelligence, specifically using traffic accident datasets from **Austin**, **Chicago**, and **New York City**. The aim is to integrate these datasets, process the data using **ETL** (Extract, Transform, Load) workflows, and provide valuable insights to enhance traffic safety and management.

## Key Components

### **1. Data Profiling and Analysis**
Three datasets were analyzed:
- **Austin Crash Dataset**: 147,750 observations with 21.6% missing data, highlighting challenges related to missing values and the importance of data imputation strategies.
- **Chicago Crash Dataset**: 817,723 observations with 21.1% missing data, focusing on resolving data gaps and improving predictive modeling.
- **New York City Crash Dataset**: 2,075,427 observations with 29.5% missing data, a large dataset requiring effective data handling techniques to maintain analysis quality.

### **2. ETL (Extract, Transform, Load) Process**
Using **Talend**, data from all three cities underwent a series of transformations to clean, format, and standardize the datasets:
- **Staging Tables**: Raw data was first loaded into staging tables for initial cleaning and validation.
- **Transformations**: Data was processed with business rules (e.g., handling null values, concatenating fields, type conversions) using Talend’s **tMap** components.
- **Loading**: Data was then loaded into dimension and fact tables that enabled analytical insights.

### **3. Dimensional Modeling**
The project utilized a **Star Schema** with the following tables:
- **Dimension Tables**:
  - `Dim_Date`, `Dim_Location`, `Dim_Time`, `Dim_Source`, `Dim_Contribute`, `Dim_Vehicle`.
- **Fact Tables**:
  - `Fact_Mishaps`, `Fact_ContributingFactors`, `Fact_UnitsInvolved`.
- **Slowly Changing Dimensions** were implemented to track historical changes over time, especially for accident-related contributing factors.

### **4. Business Intelligence and Reporting**
Several **business questions** were answered through data visualization and reporting:
- How many accidents occurred in each city?
- Which areas had the most accidents (top areas per city)?
- Accident seasonality and time-of-day analysis.
- Pedestrian involvement in accidents and injury/fatality analysis.
- Contributing factors and trends across locations and time.

### **5. Geospatial Data Enrichment**
To enhance the dataset for better geographical analysis, the project initially used **Google’s Geocoder API** but switched to **Microsoft Power Query** for geocoding due to budget and system integration challenges. This transition improved the scalability and cost-efficiency of the geospatial data processing.

---

## Project Workflow

1. **Data Extraction**:
   - Data from three cities (Austin, Chicago, NYC) was ingested from external sources using Talend's input components.
   
2. **Data Transformation**:
   - Applied various **ETL transformations** to clean, normalize, and structure the data (e.g., handling null values, concatenating fields, converting data types).
   
3. **Data Loading**:
   - Loaded processed data into **staging tables** for further validation, then into **dimension and fact tables** for comprehensive analysis.

4. **Data Analysis and Reporting**:
   - Generated insights using **SQL queries** and **business intelligence tools** to visualize accident trends, factors, and hotspots in different cities.

---

## Technologies Used
- **ETL Tool**: Talend
- **Database**: MySQL for staging and dimension/fact tables
- **Data Processing**: Talend’s tMap for data transformation
- **Geospatial Processing**: Microsoft Power Query (used for geocoding)
- **Visualization Tools**: Power BI or other BI tools (for data analysis and reporting)

---

## Challenges and Solutions
- **Missing Data**: High percentages of missing data in accident records were handled by imputation or exclusion methods.
- **Geospatial Integration**: Initially using Google's Geocoder API, the project switched to Microsoft Power Query to address system integration issues and reduce costs.
- **Scalability**: Despite the large volume of data (millions of rows), the ETL processes were optimized for performance, making use of modern computing resources.

---

## Conclusion
This project demonstrates the application of advanced data architecture and ETL workflows for the analysis of traffic accidents. By integrating and processing large datasets from multiple cities, it provides actionable insights that can contribute to safer city traffic management. The final dimensional model supports detailed analysis, with capabilities for trend forecasting and contributing factor identification.

---

## Future Work
- **Predictive Modeling**: Using the cleaned datasets for machine learning models to predict accident hotspots and potential contributing factors.
- **Real-time Data Integration**: Integrating live accident data feeds into the current model for more timely insights.
- **Advanced Geospatial Analysis**: Enhance the geospatial capabilities to provide real-time location-based insights.

---

Feel free to explore the repository for more detailed workflows, data transformations, and visualizations used in this project!

---

This README file provides a concise yet comprehensive summary of the project. You can modify or expand on it based on further details you may wish to include.

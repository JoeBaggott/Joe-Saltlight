# StreetView-Informed Voting Analysis: Data Collection & Processing  

## Overview  
This repository contains the outputs from a large-scale data collection and analysis project aimed at understanding voting patterns in South Africa through a combination of multimodal data sources. The project integrates **StreetView imagery, satellite land-use data, crime statistics, and municipal financial data** to build predictive models that examine how environmental and socioeconomic conditions influence voter behavior.  

The data collected showcases the ability to extract insights from **diverse, large-scale datasets**, demonstrating an approach that merges geospatial analysis, computer vision, and machine learning to enhance political and social research.

---

## Data Collection & Sources  

The dataset was constructed using a range of publicly available and API-accessible data sources:  

- **Google StreetView API**: Used to collect imagery from road networks across South Africa. A novel methodology was developed to select optimal locations for data collection, ensuring scalable and efficient retrieval of images.  
- **OpenStreetMap (OSM)**: Provided road network data, which was processed to filter out non-relevant roads (e.g., highways, footpaths) and select only roads covered by StreetView.  
- **South African National Land-Cover Dataset**: GIS-based raster data was converted into vector format to extract land-use features for each region.  
- **South African Police Service Crime Reports**: Crime statistics were aggregated at the municipal level, linking police station-level data to administrative regions.  
- **South African National Treasury Municipal Finance Data**: Extracted from [municipaldata.treasury.gov.za](https://municipaldata.treasury.gov.za/), this dataset provides insights into municipal financial management, expenditure, and infrastructure investment.  

Each of these data sources was cleaned, processed, and integrated into a structured dataset, allowing for predictive modeling at both the **ward** and **municipal** levels.

---

## Key Features of the Dataset  

- **Geospatially-Tagged Data**: Every data point is linked to specific administrative regions (wards and municipalities) for spatial analysis.  
- **StreetView-Derived Features**: Object detection models (trained using YOLOv8) were applied to images to extract features such as **potholes, illegal dumping, pedestrian activity, and vehicle types**, serving as proxies for infrastructure quality and socioeconomic conditions.  
- **Land-Use and Road Features**: Features derived from land classification and road type distributions were included to understand how built environments impact voter behavior.  
- **Crime and Financial Data**: Socioeconomic indicators were integrated to analyze their relationship with electoral outcomes.  

---

## Modeling & Analysis  

The dataset was used to train and evaluate both **regression and classification models**:  

- **Machine Learning for Ward-Level Predictions**: Random Forest and Linear Regression models were trained using features derived from StreetView and land-use datasets to predict voting patterns.  
- **Statistical Regression for Municipality-Level Predictions**: Lasso, Ridge, and Elastic Net regression techniques were used to identify the most significant predictors of voting patterns at a municipal level.  
- **Classification of Majority Party in Wards**: A classification approach using **logistic regression** and **Random Forest classifiers** was used to determine the dominant political party in each ward.  

---

## Significance of the Project  

This repository demonstrates the ability to collect and integrate data from **diverse sources**, ranging from real-world imagery to structured financial datasets. The methodology developed here can be extended to a variety of geospatial and social science research applications, particularly those that rely on unconventional, multimodal data sources.  

By leveraging **computer vision, geospatial analysis, and statistical modeling**, this project presents an innovative approach to studying voting behavior and broader socioeconomic trends.

---

## How to Use This Repository  

- **Data Outputs**: Processed datasets, extracted features, and final structured data files are available in this repository.  
- **Methodology Documentation**: Detailed explanations of the data collection process, feature engineering techniques, and modeling approaches can be found in the associated research paper/thesis.  
- **Reproducibility**: Scripts and methodologies are structured to allow for re-execution in different contexts, enabling further research and analysis.  

---

## Future Work  

- Expanding the dataset to additional regions and elections.  
- Refining object detection models for more precise classification.  
- Exploring additional data sources, such as census and survey data, to enhance predictive capabilities.  

---

## Contact & Acknowledgments  

This project was conducted as part of a broader research initiative on political and socioeconomic analysis using computational methods. For any questions, collaboration opportunities, or access to additional data, please reach out via GitHub Issues or the provided contact information.

---

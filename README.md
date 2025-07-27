# Branching Toward Sustainability: How NYC's Urban Forest Supports a Healthier City
## Objective:
This project explores the relationship between urban trees and environmental health in New York City. By combining data from the NYC Tree Census with NYC air quality data, the project investigates whether the presence, amount, and condition of trees contribute to a cleaner, more sustainable city. The analysis focuses on identifying patterns that might suggest how urban greenery supports public health and environmental resilience. Findings from this work could inform future decisions in urban planning, environmental policy, and climate adaptation strategies.



## Project Setup Instructions-
step by step directions how to download, install, and run project
instruction for setting up the virtual environment


## Project Overview-
Description of what the user should expect once the project is running
clear and simple language


## TECHNOLOGIES USED:

**Languages & Core Libraries:**
Python – primary language for data analysis and project development\
Pandas – for data cleaning, transformation, and analysis\

**Visualization Tools:**
Matplotlib – for basic charts and static visualizations\
Plotly – for interactive graphs and visual exploration\
Tableau – for building interactive dashboards and communicating insights visually\

**Data Storage & Querying:**
SQLite – for lightweight, file-based data storage and SQL querying\

**Development Environment:**
Jupyter Notebook – for exploratory data analysis and documenting workflows\
VS Code – for script development and file management\

**Version Control & Documentation:**
Git & GitHub – for version control and project sharing\
Markdown – for notes, documentation, and explanations\




## Data Dictionary(from cleaned data)-

**Variables from tree_summary_by_cb.csv:**
tree_id (object)- Unique identifier for each tree record.\
cb_num (int)-  Community District where trees are located.\
tree_count (int)-  Number of trees in the specified area.\
avg_health_score (float)-  Average health score of trees (rating scale: 3= Good, 2= Fair, 1= Poor).\
dbh_mean (float)-  Average 'diameter at breast height' (DBH) of trees, in inches.\
dbh_max	(float)-  Maximum DBH observed in the area.\
unique_species (int)-  Count of unique tree species in the area.\

**Variables from Air_quality_by_CD.csv:**
id	(int)-  Unique identifier for the air quality record.\
Geo_Join_ID	(float)-  Community District ID used to join spatial datasets(matches cb_num from tree data).\
Time_Period	(object)-  Time period when the air quality measurement was taken (Summer, Winter, and Average).\
Name (object)-  Name of the air quality indicator (Nitrogen dioxide (NO2), Fine particles (PM 2.5), Ozone (O3)).\
Data_Value (float)-  Measured value of the air quality indicator.\
Measure_Info (object)-  Units or measurement description.\

**Variables from borough_tree.csv:**
boroname (object)-	Name of the borough.\
unique_species (int)-  Total number of unique tree species within the borough.\
avg_dbh (float)-  Average 'diameter at breast height' (DBH) of trees, in inches.\
total_dbh (float)-  Sum of DBH measurements for all trees in the borough.\
avg_health_score (float)-  Average health score of trees in the borough(rating scale: 3= Good, 2= Fair, 1= Poor).\
total_trees	(int)-  Total number of trees in the borough.\





## Data Summary  

Total Records:\
Tree dataset:   683,788 rows,  41 columns\
Air dataset:    18,025 rows,  12 columns\

Date Range: \
Tree dataset: 2015\
Air dataset: filtered to include only 2015(original range: 2009-2022)\

Basic Stats(using the 59 Community District Boundaries of NYC):\
Tree Count:\
    mean\
    median\
    max\
DBH(diameter at breast height):\
    mean\
    median\
    max\
Air Quality(Nitrogen Dioxide):\
    Summer mean\
    Summer range\
    Winter mean\
    Winter range\






## Data Sources
https://www.kaggle.com/datasets/kaggleprollc/air-quality-data-nyc\
https://www.kaggle.com/datasets/alistairking/nyc-building-energy-efficiency-ratings\
https://www.kaggle.com/datasets/nycparks/tree-census\


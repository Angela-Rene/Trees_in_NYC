# Branching Toward Sustainability: Does NYC's Urban Forest Support a Healthier City?
---
## Objective:
This project investigates whether the presence, amount, and condition of trees in NYC contribute to a cleaner, more sustainable city. By combining data from the NYC Tree Census with NYC air quality data, the project explores the relationship between urban trees and environmental health. The analysis focuses on identifying patterns that might suggest how urban greenery supports public health and environmental resilience. Findings from this work could inform future decisions in urban planning, environmental policy, and climate adaptation strategies.

---

## Project Overview:

This project explores the relationship between trees and air quality in New York City. Using data from the NYC Tree Census and NYC air quality data, it looks for signs that more trees might mean cleaner air.

Once the project is running, it will:

+ Clean and prepare the data to make sure it's accurate and usable.

+ Group the tree data by community district so it can be compared directly with the air quality data(that is also grouped by community district).

+ Combine the tree and air datasets to look for connections between them.

+ Create simple visualizations to help show any patterns or relationships between tree coverage and air quality.

+ Help answer the question: Do areas with more or larger trees tend to have better air quality?


---


## Project Setup Instructions:

+ Copy the code link to this repository and clone to your computer.
+ Open the repository folder in a code editor, and create the virtual environment in that folder.
+ Create and Activate a Virtual Environment(commands in table below)
+ Install the `requirements.txt` file

+ Start by opening `data_cleaning_and_eda.ipynb`  to see the cleaning and EDA of original data sources.
+ Then open `sql_database_and_plots.ipynb` to see the SQL database, tables, and plots.
+ Finally open `project_summary.ipynb` for a full project summary and a link to Tableau dashboard.
+ When you are finished, deactivate the virtual environment and close the repository folder.

## Virtual Environment Commands 
| **Command** |           **Linux/Mac**               |         **Windows/GitBash**          |
| ----------  | ------------------------------------- | ------------------------------------ |
|  Create     |    `python3 -m venv venv`             |   `python -m venv venv`              |
|  Activate   |    `source venv/bin/activate`         |   `source venv/Scripts/activate`     |
|  Install    |    `pip install -r requirements.txt`  |   `pip install -r requirements.txt`  |
|  Deactivate |    `deactivate`                       |   `deactivate`                       |

---


## Data Summary:  

**Total Records:**\
Tree dataset:   683,788 rows,  41 columns\
Air dataset:    18,025 rows,  12 columns

**Date Range:**\
Tree dataset: 2015\
Air dataset: filtered to include only 2015(original range: 2009-2022)

**Basic Stats(using the 59 Community District Boundaries of NYC):**\
Tree Count:\
    mean: 11,037\
    median: 8,474\
    max: 51,842

DBH(diameter at breast height in inches):\
    mean: 10.87\
    max: 425.00

Air Quality(Nitrogen Dioxide(ppb)):\
    Summer mean: 16.02\
    Summer range: 6.6-29.7\
    Winter mean: 23.96\
    Winter range: 16.6-33.4







## Data Dictionary(from cleaned data):

**Variables from tree_summary_by_cb.csv:**
+ tree_id (object)- Unique identifier for each tree record.
+ cb_num (int)-  Community District where trees are located.
+ tree_count (int)-  Number of trees in the specified area.
+ avg_health_score (float)-  Average health score of trees (rating scale: 3= Good, 2= Fair, 1= Poor).
+ dbh_mean (float)-  Average 'diameter at breast height' (DBH) of trees, in inches.
+ dbh_max	(float)-  Maximum DBH observed in the area.
+ unique_species (int)-  Count of unique tree species in the area.

**Variables from Air_quality_by_CD.csv:**
+ id	(int)-  Unique identifier for the air quality record.
+ Geo_Join_ID	(float)-  Community District ID used to join spatial datasets(matches cb_num from tree data).
+ Time_Period	(object)-  Time period when the air quality measurement was taken (Summer, Winter, and Average).
+ Name (object)-  Name of the air quality indicator (Nitrogen dioxide (NO2), Fine particles (PM 2.5), Ozone (O3)).
+ Data_Value (float)-  Measured value of the air quality indicator.
+ Measure_Info (object)-  Units or measurement description.

**Variables from borough_tree.csv:**
+ boroname (object)-	Name of the borough.
+ unique_species (int)-  Total number of unique tree species within the borough.
+ avg_dbh (float)-  Average 'diameter at breast height' (DBH) of trees, in inches.
+ total_dbh (float)-  Sum of DBH measurements for all trees in the borough.
+ avg_health_score (float)-  Average health score of trees in the borough(rating scale: 3= Good, 2= Fair, 1= Poor).
+ total_trees	(int)-  Total number of trees in the borough.






## TECHNOLOGIES USED:

**Languages & Core Libraries:**\
_Python_ – primary language for data analysis and project development\
_Pandas_ – for data cleaning, transformation, and analysis

**Visualization Tools:**\
_Matplotlib_ – for basic charts and static visualizations\
_Plotly_ – for interactive graphs and visual exploration\
_Tableau_ – for building interactive dashboards and communicating insights visually

**Data Storage & Querying:**\
_SQLite_ – for lightweight, file-based data storage and SQL querying

**Development Environment:**\
_Jupyter Notebook_ – for exploratory data analysis and documenting workflows\
_VS Code_ – for script development and file management

**Version Control & Documentation:**\
_Git & GitHub_ – for version control and project sharing\
_Markdown_ – for notes, documentation, and explanations


---


## Data Sources:
https://www.kaggle.com/datasets/kaggleprollc/air-quality-data-nyc\
https://www.kaggle.com/datasets/nycparks/tree-census


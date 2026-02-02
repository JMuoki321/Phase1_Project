# **Project Overview**
This project explores historical aviation accident data to identify safety patterns related to aircraft operations. The analysis focuses on accident outcomes such as fatalities and damage severity, using data from the National Transportation Safety Board covering incidents from 2018 to 2022.

The project applies data cleaning, aggregation, and visualization techniques to uncover trends and support high-level insights. These insights are later translated into recommendations relevant to aviation-related business decisions.

## Business Understanding
The company is considering entering the aviation industry and needs to understand the risks associated with different aircraft. This analysis uses historical accident data to identify lower-risk aircraft options.

## Data Understanding
The dataset contains 2,500 records and 8 columns. Several columns, including registration, operator, and fatalities, contain missing values, indicating the need for data cleaning. Most variables are stored as object types.Registration column has 92 missing values, operator column has 14 missing values, fatalities column has 12 missing values.

## Data Preparation
Dropped the index column and now columns have reduced from 8 to 7
Since the analysis will focus on fatalities, only rows with missing fatality values will be removed. Dropping all missing values would affect the quality of the dataset.
After handling missing fatality values, the dataset was reduced to 2,488 rows.
Missing values in categorical columns were filled with ‘Unknown’ to preserve the dataset.

The data is stored as objects, so it needs to be converted to numeric values in order to analyze accidents over time. Target columns are the accident date and the fatalities.
Successfully dropped 1225 duplicates.

Since our main objective is to identify the lower risk aircraft, create a year column which will help us to compare accident risks overtime (1962-2023), show whether safety has improved over the years and be able support our recommendations.

# Create a clean copy of the DataFrame to avoid SettingWithCopyWarning
df = df.copy()
3 records contain incomplete accident dates, resulting in missing year values. These records will be retained since they still contain valid fatality and aircraft information relevant to risk analysis.

## Data Analysis and Visualizations
Aircraft Type vs Fatalities analysis because the company wants to know which aircraft are lowest risk
Aircraft types with the highest total fatalities were visualized to highlight higher-risk options. This allows the company to avoid these aircraft and focus on lower-risk alternatives.
The visualization shows how total aviation fatalities have changed over time, providing historical context for assessing aircraft risk.In 2018 there were more fatalities compared to 2022. From the graph above we can see that the number of fatalities has reduced overtime.
From the graph above, its clear that Cessna 208B Grand Caravan had more accidents than Airbus A320-232 hence having high risk.
## Recommendation
The company should prioritize aircraft types with historically low fatalities and accident counts, as these represent the lowest operational risk for entering the aviation business.
## Data Export for Visualization
The cleaned dataset will be exported for further visualization and dashboard creation in Tableau.
## Tableau Link
https://public.tableau.com/views/Phase1_Projectflightdata/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

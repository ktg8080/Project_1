# Chicago Crime Analysis and Visualization

## Overview

This project aims to analyze and visualize crime data from the city of Chicago, focusing on the top 6 most common crimes across different wards from 2010 to 2024. The analysis includes understanding crime distribution across wards, examining correlations between ward numbers and crime incidence, identifying locations with the highest crime rates, and comparing arrest rates to overall crime rates. Additionally, the project examines how arrest rates have changed from 2022 to 2023. A geographic heatmap is generated to visualize the prevalence of these crimes across Chicago's wards.

## Table of Contents

- [Project Structure](#project-structure)
- [Data Sources](#data-sources)
- [Installation](#installation)
- [Data Preparation](#data-preparation)
- [Analysis and Findings](#analysis-and-findings)
  - [What are the 6 most common crimes in Chicago from 2010-2024?](#what-are-the-6-most-common-crimes-in-chicago-from-2010-2024)
  - [Which wards are most & least affected by these crimes?](#which-wards-are-most--least-affected-by-these-crimes)
  - [Is there a correlation between instance of crime and ward?](#is-there-a-correlation-between-instance-of-crime-and-ward)
  - [Which Location types show the highest rate of crime?](#which-location-types-show-the-highest-rate-of-crime)
  - [How do arrest rates compare to crime rates?](#how-do-arrest-rates-compare-to-crime-rates)
  - [How have arrest rates changed from 2022 to 2023?](#how-have-arrest-rates-changed-from-2022-to-2023)
  - [Data Quality Concerns and Potential Skewness](#data-quality-concerns-and-potential-skewness)
- [Visualization](#visualization)
- [Results](#results)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Structure
├── data
│ ├── chicago_crime_data.csv # Raw crime data
│ ├── chicago_wards_shapefile.shp # Shapefile for Chicago wards (geographic data)
│ ├── chicago_wards_shapefile.shx # Index file for shapefile
│ ├── chicago_wards_shapefile.dbf # Attribute data for shapefile
├── notebooks
│ ├── crime_analysis.ipynb # Jupyter notebook for data analysis and visualization
├── output
│ ├── crime_heatmap.png # Generated heatmap of crime distribution
│ ├── top_6_crimes_trend.png # Trend visualization for top 6 crimes
│ ├── crime_vs_arrest_rates.png # Comparison of crime rates and arrest rates
├── README.md # Project README file
├── requirements.txt # List of required Python packages
└── LICENSE # License for the project
## Data Sources

1. **Chicago Crime Data**: 
   - Source: [Chicago Data Portal](https://data.cityofchicago.org/)
   - Description: This dataset contains detailed information on reported crimes in Chicago, including the date, location, and type of crime.

2. **Chicago Wards Shapefile**:
   - Source: [Chicago City Government or GIS Data Repository]
   - Description: Geographic data for the boundaries of Chicago’s wards, used for spatial analysis and visualization.

## Installation

### Prerequisites

- Python 3.x
- Jupyter Notebook (optional for running notebooks)
- Geopandas, Pandas, Matplotlib libraries

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/chicago-crime-analysis.git
   cd chicago-crime-analysis
   python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
Data Preparation
Loading Crime Data:

The raw crime data is loaded from chicago_crime_data.csv.
Data is filtered to focus on the top 6 most common crime types.
Loading and Preparing Geographic Data:

The shapefile for Chicago's wards is loaded using the geopandas library.
Crime data is aggregated by ward and merged with the geographic data for visualization.
Data Validation:

During analysis, discrepancies between the raw data and calculated metrics were observed, indicating potential data quality issues. These discrepancies may affect the reliability of the results.
Analysis and Findings
What are the 6 most common crimes in Chicago from 2010-2024?
Finding
The analysis identified the following as the top 6 most common crimes in Chicago from 2010 to 2024:

Assault
Battery
Criminal Damage
Deceptive Practice
Motor Vehicle Theft
Theft
These crimes were consistently prevalent throughout the period, with significant shifts during certain years, particularly during the COVID-19 pandemic (2020-2022).

Implication
Understanding the most common crime types helps prioritize law enforcement efforts and resource allocation. It also aids in tailoring crime prevention strategies to address the specific types of crimes most prevalent in the city.

Supporting Visualization
A line plot was used to visualize the trends of these top 6 crimes over time, highlighting significant changes, especially during the pandemic.

Which wards are most & least affected by these crimes?
Finding
The analysis revealed that certain wards in Chicago are significantly more affected by crime than others. Wards 27, 28, and 6 were among the most affected, while Wards 39, 47, and 23 were among the least affected by these crimes.

Implication
Identifying the wards most and least affected by crime allows law enforcement to focus their efforts and resources more effectively. High-crime wards may require more intensive policing and community programs, while low-crime wards might benefit from maintaining vigilance to keep crime rates low.

Supporting Visualization
Bar charts were used to display the wards with the highest and lowest crime rates, providing a clear comparison of crime distribution across the city.

Is there a correlation between instance of crime and ward?
Finding
Our analysis revealed a moderate negative correlation (-0.32) between ward numbers and crime incidence, suggesting that as the ward number increases, the number of crimes tends to decrease. This trend may reflect socioeconomic or geographic factors influencing crime rates, where certain wards possess characteristics that either deter or attract criminal activity.

Implication
Understanding the correlation between ward numbers and crime incidence helps in planning targeted interventions. Law enforcement agencies can use this insight to allocate resources more efficiently and design community engagement programs tailored to specific wards.

Supporting Visualization
A scatter plot with a regression line was used to visualize the relationship between ward numbers and crime incidence, clearly demonstrating the negative trend.

Which Location types show the highest rate of crime?
Finding
The analysis of crime distribution across different location types identified streets, apartments, and residences as the top locations with the highest crime rates. On the other end of the spectrum, locations like rivers, church properties, and police facilities showed much lower crime rates.

Implication
Identifying high-risk locations is crucial for targeted crime prevention efforts. Law enforcement agencies can use this information to deploy resources more effectively, increase surveillance in high-crime areas, and develop community programs aimed at reducing crime in these specific locations.

Supporting Visualization
Bar charts displayed the top 10 and bottom 10 location types by crime rate, providing a clear and accessible way to compare different environments.

How do arrest rates compare to crime rates?
Finding
The comparison between arrest rates and crime rates revealed that while the total number of crimes fluctuated over time, the arrest rates did not always follow the same pattern. In some cases, arrest rates decreased even as crime rates increased, possibly indicating strained law enforcement resources or shifts in policing strategy.

Implication
This finding suggests that while crime rates are a critical metric, arrest rates offer additional insight into law enforcement effectiveness and the criminal justice process. Discrepancies between crime and arrest rates can indicate areas where further investigation or intervention is needed, such as improving response times, increasing patrols, or addressing systemic issues in law enforcement.

Supporting Visualization
A dual-axis line chart was used to compare total crime rates and arrest rates over time, highlighting periods of divergence between the two metrics.

How have arrest rates changed from 2022 to 2023?
Finding
Arrest rates experienced a noticeable decline from 2022 to 2023, continuing a trend observed in the years prior. This decline contrasts with the increase in crime rates during the same period, raising concerns about the effectiveness of law enforcement strategies.

Implication
The declining arrest rates in the face of rising crime rates suggest potential challenges in law enforcement, such as resource limitations or shifts in policing strategies. Addressing these challenges may require a reevaluation of current practices and a focus on improving arrest rates to match the levels of criminal activity.

Supporting Visualization
A dual-axis line chart was used to show the changes in arrest rates alongside crime rates, with a specific focus on the years 2022 to 2023.
Data Quality Concerns and Potential Skewness
Observation
During our analysis, we observed discrepancies between the raw data and the calculated metrics, such as crime rates and arrest rates. Specifically, the numbers in the raw data did not always align with the trends and correlations identified. This inconsistency suggests that the data may be skewed or contain inaccuracies, which could potentially affect the reliability of our findings.

Implication
The potential skewness or inaccuracy in the data highlights the need for cautious interpretation of the results. Policymakers, law enforcement, and other stakeholders should consider these discrepancies when using the findings to inform decisions. It may also be necessary to further investigate the data sources and methodologies used in data collection to ensure accuracy. Future analyses might benefit from cross-referencing with additional data sources or conducting data validation checks to improve the robustness of the conclusions.

Visualization
Scatter Plot with Regression Line:

Visualizes the correlation between ward numbers and crime incidence.
Line Plot for Crime Trends:

Shows the prevalence of the top 6 crimes over time, focusing on the impact of the COVID-19 pandemic.
Dual-Axis Line Chart:

Compares total crime rates with arrest rates over time, highlighting periods of divergence.
Heatmap of Crime Distribution:

A geographic heatmap showing the distribution of the top 6 crimes across Chicago’s wards.
Results
Correlation Analysis: Found a moderate negative correlation between ward numbers and crime incidence.
Trend Analysis: Significant changes in crime patterns during the COVID-19 pandemic, with some crimes increasing while others remained stable or decreased.
Arrest Rate Analysis: Discrepancies between crime rates and arrest rates suggest possible areas for improvement in law enforcement strategies.
Geographic Analysis: The heatmap identified high-risk and low-risk areas across Chicago, helping target resources effectively.
Usage
To reproduce the analysis and visualizations:

Open the crime_analysis.ipynb notebook in Jupyter.
Run the cells step by step to load the data, perform the analysis, and generate the visualizations.
The generated visualizations will be saved in the output directory.
Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your improvements.
License
This project is licensed under the MIT License - see the LICENSE file for details.

### Explanation:

- **Incorporation of Topics:** The new summary with specific topics has been integrated into the "Analysis and Findings" section, making it more structured and aligned with the project's goals.
- **Table of Contents:** This allows users to quickly navigate through the README file, especially in a long document like this.
- **Detailed Sections:** Each section now clearly corresponds to the topics you wanted to focus on, ensuring that the README file is comprehensive and informative.

This README file provides clear guidance and detailed information about the project's structure, data sources, installation, analysis, and results, making it accessible and useful for other developers, analysts, or stakeholders interested in this crime data analysis project.

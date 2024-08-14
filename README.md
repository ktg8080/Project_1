# Project_1
Project 1

Title: Sherlock in Chicago

Team Members: Chi-Town Coders
Jonas Elterich
Kyle Goodwin
Aparajita Mondal
Jean Ryan-Lozon

Project Description:
We are analyzing data about crimes in Chicago from 2010-2024.

Research Questions:
What are the 6 most common crimes in Chicago from 2010-2024?
Which wards are most & least affected by these crimes?
Is there a correlation between instance of crime and ward?
Which Location types show the highest rate of crime?
How do arrest rates compare to crime rates?
How have arrest rates changed from 2022 to 2023?

Dataset:
https://data.cityofchicago.org/stories/s/Crimes-2001-to-present-Dashboard/5cd6-ry5g
City of Chicago Data Portal
Crimes 2001 to Present
Edited csv to only include data from 2010 to 2024. Edited CSV can be found in the "data" folder.
API Documentation: https://dev.socrata.com/foundry/data.cityofchicago.org/ijzp-q8t2

Breakdown of Tasks:
-All team members will do every task, and the best iteration of each subset will be used in our final presentation.

Discarded Questions (8/12/24):
How has the prevalence of these crimes changed over time?
What trends appeared in these crimes during the initial years of the Covid19 pandemic (2020-2022)?
How do arrest rates & crime rates compare across mayoral terms?

Notes for Data Cleaning

Remove columns:
Case Number
IUCR
Beat
District
Community Area
FBI Code
X Coordinate
Y Coordinate
Location

Do Not Remove rows with null values. Most NaN values are in the location, lat, and long columns. Removing them would skew the crime count.

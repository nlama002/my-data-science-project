# my-data-science-project

A Data Science Journey to Understand and Improve Road Safety

#Project Overview
This project analyzes the NYC OpenData Motor Vehicle Collisions - Crashes dataset to uncover patterns in crash occurrences, contributing factors, and their impacts across time and space. Starting with environment setup and exploratory data analysis (EDA), it progresses through data ethics, time series analysis, geospatial mapping, and culminates in a self-guided research question. Built in Google Colab using Python, this work aims to provide actionable insights for safer roads.
Goal: Leverage data science to identify crash trends and recommend safety improvements for the Department of Transportation.
Key Features
Tools Used: Pandas, Matplotlib, Seaborn, Folium, Statsmodels  
Dataset: NYC OpenData Motor Vehicle Collisions (police-reported crashes)  
Milestones:  
Environment setup and basic EDA  
Data ethics and preprocessing  
Time series analysis of crash trends  
Geospatial analysis of crash locations  
Self-guided research question  
Data storytelling via a virtual poster
Setup and Libraries
To get started, I set up my environment in Google Colab and installed key libraries:  
python
import pandas as pd              # Data manipulation and analysis
import matplotlib.pyplot as plt  # Basic visualizations (e.g., bar charts)
import seaborn as sns           # Enhanced plotting (e.g., heatmaps)
import folium                   # Geospatial mapping
from google.colab import drive  # Mount Google Drive for data access
Pandas: Structures data into DataFrames for efficient analysis.  
Matplotlib: Creates foundational plots like bar charts of crash factors.  
Seaborn: Adds aesthetic and statistical depth to visualizations.  
Folium: Maps crash locations with heatmaps and severity markers.
Data Exploration Highlights
Dataset Size: Millions of rows, each representing a crash event.  
Key Columns: Crash date/time, location (lat/long), injuries, fatalities, vehicle types, contributing factors.  
Initial Findings:  
Average injuries per crash: ~0.305; max: 43.  
Fatalities rare: ~0.00146 per crash; max: 8.  
Missing data in vehicle type and location fields due to incomplete reporting.
python
# Loading and previewing data
drive.mount('/content/drive')
data = pd.read_csv('/content/drive/MyDrive/Motor_Vehicle_Collisions.csv')
print(data.head())  # First 5 rows
print(data.describe())  # Summary stats
Milestone Insights
1. Exploratory Data Analysis
Top Contributing Factors: Excluding "Unspecified," the top 3 are:  
Driver Inattention/Distraction  
Following Too Closely  
Failure to Yield Right-of-Way
Top Vehicle Types: Sedans, Station Wagons, and Passenger Vehicles dominate crashes, likely due to their prevalence on NYC roads.  
Recommendation: Increase driver education on focus and spacing.
2. Data Ethics and Preprocessing
Missing Values: High in secondary vehicle/factor fields (e.g., VEHICLE TYPE CODE 5: 90% missing) and street names (30%).  
Ethical Concern: Under-resourced areas may underreport crashes, skewing data toward well-monitored zones.  
Action: Flagged missing lat/long (一致 across fields) for potential bias analysis.
3. Time Series Analysis
Peak Crash Hour: 4 PM - 6 PM (rush hour).  
COVID-19 Impact: Sharp drop in crashes in March 2020, followed by a gradual rise—likely due to lockdown reductions in traffic.  
Trend: Slight decrease in crashes from 2014-2022, with residuals showing a major dip in 2020 (pandemic effect).
Crash Trend
Monthly crash counts showing a COVID-19 dip.
4. Geospatial Analysis
Borough Breakdown: Brooklyn (Kings County) has the most crashes; Staten Island the fewest.  
Heatmap: High crash density in Manhattan and Brooklyn intersections.  
Severity Map: Coded fatalities (triangles), injuries (circles), and minor crashes (squares) for accessibility.
Heatmap
Sample heatmap of crash hotspots.
5. Self-Guided Research Question
Question: "Which day of the week sees the most severe crashes?"  
Finding: Fridays have the highest injury/fatality counts, possibly due to end-of-week traffic spikes.  
Visualization: Bar chart of crash severity by day (built in Colab).
6. Data Storytelling
Created a virtual poster summarizing findings and recommending:  
Targeted signage at high-risk intersections.  
Enhanced rush-hour traffic management.  
Data collection improvements in underreported areas.
How to Explore This Project
Run It: Open the notebook in Colab: NYC Crash Analysis Notebook.  
View Code: Check out the repo: github.com/<your-username>/nyc-crash-analysis.  
Live Demo: See the hosted visuals: your-username.github.io/nyc-crash-analysis.
Note: Replace <your-username> and links with your actual details after setup.
Why This Matters
This project demonstrates my ability to:  
Wrangle Data: Handle large, messy datasets with missing values.  
Analyze Trends: Use time series and geospatial techniques to extract insights.  
Communicate: Translate complex findings into actionable recommendations.  
Think Ethically: Consider bias and its implications on public policy.
For recruiters, this showcases a blend of technical proficiency (Python, Pandas, visualization libraries) and practical problem-solving applied to real-world safety challenges.


# Cyclistic-Bike-Share-Data-Analysis

Project Overview

This project analyzes Cyclistic's 2023 bike-share data to uncover differences in how annual members and casual riders use bikes, with the goal of informing marketing strategies to convert casual riders into annual members. Using Divvy’s open-source trip data (Cyclistic’s real-world counterpart), the analysis leverages SQL (PostgreSQL) for data processing and Python for visualizations to deliver actionable insights.

## Business Problem

Cyclistic, a bike-share company, seeks to increase annual memberships for sustainable growth. This project identifies usage patterns to design targeted marketing campaigns that convert casual riders into loyal members.

## Dataset

- **Source**: Divvy Bike Data Portal (Jan-Dec 2023)
- **License**: Open data license by Motivate International Inc.
- **Size**: 5.7 million rows, \~1.3 GB (sample data included in `/data`)
- **Link**: Divvy Data Portal
- **Attributes**: ride_id, rideable_type, started_at, ended_at, start_station_name, start_station_id, end_station_name, end_station_id, start_lat, start_lng, end_lat, end_lng, member_casual, ride_length, day_of_week

## Repository Structure

- `/data`: Sample dataset (`202301-divvy-tripdata.csv`)
- `/scripts`:
  - `data_cleaning.sql`: SQL queries for cleaning and transforming data
  - `analysis.sql`: SQL queries for ride statistics, daily/hourly trends, etc.
- `/notebooks`: `cyclistic_analysis.ipynb` (Jupyter Notebook with analysis and visuals)
- `/visualizations`: Output charts (`total_rides.png`, `ride_duration_distribution.png`, etc.)
- `/docs`: Data cleaning log and methodology summary

## Methodology

1. **Data Preparation**:
   - Imported 12 months of Divvy data (CSV format) into PostgreSQL using `\copy`.
   - Cleaned data: removed rows with `ride_length <= 0`, added `ride_length` and `day_of_week` columns.
   - Verified data integrity (no duplicates, consistent formats).
2. **Analysis**:
   - Used SQL to aggregate ride counts, durations, and trends by rider type.
   - Analyzed daily/hourly patterns and popular start stations.
   - Grouped ride durations into buckets (0-15 min, 15-30 min, etc.).
3. **Visualization**:
   - Generated pivot charts in Excel.

## Key Findings

- **Ride Volume**: Annual members account for 64% of rides, while casual riders make up 36%.
- **Ride Duration**: Members take shorter, consistent trips (mostly &lt;15 min), indicating commuting. Casual riders take longer trips (often &gt;60 min), suggesting leisure use.
- **Daily Trends**: Members ride more on weekdays (peaking Tuesday-Thursday), while casual riders peak on weekends (Friday-Sunday).
- **Hourly Trends**: Members show commuting peaks at 8 AM and 5 PM; casual riders peak at 5 PM with gradual increases.


## Recommendations

1. **Casual Riders**:
   - Offer weekend ride packages to capitalize on peak usage.
   - Provide discounts for long-duration rides to encourage membership.
   - Promote app sign-ups with loyalty perks.
2. **Annual Members**:
   - Launch referral programs to grow membership.
   - Offer weekday usage incentives (e.g., bonus points).
3. **Both Groups**:
   - Increase bike availability during peak hours (8 AM, 5 PM).
   - Optimize bike placement at high-traffic stations based on start station data.

## How to Run

1. Download the full dataset from the Divvy Data Portal or use `/data/202301-divvy-tripdata.csv`.
2. Set up a PostgreSQL database and import data using `scripts/data_cleaning.sql`.
3. Run `scripts/analysis.sql` to generate aggregated insights.
4. Create visualizations using Excel Pivot Charts to uncover trends, compare user behavior, and present insights in a clear and interactive format.
5. Explore the full analysis in `notebooks/cyclistic_analysis.ipynb`.

## Tools Used

- **Data Processing**: PostgreSQL, SQL
- **Visualization**: Excel
- **Cleaning**: Microsoft Excel, PostgreSQL
- **Documentation**: Markdown, Jupyter Notebook

## Kaggle Notebook

View an interactive version of this analysis: Cyclistic Bike-Share: Data Analysis and Insights.

## Contact

- **Author**: Prince Edem Amenyenu
- **Email**: \[datawithedem@gmail.com\]
- **LinkedIn**: \[https://www.linkedin.com/in/prince-edem-amenyenu-6979591b8/\]

## License

This project is licensed under the MIT License. Data usage is subject to Divvy’s open data license.

## Acknowledgments

- Divvy and Motivate International Inc. for providing the dataset.
- Cyclistic case study inspired by real-world bike-share operations.


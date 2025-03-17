# tableau-challange
# Citi Bike Trip Analysis 

## Overview
This project aggregates data from the Citi Bike Trip History Logs to uncover two unexpected phenomena. By analyzing the data, designing visualizations, and creating dashboards, we aim to provide insights for city officials to improve New York City's bike-sharing program. The findings will be presented in a Tableau story, including static or dynamic maps as specified.

## Key Questions to Explore
- Total number of trips during the selected period.
- Percentage growth in total ridership.
- Changes in proportions of short-term customers vs. annual subscribers.
- Peak hours of usage during summer and winter months.
- Identification of the top and bottom 10 stations for starting and ending journeys.
- Analysis of trip duration by user type.
- Average distance of bike trips.
- Identification of bikes (by ID) likely due for repair or inspection.
- Variability in bike utilization.

## Citibike Solution
- [Citi Bike Tableau Story](https://public.tableau.com/app/profile/saurabh.lakhanpal/viz/CitiBikeAnalysis_17422278378610/JerseyCityBikesStory)
- [Ourliers Tableau Dashbaord](https://public.tableau.com/app/profile/saurabh.lakhanpal/viz/CitiBikeAnalysis-Outliers/Outliers)
- To use this Repository:
  - Clone the repository.
  - Run the ETL File.
  - This shall scrape the data csvs and create a clean useable file in Resources/Tableau folder.
  - Use the created Jul22_to_Jul23.csv in Tableau for Analysis.

## **Analysis**

**1. Summary Data:**

  Citibike Start Stations are primarily concentrated in zip codes 07302 (Kearney) and 07030 (Hoboken).
  Member rides account for 70% of total rides, with casual rides making up the remaining 30%. 
  Classic bikes are the most popular choice, representing 78% of all rides, followed by electric bikes at 21%, and docked bikes at 1%. 
  The average distance traveled per ride is 1.164 kilometers, with an average duration of 10.19 minutes.
  This aligns with the bike hire policy, which encourages rides of no more than 30 minutes for casual riders and 45 minutes for members at a time.
  
![image](https://github.com/user-attachments/assets/cfe3ae00-1257-43ed-a74b-1acd38a80e2f)

**2. Peak Times to Ride:**

  Peak ride hours are typically around 5 pm and 6 pm, with summer being the preferred season due to favorable weather. Midweek, specifically Wednesday, Thursday, and Friday, sees the highest ridership. Daily ridership shows a seasonal pattern, with fewer rides in winter and the most in summer.
  Members primarily use bikes for commuting, with peak usage in the mornings (8 am) and evenings (5 pm, 6 pm) on weekdays, peaking on Wednesdays. Their usage follows a seasonal trend throughout the year.
  Casual riders favor evening rides, with summer and fall being their top seasons, and weekends, especially Saturdays, are popular. The yearly trend for casual riders is also seasonal, with a higher proportion during the summer, likely due to tourists visiting the city.

![image](https://github.com/user-attachments/assets/029ae0ba-60d2-4045-8d02-8bac4c465268)

**3. Top 10 Stations:**

  The top 10 Start Stations by average daily rides are identical to the top 10 End Stations, and they are in the same order. Four stations (2. Hoboken Terminal - River St & Hudson Pl, 3. South Waterfront Walkway, 4. Hoboken Terminal - Hudson St & Hudson, and 5. City Hall) are located within a 300m radius in zipcode 07030. The other two stations within 200m of each other in the top 10 are Newport PATH and Newport Pkwy in zipcode 07310. Additionally, most Start and End Stations tend to be within 2 kilometers of each other and are usually located within the same zipcode.

![image](https://github.com/user-attachments/assets/221c5013-bfd4-4a7d-b7ad-d55db286ea4d)

**4. Casual vs Member Rides:**

  Casual rides have a longer average duration and cover more distance than member rides. This also holds true for classic and electric bikes. Note. 'docked bikes' are only used in casual rides.
  Member rides tend to cover a slightly larger area of New Jersey compared to casual rides. The majority of both member and casual rides start in areas with '2018 Per Capita Income' ranging from $37,200 to $461,000, as indicated by the grey shades in the background. Interestingly, these areas coincide with the two zip codes where most rides begin, namely 07030 (Hoboken) and 07302 (Kearny).

![image](https://github.com/user-attachments/assets/d3eb8140-15ba-4028-a3bf-7aafa078ff32)

**Outliers Dashboard:**

  Citibike riders have specific ride duration allowances: Casual riders get 30 minutes per ride and are billed $0.26/minute afterward, while Members get 45 minutes per ride and are billed $0.17/minute afterward.
  Most rides fall within a 15-minute duration, as seen in the histogram of ride counts by duration. The billing structure encourages shorter rides to limit both distance and bike availability for others.
  When examining bike types, docked bikes show a longer average duration but the shortest distance. This suggests possible docking issues or faults. Note that rides by staff or during servicing have already been excluded from the data.
  Rides with durations exceeding 120 minutes were removed from the analysis to prevent skewing the results.

![image](https://github.com/user-attachments/assets/5a902e97-0cc0-4b2e-a5c3-8272fa609b32)

**Data:** https://s3.amazonaws.com/tripdata/index.html
  - JC-202207-citbike-tripdata.csv
  - JC-202208-citibike-tripdata.csv
  - JC-202209-citibike-tripdata.csv
  - JC-202210-citibike-tripdata.csv
  - JC-202211-citibike-tripdata.csv
  - JC-202212-citibike-tripdata.csv
  - JC-202301-citibike-tripdata.csv
  - JC-202302-citibike-tripdata.csv
  - JC-202303-citibike-tripdata.csv
  - JC-202304-citibike-tripdata.csv
  - JC-202305-citibike-tripdata.csv
  - JC-202306-citibike-tripdata.csv
  - JC-202307-citibike-tripdata.csv

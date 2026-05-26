## Research Question
Do PM2.5 exposure and median household income percentile predict asthma-related incidents across NYC zipcodes?

## Methodology (R studio)
1) Download a shapefile of zip codes and filter by NYC zip codes.
2) Download the PM2.5 raster data as the mean for 2023 and aggregate by ZIP code.
3) Download the EMS Incident Dispatch data filtered by Final Call Type: Asthma, and Year 2023. Create a new column, incident_count, which counts the number of Asthma-related incidents by zipcode.  
4) Access the census data for median income through the census API key, and only keep the median income information for the NYC zipcodes. 
5) Join the EMS, census, and PM2.5 data for 2023 into one sf object. Create a new column med_income_pct for income percentile.   
6) Create static maps for PM2.5 levels, EMS Asthma-related incidents, and Median income percentile.
7) Create scatter plots using ggplot for Average PM2.5 vs Asthma-related incidents, Median income percentile vs Asthma-related incidents, and Median Income percentile vs Mean PM2.5.
8) Create a leaflet web interactive map for PM2.5, median income percentile, and EMS Asthma-related incidents. 
9) Create a linear regression model for EMS incidents by PM2.5 and median income. Format the results using the stargazer package.
    
## Results
1) Both PM2.5  and median household income are important in predicting asthma-related EMS calls (p < 0.01).
2) For every 1µg/m³ increase in PM2.5, Asthma-related incidents increase by 17.7.
3) For every 1 percentile decrease in median income, incidents increase by 0.82.
4) Variation in EMS incidents across zipcodes is 47%.
   
## Next Steps
To expand this project further, I would like to add race proportions into the regression model to examine if it contributes to higher or lower EMS asthma-related calls. This would lead to a more interesting environmental justice analysis. I would also like to add nitrogen dioxide raster data for the year 2023 when it becomes available. I would also like to investigate different years to see whether the trends that I see in 2023 persist or change across decades or years.  

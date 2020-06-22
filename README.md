# PyBer Analysis Report

## Background and Results

### Purpose
The purpose of the Analysis Report is to:
1. Create a summary DataFrame of the key metrics for the ride-sharing data by city type
2. Create a multiple-line graph that shows the total fares for each week by each city type
3. Submit a written report on the results of the new analysis, challenges encountered and overcame, and any future recommendations for analysis

### Technical Analysis

In order to perform the additional analysis, the following files have been used:
- city_data.csv
- ride_data.csv

*Files are available under "Resources/" folder*

In order to complete assignment 1. both data included in .csv files were merged using pandas library.
During previous analysis, we noticed that data was readable and directly usable without any alteration.
A recap DataFrame was built in order to summarize the metrics below:
- Total Rides
- Total Drivers
- Total Fares
- Average Fare per Ride
- Average Fare per Driver

For assignment 2., the starting point was the same as for the DataFrame summary: the merged data from the two .csv files.
Methods from both Pandas and Matplotlib libraries were used to create a graph to outline the sum of the weekly fares for each city type from January 1st, 2019 to April 28th, 2019.

*Code for both assignments is in the PyBer_Challenge.ipynb file*


### Results
Below are the results for the first two assignments.
Both results are analyzed in the **Summary** part below.

#### Summary DataFrame
![Summary_DataFrame](Analysis\Summary_DataFrame.png)

#### Multiple-Line Plot for the Sum of the Fares for Each City Type
![Multiple-Line_Plot](Analysis\Fig_Challenge.png)

### Summary

#### Summary DataFrame
Regarding the DataFrame Summary, we could notice than rural cities have the highest average fare by ride, followed by suburban cities and urban cities. However, values are quite in the same range (about $30).
Regarding the average fare by driver, the discrepancies are more explicit: for rural cities, the values are more than three times the ones for urban cities and almost 50% higher than suburban cities.

Based on these results, increasing the number of drivers in rural and suburban cities should not lower a lot the cost of a ride but would probably cut down the revenue for the current active drivers in those aeras. We should, thus, focus on hire more drivers in suburban and rural cities to potentially increase revenue.

#### Multiple-Line Plot for the Sum of the Fares for Each City Type

For the targeted time frame, we can notice than the total fare repartition stays quite the same between all type of cities and stays in ranges:
- Urban: between $1,750 and $2,500
- Suburban: between $750 and $1,500
- Rural: between $250 and $500

For urban and suburban cities, the results show a slightly increase of the total fare with seasonal variations during the period: for urban cities, total fare went from $1,750 to 2,250$ and for suburban cities, it went from $750 to $1,250.
For rural cities, the total fare did not increase during the period despite some seasonal variations.

## Challenges Encountered and Overcome

### Challenges and Difficulties Encountered

There were two relevant difficulties encountered during the assignments:
- getting the total drivers for each kind of cities
- changing the format of the index for the DataFrame used to plot the multiple-lines chart

### Technical Analyses Used
After checking online, challenges were overcame by:
- getting the total drivers for each kind of cities => using the groupby() with multiples parameters (needed to remember that this method allow multiple parameters)
![Difficulty_1](Analysis\Diff_1.png)

- changing the format of the index for the DataFrame used to plot the multiple-lines charts => using the pandas.to_datetime() method
![Difficulty_2](Analysis\Diff_2.png)


## Recommendations and Next Steps

For addressing the disparities among the city types, and based on the data provided, drivers in suburban and rural cities should be increased. The goal is that for every type of cities, average fare per ride and average fare by drivers should tend to be equal.
The summary DataFrame built could be useful to track and follow this goal and the multiple-line chart could also be re-used: suburban and rural lines should get closer to the urban one (but should still respect the drivers number repartition between each city type which is currently 81%, 16% and 3% for respectively urban, suburban and rural cities).


### Recommendations for Future Analysis

### Additional Analysis 1

#### Description of Approach

In order to better find another trends, we should expend our data history to include the whole 2019 year and the two prior years (2018 and 2017). 

#### Technical Steps

We can add the additional years in our summary DataFrame to visualize the evolution of the ratios and maybe identity some trends.
Multiple-lines chart could also benefit from this wider time frame and trends might appear.

### Additional Analysis 2

#### Description of Approach

We focused on city types during the analysis but we could dive a little bit further into each city type: some urban cities are maybe lacking drivers too or some suburban cities maybe have, on the opposite, already too many drivers.
In addition, we know about each ride made but it would be really helpful to know how many ride requests are made and if all of them are fulfilled for each city. It will help the company to focus of these specific cities first to capture this potential lost revenue.

#### Technical Steps

We could compute percentages of ride requests achieved for each city first. Then, we could cut each city type into several and adequate bins to help prioritize the actions to be taken.  

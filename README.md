## **Air Emissions Exploratory Data Analysis**
![Image of Emissions](https://www.sciencealert.com/images/2019-03/processed/COALuseIncreasing2018_1024.jpg)

### **Data:**
This data set looks at four of the six criteria pollutants set by the EPA: carbon monoxide, ground-level ozone, nitrogen dioxide, and sulfur dioxide. The standards are set at a level that protects public health with an adequate margin of safety. 
The data frame contained 29 Columns and 1.75 million rows detailing the sampling location, date of sample and emissions data. Pollutants were recorded by day as mean, max value, hour of max value, and Air quality Index (AQI) for that pollutant.
The dataset used was retrieved from kaggle: https://www.kaggle.com/sogun3/uspollution




### **Cleaning:**
Missing Data:  About half of the Air Quality Index data points (over 800,000) were missing for SO2 and CO in the initial dataset.  There were some readings of negative values and those were removed as you cannot have a negative concentration.  There were also duplicate readings for some days, to handle this the data was averaged and aggregated,  this aggregation reduced the missing data points to 589 for Sulfur Dioxide and 225 for Carbon Monoxide.  Several columns were removed that didn’t seem to add to this specific analysis including County code, State code, Site Number, County, Address, City.  Pollutant units were removed from the data set and any aggregation of all pollutants was based on the AQI which is unitless.
The resulting cleaned dataset that was used for Exploratory Data Analysis (EDA) consisted of 400,000 rows and 18 columns.





### **Data Analysis:**
The data provided opportunities for grouping by geography as well as time, the most interesting visualization was the seasonal trend that emerged when graphing by monthly mean values.  As you can see below:
* NO2 increases in the winter as energy use ramps up and is broken down slowly due to limited sunlight.  
* Carbon Monoxide increases in the winter when combustion for heating is increased.  
* Ozone peaks in the summer when production is increased by sunlight reacting with nitrous oxides and volatile organic compounds.

![Monthly Average Pollutants](https://github.com/slindhult/Capstone-1/blob/master/Images/monthly.jpg?raw=true)











#### AQI Levels
AQI is a great way to compare the pollutants, it extrapolates their health effects based on concentration and gives you a numer that is comparable.  Since Carbon Monoxide and Ozone are measured in parts per million (ppm) and Sulfur Dioxide and Nitrogen Dioxed are measured in parts per billion (ppb) it is difficult to do otherwise.
The EPA uses the Air Quality Index to determine the level of safety for the public.  It is broken into five categories: Good, Moderate, Unhealthy for Sensitive Populations, Unhealthy, and Hazardous.   On 65 days the level rose to  Very Unhealthy, 28 times in California, 13 in Pennsylvania, and 10 in Texas.  The max Total AQI in the dataset was 218 in California for Ozone which was the main cause of Very Unhealthy AQI days.  You can check the current AQI here: https://airnow.gov/
![AQI Levels](https://github.com/slindhult/Capstone-1/blob/master/Images/combined.jpg?raw=true)


### **Hypothesis Testing:**

In analyzing this data I wanted to see if there was a statistically significant change in Air Quality between the year 2000 and 2015 (the most recent full year of data.)  Below is a graph of each pollutant, you can see that AQI for CO, SO2 and NO2 was improved but that Ozone increased. 
![2000 vs 2015](https://github.com/slindhult/Capstone-1/blob/master/Images/overtime.jpg?raw=true)

Here is a visualization of the highest AQI level for each month of 2015:
![Alt Text](https://github.com/slindhult/Capstone-1/blob/master/Images/monthlyaqi.gif?raw=true)

### **Sources**
https://www.airnow.gov/index.cfm?action=aqibasics.aqi

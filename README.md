## **Air Emissions Exploratory Data Analysis**
![Image of Emissions](https://www.sciencealert.com/images/2019-03/processed/COALuseIncreasing2018_1024.jpg)

### **Data:**
The Clean Air Act requires the EPA to set National Ambient Air Quality Standards (NAAQS) for maximum allowable concentrations of six "criteria" pollutants in outdoor air. This data set looks at four of the six pollutants: carbon monoxide, ground-level ozone, nitrogen dioxide, and sulfur dioxide. The standards are set at a level that protects public health with an adequate margin of safety. 

The dataset contained 29 Columns and 1.75 million rows detailing the sampling location, date and emissions data. Pollutants were recorded by day as mean, max value, hour of max value, and Air quality Index (AQI) for that pollutant.


### **Cleaning:**

The dataset contained air emissions records from 47 states, the District of Columbia and the Country of Mexico.  The states missing throughout were Mississippi, Montana, Nebraska, Vermont, West Virginia.  There were fewer states in the earlier years and some states were missing a month here and there.
Missing Data:  About half of the Air Quality Index data points (over 800,000) were missing for SO2 and CO in the initial dataset.  There were some readings of negative values and those were removed as you cannot have a negative concentration.  There were also duplicate readings for some days, to handle this the data was averaged and aggregated,  this aggregation reduced the missing data points to 589 for Sulfur Dioxide and 225 for Carbon Monoxide.  Several columns were removed that didn’t seem to add to this specific analysis including County code, State code, Site Number, County, Address, City.  Pollutant units were removed from the data set and any aggregation of all pollutants was based on the AQI which is unitless.
The resulting cleaned dataset that was used for Exploratory Data Analysis (EDA) consisted of 400,000 rows and 18 columns.



![Monthly Average Pollutants](https://github.com/slindhult/Capstone-1/blob/master/Images/monthly.jpg?raw=true)

### **Data Analysis:**

![States Total Mean AQI](https://github.com/slindhult/Capstone-1/blob/master/Images/USAAQI.jpg?raw=true)


![Daily Average Pollutants](https://github.com/slindhult/Capstone-1/blob/master/Images/byday.jpg?raw=true)


The EPA uses the Air Quality Index to determine the level of safety for the public.  It is broken into five categories: Good, Moderate, Unhealthy for Sensitive Populations, Unhealthy, and Hazardous.   On 65 days the level rose to  Very Unhealthy, 28 times in California, 13 in Pennsylvania, and 10 in Texas.  The max Total AQI in the dataset was 218 in California for Ozone.  You can check the current AQI here: https://airnow.gov/
![AQI Levels](https://github.com/slindhult/Capstone-1/blob/master/Images/leveldays.jpg?raw=true)


### **Hypothesis Testing:**

In analyzing this data I wanted to see if there was a statistically significant change in Air Quality between the year 2000 and 2015 (the most recent full year of data.)  Below is a graph of 
![2000 vs 2015](https://github.com/slindhult/Capstone-1/blob/master/Images/overtime.jpg?raw=true)


![Alt Text](https://github.com/slindhult/Capstone-1/blob/master/Images/new_map_normal.gif?raw=true)

### **Future:**


### **Sources**
https://www.airnow.gov/index.cfm?action=aqibasics.aqi

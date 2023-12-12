# Part 1 - DATA 512 

# Common Analysis for the Wildfire impact on Cladwell city in the state of Idaho

**Introduction**

In recent years, the western United States has experienced a notable uptick in the occurrence of extensive wildfires, resulting in the widespread dispersion of smoke across multiple states. This concerning trend has prompted discussions about its potential causes, including factors such as climate change, US forestry policies, and a heightened societal awareness of the issue. Regardless of the underlying drivers, the impacts of these wildland fires are profoundly felt. Extensive research now underscores the adverse effects of smoke on various aspects of society, including health, tourism, property values, and more.

This course project endeavors to delve into a detailed analysis of the ramifications of wildfires on a specific city within the United States. The overarching goal is to equip key stakeholders such as policymakers, city managers, city councils, and civic institutions with the necessary insights to make well-informed decisions regarding the formulation of plans aimed at mitigating future impacts stemming from wildfires.

# Data Resources

We were provided with website links from where we scrapped data and also with some initial code to start with. Here are some of the links:

1) Data Source: https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81
2) AQI information source: https://www.airnow.gov/sites/default/files/2020-05/aqi-technical-assistance-document-sept2018.pdf
3) The [wildfire](https://github.com/aditikharkwal/DATA-512_Project/tree/main/Project%201/wildfire) folder with beginner code was provided to us by Dr. McDonald.

# Implementation

I have implemented the steps till estimation of smoke from my city, some relevant visualizations and forecasting in the .ipynb file titles - "Project 1 - part 1.ipynb" (Step 1: (1-3))

The second part of the project implementing the AQI part in the file named - "Project 1 - part 2.ipynb" (Step 1: (4-5))

**Step 1: Create fire smoke estimates**

1) Explore wildfire data using Python's GeoJSON and ArcGIS file readers, or leverage pandas for data extraction. Alternatively, utilize a custom GeoJSON reader for a tailored approach. Select the method that aligns best with your expertise for efficient data processing.
2) After successfully reading the wildfire data, the next step is to implement a geodetic distance computation to identify all fires located within a specified distance from your chosen city. This crucial process will enable precise spatial analysis for a comprehensive assessment of wildfire impacts.
3) The third task involves devising a method to estimate smoke levels for your selected city. It's logical to assume that a large, proximate fire burning a substantial area would emit more smoke into the city compared to a smaller, distant fire. Define your smoke estimation approach and systematically apply it to each fire within the city's vicinity. Consider whether the estimate should accumulate throughout the year or be distributed over the fire season. Document the rationale behind your decision-making process and outline the steps taken to formulate the smoke estimate.
4) Compare your smoke estimate with available Air Quality Index (AQI) data from the US EPA. Since the EPA's monitoring infrastructure is limited, estimating AQI for your city may be necessary. Access the US EPA Air Quality System API with a required API key, and determine if data is available based on your city's county or through a geodetic bounding box. Keep in mind that your city may not have a monitoring station within its bounds, so indirect estimates may be required. Consider the nature of AQI measures, their computation, and their relevance to fire smoke when making comparisons.
5) Create a predictive model using fire data and the smoke estimate for your designated city. The model should forecast smoke estimates for each year over the next 25 years (2024-2049). Pay careful attention to convey the appropriate levels of uncertainty in your predictions to ensure accurate and reliable forecasts.


**Step 2: Visualize aspects of your analysis**

You will illustrate the work of your analysis with a few time series graphs. The wildfire data is annual, so your time series will be on an annual basis. All the time series should cover the analysis range defined above, but not the prediction range.

1) Produce a histogram showing the number of fires occurring every 50 mile distance from your assigned city up to the max specified distance.
2) Produce a time series graph of total acres burned per year for the fires occurring in the specified distance from your city.
3) Produce a time series graph containing your fire smoke estimate for your city and the AQI estimate for your city.


**Results of Visual Analysis and Forecasting**

Following are some results out of my visual analysis and forecasting:

1) Number of Fires vs Distance

![image](https://github.com/aditikharkwal/DATA-512_Project/assets/38849313/b9dc9835-8503-450a-a518-d4307bf9bce6)

2) Total Acres Burned per year
   
![image](https://github.com/aditikharkwal/DATA-512_Project/assets/38849313/738039a7-cf54-48e3-8030-840332dec8c0)
 
4) Time series graph and AQI estimate of my city
   
![image](https://github.com/aditikharkwal/DATA-512_Project/assets/38849313/7bd3398e-edf7-4547-ab0e-bcfe43d4994c)

6) Time series analysis of yearly smoke estimates for the next 25 years
   
![image](https://github.com/aditikharkwal/DATA-512_Project/assets/38849313/d3d4f504-70e0-493b-be55-b80034fd9501)


# Reproducing the Analysis
To replicate this analysis, adhere to the following instructions:

Clone this repository to your local machine. Ensure Python is installed with the required libraries. Within the project directory, create a 'data' folder. Download the GeoJSON Files.zip from this link, extract the "USGS_Wildland_Fire_Combined_Dataset.json" file, and place it in the 'data' folder. Execute 'wildfire_analysis.ipynb' to generate analyses such as smoke analysis, AQI analysis, and their comparison. Examine the results and interpret the findings accordingly.

# License
This project is licensed under the MIT License - see the LICENSE file for details.


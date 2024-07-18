# Final Assignment - Applied Plotting, Charting & Data Representation in Python (University of Michigan offered via Coursera)

## Getting started

To open and run the notebook in VSCode [use the conda environment](https://code.visualstudio.com/docs/python/environments#_python-environment-tools).

## Introduction

The final assignment in the course 'Applied Plotting, Charting & Data Representation in Python' (University of Michigan), was to create a visualization using publicly available data, which would aid in answering a pre-specified question. The assignment included the following criteria:

- You must state a question you are seeking to answer with your visualizations.
- You must provide at least two links to available datasets. These could be links to files such as CSV or Excel files, or links to websites which might have data in tabular form, such as Wikipedia pages.
- You must upload an image which addresses the research question you stated. In addition to addressing the question, this visual should follow Cairo's principles of truthfulness, functionality, beauty, and insightfulness.
- You must contribute a short (1-2 paragraph) written justification of how your visualization addresses your stated research question.

For this assignment I asked the question: What is the recent impact that global climate change has had on yearly and seasonal wind speeds in the state of Washington? 

## Methods

My project used the following 4 datasets, which I downloaded from Open-Meteo (https://open-meteo.com/en/docs), and are available in the 'data' folder:

#Seattle
'https://raw.githubusercontent.com/e-t-h-a-n-w/datavis_final/main/open-meteo-47.63N122.32W59m_SEA.csv'
#Yakima
'https://raw.githubusercontent.com/e-t-h-a-n-w/datavis_final/main/open-meteo-46.57N120.53W325m_YAK.csv'
#Bellingham
'https://raw.githubusercontent.com/e-t-h-a-n-w/datavis_final/main/open-meteo-48.75N122.44W23m._BHM.csv'
#Spokane
'https://raw.githubusercontent.com/e-t-h-a-n-w/datavis_final/main/open-meteo-47.63N117.43W520m_SPO.csv'

in order to generate the datasets from the website, I searched for each of the 4 cities in the search bar under the "Location and Time" section and I subset to the days between 01JAN2010-31DEC2019. The output generated in my project makes use of the "Daily Weather" variable "Maximum Wind Speed (10 m)". For a given city and year, seasonal averages are calculated as the average daily maximum windspeed, as measured at 10 meters of altitude. Seasons were binned according to: 
  - winter (January, February, March)
  - spring (April, May, June)
  - summer (July, August, September)
  - fall (October, November, December)
  
The 'code' directory contains the jupyter notebook file used in this project ("assignment4.ipynb"), which produces the two outputs: "10 year change in average daily max wind speed.pdf" and "Seasonal change in average daily max wind speed across 10 years.pdf", which are also located in the 'output' directory. 

## Results
These visualizations utilized 10 years (2010-2019) of wind speed data, with measurements taken in 4 major cities (Bellingham, Seattle, Yakima, Spokane) in the state of Washington. These cities were chosen for their geographic diversity as well as their distribution across the state, so that any conclusions would be representative of the entire state. I chose to model seasonal averages of daily max wind speed, as a compromise between daily time series data (which can be messy and difficult to interpret) and yearly data (which would obscure seasonal wind patterns).

The results were interesting! Seattle and Bellingham (both coastal western cities) showed nearly the exact same seasonal trends, experiencing a significant increase in average seasonal wind speeds in the last 3 years analyzed (2017-2019), while each city shows seasonal wind trends (lower wind speeds in the spring and summer) there was no evidence of a temporal-seasonal trend, in that the observed change in wind speed over time was the similar regardless of season. Spokane (eastern WA) showed evidence of decreasing wind speeds over time, which was fairly consistent across seasons. Yakima (central WA) stands out in that the average yearly wind speed (aggregated across seasons) remained stable across the 
10 year span, however the seasonal changes over time were significant. An increase in wind speeds in the spring and summer was observed, along with a simultaneous and nearly equally decrease in wind speeds in the winter and fall seasons.

## Discussion
The following is a summary of the design choices for my visuals in regard to Cairo’s principles of truth, beauty, function, and insight:
 - Truthfulness: The selection of cities in the state of WA was intended to provide the most representative analysis with regard to the spatial and geographical extent of the state. The diversity of conclusions about temporal and seasonal trends across cities lends credibility to the assertion that I did not try to alter or obscure outcomes
 - Beauty: the color gradient, neat organization, trimming of unnecessary axis ticks, and removal of duplicate y-axis labels where they are not needed 
 - Functionality: Plotting seasonal averages instead of daily averages allows the viewer to observe trends, which would otherwise be impossible to see on a daily scale, because the data is too much and too variable. Legends, axes, and titles are labelled and sized for easy and accurate viewing.
 - Insightfulness: the color gradient goes from light to dark with time, so that the reader can easily see the temporal patterns

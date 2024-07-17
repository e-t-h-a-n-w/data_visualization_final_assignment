As a final assignment in the course 'Applied Plotting, Charting & Data Representation in Python' (University of Michigan), we were tasked with the following:

  -You must state a question you are seeking to answer with your visualizations.
  -You must provide at least two links to available datasets. These could be links to files such as CSV or Excel files, or links to websites which might have data in tabular form, such as Wikipedia pages.
  -You must upload an image which addresses the research question you stated. In addition to addressing the question, this visual should follow Cairo's principles of truthfulness, functionality, beauty, and insightfulness.
  -You must contribute a short (1-2 paragraph) written justification of how your visualization addresses your stated research question.

PROMPT
Create a research question about the domain category and region that you identified.

RESPONSE
What is the recent impact that global climate change has had on yearly and seasonal wind speeds in state of Washington?

********************************

PROMPT
Provide at least two links to publicly accessible datasets. These could be links to files such as CSV or Excel files, or links to websites which might have data in tabular form, 
such as Wikipedia pages.

RESPONSE
My project used the following 4 datasets, which I downloaded from Open-Meteo (https://open-meteo.com/en/docs), and uploaded to this repository:

#Seattle
'https://raw.githubusercontent.com/e-t-h-a-n-w/datavis_final/main/open-meteo-47.63N122.32W59m_SEA.csv'
#Yakima
'https://raw.githubusercontent.com/e-t-h-a-n-w/datavis_final/main/open-meteo-46.57N120.53W325m_YAK.csv'
#Bellingham
'https://raw.githubusercontent.com/e-t-h-a-n-w/datavis_final/main/open-meteo-48.75N122.44W23m._BHM.csv'
#Spokane
'https://raw.githubusercontent.com/e-t-h-a-n-w/datavis_final/main/open-meteo-47.63N117.43W520m_SPO.csv'

in order to generate the datasets from the website, I searched for each of the 4 cities in the 'search' bar under the "Location and Time" section. 
and I subset to the days between 01JAN2010-31DEC2019. The output generated in my project makes use of the "Daily Weather" variable "Maximum Wind Speed (10 m)".

********************************

PROMPT
Upload an image which addresses your research question. 
In addition to addressing your research question, this visual should address Cairo's principles of truthfulness, functionality, beauty, and insightfulness.

RESPONSE
Seasonal Change in Wind Speed in 4 Cities Across Washington State (2010-2019)

For a given city and year, seasonal averages are calculated as the average daily maximum windspeed, as measured at 10 meters of altitude. 
Seasons are binned as: 
  -winter (January, February, March)
  -spring (April, May, June)
  -summer (July, August, September)
  -fall (October, November, December)

********************************

PROMPT
Provide a short (1-2 paragraphs) justification of how your visual addresses your research question.

RESPONSE
This visualization utilized 10 years (2010-2019) of wind speed data, with measurements taken in 4 major cities (Bellingham, Seattle, Yakima, Spokane) in the state of Washington. 
These cities were chosen for their geographic diversity as well as their distribution across the entire state, so that any conclusions would be representative of the entire. 
I chose to model seasonal averages of daily max wind speed, as a compromise between daily time series data (which can be messy and difficult to interpret) and yearly data 
(which would obscure seasonal wind patterns).

The results were interesting! Seattle and Bellingham (both coastal western cities) showed nearly the exact same seasonal trends, experiencing a significant increase in average 
seasonal wind speeds in the last 3 years analyzed (2017-2019), while each city shows seasonal wind trends (lower wind speeds in the spring and summer) there was no evidence of a 
temporal-seasonal trend, in that the observed change in wind speed over time was the similar regardless of season. Spokane (eastern WA) showed evidence of decreasing wind speeds 
over time, which was fairly consistent across seasons. Yakima (central WA) stands out in that the average yearly wind speed (aggregated across seasons) remained stable across the 
10 year span, however the seasonal changes over time were significant. An increase in wind speeds in the spring and summer was observed, along with a simultaneous and nearly equally 
decrease in wind speeds in the winter and fall seasons.

********************************

PROMPT
As this assignment is for the whole course, you must incorporate and defend the principles discussed in the first week, specifically, 
Cairo’s principles of truth, beauty, function, and insight.

For each of the following prompts, please provide a response that links each principle to one or more elements of your visual. 

  -Describe your design choices for your visual in regards to Cairo's principle of truthfulness.
  -Describe your design choices for your visual in regards to Cairo's principle of beauty.
  -Describe your design choices for your visual in regards to Cairo's principle of functionality. 
  -Describe your design choices for your visual in regards to Cairo's principle of insightfulness. 

RESPONSE
  -Truthfulness: The selection of cities in the state of WA was intended to provide the most representative analysis with regard to the spatial and geographical extent of the state. 
  The diversity of conclusions about temporal and seasonal trends across cities lends credibility to the assertion that I did not try to alter or obscure outcomes
  
  -Beauty: the color gradient, neat organization, trimming of unnecessary axis ticks, and removal of duplicate y-axis labels where they are not needed 
  
  -Functionality: Plotting seasonal averages instead of daily averages allows the viewer to observe trends, which would otherwise be impossible to see on a daily scale, 
  because the data is too much and too variable. Legends, axes, and titles are labelled and sized for easy and accurate viewing.
  
  -Insightfulness: the color gradient goes from light to dark with time, so that the reader can easily see the temporal patterns

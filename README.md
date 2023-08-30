# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
The primary aim of this project was to gather data from multiple API sources. This included extracting bike station data from city bikes for a specific city, along with information about businesses situated within a 1000m radius of those bike stations, utilizing both the Foursquare and Yelp APIs. 

The project's objectives encompassed the creation of dataframes, a comprehensive amalgamated dataframe comprising all three datasets featuring pertinent details, and the initiation of Exploratory Data Analysis (EDA) procedures. EDA encompassed data refinement, visualization, and insight generation. 

Additionally, the project involved constructing a regression model using the collected data to uncover potential correlations between bike station statistics and the attributes of businesses within a 1000m radius. The endeavor also involved the establishment of a SQLite database located in the data folder. This database hosted the resulting dataframes, each represented as a data table within the database structure.


## Process
Initiated connections to both APIs, utilizing a permanent environment variable as the API key when necessary. Extracted data in JSON format and systematically parsed through each dataset. Constructed dictionary-like structures for each dataset, encapsulating pertinent business details. These dictionaries were subsequently transformed into dataframes and persisted as CSV files.

Merged the three resultant dataframes, amalgamating the relevant information intended for use in the statistical model. Undertook Exploratory Data Analysis (EDA) on the merged dataframe, encompassing data cleansing and visualization to gain initial insights.

Established a SQLite database featuring data tables corresponding to each dataframe. The dataframe contents were inserted into their respective database tables. Both pre- and post-join datasets were meticulously examined and verified for accuracy.

Developed a multivariate regression model using the consolidated data. Employed backward stepwise selection on the independent variables to iteratively refine the model. Attained a final model outcome after this iterative process.

## Results
The utilization of the Yelp API enriched our dataset considerably by furnishing more comprehensive business details, particularly crucial attributes such as ratings, review counts, and pricing information. Furthermore, the Yelp API yielded a substantially larger number of businesses compared to the FourSquare API. This might stem from the fact that the Yelp API dynamically adjusted the search radius based on area density, or perhaps, it is indicative of Yelp having a more extensive repository of business data.

An additional distinction lies in the precision of distance data. While the Yelp API returned exact distances, the FourSquare API provided distances rounded to whole units. In terms of the outcomes from the multivariate regression model, even after excluding high P-values and attaining P-values of 0.000 for latitude and longitude, the adjusted R-squared value remains at a low 0.174. This value experiences a minor decline with each elimination of a high P-value factor from the model.

The coefficients associated with latitude and longitude are inconsequential within this context. They signify changes in geographical location but lack the capacity to indicate variations in magnitude. Consequently, the negative values of these coefficients don't infer a negative correlation between the variables. As a result, it can be deduced that although a notable connection exists between the total count of bikes and their location, the model inadequately fits the dataset. This could arise from either the inherent lack of a strong linear relationship between the dataset values, or the insufficiency of data to establish a robust linear relationship. The latter explanation seems more plausible, particularly considering that Portland, being a relatively smaller city, offers a limited number of bike stations and businesses, leading to a scarcity of available data points.

## Challenges 
Data Cleaning and Preprocessing
API key getting disabled and having to wait 
Data Integration and Joining

## Future Goals
Propose potential improvements for the models, data collection process, or analysis methodology.
Consider how the project findings can be used for real-world applications or further research.


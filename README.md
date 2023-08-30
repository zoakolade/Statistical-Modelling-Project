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
The Yelp API afforded us substantially more comprehensive data by furnishing additional business details, particularly critical ones like ratings, review counts, and pricing. Furthermore, the Yelp API presented a notably larger number of businesses when compared to the FourSquare API. This variance might be attributed to the Yelp API's automated adjustment of the search radius based on area density or the possibility that Yelp has access to a more extensive business dataset. Additionally, the Yelp API offered precise distance measurements, whereas the FourSquare API provided distances rounded to the nearest value.

## Challenges 
Data Cleaning and Preprocessing
API key getting disabled and having to wait 
Data Integration and Joining

## Future Goals
Propose potential improvements for the models, data collection process, or analysis methodology.
Consider how the project findings can be used for real-world applications or further research.


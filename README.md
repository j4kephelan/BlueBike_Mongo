# Blue Bikes Mongo DB
This report is an investigation of the usage of Bluebikes in the greater Boston metro from January 2019 to March 2024. The database includes data from 15 million rides, between 558 stations and in 13 separate municipalities. <br/>
This report is also a demonstration of the ability of the document style database Mongo DB to handle large amounts of data. <br/>
## Project Outline
the data for this project was sourced from Blue Bikes website where both the [trips and stations](https://bluebikes.com/system-data) data is published regularly. This data is in CSV form which needed to be converted to JSON to be insterted into Mongo DB. This is where other cleaning was done as well, for the stations [stations_dict.ipynb](https://github.com/j4kephelan/BlueBike_Mongo/blob/main/stations_dict.ipynb) and for the trips in [trips_cleaning.ipynb](https://github.com/j4kephelan/BlueBike_Mongo/blob/main/trips_cleaning.ipynb). <br/>

After loading the two JSON files into our mongo db database we used a python script connected to our database to ask several queries of our data in the [queries.ipynb](https://github.com/j4kephelan/BlueBike_Mongo/blob/main/queries.ipynb) file. <br/>

You can see the visual results of our queries as well as our analysis of bike rider behavior in [the pdf report](https://github.com/j4kephelan/BlueBike_Mongo/blob/main/DS%204300%20Final%20Project%20Report.pdf) or in the [presentation deck](https://github.com/j4kephelan/BlueBike_Mongo/blob/main/HW6%20Presentation%20Slides.pdf). <br/>

## Recreation instructions
If you wanted to recreate this project for your own analysis you will need
1. Install your own Mongo DB server which you can do with their free [community edition](https://www.mongodb.com/try/download/community)
2. Install [Python](https://www.python.org/downloads/) and dependent packages, we use pymongo (connect to mongo db), matplitlob (data visualizations), pandas (data manipulation), and altair matplitlob (data visualizations) for this project.
3. Download the datafrom Blue bokes. you can find the trips [here](https://s3.amazonaws.com/hubway-data/index.html) and the stations [here](https://bluebikes.com/system-data). Note there is a lot of data here. Our analysis which spanned from Jan 2019-April 2024 took up 5GB of storage once put into JSON form. Consider subset ting the data for your analysis.  

If setting up your own verson of this project you will want to gitignore all the data scource files as we have done here as otherwise the project will be too large to host on github.

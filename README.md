# Movies-ETL

#### *ETL pipeline on movie data using Python and postgreSQL*

## Overview
This project consisted on a automated Extraction, Transformation and Load pipeline. This ETL extracted movie data from wikipedia, kaggle, and MovieLens to clean it, transform it, and merge it using Pandas. The product was a merged table with movies and ratings loaded to PostgreSQL. 

## Resources
- Data sources:
  - movies_metadata.csv
  - ratings.csv
  - wikipedia_movies.json

- Software:
  - Python
  - PostgreSQL
  - Pandas
  - SQLAlchemy

## Results
- Final output table: 
[FINAL_Merged_Movies_and_Ratings.csv](https://github.com/nicoserrano/Movies-ETL/files/6779557/FINAL_Merged_Movies_and_Ratings.csv)

- Datasets uploaded to PostgreSQL for other users to analyze movie data (Hacketon): 
![movies_query](https://user-images.githubusercontent.com/83378141/124815489-5529de00-df35-11eb-8a4a-517ed0a51060.png)
![ratings_query](https://user-images.githubusercontent.com/83378141/124815490-55c27480-df35-11eb-8ec6-20c28ca7a649.png)


## Summary
The pipeline was created under the following assumptions:
- I was able to join the wikipedia, kaggle, and ratings movie data on the IMDB ID column.
- The wikipedia dataset didn't have a IMDB ID, so I had to extract it from the url link given. 
- Each dataset had to be cleaned on their own because they had overlapping columns, suck as 'Director' and 'Directed By', unecessary columns, many null values, TV shows, outliers, duplicates, incorrect data types, formatting, and other errors. 
- The wikipedia movie data was in a json format. 
- The ratings dataset had more than 26 million entries which generated a time constraint and a processing data challenge.
- Not every every movie had a rating for each rating level. 

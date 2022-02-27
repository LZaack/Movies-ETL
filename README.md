# Movies ETL
## Overview

Britta asked me to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. I refactored the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the Movie Lens rating data—and performed the ETL process by adding the data to a PostgreSQL database.

## Results

`(i)` Deliverable 1: Write an ETL Function to Read Three Data Files;

I wrote a function that reads in the three data files and created three separate Data Frames.

`(ii)` Deliverable 2: Extract and Transform the Wikipedia Data;

I extracted and transformed the Wikipedia data so I could merge it with the Kaggle metadata. While extracting the IMDb IDs I used a regular expression string and dropping duplicates, used a try-except block to catch errors.

`(iii)` Deliverable 3: Extract and Transform the Kaggle data;

I extracted and transformed the Kaggle metadata and Movie Lens rating data, then I converted the transformed data into separate Data Frames. Then, I merged the Kaggle metadata Data Frame with the Wikipedia movies Data Frame to create the movie’s Data Frame. Finally, I merged the Movie Lens rating Data Frame with the movie’s Data Frame to create the `movies_with_ratings_df`

`(iv)` Deliverable 4: Create the Movie Database.
Finally, I added the movie’s Data Frame and Movie Lens rating CSV data to a SQL database. I confirmed that the movies table has 6,053 rows and the rating table has 26,024,289 rows, as it is shown with the following screenshots.

![movies_query.png](/Resources/movies_query.png)

![ratings_query.png](/Resources/ratings_query.png)



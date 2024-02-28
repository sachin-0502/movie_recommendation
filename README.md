# Movie Recommendation System


### Project Overview
This project aims to recommend the top 10 similar movies based on the movie which is input by the user. The projects works in such a way that the content of input movie and content of the recommended movies will be the best possible similar match.
Although the recommendation system is also possible in the form of collaborative filtering based method which recommend movie based on the user interest but, here I used the content based approach.

### Data Sources
TMDB Movies dataset from Kaggle which consists two csv files containing data of 5000 movies.
- tmdb_5000_credits = | movie_id | title | cast | crew |
- tmdb_5000_movies  = | budget | genre | homepage | id | keywords | original_language | orginal_title | overview | popularity | production_companies | tagline | title | vote | budget | runtime | status | spoken_language |
- 
### Data Preprocessing
1. Merge both datasets by considering 'title' as the foreign key
- movies.merge(credits,on='title')
2. Feature Selection to use only required columns
- genres, movie_id, keywords, title, overview, cast, crew
3. Changed the data type of every column as per the requirement
4. Created useful tags using:
- tags = genres + keywords + top 3 cast + only director from crew + overview
5. Remove same word ambiguity ( remove blank spaces )
6. convert generated tags into lower case.

### Processed Data

 

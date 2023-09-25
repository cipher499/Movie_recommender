# Movie recommender system: Overview
A Streamlit-based web application for a movie recommender system to help users discover personalized movie recommendations with ease. This project involved various steps, including data preprocessing, feature engineering, modeling, and the development of a user-friendly interface. <br>

## Code and Resources used
**Python Version:** 3.10.12 <br>
**Packages:** pandas, numpy, ast, sklearn, nltk, pickle, streamlit <br>
**For Web Framework Requirements:** pip install -r requirements.txt <br>
**Dataset:** https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?select=tmdb_5000_credits.csv

## Data wrangling & Feature engineering:
* Merged two datasets based on the 'title' column to create a comprehensive movie dataset.
* Removed null values to ensure data quality.
* Engineered functions to extract relevant tags such as title, director, and cast from various columns.
* Cleaned and consolidated the tags into a single 'tags' column for efficient processing.

## Modeling
* Utilized sklearn's CountVectorizer to vectorize the 'tags' column, preparing the data for similarity calculations.
* Implemented text preprocessing by applying nltk's PorterStemmer to enhance feature extraction.
* Created a similarity matrix for the movies using sklearn's cosine_similarity, enabling accurate movie recommendations.
* Developed a function that takes a movie title as input and returns the top 5 movies with the highest similarity scores.

## Streamlit Web Application
* Serialized the cleaned dataset and the similarity matrix into pickle files for easy access.
* Integrated with the TMDB API to fetch movie posters for the 5 most similar movies.
* Designed an intuitive user interface through Streamlit, allowing users to search for movie recommendations easily.


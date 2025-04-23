# Netflix-Data-Exploration-and-Visualisation

## Problem Statement:
Netflix hosts a vast and diverse content library with a global subscriber base exceeding 222 million. However, viewer preferences vary significantly across regions.To sustain growth and improve user engagement, Netflix needs to identify which types of content (by genre, duration, ratings, and release timing) perform best in different countries. The goal is to generate actionable insights that can guide content production, regional marketing strategies, and platform personalization to better cater to local audiences and expand Netflix's global footprint.
This project analyzes Netflix's global content library to uncover viewer preferences by genre, country, duration, director, cast, rating and time. Insights will guide Netflix on what types of shows or movies to produce and how to grow its subscriber base across different regions.

## EDA Insights:
* The Dataset has 8807 rows and 12 columns
* Dataset had 4307 null values mainly in Director, cast, country,rating and duration column 
* Rating column had 3 entries which belongs to duration column, it was later replaced 
* Cast, Directors, listed_in and country columns had multiple values in each cell hence we created separate dataframe by unnesting these columns(that is creating separate line for each cast or director in a movie) with title column with .str.split() and explode() function.
* Merge all 4 Dataframes into a Single DataFrame.
* Merged the unnested dataframe with the original dataframe to get the final dataframe to work on analysis.
* Replaced Null values in director column with 'Unknown director'
* Replaced Null values in Cast column with 'Unknown Actor'
* Replaced Null values in Rating column with 'NR'-Not rated.
* Replaced Null values in date_added with column with the mode of release year
* Replaced Null values in country column with Mode of Directors, Mode of cast and remaining null values were replaced with 'Unknown Country'
* converted movie durations in to categorical data for better analysis

## Analysis Insights:

* The most popular Genres across the countries and in both TV Shows and Movies are Drama, Comedy and International TV Shows/Movies.
* TV Shows are added in July/August and Movies in last week of the year/first month of the next year.
* For USA audience 80-120 mins is the recommended length for movies and Kids TV Shows are also popular along with the genres in first point.
* The target audience in USA and India is recommended to be 14+ and above ratings while for Japan and south korea its 14yrs+ and mature content.
* Movies for Indian Audience has been declining since 2018.
* Anime Genre for Japan and Romantic Genre for South Korean and International Tvshows for both are popular.
* While creating content, take into consideration the popular actors/directors
for that country. Also take into account the director-actor combination which 
is highly recommended. 

## Recommendation for Netflix:
* Focus production and licensing on high-performing genres like Drama, Comedy, and International TV Shows across markets.
* Invest in original anime or co-productions with Japanese studios.
* Invest in Korean Romantic Drama.
* Since Indian movies are declining since 2018, it would be best to focus on original webseries rather than movies.
* Target Movie release on year end holidays - December and January
* Run local Marketing on school breaks and during festivals.
* for USA : Highlight family content, movies under 2 hours, and trending kids TV shows
* for Japan and South Korea: Push mature-rated content and international titles in user homepages.
* for India: Emphasize titles rated 14+ and above and deprioritize low-performing movie genres.
* Promote content based on popular genres such as Anime for Japan and Romantic content for South Korea
* Work with Japanes, korean and Indian Production firms to produce high qualtiy content in target genres.
* While creating content take the popular director/Actors into consideration and popular actor and director combinations .

Team Anime
12/6/18
Team member: Meng, Jessie, Saurabh

1. Extract
We worked with data offered in Kaggle challenge which asks analysts to build a better anime 
recommendation system based only on user viewing history. There are two dataset we worked with. 
One is anime.csv which includes information of anime name, anime ID on MyAnimeList.net, rating, 
genre, number of episodes. Another file we worked with is rating.csv which includes some users'
anime list (anime ID on MyAnimeList.net, anime name) and their ratings per anime. 


2. Transform
Data cleaning specs:
1) anime.csv

Here's the data type information of all the variables in anime.csv

anime_id      int64
name         object
genre        object
type         object
episodes     object
rating      float64
members       int64

We turned genre into category variable and episodes into integer variable during cleaning for further analysis. 

We also dropped rows of data that has null values. 


2) rating.csv

Through running descriptives, we learned that some rating values are negative so we dropped it. 

3. Load
We loaded both of the csv file back to mysql, and we joined the two data file on the column anime_id
because the anime_id is the official ID in MyAnimeList.net that is shared across both table. 
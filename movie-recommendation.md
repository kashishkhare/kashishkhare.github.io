[<- Return To Home...](./)

# Movie Recommendation

* * *
### [](#header-3)Code Files

[https://github.com/kashishkhare/Movie-Recommendation](https://github.com/kashishkhare/Movie-Recommendation)
* * *

### [](#header-3)Introduction

A way to get recommendations for products, movies or restaurantsis toask our friends. A person relies on his/her social circle to find out what is available according to his choice or what might interest him/her based on similar interest within the group. But, in this era of huge databases, one person cannot consider all the options of what is available for or might interest him/her. To aid a person in broadening his/her interest recommendation systems are developed.

There are various examples of recommendation systems that are used by e-commerce websites, movie recommendation websites, news websites and many more. For example, In Netflix a user gets recommendation based on movies he/she has watchedin the past. In Amazon website, a user gets recommendation of products based on his/her buying as well as browsing history. And in Amazon,a user also gets recommendation based on what other peoplewith similar interest have liked/bought. In this project, I studied various types of recommendation systems used to predict the interest of different people based on their as well as others interest. I will make some recommendation systems, test them on a data set of movies and compare the results obtained by each one of them.

### [](#header-3)Recommendation Systems

>>“Recommender systems are software tools and techniques providing suggestions for items to be of use to a user. The suggestions relate to various decision-making processes, such as what items to buy, what music to listen to, or what online news to read” © [Ricci et al. Recommender Systems Handbook 2011].

A recommender system helps make a choice without personal knowledge of a particular domain:
* Generate a suggestion about a product to buy or consume
* To provide customers with information to help make a decision on purchasing or consuming of an item

The goal of recommender systems is to generate a suggestion about a product or to predict the utility of a particular itemfor a user.

### [](#header-3)Types of Recommendation Systems

Commonly used in the recommendation systems are categorized as follows:
* Content-based recommendationsystems
* Collaborative filtering recommendationsystems

### [](#header-5)Content Based Recommendation Systems

Content-based (CB) filtering systems are systems recommending items similar to items a user liked in the past. They consider only properties of the items. These systems assemble users preferences into user’s profiles and all items information into items’ profiles. Then they recommend those items close to the user by similarity of their profiles.

For example, in movie recommendation system, if a user has seen mostly “Comedy” movies then Content-based system will recommend him movies that are in “Comedy” genre only. It will not recommend movie that are in any other genre.

### [](#header-5)Collaborative Filtering Recommendation Systems

In Collaborative Filtering recommendations were given by others who have similar taste in the past, but who already experienced an item yet unknown to the current user. Collaborative filtering systems require users to express opinions on items. They collect opinions and recommend items based on people’s opinions similarity. 

A key advantage of the collaborative filtering approach is that it does not rely on machine analyzable content and therefore it is capable of accurately recommending complex items such as movies without requiring an "understanding" of the item itself. Collaborative filtering is based on the assumption that people who agreed in the past will agree in the future, and that they will like similar kinds of items as they liked in the past.

For example, in movie recommendation system, if an user has given rating to a movie then collaborative filtering based algorithm will find users who have givenrating to same movie and then calculate a similarity score, and according to that similarity score it will recommend the movies which are not yet viewed by 1st user but 2nd user has rated them.

### [](#header-3)Implementation

I have implemented recommendation system with both approaches and compared the result of each approach. To compare the results, I have tested recommendation algorithms on a collection of movies rated by different users.

### [](#header-5)DataSource

I have collected data to test the recommendation algorithms. Dataset collected from grouplens.org. grouplens.org has a collection 1,000,209 anonymous ratings of approximately 3,900 movies made by 6,040 MovieLens users.

Movies are stored in a file in the following format MovieID::Title::Genres. Genres are pipe-separated.

Ratings are made on a 5-star scale. All ratings are contained in a separate file in the following format: UserID::MovieID::Rating::Timestamp

### [](#header-5)Data Storage

For Content-Based Recommendation System, I have created 3 dictionaries:
* movie_name – It contains movie-id and title of the movie
* movie_genre – It contains movie-id and list of genres of that movie
* movie_ratings – It contains movie-id and average rating of that movie given by all users

For Collaborative-Filtering Recommendation System, I have created 2 nested dictionaries:
* user – It contains all the movies and their ratings, rated by the user
* movies – It containsall the users and rating given by them for a particular movie

### [](#header-5)Content-Based Recommendation System

This function, takes a movie, list of genre and rating of movie and based on genres and range of rating it recommends top 10 movies. In this function, I make a list of all movies within a range of ±1 rating with the rating given by userand another list of moviesin allgenres listed by user. Then I take common movies between the two list and sort them based on their highest ratingand the highest number of genre match from thelist of genre provided by user.And display top ten movies recommended to user.When I givea movie as input to this function, I getrecommendation similar to the movies that I have entered.4.4Similarity ScoreForcollaborative filtering, we need to find a similarity score between two items. Similarity score can be found in many ways. In this project I have used Euclidean Distance Score, a very simple approach to calculate similarity score.In Euclidean Distance Score, we take items that people have ranked in common hand uses them as axes for a chart and then plotthe people onchart. Two people who are closer in chart will have more similar interest.To calculate the distancebetween twopeople, take the difference in each axis, squarethem and add themtogether, then take the squareroot of thesum.This formula will give the 



[<- Return To Home...](./)
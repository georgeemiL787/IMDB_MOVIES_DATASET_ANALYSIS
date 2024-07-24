# IMDB movies analysis
### project overview
this data project aims to provide insights into the movies industry over the past years. regarding movie ratings, genres, release years, and other relevant attributes.
### Table of Contents  
[Project Objectives](#headers)  
[Dataset Description](#emphasis) <br />
[Tools](#emphasis)   
[Project Steps](#emphasis)   
[Data cleaning](#emphasis)   
[Derived column](#emphasis)  
[Data visualization](#emphasis)  
[Bussiness analysis](#emphasis)   
[resorces](#emphasis)
<a name="headers"/>
<a name="emphasis"/>
<a name="emphasis"/>
<a name="emphasis"/>
<a name="emphasis"/>
<a name="emphasis"/>
<a name="emphasis"/>
## Project Objectives
#### Analyze the IMDB movies dataset to uncover patterns and trends
#### Derive insights regarding movie ratings, genres, release years, and other relevant attributes.
#### Visualize key findings for better understanding and communication.
## Dataset Description
#### source : IMDB
#### Content: Information about movies, including:
#### director_name
#### num_critic_for_reviews
#### gross
#### genres
#### actor_1_name
#### movie_title
#### num_voted_users
#### plot_keywords
#### num_user_for_reviews
#### language
#### country
#### budget
#### title_year
#### imdb_score
## Tools
I used only excel in my project
## project steps
1. read the data: after obtain the data I needed to undrstand the data and get it ready for the next step 
2. cleaning: see if the data contains blanks , duplicates , numerical outliers , string cleaning  
3. Exploratory Data Analysis (EDA): Frequency counts for categorical.  columns Distribution of ratings, release years, and durations. Correlation analysis to find relationships between variables.
4. Data Visualization: start represent some of these correlations in visual way so it be easier to understand and to summarize data and explore multidimensional data
5. Conclusion and Recommendations
## Data cleaning
I started off removing records which have blanks (missing value column) so i found blanks in 2 columns (plot_keywords,langue).<br />
Didn't find duplicates records so I moved on to numerical outliers and found a global outliers in budget column due to the currency differance so i kept it.<br />
In string cleaning column  movie title has a wrong character at the end Â  (using find & select) , (©) removed this letter from the dataset .<br />
## Derived column
It's a column I need to make or calculate to use it again for analysis in further steps.
starting i made a coulmn contains the name of the director and actor_1_name and called it  director/actor using (=col1,"|",col2) and mark the duplicates using condition formatting 

![image](https://github.com/user-attachments/assets/b05b38bb-c5b0-4634-8764-57a75e590af1)

after that I derived another column and named it main genre as every movie has it's main genre and i assumed it's the first genre in genres column.
the function used was ( =LEFT(D2, FIND("|", D2 & "|") - 1) ) where left : make supstring from thee main string in D column and find -1 = get the index i want to stop at without ("|") 

  ![image](https://github.com/user-attachments/assets/a361c5dd-fe69-4a52-ad29-df4ae97cbb4b)
   ![image](https://github.com/user-attachments/assets/cc1f0639-a6e7-4ff3-908e-058b592c4dbd)
 
and the last 2 columns was related first is profit and second is earining persentage 
profit was claculated by subtracting budget from gross <br />
And earining persentage was calculated by (profit/budget)*100 if the output is negative in both columns this mean that the movie lost money 

![image](https://github.com/user-attachments/assets/0da5fc61-46c4-4b33-b253-0db7535de2bc)

## Data visualization
Using pivot tables as it's a data visualization tool so you need to add the columns having a relation to make analysis <br />
### First pivot table 
named best duo in this imdb movies list helps me to get the highest average rating duo <br />
Starting with adding (director / actor) column , Count of movie_title to get the number of movies the duo did together and sum for imdb score 
to calculate average rating for every duo in the list <br />
by using this formula (Sum of imdb_score/(Count of movie_title*10)) and change the result to precentage formula 

![image](https://github.com/user-attachments/assets/53f746f7-d59c-4a72-9cf0-741e0c662fe8)

After that I extracted the most working together duos to make a barchar for the best duo

![image](https://github.com/user-attachments/assets/61138e02-ffd1-4b55-a674-66750a01947c)

And found that statically <br />
[Martin Scorsese|Robert De Niro](#emphasis) were the highest average rating duo <a name="emphasis"/>

![image](https://github.com/user-attachments/assets/f65da188-5077-4b37-af09-8102ee0a5229)

And found out that from the top 20 rated movies there are 9 duo worked together

![image](https://github.com/user-attachments/assets/5e14edd9-3aaf-4f76-9c83-c7f90139d468)


### Second pivot table
named best directors to get the highest average rating directors in this imdb list
starting with adding (director name) column and (sum of imdb scores) to get every director total score and last column (count movie title) so I get the number of movies each director have in the list <br />
from this we can calculate average rating of every director by divid sum of imdb scores with count movie title multiply 10 (sum of imdb scores/(count movie title*10)) and change the result to precentage formula  <br />
After that extract the data to external table so it can be visualized 

![image](https://github.com/user-attachments/assets/da5ffa4c-144b-4bec-b910-1e7e43d84590)

And found that statically <br />
[Christopher Nolan](#emphasis) have the highest average rating director <a name="emphasis"/>

![image](https://github.com/user-attachments/assets/f04b0c31-3f0f-47d5-9704-30e281530cd1)

### Third pivot table
named best genre to get highest average rating genre to make a movie <br />
Adding the derived coulmn (main genre) with 2 value fields columns (Sum of imdb_score,Count of imdb_score2)
from this pivot table we calculated average rating each genre have (Sum of imdb_score/(Count of imdb_score2*10)) and there distribution on the movie list <br />

![image](https://github.com/user-attachments/assets/c665bf69-8fa1-43c5-b7af-e26d70e7d381)

From this 2d pie chart we get to know that the most used genres are (action,comedy,drama) 

![image](https://github.com/user-attachments/assets/4b02934b-5107-4a4b-b5cb-33b949e96c1c)

and From this bar chart we get to know that the highest average rating are (biography , crime , drama)  <br />
therefore after analyze the 2 graphs get to conclusion that [Drama](#emphasis) has the highest average rating genre <a name="emphasis"/>

### Forth pivot table 
named best actor to get the highest average rating actor in this imdb list
starting with adding (actor name) column and (sum of imdb scores) to get every actor total imdb score and last column (count movie title) so I get the number of movies each actor have in the list <br />
from this we can calculate average rating of every actor by divid sum of imdb scores with count movie title multiply 10 (sum of imdb scores/(count movie title*10)) and change the result to precentage formula  <br />
After that extract the data to external table so it can be visualized 

![image](https://github.com/user-attachments/assets/678bd364-b45e-4f05-ac6b-d62127692d73) ![image](https://github.com/user-attachments/assets/a9f5555c-614b-442d-803f-f84bd50dbf06)
And found that statically <br />
[Tom Hanks](#emphasis) have the highest average rating actor <a name="emphasis"/>

### Fifth pivot table
named best country we get the highest rating country and also get the highest earning percentage in every country getting the average rating was like the other categories  <br />
to get the earning percentage we used the derived column we calculated (earning percentage) so we added the country name and sum of earning pecentage of every movie depend on the country name 
and then get every counry number of movies in the list and calculated the earning percentage (Sum of earining persentage of the movies/ Count of movie_title*100 ) and change the result to precentage formula <br />
I got top 5 countries having number of movies in this list to know the best country to make a movie depend on rating and earning percentage 

 ![image](https://github.com/user-attachments/assets/104240c6-7bc5-4e9d-a269-1806e63a10ae) ![image](https://github.com/user-attachments/assets/fb79795a-a855-4aab-b4fe-75642b133061)

From this we get to know that rating doesn't depend on country but the earning percenage depends so that [USA](#emphasis) have the highest earning percentage in movie industry  <a name="emphasis"/>

### sixth and the last pivot table 
named movies over the years contains 2 columns the years and count title movies to count the number of movies in every year 

![image](https://github.com/user-attachments/assets/b780b841-60b4-40b1-b013-caec1e8f5481)

from this visualization we get to know that the starting of the past century movie industry wasn't that big and it start to grow making a trend it's peak was at the first decad of this century <br /> 
at the end of the graph we see the number of movies start to decrease which we will discuss at the bussiness analysis.
## Bussiness analysis
### Executive Summary
The IMDB movies analysis project aims to uncover patterns and trends in the movie industry using historical data from IMDB. The analysis focuses on various attributes such as movie ratings, genres, release years, and financial performance. This comprehensive analysis will help stakeholders understand the dynamics of the movie industry and make informed decisions.
### key findings 
#### 1. Best Director-Actor Duo:
Martin Scorsese and Robert De Niro are the highest average rating duo, indicating a successful and well-received collaboration. <br />
Out of the top 20 rated movies, 9 are the result of director-actor duos working together. <br />
#### 2. Top Directors: 
Christopher Nolan has the highest average rating among directors, signifying his consistent ability to produce high-quality movies.<br />
#### 3. Popular and High-Rating Genres:
The most used genres in movies are Action, Comedy, and Drama.<br />
However, the highest average rating genres are Biography, Crime, and Drama.<br />
Drama emerges as the genre with both high usage and high ratings, making it a safe and potentially profitable choice for new productions.<br />
#### 4. Top Actors:
Tom Hanks has the highest average rating among actors, reflecting his popularity and consistent performance.<br />
#### 5. Country Analysis:
The analysis reveals that while the average movie rating does not significantly depend on the country, the earning percentage does.<br />
USA stands out with the highest earning percentage, making it a lucrative location for movie production.<br />
#### 6. Trends Over the Years:
The movie industry saw gradual growth throughout the 20th century, peaking in the first decade of the 21st century.
There has been a noticeable decline in the number of movies produced in recent years, which requires further investigation to understand the underlying reasons.
which I think is because of the increase in production in reality tv shows and the platform numbers increase which led to decrease the number of movies and cinema production.
### Resorces 
1. https://atlan.com/data-quality-issues/#in-conclusion
2. https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/
3. https://medium.com/analytics-vidhya/different-types-of-outliers-dd6363983744
4. https://www.ablebits.com/office-addins-blog/excel-left-function/
5. https://www.youtube.com/watch?v=-MiAmeuzrSQ
6. https://www.youtube.com/watch?v=OrsuYT_OMtQ

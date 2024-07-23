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
Using A pivot table as it's a data visualization tool so you need to add the columns having a relation to make analysis <br />
First pivot table called best duo in this imdb movies list <br />
Starting with adding (director / actor) column , Count of movie_title to get the number of movies the duo did together and sum for imdb score 
to calculate average rating for every duo in the list <br />
by using this formula (Sum of imdb_score/(Count of movie_title*10)) and change the result to precentage formula 

![image](https://github.com/user-attachments/assets/53f746f7-d59c-4a72-9cf0-741e0c662fe8)

After that I extracted the most working together duos to make a barchar for the best duo

![image](https://github.com/user-attachments/assets/61138e02-ffd1-4b55-a674-66750a01947c)

And found that statically <br />
[Martin Scorsese|Robert De Niro](#emphasis) were the best duo <a name="emphasis"/>

![image](https://github.com/user-attachments/assets/f65da188-5077-4b37-af09-8102ee0a5229)

And found out that from the top 20 rated movies there are 9 duo worked together

![image](https://github.com/user-attachments/assets/5e14edd9-3aaf-4f76-9c83-c7f90139d468)


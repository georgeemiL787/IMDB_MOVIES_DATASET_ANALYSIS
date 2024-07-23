# IMDB movies analsis
### prject overview
this data project aims to provide insights into the movies industry over the past years. regarding movie ratings, genres, release years, and other relevant attributes.
### Table of Contents  
[Project Objectives](#headers)  
[Dataset Description](#emphasis) <br />
[Tools](#emphasis)   
[Project Steps](#emphasis)   
[Data cleaning](#emphasis)   
[Derived column](#emphasis)  
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
4. Data Visualization: start represent some of these correlations in visual way so it be easier to understand
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

and the last 2 columns was related first is profit and second is earining persentage 
profit was claculated by subtracting budget from gross <br />
And earining persentage was calculated by (profit/budget)*100 if the output is negative in both columns this mean that the movie lost money 





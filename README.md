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
I started off removing records which have blanks (missing value column) so i found blanks in 2 columns (plot_keywords,langue).
Didn't find duplicates records so I moved on to numerical outliers and found a global outliers in budget column due to the currency differance so i kept it.
In string cleaning column  movie title has a wrong character at the end Â  (using find & select) , (©) removed this letter from the dataset .
## Derived column
It's a column I need to make or calculate to use it again for analysis in further steps.
starting i made a coulmn contains the name of the director and actor_1_name and called it  director/actor using (=col1,"|",col2) and mark the duplicates using condition formatting 



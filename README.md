# Welcome to My Allocine
Description
This project will tackle one of the main tool to work with Data. You've probably heard of this tool: SQL.
SQL (Structured Query Language) is a standardized programming language that's used to manage relational databases and perform various operations on the data in them. Initially created in the 1970s, SQL is regularly used not only by database administrators, but also by developers writing data integration scripts and data analysts looking to set up and run analytical queries.
The uses of SQL include modifying database table and index structures; adding, updating and deleting rows of data; and retrieving subsets of information from within a database for transaction processing and analytics applications. Queries and other SQL operations take the form of commands written as statements -- commonly used SQL statements include select, add, insert, update, delete, create, alter and truncate.
SQL became the de facto standard programming language for relational databases after they emerged in the late 1970s and early 1980s. Also known as SQL databases, relational systems comprise a set of tables containing data in rows and columns. Each column in a table corresponds to a category of data -- for example, customer name or address -- while each row contains a data value for the intersecting column.
The sample database represents some of the data storage and retrieval about a movie related industry. Most of the people loves to watch movie, and for all of them we are providing a sample information about the movie related questions coming to their mind. This design of database will make it easier to the movie lovers to know the curiosities about the movies.
In this project, you will have to work with a database containing multiple tables. Here a description of all the tables:
Description of tables:
actors:
id – this is a unique ID for each actor
act_fname – this is the first name of each actor
act_lname – this is the last name of each actor
act_gender – this is the gender of each actor
genres:
id – this is a unique ID for each genres
gen_title – this is the description of the genres
directors:
id – this is a unique ID for each director
dir_fname – this is the first name of the director
dir_lname – this is the last name of the director
movies:
id – this is the unique ID for each movie
mov_title – this column represents the name of the movie
mov_year – this is the year of making the movie
mov_time – duration of the movie i.e. how long it was running
mov_lang – the language in which movie was casted
mov_dt_rel – this is the release date of the movie
mov_rel_country – this is the name of the country(s) where the movie was released
movies_genres:
mov_id – this is the ID of the movie, which is referencing the mov_id column of the table movies
gen_id – this is the ID of each genres, which is referencing the gen_id column of the table genres
directors_movies:
dir_id – this is the ID for each director, which is referencing the dir_id column of the table directors
mov_id – this is the ID of the movie, which is referencing the mov_id column of the table movies
reviews:
id – this is the unique ID for each reviewer
rev_name – this is the name of the reviewer
movies_ratings_reviews:
mov_id –this is the ID of the movie, which is referencing the mov_id column of the table movies
rev_id – this is the ID of the reviewer, which is referencing the rev_id column of the table reviews
rev_stars – this is indicates how many stars a reviewer rated for a review of a movie
num_o_rating – this indicates how many ratings a movie achieved
movies_actors:
act_id – this is ID of actor, which is referencing the act_id column of actors table
mov_id – this is the ID of the movie, which is referencing the mov_id column of the table movies
role – this is the name of a character in the movie, an actor acted for that character
Objectives
Write SQL requests. Simple, and some more complicated ;-)
Submit your work
For automatic tests purposes, you will write your SQL requests inside a file named: my_allocine.rb.
It will be formatted like this:
requests[REQUEST_DESCRIPTION_1] = "SQL_REQUEST_1"
requests[REQUEST_DESCRIPTION_2] = "SQL_REQUEST_2"
We are providing the file with all the description, your mission will be to write all the corresponding sql request.
Here is the file:
requests['Display all actors'] = "SELECT * FROM actors;"
requests['Display all genres'] = ""
requests['Display the name and year of the movies'] = ""
requests['Display reviewer name from the reviews table'] = ""
requests["Find the year when the movie American Beauty released"] = ""
requests["Find the movie which was released in the year 1999"] = ""
requests["Find the movie which was released before 1998"] = ""
requests["Find the name of all reviewers who have rated 7 or more stars to their rating order by reviews rev_name (it might have duplicated names :-))"] = ""
requests["Find the titles of the movies with ID 905, 907, 917"] = ""
requests["Find the list of those movies with year and ID which include the words Boogie Nights"] = ""
requests["Find the ID number for the actor whose first name is 'Woody' and the last name is 'Allen'"] = ""
requests["Find the actors with all information who played a role in the movies 'Annie Hall'"] = ""
requests["Find the first and last names of all the actors who were cast in the movies 'Annie Hall', and the roles they played in that production"] = ""
requests["Find the name of movie and director who directed a movies that casted a role as Sean Maguire"] = ""
requests["Find all the actors who have not acted in any movie between 1990 and 2000 (select only actor first name, last name, movie title and release year)"] = ""
Tools
It's the time to improve your skills with Sqlite.
1# Download the database:
wget https://storage.googleapis.com/qwasar-public/track-claris/movies.db
2# Connect to the database with Sqlite:
$>sqlite3 movies.db
SQLite version 3.32.3 2020-06-18 14:16:19
Enter ".help" for usage hints.
sqlite>
3# Type in the command line to perform sql queries:
sqlite> SELECT * FROM genres;
1001|Action
1002|Adventure
1003|Animation
1004|Biography
1005|Comedy
1006|Crime
1007|Drama
1008|Horror
1009|Music
1010|Mystery
1011|Romance
1012|Thriller
1013|War
sqlite>
4# exit with: Ctrl + D
TIPS
Research keywords SELECT, *, FROM, JOIN, WHERE, ...
SQL requests have a semi colon at the end.
The problem in this code is that it is incomplete and contains syntax errors. It seems that some of the SQL queries are cut off, and the code snippet provided does not include the necessary Ruby code to execute the queries and retrieve the results from the database.
The challenge with this code is that it lacks the necessary context and implementation details to fully understand and run the queries. It would require additional code to establish a connection to the database, execute the SQL queries, and retrieve the results. Additionally, the code snippet does not include error handling or exception management, which is important for robust code.
To address these challenges and make the code functional, the following steps could be taken:
Include the necessary Ruby code to establish a connection to the database using a suitable library (e.g., pg for PostgreSQL, mysql2 for MySQL).
Ensure that the required database configuration (e.g., host, port, username, password) is properly set up.
Use the appropriate library functions to execute the SQL queries against the database.
Handle any errors that may occur during the execution of the queries and provide appropriate feedback or error messages to the user.
Retrieve and process the query results as needed, and format them for display or further processing.
By addressing these issues and providing the missing code, the functionality of the queries can be realized, and the code can be effectively executed against the database.
## Task
 What is the problem? And where is the challenge?
Write SQL requests. Simple, and some more complicated

## Description
How have you solved the problem?
I identified the requirements for the README file, which included providing an overview of the project, explaining the setup process, demonstrating the usage of SQL queries
I created a README template with appropriate headings and sections.
I filled in the template with project-specific information, such as the project name, description, and setup instructions.
I included examples of SQL queries that can be used to retrieve specific information from the movie database.
I ensured that the README file provided clear instructions and contact information for any questions or issues.
## Installation
How to install your project? npm install? make? make re?
there were no instalations for this project 


## Usage
 How does it work?
 The project includes a file named queries.js that contains a collection of SQL queries. These queries can be executed to retrieve specific information from the movie database. Below are some examples of the available queries:
Display all actors: SELECT * FROM actors;
Display all genres: SELECT * FROM genres;
Display the name and year of the movies: SELECT mov_title, mov_year FROM movies;
Display reviewer names from the reviews table: SELECT rev_name FROM reviews;
Feel free to explore the queries.js file to find more SQL queries for retrieving different types of information from the database.
```
./my_project argument1 argument2
```

### The Core Team


<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering School</a></i></span>
<span><img alt='Qwasar SV -- Software Engineering School's Logo' src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px'></span>

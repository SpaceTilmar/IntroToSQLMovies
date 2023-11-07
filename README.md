# Create a database and a Movies table.

|Title	| Runtime	| Genre	| IMDB Score|	Rating|
|:------|:--------:|:-----|:----------|:-------|
|Howard the Duck|	110|	Sci-Fi|	4.6|	PG
Lavalantula| 83|	Horror|	4.7|	TV-14
Starship Troopers|	129|	Sci-Fi|	7.2|	PG-13
Waltz With Bashir|	90|	Documentary|	8.0|	R
Spaceballs|	96|	Comedy|	7.1|	PG
Monsters Inc.|	92|	Animation|	8.1|	G

# Answer the questions below with SQL

- Add two more movies of your choosing to the table.

- Create a query to find all movies in the Sci-Fi genre.
- | Title             | Runtime | Genre  | IMDB_Score | Rating |
+-------------------+---------+--------+------------+--------+
| Howard the Duck   |     110 | Sci-Fi |        4.6 | PG     |
| Starship Troopers |     129 | Sci-Fi |        7.2 | PG-13  |
| Pacific Rim       |     120 | Sci-Fi |        8.2 | PG-13  |
| Star Wars         |     118 | Sci-Fi |        9.2 | PG     |
+-------------------+---------+--------+------------+--------+

- Create a query to find all films that scored at least a 6.5 on IMDB
- +-------------------+---------+-------------+------------+--------+
| Title             | Runtime | Genre       | IMDB_Score | Rating |
+-------------------+---------+-------------+------------+--------+
| Starship Troopers |     129 | Sci-Fi      |        7.2 | PG-13  |
| Waltz With Bashir |      90 | Documentary |        8.0 | R      |
| Spaceballs        |      96 | Comedy      |        7.1 | PG     |
| Monsters Inc.     |      92 | Animation   |        8.1 | G      |
| Pacific Rim       |     120 | Sci-Fi      |        8.2 | PG-13  |
| Star Wars         |     118 | Sci-Fi      |        9.2 | PG     |
+-------------------+---------+-------------+------------+--------+

- For parents who have young kids, but who don't want to sit through long children's movies, create a query to find all of the movies rated G or PG that are less than 100 minutes long.
| Title         | Runtime | Genre     | IMDB_Score | Rating |
+---------------+---------+-----------+------------+--------+
| Spaceballs    |      96 | Comedy    |        7.1 | PG     |
| Monsters Inc. |      92 | Animation |        8.1 | G      |
+---------------+---------+-----------+------------+--------+
- Create a query to show the average runtimes of movies scoring below a 7.5 on imdb, grouped by their respective genres.
+--------+----------------+
| Genre  | AverageRuntime |
+--------+----------------+
| Sci-Fi |       119.5000 |
| Horror |        83.0000 |
| Comedy |        96.0000 |
+--------+----------------+
- There's been a data entry mistake; Starship Troopers is actually rated R, not PG-13. Create a query that finds the movie by its title and changes its rating to R.

- Show the ID number and rating of all of the Horror and Documentary movies in the database. Do this in only one query.
+-------------------+--------+
| Title             | Rating |
+-------------------+--------+
| Lavalantula       | TV-14  |
| Waltz With Bashir | R      |
+-------------------+--------+
- This time let's find the average, maximum, and minimum IMDB score for movies of each rating.
+--------+--------------+----------+----------+
| Rating | AverageScore | MaxScore | MinScore |
+--------+--------------+----------+----------+
| PG     |      6.96667 |      9.2 |      4.6 |
| TV-14  |      4.70000 |      4.7 |      4.7 |
| R      |      7.60000 |      8.0 |      7.2 |
| G      |      8.10000 |      8.1 |      8.1 |
| PG-13  |      8.20000 |      8.2 |      8.2 |
+--------+--------------+----------+----------+
- That last query isn't very informative for ratings that only have 1 entry. Use a HAVING COUNT(*) > 1 clause to only show ratings with multiple movies showing.
+--------+--------------+----------+----------+
| Rating | AverageScore | MaxScore | MinScore |
+--------+--------------+----------+----------+
| PG     |      6.96667 |      9.2 |      4.6 |
| R      |      7.60000 |      8.0 |      7.2 |
+--------+--------------+----------+----------+
- Make the movie list more child-friendly. Delete all entries that have a rating of R. Remember to record your queries in a README.md file
DELETE FROM Movies WHERE Rating = 'R';
> Remember to record your queries in a README.md file before the last two commands below

- Delete the Movies Table
DROP TABLE Movies;
- Delete the Database
DROP DATABASE Movies;



NOTES ----
One-to-one relationship: Only one data in one table relates to one day in another table.
One-to-many relationship: If only one data relates to multiple data in another table.
Many-to-many relationship: If multiple data in one table relates to multiple data in another table.

# Database-with-python
Database Population with Information from JSON using SQLite and Python

# Description
This code establishes a connection to an SQLite database named 'rosterdb.sqlite' and creates three tables: 'User', 'Course', and 'Member'. The 'User' table has columns for 'id' and 'name', where the 'id' is a unique auto-incrementing integer and the 'name' is a unique text value. The 'Course' table has columns for 'id' and 'title', following the same structure as the 'User' table. The 'Member' table has columns for 'user_id', 'course_id', and 'role', with the primary key set as a combination of 'user_id' and 'course_id'.

The code prompts the user to enter a file name. If no name is provided, it defaults to 'roster_data_sample.json'. It then reads the contents of the specified file, assuming it is in JSON format. The JSON data is parsed and stored in the 'json_data' variable.

Next, the code iterates over each entry in the 'json_data' list. Each entry represents a user, course, and their respective roles. The name, title, and role are extracted from each entry. The extracted data is printed.

The code then performs several database operations. It attempts to insert the user's name into the 'User' table, ignoring if the name already exists. It retrieves the 'id' of the user from the 'User' table. It does the same for the course, inserting the title into the 'Course' table and retrieving the 'id' of the course. Finally, it inserts or replaces a record into the 'Member' table with the 'user_id', 'course_id', and 'role' values.

After each iteration, the changes are committed to the database using conn.commit().

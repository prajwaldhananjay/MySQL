# MySQL
MySQL Course Material

What is a db ? 
1. A collection of data. Ex : Phonebook 
2. A method of accessing and managing data. Ex : DBMS like MySQL

SQL - Structured Query Language
It's a language used to  talk to the database
It's not unique to MySQL. Even PostgreSQL uses SQL. 

For the udemy course, I'm using Groom.io
In groom IDE,
To start the mysql server, #mysql-ctl start
"   stop "   "      "    , #mysql-ctl stop
To stop and start #mysql-ctl cli
To exit from mysql ---> exit

To see the existing databases <br>
  show databases;
  
Creating a new database <br>
  CREATE DATABASE database_name;
  
To delete a database <br>
  DROP DATABASE database_name;
  
To know what database you're currently working on, <br>
  SELECT database();
  
To use a particular database <br>
  USE database_name;
  
There are lot of diff datatypes used in MySQL <br>
INT, LONGINT, FLOAT, DOUBLE, etc <br>
CHAR, VARCHAR, TEXT, ENUM, etc <br>
DATE, DATETIME, TIMESTAMP, etc 

INT is used to represent all numbers ( +ve, -ve, big or small) <br>
VARCHAR is used to represent text ( Variable length string ) varchar(100) represents 100 characters 
                                               
To create a table <br>
  CREATE TABLE table_name
  (
    column_name data_type,
    column_name data_type
   ); 
   
To view tables, <br>
SHOW TABLES; <BR>
SHOW COLUMNS FROM table_name; <br>
DESC table_name; 
  
To delete a table, <br>
  DROP TABLE table_name;
  
To insert data into a table <br>
  INSERT INTO table_name(column_name1, column_name2)
  VALUES('data_for_column1', 'data_for_column2');
  
To view the data in a table <br>
  SELECT * FROM table_name;
 
To view what the warning was <br>
  SHOW WARNINGS;
  
NULL - The value is not knwon ( Does not mean zero ) <br>
  By default a column takes in NULL entries. So while creating a table, NOT NULL must be mentioned to change it. <br>
  CREATE TABLE table_name( column_name data_type NOT NULL ); <br>
  So by default, int type stores 0 and varchar type sets black space to that row
  
To set a default value, <br>
  CREATE TABLE table_name( column_name data_type NOT NULL DEFAULT 'unnamed'); <br>
  Ex : DEFAULT '99' set for INT
  
PRIMARY KEY <br>
  It is a unique identifier for a row. <br>
  CREATE TABLE table_name
  (
    column_name1 data_type,
    column_name2 data_type,
    PRIMARY KEY (column_name1)
   );
  
  Example <br>
  CREATE TABLE unique_cats2 ( <br>
    cat_id INT NOT NULL AUTO_INCREMENT, <br>
    name VARCHAR(100), <br>
    age INT, <br>
    PRIMARY KEY (cat_id) <br>
);  <br>
  
*----------*-----------* <br>

CRUD
  
SELECT age FROM cats; <br>
SELECT name FROM cats; <br>
SELECT name, age FROM cats; 
  
WHERE Clause <br>
SELECT * FROM cats WHERE age=4; <br>
SELECT * FROM cats WHERE name = 'blue'; <br>
SELECT * FROM cats WHERE cat_id=age; <br>
  
ALIASES <br>
SELECT cat_id AS ID FROM cats; <br>
SELECT name AS cat_name, breed AS kitty_breed FROM cats; <br>

UPDATE COMMAND
  UPDATE cats SET breed='Shorthair' WHERE breed='Tabby'; <br>
  UPDATE cats SET age=14 WHERE name='Misty'; <br>
  
DELETE COMMAND
  DELETE FROM table_name; // Deletes all the entries in the table. DIff from Drop Table <br>
  DELETE FROM cats WHERE name = 'Misty'; //Will delete the entry with name MIsty <br>
  
DISTINCT - used to get distinct rows only. <br>
SELECT author_lname FROM books; <br>

SELECT DISTINCT author_lname FROM books; <br>
 
SELECT author_fname, author_lname FROM books; <br>
 
SELECT DISTINCT CONCAT(author_fname,' ', author_lname) FROM books; <br>
 
SELECT DISTINCT author_fname, author_lname FROM books; <br>
  
ORDER BY - used to sort the data.
  
SELECT author_lname FROM books ORDER BY author_lname;  // sorts based on author_lname <br>
 
SELECT title FROM books ORDER BY title; // sorts title of books based on title <br>
By default, it's sorted in Ascending order.
 
SELECT released_year FROM books ORDER BY released_year DESC; // DESC is used to sort in descending order <br>
SELECT name, breed FROM cats ORDER BY 2; // 2 refers to the 2nd column i.e breed. <br>
SELECT name, breed FROM cats ORDER BY 2,1; // First sort by 2, then sort similar ones by 1.
  
LIMIT - Used to limit the number of entries. <br>
  SELECT title FROM books LIMIT 10; // Gives the top 10 entries from books <br>
  SELECT * FROM books LIMIT 1; // First row of the table <br>
  SELECT title, released_year FROM books  
ORDER BY released_year DESC LIMIT 5; // Gives top 5 entries of title and released_year sorted in descending order by released_year <br>
  1st row is 0, 2nd row is 1 and so on
  
SELECT title, released_year FROM books 
ORDER BY released_year DESC LIMIT 0,5; // 0 is the first row that it'll retrieve and upto the 5th row.  <br>

LIKE - It's keyword used to match a pattern. Used along with WHERE. <br>
  SELECT title, author_fname FROM books WHERE author_fname LIKE '%da%'; // Retrieves author_fname which has 'da' in it. <br>
  _ underscore refers to one character. LIKE '_ad_' refers to a 4 character word with ad in between. <br>
  Use \% or \_ if you want to look for actual % or _.
  
  
DATE, DATETIME AND TIMESTAMP
  To print the current time <br>
  SELECT CURTIME();
  
  To print the current date <br>
  SELECT CURDATE();
  
  To print the day of the week in number. Ex : Sunday is 0 <br>
  SELECT DATE_FORMAT(NOW(), '%w');
  
  
  To print the day of the week in day. Ex : Sunday <br>
  SELECT DATE_FORMAT(NOW(), '%W');
  
  
  


  




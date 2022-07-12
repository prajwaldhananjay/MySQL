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
  

  


  




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
  

  




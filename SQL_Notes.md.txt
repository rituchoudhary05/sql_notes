```
SQL DOWNLOAD:
1)MYSQL download on google (MYSQL.COM)
2)Downloads
3)MySQL Community (GPL) Downloads »
3)MySQL Installer for Windows
4)565.9M
5)no thanks start download

6)Setup type -full
7)execute
8)next->next->username :ritu,User :localhost->next->next
9)password:12345
10)finish


----------------------------------------------------------------------------------------------------------------------------

SQL:DBMS(data base management system)
->SQL(DBMS) ->DATABASES (eg. student,hospital) ->TABLES (eg. student_details,teachers_detail)

DAY1::
-DATABASE=Collection of data in can be in tabular form/
-TABLE->ROW(record)
      ->COLUMN(field name)
-4 operations=CRUD(CREATE,READ(Search,sort),UPDATE(alter),DELETE)
-phle aaya Microsoft ka Excel , then access, aab SQL(PAID/licensed), so we use MYSQL(Open source)jika koi owner nhi
-scientific family(eg.php , ruby , c) /database family(eg. sql, mongoDB )
-port no.:3306
-------------------------------------------------------------------------------------------------------------------------------
DAY2::
-data= raw facts (before process)
-information= processed data
-student table:xyz1
 
STUDENT_ID	STUDENT
_NAME	STUDENT_ADRESS	STUDENT_MARKS	PASS_FAIL
1	RITU	ABC	70	PASS
2	SONA	BCD	80	PASS
3	DEEP	CDE	20	FAIL
4	YOGI	DEF	66	PASS

-RDBMS=Relational DBMS(maintain the relation between databases)
-DATATYPES:
	-Boolean(bool)
	-integer(int)
	-float
	-string (char-memory waste ,varchar-memory used that was needed only) etc
-Ctrl+Enter =to execute in sql
-Interfaces:GUI(Graphical user interface),CLI(command line interface)
-real instance of a class is object
-TYPES OF SQL COMMANDS

1. DDL – Data Definition Language
Purpose: Used to create and modify the structure of database objects.

Commands:
CREATE – Creates a new database object.
ALTER – Modifies the structure of an existing object.
DROP – Deletes the database object.
TRUNCATE – Removes all records from a table.

Example:
CREATE TABLE students (
    id INT,
    name VARCHAR(50),
    marks INT
);


2. DML – Data Manipulation Language
Purpose: Used to add, modify, and delete data from tables.

Commands:
INSERT – Adds new records.
UPDATE – Modifies existing records.
DELETE – Deletes records.

Example:
INSERT INTO students VALUES (1, 'Ritu', 90);

UPDATE students
SET marks = 95
WHERE id = 1;

DELETE FROM students
WHERE id = 1;


3. DQL – Data Query Language
Purpose: Used to retrieve data from the database.

Command:
SELECT – Retrieves data from a table.

Example:
SELECT * FROM students;

SELECT name, marks
FROM students
WHERE marks > 80;


4. DCL – Data Control Language
Purpose: Used to control access and permissions in the database.

Commands:
GRANT – Gives permissions to a user.
REVOKE – Removes permissions from a user.

Example:
GRANT SELECT ON students TO user1;

REVOKE SELECT ON students FROM user1;


5. TCL – Transaction Control Language
Purpose: Used to manage transactions in a database.

Commands:
COMMIT – Permanently saves changes.
ROLLBACK – Undoes changes.
SAVEPOINT – Creates a point to which a transaction can be rolled back.

Example:
UPDATE students
SET marks = 95
WHERE id = 1;

COMMIT;


EASY WAY TO REMEMBER:

DDL → Structure
DML → Modify Data
DQL → Retrieve Data
DCL → Permissions and access
TCL → Transactions



---------------------------------------------------------------------------------------------------------------------------------------------------------------------------DAY 3::

-Operators eg:
   -> =,>,<,>=,<=
   -> =,!= / <>
   ->or,and

-CONSTRAITS:
 Constraints are rules applied to columns in a table to control the type of data that can be stored.
 a)not null
 b)unique
 c)primary key
 d)foreign key
 e)default
 f)check

-candidate key-A column/set of columns capable of becoming the primary key
-alternate key-A candidate key that was not selected as the primary key

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
DAY 4::




---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
QUERIES/COMMANDS:

-ctrl +2 finger to zoom in and zoom out
-ctrl+enter -to execute the command

1)CREATE DATABASE xyz;   -create database with name xyz
2)SHOW DATABASES;   -show all database present
3)USE xyz;   -to enter in database xyz
4)SHOW TABLES;   -to see tables in database
5)CREATE TABLE xyz1
(
   student_id int,
   student_name varchar(20),
   student_adress varchar(80),
   student_marks int,
   pass_fail char(4)
);
6)DESC xyz1;   -to see the table you created
7)SELECT * FROM xyz1;   -retrieve all columns from table xyz1
8)SELECT student_name,student_marks FROM xyz1;   -retrieve particular columns from table xyz1
9)INSERT INTO xyz1 VALUES(1,"ritu","pt.20,khatipura",78,"pass")
10)INSERT INTO xyz1(student_name,student_id) VALUES("palak",2)

12)SELECT * FROM xyz1 WHERE student_marks=50;   -where is a clause use to give conditions
13)SELECT * FROM xyz1 WHERE adress="Jaipur" and pass_fail="pass";   -and is use to give multiple conditions
14)5)CREATE TABLE xyz2
(
   student_id int not null unique,
   student_name varchar(20) not null,
   student_adress varchar(80)not null,
   student_marks int not null default 0,
   pass_fail char(4) not null default 'fail'
);                                             -table with constraits

15)INSERT INTO xyz2(student_id ,student_name,student_adress) VALUES( 1,"ritu","jaipur",default,default)---when you want to use default value by giving field names
16)INSERT INTO xyz2 VALUES( 1,"ritu","jaipur",default,default)---when you want to use default value without giving field name
```
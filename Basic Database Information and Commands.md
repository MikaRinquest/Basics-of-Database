Basic Database Information and Commands
Basic Database Information and Commands

## DATABASE

    Types of Databases
    	-Network Databases:
    	-Relational Databases:
    	-Hierarchial Databases:

## 4 Main Parts of SQL:

    	-Data Definition Language: Used to create, modify and delete the structures of a database and its objects(tables).
    			DROP:--> This command is used to delete objects from the database.
        		ALTER:--> This is used to alter the structure of the database.
        		TRUNCATE:--> This is used to remove all records from a table, including all spaces allocated for the records are removed.
        		COMMENT:--> This is used to add comments to the data dictionary.
        		RENAME:--> This is used to rename an object existing in the database

    	-Data Manipulation Language: Allows you to update, add, or delete query data.
    			INSERT :--> It is used to insert data into a table.
                UPDATE:--> It is used to update existing data within a table.
                DELETE :--> It is used to delete records from a database tab

    	-Data Control Language: Allows admins to grant or revoke privileges and roles from other users.
    			GRANT:--> This command gives users access privileges to the database.
                REVOKE:--> This command withdraws the user’s access privileges given by using the GRANT command.

    	-Data Query Language: Allows users to retrieve data (The select command).
    		SELECT: It is used to retrieve data from the database.

    	-Transaction Control Language: Used to manage transactions.
    		(Transaction= Group of tasks in done in a single execution. It can only be a success or a failure.)
    			COMMIT:--> Commits a Transaction.
                       		ROLLBACK:--> Rollbacks a transaction in case of any error occurs.
                      		SAVEPOINT:--> Sets a savepoint within a transaction.
                		SET TRANSACTION:--> Specify characteristics for the transaction.

## Key Concepts

    	Data: Information that is not processed, therefore temporarily useless to the business. (Unsorted information)
    	Information: Data that is processed, making it useful to the business. (Sorted information)
    	Field: Each column in a database table.
    	Record: A combination of fields.
    	Table: A collection of related records.
    	Primary Key: Used to identify records in a table. (Only applies 1 column)
    		Composite key: A primary key that applies to 2 columns. (Is possible to span over more than 2, however, if you need 3 columns to uniquely identify information then the table has too many redundancies.)
    	Foreign Key:Establishes a relationship between tables.
    	Database Management System: Software system that allows users to manage a database.
    	Database Relationships/ joins: Shows an association between 2 or more different entities that are related in some way (lecturer and students). There are 2 types: 1) One-to-one : 2) One-to-many.
    	ERD - Entity Relationship Diagram:
    	Data Entities:

    placeholder

## Data Types

    	Numeric:
    		INT
    		SMALLINT
    		BIGINT
    		FLOAT
    		DOUBLE
    		DECIMAL(p,a)- Allows the database to input decimals as an option.
    			p= the maximum amount of characters that can be input on either side of the comma.
    			a= the amount of numbers that will show up in the table.

    	Date and Time:
    		DATE
    		DATETIME
    		TIMESTAMP
    		TIME
    		YEAR


    	String Data Types
    		CHAR-
    		VARCHAR
    		TINYTEXT
    		MEDIUMBLOB
    		TEXT
    		LONGBLOB
    		ENUM- adds mutiple options for the user to choose from.
    		BOOLEAN- Given 2 options to choose from.

## How to make a table in MySQL

    	{Does not have to be all caps} CREATE TABLE TABLENAME (FIRSTROW DATATYPE, SECONDROW DATA TYPE, etc) [One of the rows must have "PRIMARY KEY" inside]
    		auto-_increment(start)= Tells the table to start with a specific number. Every number after the first will have one added to it.
            Example: "CREATE TABLE users (
    -> user_id INT PRIMARY KEY NOT NULL AUTO_INCREMENT,
    -> type VARCHAR(20) NOT NULL,
    -> email VARCHAR(30) NOT NULL UNIQUE,
    -> password VARCHAR(10) NOT NULL,
    -> shipping_address VARCHAR(25) NOT NULL,
    -> phone_number VARCHAR(12) NOT NULL)
    -> ;"

## MySQL Commands

    	create database __; (Creates a database)
    	show databases; (Shows all available databases)
    	use __; (Selects a database to use)


    show tables; (Shows available tables in the database)
    	describe __; (Shows the content of a table shown)
    	select * from [tablename]; (Displays the contents of a table)
    	insert into [tablename] values ____; (Inserts data into the columns)
    	alter table ____; (Changes elements of a table)
    		change column [original column name] [new column name] [constraint] [extra] (Changes name of column)
    		add column _____ (Adds a new column)
    		drop column ____ (Deletes column specified)
    	drop ____; (Completely wipes out whatever is chosen)
    	truncate table [tablename]; (Used to delete all the contents in a table)
    	/*[content*/ ; (Used to add comments)
    	rename [oldname] to [newname]; (Renames a table or database)

## Operators

    	WHERE
    	AND
    	OR
    	NOT
    	ORDER BY- used with "select * from [tablename] order by [row_name/order]
    		Orders= DESC( Descending), ASC (Ascending).
    	LIKE	select [columns name / *] from [table name] where [column name(s)] like [look below for examples]
    		"a%"= Values that start with an 'a'.
    		"%a"= Values that end with an 'a'.
    		"%a%"= Values that have 'a' in any position.
    		"_r%"= Values that have 'r' in the second postion.
    		"r__%"= Values that start with 'r' and have at least 2 characters after it.
    		"a%o"= Values that end with 'a' and ends with 'o'.
    	LIMIT- used with "select * from [tablename] limit [offset] [row start, row end];"
    			Inside of offset would be rows you want excluded.
    	GROUP BY
    		Aggregrate functions

## Arithmetic Operators

    		+ : Addition
    		- : Subtraction
    		* : Multiplication
    		div : Integer Division
    		/ : Division
    		% OR mod : Modulus Operator (Takes the 2 numbers and gives back the amount of remainders)

## Aggreagate Functions

    		Count() - Returns number of rows, including the ones with null values.
    		Max() - Returns highest number.
    		Min() - Returns lowest number.
    		FIrst() -
    		Last() -
    		Avg() - Calculates the average value of everything.
    		Sum() - Adds all the values in a column.

## Numeric Functions

    		AVG - Returns the average.
    		CEIL - Rounds up decimals.
    		COUNT - Returns number of records OR values.
    		FLOOR - Rounds down decimals.
    		BIN - Returns number as binary.
    		GREATEST - Returns the highest value.
    		LEAST - Returns the lowest value.
    		PI - Returns the value of pi.
    		POW - Returns number to the power of.
    			Example: SELECT POW(4,3) = 64
    		RAND - Returns random number. Range can be altered.
    		ROUND - Used to round number to x amount of decimals
    				Example: select round (356.21, 1);
    		SQRT - 	Square roots a number

    		TRUNCATE - Truncates number to specific number of decimals
    				Example: select truncate (345.3456, 2); = 345.34

# CONSTRAINTS

    	NULL- Means that the field can be left blank.

    	DEFAULT - Gives a set answer if the column is left empty.
    		How to use: [column_name] [data_type] default '[what the default should be]',

    	UNIQUE - Ensures that the data in the column never repeats.
    		How to use: [column_name] [data_type] unique,

    	PRIMARY KEY - Used to identify data in a table
    			How to use: [column_name] [data_type] primary key,

    	FOREIGN KEY - Used to link tables together
    			How to use: CREATE TABLE EX([column1], [column2], foreign key([column name that should be foreign key]) references [table_name]([primary key of the table]));

    	CHECK - Gives the column set rules it has to first abide by, else the data is considered invalid.
    		How to use (REMEMBER THIS GOES AFTER THE COLUMNS): [column1 details], [column2 details], constraint ([constraint detail])
    			Example: create table Ex  (name varchar(10) not null, age int, check (Age > 18);
    				This is saying that the value for age must be greater than 18, else an error will appear.

    	CREATE INDEX - Helps user look for information in a table. Does not appear anywhere.

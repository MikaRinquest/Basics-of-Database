# JOINS IN SQL

# WHAT ARE JOINS IN SQL?

    		Commands used to join multiple rows with similair information that is in different tables.Typically used when extracting data from one-to-many or many-to-many relationships.

# TYPES OF JOINS

## INNER JOIN

    			Returns records from the tables that has matching values
    			syntax: select [table1.column1, table1.column2, table2.column1, table2.column2 etc] from table1 inner join table2 on table1.[matching_column]= table2.[matching_column]
    					{the selected columns is what columns will display in the new table} 		{the 2 tables that must be inner joined}	{the matching decides which data to pull}

## LEFT JOIN (LEFT OUTER JOIN)

    			Returns information from the left table that satisfies the conditions from the right table. For records that do not have matching values, it will have the NULL value (the cell will be blank).
    				syntax: select [table1.column1, table1.column2, table2.column1, table2.column3 etc] from table1 (the left table) left join table2 on table1[matching_column] = table2[matching_column]

## RIGHT JOIN (RIGHT OUTER JOIN)

    			Returns information from the right table that satisfies the condition from the left table. For record that do no have matching values, it will appear NULL.
    				syntax: select [table1.column1, table1.column2, table2.column1, table2.column3 etc] from table1 right join table2 (the right table) on table1[matching_column] = table2[matching_column]

## FULL JOIN (FULL OUTER JOIN)

    			Returns all records that match either the left or the right table.
    				syntax: select [table1.column1, table1.column2, table2.column1, table2.column3 etc] from table1 full join table2 on table1[matching_column] = table2[matching_column]

## NATURAL JOIN VERSUS INNER JOIN

    			When using inner join, the column will be repeated, whereas with a natural join the columns will not be repeated.

## HASH JOIN

    			Used to join large tables or when the user wants the most amount of rows

## SELF JOIN

    			Joining a table to itself.

## CROSS JOIN

    			The join clause is applied to every row of both tables. When WHERE is used, it acts like an inner join

    	*To join 3 tables, you'd need 2 joins.

# SQL
This repository contains the [**SQL**](https://en.wikipedia.org/wiki/MySQL) queries I am writing using [**MYSQL**](https://www.w3schools.com/sql/sql_intro.asp) database language in  [**hackerrank**](https://www.hackerrank.com/domains/sql). I will update my repository time to time , and add relavent resources. 

I'm also writing down some important syntaxes for SQL over here in this **README**, so it might be useful for quick reference.
You can also refer [this](https://www.w3schools.com/sql) site for understanding SQL quickly, as I will be summarizing all syntaxes here using that various resources and my experience of writing queries as reference. Feel free to suggest me any changes in the content through my mail neerajsirvisetti@gmail.com or you can make me your connection on [**LinkedIN**](https://www.linkedin.com/in/neeraj-sirvisetti/).

**Commands** | **Syntax** | **Function**
------------ | ------------- | --------------------
 SELECT| SELECT *column1, column2, ...* FROM *table_name*; | select statement is used to select the columns we want in the data from a database.
 SELECT| SELECT * FROM *table_name*; | This statement is used to select all the columns from the database.
 SELECT| SELECT DISTINCT *column1, column2, ...* FROM *table_name*; | This statement is used to return only distinct (different) values.
 WHERE | SELECT *column1, column2, ...* FROM *table_name* WHERE *condition*; | The WHERE clause is used to extract only those records that fulfill a specified condition.
 WHERE | SELECT *column1, column2, ...* FROM *table_name* WHERE *condition1* AND *condition2* OR *condition3 ...*; | The WHERE clause can be combined with AND, OR, and NOT operators
 ORDER BY | SELECT *column1, column2, ...* FROM *table_name* ORDER BY *column1, column2, ...* ASC|DESC; | The ORDER BY keyword is used to sort the result-set in ascending or descending order.
 INSERT INTO |INSERT INTO *table_name* *(column1, column2, column3, ...)* VALUES *(value1, value2, value3, ...)*; | Specifying both the column names and the values to be inserted
 INSERT INTO | INSERT INTO *table_name* VALUES (*value1, value2, value3, ...*); | Adding values for all the columns of the table.
 |  |   |    Note: make sure the order of the values is in the same order as the columns in the table.
 UPDATE | UPDATE *table_name* SET *column1 = value1, column2 = value2, ...* WHERE *condition*; | This statement is used to modify the existing records in a table.
 DELETE | DELETE FROM *table_name* WHERE *condition*; | This statement is used to delete existing records in a table.
 LIMIT  | SELECT *column_name(s)* FROM *table_name* WHERE *condition* LIMIT *index*,*count*; | This clause is used to specify the number of records to return and from which index.
  MIN() |SELECT MIN(*column_name*) FROM *table_name* WHERE *condition*; |This function returns the smallest value of the selected column.
  MAX() |SELECT MAX(*column_name*) FROM *table_name* WHERE *condition*; |This function returns the maximum value of the selected column.
  COUNT() |SELECT COUNT(*column_name*) FROM *table_name* WHERE *condition*; |This function returns the number of rows that matches a specified criteria.
  AVG() |SELECT AVG(*column_name*) FROM *table_name* WHERE *condition*; |This function returns the average value of a numeric column.
  SUM() |SELECT SUM(*column_name*) FROM *table_name* WHERE *condition*; |This function returns the total sum of a numeric column.
  LIKE | SELECT *column1, column2, ...* FROM *table_name* WHERE *columnN* LIKE *pattern*; | The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.
  IN | SELECT *column_name(s)* FROM *table_name* WHERE *column_name* IN (*value1, value2, ...*);| The IN operator allows you to specify multiple values in a WHERE clause.
   IN    | SELECT *column_name(s)* FROM *table_name* WHERE *column_name* IN (SELECT *STATEMENT*); |
  BETWEEN | SELECT *column_name(s)* FROM *table_name* WHERE *column_name* BETWEEN *value1* AND *value2*; | The BETWEEN operator selects values within a given range(**INCLUSIVE**). The values can be numbers, text, or dates.
  AS | SELECT *column_name* AS *alias_name* FROM *table_name*; | SQL aliases are used to give a table, or a column in a table, a temporary name.
   AS   | SELECT *column_name(s)* FROM *table_name* AS *alias_name*;  |
 GROUP BY | SELECT *column_name(s)* FROM *table_name *WHERE *condition* GROUP BY *column_name(s)* ORDER BY *column_name(s)*; | The GROUP BY statement group rows that have the same values into summary rows.
  
There are two wildcards often used in conjunction with the LIKE operator:
1. % - The percent sign represents zero, one, or multiple characters
2. _ - The underscore represents a single character 
  
  **LIKE Operator**	 | **Description**
  ------------ | ------------- 
WHERE CustomerName LIKE 'a%' |	Finds any values that start with "a"
WHERE CustomerName LIKE '%a' |	Finds any values that end with "a"
WHERE CustomerName LIKE '%or%' |	Finds any values that have "or" in any position
WHERE CustomerName LIKE '_r%'	| Finds any values that have "r" in the second position
WHERE CustomerName LIKE 'a__%' | 	Finds any values that start with "a" and are at least 3 characters in length
WHERE ContactName LIKE 'a%o'	 | Finds any values that start with "a" and ends with "o"


## MySQL String Functions
**Function**	 | **Description**
------------ | -------------
ASCII	| Returns the ASCII value for the specific character
CHAR_LENGTH	| Returns the length of a string (in characters)
CHARACTER_LENGTH	| Returns the length of a string (in characters)
CONCAT	| Adds two or more expressions together
CONCAT_WS	| Adds two or more expressions together with a separator
FIELD	| Returns the index position of a value in a list of values
FIND_IN_SET	| Returns the position of a string within a list of strings
FORMAT	| Formats a number to a format like "#,###,###.##", rounded to a specified number of decimal places
INSERT	| Inserts a string within a string at the specified position and for a certain number of characters
INSTR	| Returns the position of the first occurrence of a string in another string
LCASE	| Converts a string to lower-case
LEFT	| Extracts a number of characters from a string (starting from left)
LENGTH	| Returns the length of a string (in bytes)
LOCATE	| Returns the position of the first occurrence of a substring in a string
LOWER	| Converts a string to lower-case
LPAD	| Left-pads a string with another string, to a certain length
LTRIM	| Removes leading spaces from a string
MID	| Extracts a substring from a string (starting at any position)
POSITION	| Returns the position of the first occurrence of a substring in a string
REPEAT	| Repeats a string as many times as specified
REPLACE	| Replaces all occurrences of a substring within a string, with a new substring
REVERSE	| Reverses a string and returns the result
RIGHT	| Extracts a number of characters from a string (starting from right)
RPAD	| Right-pads a string with another string, to a certain length
RTRIM |	Removes trailing spaces from a string
SPACE	| Returns a string of the specified number of space characters
STRCMP	| Compares two strings
SUBSTR	| Extracts a substring from a string (starting at any position)
SUBSTRING	 | Extracts a substring from a string (starting at any position)
SUBSTRING_INDEX	 | Returns a substring of a string before a specified number of delimiter occurs
TRIM	| Removes leading and trailing spaces from a string
UCASE	| Converts a string to upper-case
UPPER	| Converts a string to upper-case

## MySQL Numeric Functions
**Function**	| **Description**
------------ | -------------
ABS	| Returns the absolute value of a number
ACOS	| Returns the arc cosine of a number
ASIN	| Returns the arc sine of a number
ATAN	| Returns the arc tangent of one or two numbers
ATAN2	| Returns the arc tangent of two numbers
AVG	| Returns the average value of an expression
CEIL	| Returns the smallest integer value that is >= to a number
CEILING	| Returns the smallest integer value that is >= to a number
COS	| Returns the cosine of a number
COT	| Returns the cotangent of a number
COUNT	| Returns the number of records returned by a select query
DEGREES	| Converts a value in radians to degrees
DIV	| Used for integer division
EXP	| Returns e raised to the power of a specified number
FLOOR	| Returns the largest integer value that is <= to a number
GREATEST	| Returns the greatest value of the list of arguments
LEAST	| Returns the smallest value of the list of arguments
LN	 | Returns the natural logarithm of a number
LOG	| Returns the natural logarithm of a number, or the logarithm of a number to a specified base
LOG10	| Returns the natural logarithm of a number to base 10
LOG2	| Returns the natural logarithm of a number to base 2
MAX	| Returns the maximum value in a set of values
MIN	| Returns the minimum value in a set of values
MOD	| Returns the remainder of a number divided by another number
PI	| Returns the value of PI
POW	| Returns the value of a number raised to the power of another number
POWER	| Returns the value of a number raised to the power of another number
RADIANS	| Converts a degree value into radians
RAND	| Returns a random number
ROUND |	Rounds a number to a specified number of decimal places
SIGN	| Returns the sign of a number
SIN	| Returns the sine of a number
SQRT	| Returns the square root of a number
SUM	| Calculates the sum of a set of values
TAN	| Returns the tangent of a number
TRUNCATE	| Truncates a number to the specified number of decimal places

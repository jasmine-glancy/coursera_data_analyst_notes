#  Module 3: Database Essentials

## Large Datasets in SQL

| Concept          | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Big Query**    | - Sandbox (No Charge)<br>&emsp;• 12 projects maximum<br>&emsp;• Can’t insert new records to a database<br>&emsp;• Can’t update records                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **SQL Syntax**   | - Use all caps for clause starters <br>&emsp;• SELECT, FROM, WHERE, etc<br>    <br>- Functions should also be in all caps<br>&emsp;• SUM()<br><br>- Column names should be in all lowercase (snake_case)<br>- Table names should be in CamelCase<br>- Two situations where ‘ or “ matters:<br>&emsp; 1. When you want strings to be identifiable in *any* SQL dialect<br>&emsp; 2. When your string contains an apostrophe or quotation marks<br><br>- Most SQL dialects use single quotes for strings<br>- Keep the length of each line in a query to less than or equal to 100 characters to make queries easier to read<br>- Use `--` or `/* */` to input multi-line comments |
| **SQL Dialects** | - Slightly different variations of SQL<br>- BigQuery is case sensitive                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
## Cues

- When using SQL, the ___ clause can be used to filter a dataset of customers to only include people who have made a purchase in the past month.
- Which cases are most often used for column names in a database table and represent a SQL best practice? 
- A database table is named WebTrafficAnalytics. What type of case is this?
- What can be removed from the following query without preventing it from running or changing the results?
	```sql
	SELECT *
	FROM `Uni_dataset.new_table`
	WHERE ID = 'Lawrence'
	```

---

## Summary

When using SQL, the `WHERE` clause can be used to filter a dataset of customers to only include people who have made a purchase in the past month. `WHERE` is the section of a query that specifies criteria that the requested data must meet. Column names should be written in lowercase. Or, for names with multiple words, snake case is used to separate each word with an underscore to make it more readable. Camel case means that the first letter of each word is capitalized; however, capitalizing the first letter is optional. The backticks can be removed from the name of the dataset without preventing the query from running. Backticks can make queries more readable, but they are optional.

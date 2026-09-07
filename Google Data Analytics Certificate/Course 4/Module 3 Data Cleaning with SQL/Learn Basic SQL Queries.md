# Module 3: Data Cleaning with SQL

## Learn Basic SQL Queries

| Concept               | Notes                                                                                                                                                                |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`SELECT` & `FROM`** | - Help specify the data we want to extract from the database and use                                                                                                 |
| **Important Note**    | - SQL is easy to learn <br>&emsp;• ***The hardest part is figuring out what question you want to ask your data***<br>&emsp;• Be curious about the data you're given! |
| **`DISTINCT`**        | - Removes duplicates when included in a `SELECT` statement                                                                                                           |
| **`LENGTH`**          | - Also written as `LEN` in some SQL dialects <br>- Finds the length of a column                                                                                      |
| **`SUBSTR`**          | - Substring function <br>&emsp;• `SUBSTR([column], which letter to start with, # of letters to pull)`                                                                |
## Cues

- What are some key benefits of using SQL for data analytics projects?
- Which SQL function cleans string variables by extracting a substring from a string variable?
- What's the hardest part of learning SQL?
- What is the basic SQL formula syntax?

---

## Summary

SQL can handle huge amounts of data, can be adapted and used for multiple database programs, and offers powerful tools for cleaning data. `SUBSTR` cleans string variables by extracting a substring from a string variable.

While SQL syntax is easy to learn, the hardest part is learning which questions to ask your data. The most common structure of SQL is:

```sql
SELECT
	column names
FROM
	database.schema.table
WHERE
	filter stuff
```

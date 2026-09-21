# Module 4: Perform Data Calculations 

## Learn More SQL Calculations

| Concept               | Notes                                                                                                                                                                                                              |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Operator**          | - A symbol that names the type of ​operation or calculation to be performed in a formula<br>&emsp;•  `+` for addition<br>&emsp;• `-` for subtraction<br>&emsp;• `*` for multiplication<br>&emsp;• `/` for division |
| **Modulo**            | - An operator (`%`) that returns the remainder when one number is divided by another                                                                                                                               |
| **Underscores**       | - Lines used to underline words and connect text characters<br>- Helps keep names readable                                                                                                                         |
| **`GROUP BY`**        | - A command that groups rows that have the same values from a table into summary rows                                                                                                                              |
| **`EXTRACT` command** | - Allows us to pull one part of a given date to use<br>- `EXTRACT(YEAR FROM start_time)`                                                                                                                           |
## Cues

- When using SQL, which of the following are reasons for using underscores in column names?
- What is the purpose of the EXTRACT command in a query?
- In a SQL query, what is the purpose of the modulo (%) operator? 
- A data professional writes a query that uses more than one arithmetic operator. What do they add to the query to control the order of the calculations?
- What does the `GROUP BY` function do?

- - -
## Summary

Column names in SQL should have underscores, not spaces. Using underscores instead of spaces helps avoid potential issues with servers and applications. It also helps to keep the column names readable. The purpose of the `EXTRACT` command in a query is to extract a part from a given date. The `EXTRACT` command can extract any part from a date/time value. The modulo operator (`%`) returns the remainder of a division calculation. To control the order of calculations in a SQL query, add parentheses to control the order of calculations. In a SQL query, `GROUP BY` groups rows that have the same values from a table into summary rows.
# Module 1: Organize Data for More Effective Analysis

## Sort Data in SQL

| Concept                                                          | Notes                                                                                                                                                                                                                                                   |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sort Data by One Column**                                      | - `ORDER BY` sorts by a column in a database<br>&emsp;• Sorted by ascending order by default<br>&emsp;• You can order by descending using the syntax `ORDER BY column DESC;`                                                                            |
| **Filter and then Sort Data**                                    | - Pair `WHERE` with `ORDER BY` to filter, then sort, data<br>&emsp;• `WHERE` filters, `ORDER BY` sorts                                                                                                                                                  |
| **Filter on Two Conditions, then Sort Data in Descending Order** | - `WHERE`, `AND`, and `ORDER BY`                                                                                                                                                                                                                        |
## Cues

- Why is it useful to create tables from queries?
- Why is the ability to view specific subsets of data in a dataset important?
- Which SQL statement should you use to find the least expensive to most expensive price in a column?
- What SQL operator enables a data professional to filter for two conditions at once when using a `WHERE` statement?

- - -
## Summary

Creating tables from queries can help you perform data analysis in the future by giving you a quick reference to historical ad hoc queries. Meaning, if someone asks for a dataset once, it's possible they'll need it again. The ability to view specific subsets of data in a dataset is important because it allows you to verify smaller subsections of data before expanding to see the "big picture".
  
To find the least expensive to most expensive price in a column, you should use the syntax `ORDER BY column_name`. An `ORDER BY` statement sorts in ascending order by default. `ORDER BY column_title` is the syntax. The `AND` operator enables a data professional to filter for two conditions at once when using a `WHERE` statement.
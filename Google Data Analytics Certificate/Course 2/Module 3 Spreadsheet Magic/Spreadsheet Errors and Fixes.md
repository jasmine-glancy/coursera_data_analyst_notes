# Spreadsheet Errors and Fixes

## This Markdown File Was Adapted From the "Spreadsheet Errors and Fixes" Section of "Spreadsheet Magic".

When you are new to data analytics—and sometimes even when you aren't—spreadsheet struggles are real. It never feels good when you type in what you are sure is a perfect formula or function, only to get an error message. Understanding errors and how to fix them is a big part of keeping your data clean, so it's important to know how to deal with issues as they come up, and more importantly, not to get discouraged.

Remember, even the most advanced spreadsheet users come across problems from time to time. In this reading, you will learn about common errors and how to fix them.

But first, here are a few best practices and helpful tips. These strategies will help you avoid spreadsheet errors to begin with, making your life in analytics a whole lot less stressful:

1. Filter data to make your spreadsheet less complex and busy.
2. Use and freeze headers so you know what is in each column, even when scrolling.
3. When multiplying numbers, use an asterisk (*) not an X.
4. Start every formula and function with an equal sign (=).
5. Whenever you use an open parenthesis, make sure there is a closed parenthesis on the other end to match.
6. Change the font to something easy to read.
7. Set the border colors to white so that you are working in a blank sheet.
8. Create a tab with just the raw data, and a separate tab with just the data you need.
    

Now that you have learned some basic ways to avoid errors, you can focus on what to do when that dreaded pop-up does appear. The following table lists common spreadsheet errors and examples of each. Knowing what the errors mean takes some of the fear out of getting them.

|           |                                                                                                                  |                                                                                                                                                     |
| --------- | ---------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Error     | Description                                                                                                      | Example                                                                                                                                             |
| `#DIV/0!` | A formula is trying to divide a value in a cell by 0 (or an empty cell with no value).                           | =B2/B3, when the cell B3 contains the value 0.                                                                                                      |
| `#ERROR!` | (Google Sheets only) Something can't be interpreted as it has been input. This is also known as a parsing error. | =COUNT(B1:D1 C1:C10) is invalid because the cell ranges aren't separated by a comma.                                                                |
| `#N/A`    | A formula can't find the data.                                                                                   | The cell being referenced can't be found.                                                                                                           |
| `#NAME?`  | The name of a formula or function used isn't recognized.                                                         | The name of a function is misspelled.                                                                                                               |
| `#NUM!`   | The spreadsheet can't perform a formula calculation because a cell has an invalid numeric value.                 | =DATEDIF(A4, B4, "M") is unable to calculate the number of months because the date in cell A4 falls after the date in cell B4.                      |
| `#REF!`   | A formula is referencing a cell that isn't valid.                                                                | A cell used in a formula was in a column that was deleted.                                                                                          |
| `#VALUE!` | A general error indicating a problem with a formula or with referenced cells.                                    | There could be problems with spaces or text, or with referenced cells in a formula; you may have additional work to find the source of the problem. |

The next sections provide examples of these errors and possible solutions. There is also a pro tip at the end of this reading about how you can spot errors quickly in your spreadsheet by using conditional formatting.

Tip: If you are new to spreadsheets, focus on the descriptions of the errors in the previous table. Spend some time working with spreadsheets and then come back to read the examples below.

## #DIV/0!

A #DIV/0! error means that your formula is trying to divide a value in a cell by 0, or by an empty cell (with no value). In math, dividing by zero doesn't make sense. Dividing by zero doesn't make sense in spreadsheets either.

Assume you are trying to calculate the percentage of required tasks that have been completed in a project. Column B has the number of required tasks and Column C has the number of completed tasks. You enter the formula `=C2/B2*100` in cell D2 to calculate the percentage of completion. You copy the formula to the rest of the cells in Column D, but there is a #DIV/0! error in cell D4. No tasks are required for that particular line item so the formula is trying to divide by 0 in cell B4.

### Fixing the error

You could delete row 4, but if things change and tasks are required for that line item in the future, you would have to insert that row back into the spreadsheet.

A better solution is to have the spreadsheet enter "Not applicable" whenever a cell in the B column contains a 0 and causes the divide by zero error.

Change the formula in the D column cells so the formula in cell D4 changes from `=C4/B4*100` to `=IFERROR(C4/B4*100, "Not applicable")`. The results are still the same for all other cells in the D column, but the #DIV/0! error no longer appears in cell D4.

The IFERROR function returns the first argument (calculation) if it is not an error value, or returns the second argument when there is an error. In the example, `C4/B4*100` is the first argument and `"Not applicable"` is the second argument.

## #ERROR!

A #ERROR! error can occur if you have specified two or more cell ranges without a comma as the delimiter to separate them. The spreadsheet can't figure out what the true cell ranges are.

The following ranges written without a comma cause #ERROR! to appear:  
`=COUNT(B1:D1 C1:C10)  `
`=SUM(B2:B6 C2:C6)`

### Fixing the error

You can fix these errors by replacing the space between the cell ranges with a comma.  
=COUNT(B1:D1,C1:C10) instructs the spreadsheet to count the number of values from cell B1 through cell D1 and from C1 through C10.  
=SUM(B2:B6,C2:C6) instructs the spreadsheet to add the values in cell B2 through cell B6 and from cell C2 through cell C6.

## #N/A

A #N/A error tells you that the data in your formula or function can't be found by the spreadsheet. Generally, this means the data doesn't exist. This error most often occurs when you are using functions like VLOOKUP to look up a value in a spreadsheet based on matching criteria.

For example, if the following lookup table is at the top of a large spreadsheet, the spreadsheet could automatically look up and fill in the price of almonds anywhere in the spreadsheet that you have inserted a VLOOKUP function.

Assume cell C100 in the spreadsheet contains the formula: `=VLOOKUP(B100, $B$4:$C$6, 2, 0)`. This formula should compare the text in cell B100 with Almonds, Cashews, or Walnuts in the lookup table and insert the price for the matching nut in cell C100. But there is a #N/A error in cell C100 because the price for Almond doesn't exist in the lookup table. The plural, Almonds, is in the lookup table.

### Fixing the error

To fix the error, change Almond in cell B100 to Almonds. This will enable the spreadsheet to automatically find and insert the price for almonds from the lookup table, $2.00 in cell C4, into cell C100.

## #NAME?

A #NAME? error means that your spreadsheet needs help understanding your formula or function. To solve #NAME? errors, the first step is to check your spelling. Then, be sure to use the full name for any formulas or functions. Spreadsheet applications will suggest formulas and functions for you so it is a good idea to make use of this feature.

Here is an example of a #NAME? error resulting from an extra O in the VLOOKUP function. The spreadsheet is trying to use VLOOOKUP which doesn't exist.

### Fixing the error

To fix the error, change VLOOOKUP to VLOOKUP in the formula in cell E5.

## #NUM!

A #NUM! error means that the spreadsheet can't perform a calculation as specified. This can happen for a few reasons. The numbers might be too big or small for the spreadsheet to process, the calculation might be impossible, or there is something wrong with the variables that have been input. To fix a #NUM! error, your best bet is to just return to your formula and double-check it.

In the example below, the spreadsheet can't execute the DATEDIF formula because the Start Date is after the End Date; this needs to be corrected before the formula will work.

### Fixing the error

Change the date in cell A4 from 9/14/2020 to 10/1/2019 and the date in cell B4 from 10/1/2019 to 9/14/2020. The dates will be in the correct order for the formula to work, and the error will no longer appear.

## #REF!

A #REF! error tells you that your formula or function is referencing a cell that is no longer valid. A cell (or range of cells) may be missing because it was deleted.

In the example below, a simple formula is adding the values in cells A2, A3, and A4. =A2+A3+A4

If you delete row 4 (and the value 26 in cell A4), the #REF! error appears and the spreadsheet can no longer calculate the total.

### Fixing the error

You can fix the error by updating the formula in cell A5 to add the values from cell A2 and cell A3 only. =A2+A3

## #VALUE!

A #VALUE! error is a general error that could indicate a problem with a function or referenced cells. It might not be clear right away what the problem is, so this error could require a little more effort to fix.

In the example below, a text string "James" is in End Date column instead of a date. The spreadsheet can't perform the `=DATEDIF(A2,B2, "M")` calculation.

### Fixing the error

Replace "James" in cell B2 with an end date in the right format, and the error will no longer appear.

## Pro tip: spotting errors in spreadsheets with conditional formatting

Conditional formatting can be used to highlight cells a different color based on their contents. This feature can be extremely helpful when you want to locate all errors in a large spreadsheet. For example, using conditional formatting, you can highlight in yellow all cells that contain an error, and then work to fix them.

### Conditional formatting in Microsoft Excel

To set up conditional formatting in Microsoft Excel to highlight all cells in a spreadsheet that contain errors, do the following:

1. Click the green triangle above row number 1 and to the left of Column A to select all cells in the spreadsheet.
2. From the main menu, click Home, and then click Conditional Formatting to select Highlight Cell Rules > More Rules.
3. For Select a Rule Type, choose Use a formula to determine which cells to format.
4. For Format values where this formula is true, enter =ISERROR(A1).
5. Click the Format button, select the Fill tab, select yellow (or any other color), and then click OK.
6. Click OK to close the format rule window.
    

To remove conditional formatting, click Home and select Conditional Formatting, and then click Manage Rules. Locate the format rule in the list, click Delete Rule, and then click OK.

### Conditional formatting in Google Sheets

To set up conditional formatting in Google Sheets to highlight all cells in a spreadsheet that contain errors, do the following:

1. Click the empty rectangle above row number 1 and to the left of Column A to select all cells in the spreadsheet.
    
2. From the main menu, click Format and select Conditional Formatting to open the Conditional format rules pane on the right.
    
3. While in the Single Color tab, under Format rules, use the drop-down to select Custom formula is, enter =ISERROR(A1), select yellow (or any other color) for the formatting style, and then click Done.
    

To remove conditional formatting, click Format and select Conditional Formatting, and then click the Trash icon for the format rule.

## Spreadsheet error resources

To learn more and read about additional examples of errors and solutions, explore these resources:

- Microsoft Formulas and Functions: This resource describes how to avoid broken formulas and how to correct errors in Microsoft Excel. This is a useful reference to have saved in case you run into a specific error and need to find solutions quickly while working in Excel.
    
- When Your Formula Doesn't Work: Formula Parse Errors in Google Sheets: This resource is a guide to finding and fixing some common errors in Google Sheets. If you are working with Google Sheets, you can use this as a quick reference for solving problems you might encounter working on your own.
    

With some practice and investigative determination, you will become much more comfortable handling errors in spreadsheets. Each error you catch and fix will make your data clearer, cleaner, and more useful.
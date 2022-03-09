# Creating a Single Data Set from Multiple Data Sets

You can combine multiple data sets in the platform with SQL query functions, such as union and join. This is useful, for instance, if you have training data in one file and test data in another, and by combining them, you can train a model on all the data.

## Prerequisites

- The data sets you want to combine can come from any mix of data sources, but they must already be in the platform. 

   See "Importing Data Sets from Data Sources".

## Procedure

1. Open the platform to the **Transfer Data** tab.
2. Choose **Add from data source** from the Input Type drop-down.
3. Choose a folder to store the combined data set.
4. Enter a name for the data set.
5. Choose **Internal DB** from the Select Connection drop-down.
6. Choose **Custom Query** from the Table or Query drop-down.

   The main window shows a code entry panel. 

7. Enter the SQL query. See the Description section for details.
8. Click **Add Data**.

## Results
After the platform loads the data, the combined feature set appears in the Analyze Feature Sets tab.  

## Description

**Note**: Because SQL uses the dot "." for it's object hierarchy, you cannot use the dot for the platform folder hierarchy when specifying a data set. Use the underscore "\_" instead.

- For a union (combine all rows of selected columns), use the following general syntax (or other syntax described in SQL documentation):

  ```
  select "<column 1>", "<column 2>", "<column 3>", "<column n>" from <top dir>_<sub-folders>_<first data set name>
  union
  select "<column 1>", "<column 2>", "<column 3>", "<column n>" from <top dir>_<sub-folders>_<second data set name>
  ```
  - The columns must match for a union.
  - Add the following code to the end of each column list to add a column in the combined data set with the name of the original data set for each row:

     `'<first data set name>' as new_column_name`

     `'<second data set name>' as new_column_name`
- For a join (combine selected columns for rows that match in a key column), use the following general syntax (or other syntax described in SQL documentation):

  ```
  select tbla."<a col 1>" tbla."<a col 2>" tbla."<a col n>",
  tblb."<b col 1>" tblb."<b col 2>" tblb."<b col n>"
  from <top>_<sub-folders>_<first data set name> [inner | left | right | full outer] join <top>_<sub-folders>_<second data set name> on tbla."<tbla column to match>" = tblb."<tblb column to match>"
  ```
  - None of the column names need to match across the data sets. The match is specified by: `on <tbla col> = <tblb col>`
  - Inner, left, and right joins use this syntax, while full outside joins require the following additional code, such as: `order by <column to order>`
## Examples

- For a union, assume you have already imported a file called *train_data.csv* into a data set called train\_data, and another file called *test_data.csv* into a data set called test\_data. These data sets are in your top-level folder called *top*. You want to combine these data sets into a data set called *train_test_combined*.  

  ```
  select * from top_train_data
  union
  select * from top_test_data
  ```
  To add a column (called 'test or train') to the combined data set with the name of the original data set for each row:

  ```	
  select *,'train_data' as test or train from top_train_data
  union
  select *,'test_data' as test or train from top_test_data
  ```
- For a join, assume you have already imported a file called *server_data.csv* into a data set called server\_data, and another file called *client_data.csv* into a data set called client\_data. The client\_data data set contains a sub-set of the columns from server\_data, but they both have a column called "site". You want to join the first three columns of server\_data with the last three columns of client\_data only when "site" matches.
  ```
  select srvr."Col_1", srvr."Col_2", srvr."Col_3",
  clnt."Col_(n-2)", clnt."Col_(n-1)", clnt."Col_(n)"
  from server_data srvr inner join client_data clnt on srvr."site" = clnt."site"
  ```

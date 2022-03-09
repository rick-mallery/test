# Importing Data Sets from Data Sources

You can import a data set from any major public cloud, from local files, from existing tables, or from queries to existing data sets.

1. Open the platform to the Transfer Data tab.
2. Choose one of the following options in the **Input Type** drop-down:
   - **Add file from URL** &mdash; Enter a URL (https:// or file:///) as the data source.
   - **Add from data connection** &mdash; Enter the name of an existing table or a custom query as the data source. 
   - **Add from local file** &mdash; Choose a file from a file browser. 
3. Jump to a section below for options specific to your input type.

## Adding a File from a URL
1. Choose a folder to store the data set.
2. For **Data Set Name\***, do one of the following:
   - **New Data Set** &mdash; Enter a name for the new data set.
   - **Select Existing Data Set** &mdash; Choose a data set from the drop-down and specify whether you want to **Replace/Add new** or **Append Existing**.
3. Enter the URL in the **Source URL*** text box.
4. Enter the separator in the **Separator*** text box.
5. Add a description (optional).
6. Click **Preview Data**.
   The columns and data types appear in the main window. You can re-assign the data types, remove columns, and add columns before importing the data set.
7. Click **Upload Data**.
   The platform loads the data set. You can monitor the job status by clicking the Jobs icon in the top-right corner of the platform.
   
   When the job finishes, the data is available as a feature set under the Analyze Feature Sets tab.
   
## Adding from a Data Connection
1. Choose a folder to store the data set.
2. Enter the name of the new data set in the **Data Set Name*** text box.
3. Choose **Internal DB** from the **Select Connection*** drop-down.
4. Choose to enter either a custom query or a table name in the **Table or Query*** drop-down.
   - **Custom Query** &mdash; Enter query code for the data connection.
   - **Select Table Name** &mdash; Choose a table from the **Table*** drop-down.
5. Add a description (optional).
6. Click **Add Data**.
   The platform loads the data set. You can monitor the job status by clicking the Jobs icon in the top-right corner of the platform.
   
   When the job finishes, the data is available as a feature set under the Analyze Feature Sets tab.
   
## Adding a Local File
1. Choose a folder to store the data set.
2. For **Data Set Name\***, do one of the following:
   - **New Data Set** &mdash; Enter a name for the new data set.
   - **Select Existing Data Set** &mdash; Choose a data set from the drop-down and specify whether you want to **Replace/Add new** or **Append Existing**.
3. Click the **Choose File** button and navigate to the data source file.
4. Enter the separator in the **Separator*** text box.
5. Add a description (optional).
6. Click **Preview Data**.
   The columns and data types appear in the main window. You can re-assign the data types, remove columns, and add columns before importing the data set.
7. Click **Add Data**.
   The platform loads the data set. You can monitor the job status by clicking the Jobs icon in the top-right corner of the platform.
   
   When the job finishes, the data is available as a feature set under the Analyze Feature Sets tab.
## Related Topics
[Creating a Single Data Set from Multiple Data Sets](single_from_multiple.md)

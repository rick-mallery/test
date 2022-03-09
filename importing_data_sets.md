# Importing Data Sets from Data Sources

You can import a data set from any major public crowd, local files, or tables/queries from existing data sets.

1. Open the platform to the Transfer Data tab.
2. In the Input Type drop-down, choose one of the following options:
   - **Add file from URL** &mdash; Enter a URL (https:// or file:///) as the data source.
   - **Add from data connection** &mdash; Enter the name of an existing data set as the data source. 
   - **Add from local file** &mdash; Choose a file from a file browser. 
3. The options differ depending on which input type you select. Jump to the relevant section below.

After running one of the following procedures, the data set is available as a feature set under the Analyze Feature Sets tab.

## Adding a File from a URL
1. Choose a folder to store the data set.
2. For **Data Set Name\***, do one of the following:
   - **New Data Set** &mdash; Enter a name for the new data set.
   - **Select Existing Data Set** &mdash; Choose a data set from the drop-down and specify whether you want to **Replace/Add new** or **Append Existing**.
3. Enter the URL in the **Source URL*** text box.
4. Enter the separator in the **Separator*** text box.
5. Optionally, you can add a description.
6. Click **Preview Data**.
   The columns and data types appear in the main window. You can re-assign the data types, remove columns, and add columns before importing the data set.
7. Click **Upload Data**.
   The platform loads the data set. You can monitor the job status by clicking the Jobs icon in the top-right corner of the platform.
   
## Adding from a Data Connection
1. Choose a folder to store the data set.
2. Enter the name of the new data set in the **Data Set Name*** text box.
3. Choose **Internal DB** from the **Select Connection*** drop-down.
4. Choose to enter either a custom query or a table name in the **Table or Query*** drop-down.
   - **Custom Query** &mdash; Enter query code for the data connection.
   - **Select Table Name** &mdash; Choose a table from the **Table*** drop-down.
5. Click **Add Data**.
   
## Adding a Local File
1. Choose a folder to store the data set.
2. For **Data Set Name\***, do one of the following:
   - **New Data Set** &mdash; Enter a name for the new data set.
   - **Select Existing Data Set** &mdash; Choose a data set from the drop-down and specify whether you want to **Replace/Add new** or **Append Existing**.
3. Click the **Choose File** button and navigate to the data source file.
4. Enter the separator in the **Separator*** text box.
5. Optionally, you can add a description.
6. Click **Preview Data**.
   The columns and data types appear in the main window. You can re-assign the data types, remove columns, and add columns before importing the data set.
7. Click **Add Data**.
   The platform loads the data set. You can monitor the job status by clicking the Jobs icon in the top-right corner of the platform.


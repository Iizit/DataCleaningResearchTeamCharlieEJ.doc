# DataCleaningResearchTeamCharlieEJ.doc
This Python script preprocesses a large CSV file containing user data from Lifebear.com. 

It performs the following tasks:

Splits the Large File:
The script splits the original CSV file (assumed to be located at /content/3.6M-Japan-lifebear.com-Largest-Notebook-App-UsersDB-csv-2019.csv) into smaller, more manageable chunks. Each chunk contains a specified number of rows (chunk_size) defined in the script.

Data Cleaning:
Duplicate Removal: It removes duplicate rows based on all columns to ensure data integrity.
Missing Values: It checks for missing values in each column and reports them.
Column Renaming: It converts column names to title case (first letter uppercase) for improved readability.
Email Validation (Optional): It includes an optional function is_valid_email that can be used to identify invalid email addresses in the Email Address column (if it exists). Invalid emails can be saved to a separate CSV file in a dump folder.
Merging Chunks: Finally, the script merges the individual chunks back into a single, clean DataFrame and saves it as a new CSV file named "merge life bear clean data.csv".


Prerequisites:

Python 3.x
pandas library (pip install pandas)
os library (included in Python standard library)
re library (included in Python standard library)

How to Use:

Save the Script: Save the script as a Python file (e.g., lifebear_preprocess.py).
Set File Paths: Ensure the file paths in the script are correct for your data and desired output locations.
file_path: Path to the original large CSV file.
chunk_size: Number of rows per chunk (adjust based on your system resources).
output_directory: Directory to store the split chunks.
output_file_name: Name of the final merged clean data CSV file.
Run the Script: Execute the script from your terminal using python lifebear_preprocess.py.

Output:

The script will create a directory named output_directory (e.g., /content/chunks) containing the split CSV chunks.
If enabled, it will create a directory named dump (e.g., /content/dump) containing a CSV file with invalid email addresses (if any).
Finally, it will save the merged cleaned data as "merge life bear clean data.csv" in the specified location.
Additional Notes:

This script utilizes the pandas library for efficient data manipulation.
Consider adjusting the chunk_size based on your system's available memory to avoid resource limitations.
The email validation functionality is optional and can be enabled/disabled by commenting out the relevant code sections.








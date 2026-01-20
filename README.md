Python Web-Scraper for Academic Publications
Description
This project is a Python-based web scraper that utilizes the CrossRef API to search for academic publications. It is specifically configured to retrieve metadata related to STEM Curriculum, AI in Teaching, Human-AI Interaction, and Blockchain in Education.


The scraper extracts key information—including titles, authors, publication years, and abstracts—and processes them in batches using pagination. The final data is exported into an Excel file for easy manipulation.




Features
Multi-Category Search: Specifically tuned for STEM, AIEd, and Blockchain keywords.

Date Filtering: Automatically filters for publications between 2020 and 2025.


Pagination Support: Handles large result sets by retrieving data in batches.


Excel Export: Saves metadata (Title, Authors, Link, Abstract, Year) into a .xlsx file.



Error Handling: Includes checks for API response status and empty results.

Installation
To use the scraper, you must have Python installed along with the following libraries:


requests: For handling API requests to CrossRef.


pandas: For data organization and Excel export.

openpyxl: Required by pandas to write Excel files.

Install command:

Bash

pip install requests pandas openpyxl


How to Use the Web Scraper

Prepare the Script: Download the Python script or open the code in Google Colab or a Jupyter Notebook.

Run the Code: Execute the cells or the script. The program will initialize constants such as search terms and pagination limits.



Monitor Progress: The console will display which category is currently being searched and how many results have been retrieved.

Download Results:


Local Machine: The file stem_ai_blockchain_results.xlsx will appear in the same folder as your script.



Google Colab: Click the Folder icon in the left sidebar to find and download the Excel file.

Code Functionality
The scraper follows a structured sequence:


Initialization: Constants are defined, including keyword groups and the year range (2020–2025).


Execution: The program sends requests to the CrossRef API using boolean logic (AND/OR) for precision.


Processing: It iterates through JSON responses to extract metadata like title, authors, and abstracts.


Saving: The data is stored in a pandas DataFrame and exported to stem_ai_blockchain_results.xlsx.

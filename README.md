# nosql-challenge
Module 12 Challenge

# UK Food Standards Agency Analysis

This project analyses the food hygiene ratings of various establishments across the United Kingdom, provided by the UK Food Standards Agency. The analysis is aimed to help journalists and food critics at the food magazine Eat Safe, Love decide where to focus future articles.

# Project Structure
This project consists of three main parts:

Database and Jupyter Notebook Setup
Database Update
Exploratory Analysis

# Part 1: Database and Jupyter Notebook Setup

Objective: Set up the MongoDB database and verify the data import and connection.
Steps:
Imported the data from establishments.json into MongoDB using the following command:

mongoimport --db uk_food --collection establishments --drop --file establishments.json

![Screenshot 2025-04-22 220109](https://github.com/user-attachments/assets/d75f5931-00a8-489e-a6a3-8b942fb55e38)

Imported necessary libraries (pymongo and pprint).

Created an instance of the MongoDB client and connected to the uk_food database.

Verified the existence of the uk_food database and establishments collection.

Displayed one document from the establishments collection using find_one() and pprint.

# Part 2: Database Update

Objective: Update the database based on specific requirements from the magazine editors.
Steps:
Added a new restaurant "Penang Flavours" in Greenwich to the establishments collection.
Queried the BusinessTypeID for "Restaurant/Cafe/Canteen" and updated the new restaurant with this ID.
Removed all documents from the establishments collection where the LocalAuthorityName is "Dover".
Converted latitude and longitude fields from strings to decimal numbers.
Converted RatingValue fields from strings to integers and set non-numeric values to null.

# Part 3: Exploratory Analysis

Objective: Answer specific questions to guide the magazine's content focus.
Questions and Results:
Which establishments have a hygiene score equal to 20?
Result: Found 41 establishments. Displayed the first result and converted the results to a Pandas DataFrame.
Which establishments in London have a RatingValue greater than or equal to 4?
Result: Found 33 establishments. Displayed the first result and converted the results to a Pandas DataFrame.
What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
Result: Found and displayed the top 5 establishments meeting the criteria. Converted the results to a Pandas DataFrame.
How many establishments in each Local Authority area have a hygiene score of 0?
Result: Aggregated the data and found the top 10 Local Authority areas with the highest count of establishments having a hygiene score of 0. Converted the results to a Pandas DataFrame.

# Results

The analysis provided insights into the hygiene scores and ratings of establishments in various regions, highlighting areas of interest for future articles in the magazine.

![Screenshot 2025-04-22 222152](https://github.com/user-attachments/assets/f2025aa0-bbe9-48f1-b71a-7877b9466045)

Notebooks
NoSQL_setup.ipynb: Contains the setup and database update steps.

NoSQL_analysis_starter: Contains the exploratory analysis steps and results.

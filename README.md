# UK Food Standards Agency Establishment Ratings
This project involves working with the UK Food Standards Agency's establishment ratings data to analyze food establishments across the United Kingdom. You will perform various data manipulations, exploratory analysis, and database updates using MongoDB and Python, specifically through the use of the PyMongo library.

# Table of Contents

Part 1: Database and Jupyter Notebook Setup

Part 2: Update the Database

Part 3: Exploratory Analysis

# Part 1: Database and Jupyter Notebook Setup

Import the Data:

Using the provided establishments.json file, import the data into a MongoDB instance. The database will be named uk_food and the collection will be establishments.

# Part 2: Update the Database

In this part, you will make several updates to the database:

Add a New Establishment:
Add the new restaurant "Penang Flavours" to the establishments collection with the provided details.

Find and Update BusinessTypeID:
Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and update the newly added establishment with this ID.

Remove Dover Establishments:
Check how many establishments are located in Dover and remove them. Verify the number of documents before and after deletion:

Convert String Values to Numbers:
Update latitude, longitude, and RatingValue fields to their proper numerical types using update_many.


# Part 3: Exploratory Analysis

Answer the following questions using MongoDB aggregation and PyMongo:

Hygiene Score of 20:
Find all establishments with a hygiene score of 20 and display the first document.

Establishments in London with Rating >= 4:
Use $regex to filter establishments in London with a rating of 4 or higher.

Top 5 Establishments Near "Penang Flavours":
Use geospatial queries to find the top 5 establishments with a RatingValue of 5, sorted by the lowest hygiene score, near the "Penang Flavours" restaurant.

Hygiene Score of 0 in Local Authority Areas:
Aggregate establishments with a hygiene score of 0, grouped by LocalAuthorityName, and sort the results by the count.

# Data Files

establishments.json: The JSON file containing the data of establishments with food hygiene ratings. This file is used as the input for importing the data into MongoDB.

NoSQL_setup_starter.ipynb: A Jupyter notebook to set up and load the database.

NoSQL_analysis_starter.ipynb: A Jupyter notebook for exploratory analysis of the database.

# Libraries and Dependencies

PyMongo: Python driver for MongoDB.

pprint: Pretty printer for displaying documents in a readable format.

Pandas: For converting MongoDB query results into DataFrames and performing data manipulation.

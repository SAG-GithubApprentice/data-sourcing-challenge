# data-sourcing-challenge
Module 6 Challenge

# This Jupyter script retrieves movie reviews from The New York Times API, filters them based on specific criteria, and then extracts relevant information about the movies from The Movie Database (TMDB) API. Here's a summary of the code:

# Dependencies:

    Uses requests, time, dotenv, os, pandas, and json libraries.

# API Keys:

    Retrieves API keys for The New York Times (NYT) and TMDB from a secure location.

# NYT API Query:

    Constructs a query to the NYT API to search for movie reviews with "love" in the headline, published between specified dates.

# Data Retrieval Loop:

    Retrieves NYT reviews in batches of 10 articles per page, with a delay to stay within API limits.
    Stores retrieved reviews in a list.

# Data Processing:

    Converts the list of reviews to a Pandas DataFrame.
    Extracts the title from the "headline.main" column.
    Normalizes the "keywords" column.
    Converts the "keywords" column from a list to a string.

# TMDB API Query:

    Constructs queries to the TMDB API using movie titles extracted from NYT reviews.
    Retrieves movie details, including genres, languages, countries, etc.

# Data Storage:

    Stores TMDB results in a list and converts it to a Pandas DataFrame.
    Merges NYT and TMDB DataFrames based on the movie title.

# Data Cleaning:

    Removes list brackets and quotation marks from columns containing lists.
    Drops the "byline.person" column.
    Removes duplicate rows and resets the index.

# Data Export:

    Exports the final merged and cleaned DataFrame to a CSV file named "merged_data.csv" without the index.

# This script integrates information from NYT movie reviews and TMDB, providing a comprehensive dataset for further analysis.

# Acknowlegements:

    I would like to express my gratitude to the following sources that significantly contributed to the development of this project:

    Academic Instruction: I am grateful for the foundational knowledge and guidance received through academic instruction. The principles and skills acquired during formal education have provided the essential framework for approaching data analysis challenges

    DataCamp: The skills and techniques applied in this project were enhanced through the educational resources provided by DataCamp. The interactive courses and hands-on exercises played a crucial role in improving my data analysis and Python programming skills.

    Stack Overflow: The Stack Overflow community has been an invaluable resource throughout this project. Countless discussions and solutions on Stack Overflow have provided insights, problem-solving approaches, and best practices that were instrumental in overcoming challenges encountered during the development process.

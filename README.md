# Group_8_phase_2_project

# Project Overview

With the company’s strategic decision to enter the movie industry through the establishment of its own movie studio, our team has been assigned to conduct a data-driven exploration of the current film market. Using the datasets provided, we aim to analyze recent trends in the film industry to identify which types of films are performing best across various key performance indicators such as box office revenue, audience ratings, genre popularity, and critical acclaim.

The insights derived from this analysis will guide the decision-making process for the new studio, helping determine the best types of films to produce in order to maximize return on investment and market success. Ultimately, we aim to make strategic recommendations from these insights.

# Business Understanding

We aim to provide data-backed insights that will inform the company’s entry strategy into the movie industry. We believe this will ensure that the newly established movie studio invests in movie genres that have proven commercial and critical success.

By leveraging proven trends in the film industry, we can ensure that the company reduces the risks associated with new ventures and also position the newly establised studio for early success in a very competitive market.

# Objectives 
The main objectives for the study are:

1.**Quantify Movie Profitability** - Use financial data (production budgets and worldwide gross) to compute Return on Investment (ROI) and identify the most and least profitable films.

2.**Analyze Movie Ratings** - Explore ratings data to understand if and how factors such as runtime, publisher influence critical scores and genre correlate to movie ratings.

3.**Find blockbuster movies globally** - We aim to find movies that performed exceptionally not only domestically but also worldwide using the worldwide_gross data

4.**Investigate the runtime vs movie rating** - Find out whether the average runtime of a movie has any influence on the movie ratings.

# 1. Data Understanding
In this notebook, we explore multiple movie-related datasets to understand their structure and prepare them for further analysis. This includes data from **TMDb**, **The Numbers**, **Box Office Mojo**, and **Rotten Tomatoes**.

First we import the relevant python libraries and loading the datasets.
- `tmdb_movies`: Movies from The Movie Database (TMDb)
- `tn_movie_budgets`: Budget and revenue data from The Numbers
- `rt_reviews`: Movie reviews from Rotten Tomatoes
- `rt_movie_info`: Additional Rotten Tomatoes metadata

We explore each dataset using the imported libraries to get a glimpse of the columns present in each dataset as the shapes of the DataFrames present using methods such as; `.head()`, `.info()`, and `.tail()`.This gives us a brief understanding of what each dataset entails.
# 2. Data cleaning 
In order to perform calculations and visualizations thereafter we first prepare our raw data. We remove missing values. We drop irrelevant columns and merge some datasets with common columns to get a comprehensive view. This is the data cleaning process outlined in the following cells.
  - Cleaning Financial Figures - normalizing the data by removing currency symbols and commas, hence changing the data type to float for easier mathematical calculations.
  - Creating a ROI(Return On Investment) column by subracting production budget from worldwide gross then dividing by production budget. This helps us know which movies were profitable and those that were not.
  - Merging movie datasets - Combining the `tmdb_movies` and `tn_movie_budgets` datasets allows for more comprehensive analysis by utilizing the attributes from TMDb and the financial details from The Numbers.

# 3. Visualizations
  In order to observe trends and patterns from the datasets we construct various visualizations that will help to provide insights later on. We imported the various python libraries required for plotting.

  ## 📊  Top 10 Profitable Movies
  **Visualization of financial data using profit**
  Comparing worldwide gross with production budget to visualize the profit the movies made.

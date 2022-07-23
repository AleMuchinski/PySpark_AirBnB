# **Analysis of AirBnB Listing using PySpark**
In this project I investigate the AirBnB public database to collect findings of listings and prices in various cities around the world. Furthermore the repository uses Apache Spark functions for Python due to the volume of data available.

# Use Case

- Use Case Summary
- Objective Statement:
  * Get business insights about listing prices about short term rental in AirBnB.
  * Introduce how to handle big data using distributed computing for data processing.
  * Analyze customer reviews using sentiment analysis to understand what are the factors of satisfaction for a good stay.
  * Understand the bottlenecks through customer reviews and take action on which property types and regions are most affected by them.
  
- Challenges:
  * Large volume of data, not possible to process in traditional ways (spreedsheet, csv, etc...).
  * The prices of the stays vary a lot due to several factors (location, exclusivity, quality, reviews etc...).
  
- Methodology / Analytic Technique:
  * Descriptive analysis
  * Graph analysis
  * Sentiment analysis
  
- Business Benefit:
  * Highlight the important factors for maintaining the quality of service provided in the AirBnB application.

- Expected Outcome:
  * Understand which are the most expensive cities to rent a property in AirBnB.
  * Know what are the most rated terms for positive and negative reviews.
  * Which property types are most desired by users and which regions are the most cost-effective.
  
# Business Understanding

- Short term rental was a revolution in the so-called sharing economy in the silicon valley startup boom. Private landlords have the option to rent out their own properties to registered users on the AirBnB platform, so this project has some questions to answer using the data:
- Which neighborhoods have the highest listings in the most popular cities?
- What are the most expensive regions to rent an AirBnB?
- Which cities are the most cost-effective (average rating/average price of stay)?
- What are the busiest months in property listings?
- What are the most used criteria to evaluate a property on AirBnB?

# Data Understanding
- Data extracted using scraping from the Inside AirBnB website (http://insideairbnb.com/get-the-data/).
- The dataset has a 5.6GB size, containing 106 columns and +1 million rows.
- Data Dictionary (after cleaning):
- neighbourhood_cleansed: region inside of a city.
- property_type: type of building rented (house, apartment, villa etc..).
- city: location of the listing.
- price: daily price in local currency.
- review_scores_rating: Number from 1 to 5 about the listing.
- number_of_reviews: The number of reviews the listing has.
- id: unique ID in the database.

# Data preparation

- Code used:
- Python version 3.9.7
- Packages: Numpy, Pandas, Seaborn, Matplotlib, Puspark, ProfileReport, Pandasql

# Data Cleansing

- There are over 1 million rows in the database with 106 columns, to make the processing efficient, the number was reduced to 8 columns for the 15 cities with the most listings in the dataset.
- There are many properties with low numbers of reviews, so as not to harm the price distribution I filtered for properties that have more than 75 reviews, leading to the assumption that these are places that the owners rent constantly.
- To make the narrative intuitive, we chose a specific city (London) to evaluate the prices and availabilities by property type and neighborhood, thus making it clear what factors are important for a satisfying stay in the future using sentiment analysis.


# Recommendation
- With the massive amount of data it was possible to identify the cities with prioprieties where the users of the platform believe they have more and less benefits (Valencia and Amsterdam), so AirBnB should do a campaign to raise the quality of the listings, offering promotions or additional services to keep the recurrence of customers constant.
- With the sentiment analysis it was possible to locate the themes most used by users and cross-referencing by type and region of the property it will be possible to act precisely where the platform should evaluate the owners and provide measures that negative cases do not occur again.

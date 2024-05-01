# Project Name - AIRBNB NYC 2019 Room service Data Analysis
. Project Type-EDA
. Contribution - Individual

# Project Summary -

The "Airbnb NYC 2019 Data Analysis" project delves into a comprehensive exploration of the Airbnb dataset focusing on New York City listings throughout the year 2019. This dataset encapsulates a wealth of information encompassing various facets of Airbnb listings, including pricing dynamics, property attributes, geographical distribution, host demographics, and guest reviews. Through meticulous analysis, the project aims to unveil valuable insights into the Airbnb market landscape, facilitating a deeper understanding of the factors influencing listing prices, occupancy rates, and customer satisfaction.

Beginning with data acquisition, the project sources the Airbnb NYC 2019 dataset from reliable repositories or web scraping methodologies. Following this, a rigorous data preprocessing phase ensues, comprising tasks such as data cleaning, handling missing values, and feature engineering. This critical step ensures the dataset's integrity and sets the foundation for subsequent analyses.

The project then transitions into exploratory data analysis (EDA), employing statistical techniques and data visualization tools to uncover patterns, trends, and correlations within the dataset. EDA facilitates the identification of key variables and their interrelationships, providing valuable context for subsequent analytical endeavors.

The project culminates in the interpretation and dissemination of findings, wherein insights gleaned from the analysis are synthesized into actionable recommendations. Through compelling visualizations and comprehensive reports, stakeholders gain invaluable insights into the Airbnb market dynamics, empowering them to optimize listing strategies, enhance guest experiences, and capitalize on emerging opportunities.

# Problem Statement

The primary objective of this project is to leverage data-driven insights to address key challenges encountered by hosts and guests in the New York City Airbnb market. Specifically, the project aims to:

Understand Pricing Dynamics: Analyze factors influencing Airbnb listing prices, such as property attributes, location, seasonality, and host characteristics. By uncovering pricing patterns and trends, hosts can optimize their pricing strategies to maximize revenue while remaining competitive in the market.

Enhance Listing Performance: Identify features and amenities that correlate with higher occupancy rates, positive guest reviews, and overall customer satisfaction. Insights gained from this analysis can empower hosts to enhance their listings, cater to guest preferences, and differentiate themselves in a crowded marketplace.

Optimize Guest Experience: Explore guest sentiments and preferences through review analysis, identifying areas for improvement and opportunities to enhance the overall guest experience. By addressing pain points and exceeding guest expectations, hosts can cultivate positive reputations and drive repeat bookings.

Mitigate Regulatory Risks: Assess the regulatory landscape governing short-term rentals in New York City, including compliance with local laws and regulations. Understanding regulatory requirements is essential for hosts to operate within legal boundaries and mitigate risks associated with non-compliance.

# Define Your Business Objective?

By addressing these challenges, the project endeavors to empower both hosts and guests in the New York City Airbnb market, fostering a more transparent, efficient, and mutually beneficial ecosystem. Through actionable insights and strategic recommendations, stakeholders can navigate the complexities of the Airbnb marketplace with confidence, optimizing their experiences and unlocking the full potential of short-term rentals in the city that never sleeps

# General Guidelines : -

1. Well-structured, formatted, and commented code is required.
2. Exception Handling, Production Grade Code & Deployment Ready Code will be a plus. Those students will be awarded some additional credits. The additional credits will have advantages over other students during Star Student selection. [ Note: - Deployment Ready Code is defined as, the whole .ipynb notebook should be executable in one go without a single error logged. ]
3. Each and every logic should have proper comments.
4. You may add as many number of charts you want. Make Sure for each and every chart the following format should be answered.

# Chart visualization code
. Why did you pick the specific chart?
. What is/are the insight(s) found from the chart?
. Will the gained insights help creating a positive business impact? Are there any insights that lead to negative growth? Justify with specific reason.
. You have to create at least 20 logical & meaningful charts having important insights.

U - Univariate Analysis,

B - Bivariate Analysis (Numerical - Categorical, Numerical - Numerical, Categorical - Categorical)

M - Multivariate Analysis ]

# Import libaray 

import pandas as pd

import numpy as np

import seaborn as sns

import matplotlib.pyplot as plt

from datetime import datetime,date

# Dataset Loading
. Dataset name is AIRBNB 2019 

. Find the First 5 rows and all columns data using Head method 

. Find the last 5 rows and all columns data using tail method

. Find the any 5 rows and all columns data using sample method
. Find the data set row and columns 
. Drop the columns last_reviews and reviews_per_month Because this is not required. all ready review columns are available

# What did you know about your dataset?

. The dataset given is a dataset from Hotel industry, and we have to analysis the Airbnb ync 2019 of customers and the insights behind it.

. Airbnb ync 2019 prediction is analytical studies on the possibility of a customer abandoning a product or service. The goal is to understand and take steps to change it before the costumer gives up the product or service.

. The above dataset has 48895 rows and 14 columns. There are no mising values and duplicate values in the dataset.

# Variables Description

Variables Description Index_count : Total number of Airbnb ync 2019 data 48895 and 14 columns

host_id_Mean_or_AVG :6.70

price_Mean_or_AVG :153

Night_Mean_or_AVG : 7

N_Review_Mean_or_AVG : 23

Availablity_Mean_or_AVG : 112

Host_listing_count_Mean_or_AVG : 7

host_id_STD :7.8

price_STD :240

Night_Std :20

N_Review_STD : 44

Availablity_STD : 32

Host_listing_count_STD : 131

host_id_Min :2.4

price_Min :0

Night_Min : 1

N_Review_Min : 0

Availablity_Min : 0

Host_listing_count_Min : 1

host_id_Max :2.4

price_Max :100000

Night_Max : 1250

N_Review_Max : 629

Availablity_Max : 365

Host_listing_count_Max :327

host_id_25% :7.8

price_25% :69

Night_25% : 1

N_Review_25% : 1

Availablity_25% : 1

Host_listing_count_25% : 0

host_id_50% :3.07

price_50% :106

Night_50% : 3

N_Review_50% : 5

Availablity_50% : 45

Host_listing_50% : 1

host_id_75% :1.07

price_75% :175

Night_75% : 5

N_Review_75% : 24

Availablity_75% : 227

Host_listing_count_75% : 2

# Check Unique Values for each variable.

Unique values for variable 'id' : 48895

Unique values for variable 'name' : 47905

Unique values for variable 'host_id' : 37457

Unique values for variable 'host_name' : 11452

Unique values for variable 'neighbourhood_group' : 5

Unique values for variable 'neighbourhood' : 221

Unique values for variable 'latitude' : 19048

Unique values for variable 'longitude' : 14718

Unique values for variable 'room_type' : 3

Unique values for variable 'price' : 674

Unique values for variable 'minimum_nights' : 109

Unique values for variable 'number_of_reviews' : 394

Unique values for variable 'calculated_host_listings_count' : 47

Unique values for variable 'availability_365' : 366

# Total number State wise data

Manhattan 21661

Brooklyn 20104

Queens 5666

Bronx 1091

Staten Island 373

# Total number of city in the state ( Bie-Variant Analysis)

Bronx 1091

Brooklyn 20104

Manhattan 21661

Queens 5666

Staten Island 373

# Room Type

Entire home room : 25409

Private room : 22326

shared room : 1160

# which types of room Price 0

there are 11 rooms price is 0

Private room : 7

Entire home/apt : 2

Shared room : 2

. maximun rooms Price are 10000

# which types of room Price 10000

. There are 3 rooms price are 10k One Private room and Two Entire Home room

Entire home/apt : 2

Private room : 1

. median room price 106

# find the average Reviews of rooms type

Entire home/apt 22.84

Private room 24.11

Shared room 16.60

# Which room type maximum rooms reviews getting

name : Room near JFK Queen Bed

host_id : 47621202

host_name : Dona

neighbourhood_group : Queens

neighbourhood : Jamaica

latitude : 40.6673

longitude : -73.76831

room_type : Private room

price : 47

minimum_nights : 1

number_of_reviews : 629

calculated_host_listings_count : 2

availability_365 : 333

# Data Vizualization, Storytelling & Experimenting with charts : Understand the relationships between variables

. There 16 plot have created Using Below rule.

U - Univariate Analysis,

B - Bivariate Analysis (Numerical - Categorical, Numerical - Numerical, Categorical - Categorical)

M - Multivariate Analysis 

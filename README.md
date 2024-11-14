BG-NBD & Gamma-Gamma CLTV Prediction

Business Problem
FLO aims to establish a roadmap for their sales and marketing strategies. To help in medium-to-long-term planning, it is essential to predict the potential future value that existing customers will bring to the company.

Dataset Story
This dataset contains information on customers who made their last purchases between 2020 and 2021 across OmniChannel platforms (both online and offline). The columns in the dataset include:

master_id: Unique customer identifier
order_channel: The platform used for purchases (Android, iOS, Desktop, Mobile, Offline)
last_order_channel: The platform used for the last purchase
first_order_date: Date of the customer’s first purchase
last_order_date: Date of the customer’s last purchase
last_order_date_online: Date of the last online purchase
last_order_date_offline: Date of the last offline purchase
order_num_total_ever_online: Total number of online orders
order_num_total_ever_offline: Total number of offline orders
customer_value_total_ever_offline: Total amount spent offline
customer_value_total_ever_online: Total amount spent online
interested_in_categories_12: List of categories in which the customer has made purchases over the past 12 months

Objectives

1-Data Preparation
Load and preprocess the data.
Handle outliers using the outlier_thresholds and replace_with_thresholds functions.
Calculate the total number of purchases and total amount spent for both online and offline channels.
Convert date-related columns into datetime format for analysis.

2-CLTV Data Structure
Calculate Recency as the time since the last purchase.
Define Tenure as the time from the first purchase to the analysis date.
Compute Frequency (total purchases) and Monetary (average spend per transaction).

3-BG-NBD & Gamma-Gamma Model
Fit the BG-NBD model to predict future sales.
Predict expected sales for the next 3 and 6 months.
Fit the Gamma-Gamma model to estimate the average value of transactions.
Calculate the 6-month CLTV using the models.

4-CLTV Segmentation
Segment customers into four groups based on their standardized CLTV values (A, B, C, D).
Provide recommendations for actions based on the CLTV segments.

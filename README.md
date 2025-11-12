**Project Overview:**

This project analyses transactional data (3,900 purchases across various product categories) to understand customer shopping behaviour, identify distinct customer segments (e.g., frequent purchasers, high-spenders, discount users), explore product preferences and subscription behaviour, and translate the insights into strategic business recommendations for growth.

**Dataset**

Description:

3,900 transaction records with 18 features, including:

Customer demographics: age, gender, location, subscription status

Purchase details: item purchased, category, purchase amount, season, size, colour

Shopping behaviour attributes: discount applied, previous purchases, purchase frequency, review rating (37 missing values), shipping type

Missing values: 37 missing entries in the review_rating column

Data cleaning performed: imputed missing review_rating values with the median rating within each product category.

**Tools & Technologies**

Python (Pandas, NumPy, Matplotlib/Seaborn for exploratory data analysis)

SQL (MySQL) – for querying the transaction database and answering business-questions

Power BI – for building an interactive dashboard with filters and visuals for non-technical stakeholders

Additional tools: Jupyter Notebook, database connector (e.g., sqlalchemy or mysql-connector), GitHub for version control

**Data Loading & Initial Inspection**

Loaded CSV/transaction data into a Pandas DataFrame.

Used df.info(), df.describe(), df.head() to inspect data structure, types and summary statistics.

**Data Cleaning & Feature Engineering**

Impute missing review_rating values with median per category.

**Standardized column names to snake_case.**

Created derived features:

age_group (e.g., 18-25, 26-35, etc) by binning age.

purchase_frequency_days = days since previous purchase / frequency measure.

Checkd for redundancy: dropped promo_code_used since it is overlaping with discount_applied.

**customer behaviour Analysis using MYSQL**

Uploaded cleaned/enriched DataFrame into MySQL database through jupyter norebook.

Ran SQL queries to answer business questions such as:

Revenue by gender

Customers who used discount yet spent above average

Top 5 products by average rating

Average purchase amount by shipping type (Standard vs Express)

Subscriber vs non-subscriber spend and revenue

Repeat buyers (>5 purchases) and subscription likelihood

Revenue by age group

**Dashboard Development in Power BI**

Connected to the database for the required tables.

created the cards for showing the Total revenue generated, total customers,average rating across all age groups,revenue by subscription

Build visuals: % of customers by susbscription status,total spend, average spend by segment, purchase frequency, heatmaps for category vs spend, discount vs spend breakdown, subscriber vs non-subscriber comparison.

Add interactive filters: category, age_group, subscription_status, shipping_type, gender.

Enable stakeholder exploration:filters, slicers, dynamic visuals.

**Business Recommendations**

**Boost Subscriptions:**
Target frequent purchasers among non-subscribers with incentives or loyalty benefits.

**Enhance Low-Performing Categories:**
Introduce combo offers or seasonal discounts for Footwear and Outerwear to increase category diversity.

**Segmented Marketing:**
Focus campaigns on Young Adults and Middle-Aged groups who show the highest revenue contribution.

**Product Strategy:**
Continue prioritising Clothing (core revenue driver) but evaluate pricing strategy in Accessories to optimise margin.

**Customer Experience:**
Improve product ratings through quality checks and post-purchase feedback to raise the average rating above 4.0.

**Shipping Optimization:**
Analyse cost vs. usage for each shipping type to streamline logistics and improve customer satisfaction.

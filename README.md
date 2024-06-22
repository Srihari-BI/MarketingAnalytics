# MarketingAnalytics
Schema:

1. Campaigns Table
campaign_id: INT (Primary Key)
campaign_name: VARCHAR(100)
start_date: DATE
end_date: DATE
budget: DECIMAL(10, 2)
status: VARCHAR(50)

2. Customers Table
customer_id: INT (Primary Key)
first_name: VARCHAR(50)
last_name: VARCHAR(50)
email: VARCHAR(100)
phone: VARCHAR(20)
birthdate: DATE
registration_date: DATE
city: VARCHAR(100)
state: VARCHAR(50)
country: VARCHAR(50)

3. Interactions Table
interaction_id: INT (Primary Key)
customer_id: INT (Foreign Key referencing Customers.customer_id)
campaign_id: INT (Foreign Key referencing Campaigns.campaign_id)
interaction_date: TIMESTAMP
interaction_type: VARCHAR(50)
interaction_details: TEXT

4. Campaign Performance Table
performance_id: INT (Primary Key)
campaign_id: INT (Foreign Key referencing Campaigns.campaign_id)
impressions: INT
clicks: INT
conversions: INT
revenue: DECIMAL(10, 2)

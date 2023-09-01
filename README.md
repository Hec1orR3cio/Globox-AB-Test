# Globox-AB-Test

## Tables:

- Table 1 extracts curated data for analysis
- Table 2 tracks key metrics (conversion rate and Average Revenue per Customer (ARPU) over time

## Database access:

postgres://Test:bQNxVzJL4g6u@ep-noisy-flower-846766-pooler.us-east-2.aws.neon.tech/Globox

## ERD
![Alt text](ERD.png "ERD")

## Fields description:

**users:** user demographic information
 - id: the user ID
 - country: ISO 3166 alpha-3 country code
 - gender: the user's gender (M = male, F = female, O = other)

**groups:** user A/B test group assignment
 - uid: the user ID
 - group: the user’s test group
 - join_dt: the date the user joined the test (visited the page)
 - device: the device the user visited the page on (I = iOS, A = android)

**activity:** user purchase activity, containing 1 row per day that a user made a purchase
 - uid: the user ID
 - dt: date of purchase activity
 - device: the device type the user purchased on (I = iOS, A = android)
 - spent: the purchase amount in USD


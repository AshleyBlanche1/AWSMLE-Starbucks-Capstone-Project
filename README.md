# AWS Machine Learning Engineer Starbucks® Capstone Project #
## AWS ML Engineer Starbucks® Capstone Project ##
## Background ##
This is the final project of the Udacity Machine Learning Engineer Nanodegree Program.

Starbucks® was founded in 1971 in Seattle, Washington, by three partners: Jerry Baldwin, Zev Siegl, and Gordon Bowker where initially high-quality coffee beans and equipment were sold rather than brewed coffee. In 1982, Howard Schultz joined the company and, inspired by Italian coffeehouses, transformed Starbucks® into a coffeehouse chain serving espresso-based drinks. Schultz acquired the company in 1987, expanding rapidly beyond Seattle, including international markets. Starbucks went public in 1992, fuelling further growth and innovation, e.g. the Frappuccino and in-store Wi-Fi and mobile apps. Today, Starbucks operates over 30,000 stores worldwide, known for its premium coffee, commitment to sustainability, and continuous innovation.
The Starbucks® mobile app enhances customer convenience by allowing users to place orders in advance, make payments, and customise their drinks. Integrated with the Starbucks Rewards program, the app lets users earn and redeem stars for free items. It also features a store locator, provides menu and nutritional information, and offers personalised promotions. Once every few days, Starbucks® sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

## Project Overview ##

The goal is to determine which offer should be sent based off of previous responses provided to previous offers. Not every single user receives the same offers. To resolve this problem, the data provided by Starbucks® i.e. the json files will be utilised and I will then construct a machine learning model in order to provide predicts to the responses for customer offerings.

## Datasets and Inputs ##

The data for the Starbuck’s challenge is contained in three files:
portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.) profile.json - demographic data for each customer
transcript.json - records for transactions, offers received, offers viewed, and offers completed Here is the schema and explanation of each variable in the files:

**portfolio.json**

id (string) - offer id
offer_type (string) - type of offer ie BOGO, discount, informational difficulty (int) - minimum required spend to complete an offer reward (int) - reward given for completing an offer
duration (int) - time for offer to be open, in days
channels (list of strings)
The portfolio.json dataset does contain columns such as the ‘offer_type’ column that describes the following offers which Starbuck’s may send to customers:
1. BOGO - When an additional same, free item is provided at no additional cost. There is a threshold spend to unlock reward.
2. Discount – Percentage off of Starbuck items/products.
3. Information – Details on Starbuck products.

**profile.json**

age (int) - age of the customer
became_member_on (int) - date when customer created an app account
gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
id (str) - customer id
income (float) - customer's income
transcript.json
event (str) - record description (ie transaction, offer received, offer viewed, etc.)
person (str) - customer id
time (int) - time in hours since start of test. The data begins at time t=0
value - (dict of strings) - either an offer id or transaction amount depending on the record

**transcript.json**

event (str) - record description (ie transaction, offer received, offer viewed, etc.)
person (str) - customer id
time (int) - time in hours since start of test. The data begins at time t=0
value - (dict of strings) - either an offer id or transaction amount depending on the record

## Acknowledgements ##

This project was completed as part of the Udacity Machine Learning Engineer Nanodegree. 

The dataset as part of this project, simulates customer behavior on the Starbucks® Rewards app: Starbucks® Coffee Company.

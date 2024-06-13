Business Case Scenario

 

Time Warp: 

In this business case, we will need to do a bit of a time warp.  We are turning the clock back to pretend like today is the morning of October 4, 2020, and we received a data feed from a 3rd party sales channel for October 3, 2020.   As part of your analysis, you may want to look at existing data in the database, which covers all of 2020.  Although it conflicts with the time warp, it's fine to use data past October 4, 2020 in your analysis. 

 

Scenario:

Assume you are a data engineer working closely with the data science team at Acme Gourmet Meals (AGM).

AGM executives are considering adding a delivery option, with the hopes of increasing sales, growing the customer base, and increasing profitability.   

Management decided to do a proof of concept (POC) in the form of a three month trial run using one delivery service at the Berkeley store.    They have called upon the data science team to help with this effort.  In turn, the data science team has asked for your help in the data engineering aspects of the POC.

Management chose Peak Deliveries primarily because it's a newer operation with a model that takes a percentage cut of the product pricing instead of charging customers a delivery fee.  Peak's cut is 18 %. So, for each $ 12 meal, approximately $2.16. Customers may tip the delivery driver if they wish. AGM is not given any visibility into customer tips.  (Peak is protecting its data on good tippers.)  Peak has an outstanding reputation for great, fast, and efficient deliveries, with excellent customer service.  Peak will only deliver to zip codes within a 5 mile radius of the store.

Integration with any third party sales channel always comes with its challenges.  For large companies, like McDonalds, the delivery companies are willing to integrate and modify their computer systems as needed to get the contract.  For small companies, like AGM, our only option is to use Peak's API to send and receive data.  However, that would require us to write a lot of code, which management does not want to spend money on until the POC has proven successful. Peak can provide us with a JSON file at the end of each day with detailed sales information for that day.  Management has decided to go with the daily JSON option for now for the POC. 

For products, AGM will enter products into Peak's system.  Peak will assign an ID in their system to the product.  We will need to create a mapping table to map Peak's IDs to AGM's IDs.  In AGM's case all products cost $12 and are tax exempt.  AGM will mark them as exempt from sales tax.

Regarding the customer list, AGM does not want to give out their full customer list to third parties.  Customers will have to sign up with Peak, either using the website, the app, or by telephone.  Our executives anticipate and understand that the trade off to not giving them our customer list is that we will probably have to validate and/or cleanse the customer data.  Peak will assign their customer ID to each customer.

Regarding the store list.  In this POC we will only have 1 store and it will be the Berkeley store. Peak will create a pickup location for the store and assign their own location ID to it.  Even though all data will have the same store for now, we still want to receive it and process it so we can plan for possible future expansion to other stores and/or pickup locations.

Assume today is the day is October 4, 2020.   The first day of sales was October 3, 2020.  The JSON file came in very early this morning.  As a data engineer you need to get started with parsing, staging, validating, etc. the file as soon as possible.  

The executives are anxious to understand how good the data is, if we will be able to continue withholding the customer data from Peak, and to get some preliminary analytics.  Even thought it's just one day's worth of data, the executives want as much information as soon as they can get it (which is very typical).

The data science team has met with you, and together you came up with a plan to get the data loaded and validated, explore the customer data, and perform some preliminary analytics.   The data science team has been requested to give the executives an assessment of the customer data and whether or not they should continue to withhold customer data from Peak.  Since you are going to be the first one to have an extensive look at the data, the data science team wants and values your opinion on the customer data.

Here are the details of the plan you have come up with:

In part 2.1, you will be creating and loading the product mapping table (objective)

In part 2.2, you will be parsing Peak's sales JSON files into CSV files (objective)

In part 2.3, you will create and load staging tables (objective)

In part 2.4, you will validate data in the staging tables using SQL (objective)

In part 2.5, you will run SQL queries to explore cleansing of the customer data (objective)

In part 2.6, you will perform some preliminary analytics on data in the staging tables to answer specific questions from executives (objective)

In part 2.7, you will write an analysis on continuing to withhold customer data from 3rd party sales channels (subjective)

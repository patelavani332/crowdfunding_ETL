# crowdfunding_ETL

## Overview
For this project, an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions is built to extract and transform the data. After transforming the data, four CSV files and created and using the CSV file data an ERD and a table schema is created. Then the CSV file data is uploaded into a Postgres database.

Here, SQL querries were performed on a crowdfunding data.

## Resources
* PgAdmin 4 / MySQL 

* Jupyter Notebook / Python

* QuickDBD

## Summary

Using above resources:
* Extracted and transformed data from the crowdfunding Excel data file to clean CSV files.
* Created a PostgresSQL database and table schemas using an ERD
* Loaded CSV files into that database
* Ran queries to retrieve the data

## Extracting and Transforming the data

### Extracted and transformed the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:

A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories

A "category" column that contains only the category titles

The following image shows this category DataFrame:
![cat](https://user-images.githubusercontent.com/120197958/227374365-ebd41ed6-06ce-46ef-ae6a-82c55adcfcbf.png)

### Extracted and transformed the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:

A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories

A "subcategory" column that contains only the subcategory titles

The following image shows this subcategory DataFrame:
![subcat](https://user-images.githubusercontent.com/120197958/227374396-5543cf9c-5d65-4940-ab98-0c6484b0b9a1.png)

### Extracted and transformed the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:

The "cf_id" column

The "contact_id" column

The "company_name" column

The "blurb" column, renamed to "description"

The "goal" column, converted to the float data type

The "pledged" column, converted to the float data type

The "outcome" column

The "backers_count" column

The "country" column

The "currency" column

The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format

The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format

The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame

The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

The following image shows this campaign DataFrame:

![df](https://user-images.githubusercontent.com/120197958/227375388-d8189685-f5a6-439c-a9d7-56fb051440a8.png)


## Creating the contacts dataframe

#### Previous data:

![before1](https://user-images.githubusercontent.com/120197958/227373315-ce16be40-1a17-4197-98e3-933cfcebb4f9.png)

#### Cleaned data:

![after](https://user-images.githubusercontent.com/120197958/227372782-0ba9f37e-b41e-4105-8d55-ad3234c0393b.png)

## Creating the crowdfunding database

Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBD.

From the ERD a table schema for each CSV file is created.

![ERD - crowdfunding](https://user-images.githubusercontent.com/120197958/227365779-5d29a0f5-f2c6-4fb6-be52-1b9b52db81a4.png)






 

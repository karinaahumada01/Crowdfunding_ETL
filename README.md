# Crowdfunding_ETL

## Overview

This project demonstrates the creation of an ETL (Extract, Transform, Load) pipeline using Python, Pandas, and regular expressions or dictionary methods. The goal is to extract data from multiple sources, transform it into appropriate formats, and load it into a PostgreSQL database. The pipeline includes the generation of several datasets as CSV files, an Entity Relationship Diagram (ERD), and the construction of a database schema.

## Objective

- Extract data from given datasets (CSV and Excel files).
- Transform the data to align with project requirements by cleaning, formatting, and restructuring.
- Load the transformed data into a PostgreSQL database with proper schema design and relationships between tables.

## Project Structure

### Files in Repository

#### All .xlsx files come from project files, while all .csv files are a product of the jupyter notebook for the main analysis

- ETL_Mini_Project_CPond_LMatos_KAhumada.ipynb: main jupyter notebook analysis file that produces all .csv files for each dataframe

- category.csv: Contains unique category information with category_id and category name columns.

- subcategory.csv: Stores subcategory details with subcategory_id and subcategory name columns.

- campaign.csv: A comprehensive dataset on crowdfunding campaigns with relevant metadata such as campaign ID, goal, outcome, and launch and end dates.

- contacts.csv: Contains contact information, including first name, last name, and email.

- contacts.xlsx: Original Excel version of the contact data.

- crowdfunding.xlsx: Raw data source containing campaign and category information.

## Key DataFrames and Transformations

### Category DataFrame:

- Includes category_id (e.g., cat1, cat2...) and category name columns.
- Exported as category.csv.

### Subcategory DataFrame:

- Contains subcategory_id (e.g., subcat1, subcat2...) and subcategory name columns.
- Exported as subcategory.csv.

### Campaign DataFrame:

- Contains detailed information on campaigns such as campaign ID, contact ID, company name, goal, pledged amount, outcome, launch/end dates, and corresponding category and subcategory IDs.
- Exported as campaign.csv.

### Contacts DataFrame:

- Stores contact information (ID, first name, last name, email).
- Exported as contacts.csv.

### Database Schema

- Database Name: crowdfunding_db
- Schema File: crowdfunding_db_schema.sql

### Tables and Relationships:

- Categories and Subcategories have unique IDs, referenced by the Campaigns table.
- Campaigns link to contacts using the contact_id as a foreign key.
- Primary keys, foreign keys, and relationships ensure data integrity.

## How to Run the Project

### Data Preparation:

- Use Python and Pandas to clean and transform the raw data into the required format.
- Ensure proper ID mapping across DataFrames for category_id and subcategory_id.

### Database Setup:

- Create the PostgreSQL database using the schema defined in crowdfunding_db_schema.sql.
- Import the CSV files into their respective tables.

### Verification:

- Query the tables using SELECT * to validate the data load.

##References

ChatGPT was used for README outline and format, and troubleshooting errors for this project assignment.

- OpenAI. (October, 2024). ChatGPT (GPT-4) [Large language model]. https://chat.openai.com/

Xpert Learning Assistant was used for troubleshooting errors for this project assignment.

- Xpert Learning Assistant. (2024). Retrieved from https://bootcampspot.instructure.com/

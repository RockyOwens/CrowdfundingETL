--Project 2--

For the ETL mini project, you will work with a partner to practice building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After you transform the data, you'll create four CSV files and use the CSV file data to create an ERD and a table schema. Finally, you’ll upload the CSV file data into a Postgres database.

--Before You Begin--

1. Create a new repository, named Crowdfunding_ETL, for this project. Do not add this homework to an existing repository.

2. Clone the new repository to your computer.

3. Rename the ETL_Mini_Project_Starter_Code.ipynb file with your first name initial and last name, for example, ETL_Mini_Project_NRomanoff.ipynb. Then, add this Jupyter notebook file and the Resources folder containing the crowdfunding.xlsx and the contacts.xlsx files to your repository.

4. Push the changes to GitHub

--Instructions--

The instructions for this mini project are divided into the following subsections:

Create the Category and Subcategory DataFrames
Create the Campaign DataFrame
Create the Contacts DataFrame
Create the Crowdfunding Database

--Create the Category and Subcategory DataFrames--

1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:

A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories

A "category" column that contains only the category titles

2. Export the category DataFrame as category.csv and save it to your GitHub repository.

3. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:

A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories

A "subcategory" column that contains only the subcategory titles

4. Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

--Create the Campaign DataFrame--

Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:

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

2. Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

--Create the Contacts DataFrame--

1. Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:

Option 1: Use Python dictionary methods.

Option 2: Use regular expressions.

2. If you chose Option 1, complete the following steps:

Import the contacts.xlsx file into a DataFrame.

Iterate through the DataFrame, converting each row to a dictionary.

Iterate through each dictionary, doing the following:

Extract the dictionary values from the keys by using a Python list comprehension.

Add the values for each row to a new list.

Create a new DataFrame that contains the extracted data.

Split each "name" column value into a first and last name, and place each in a new column.

Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

3. If you chose Option 2, complete the following steps:

Import the contacts.xlsx file into a DataFrame.

Extract the "contact_id", "name", and "email" columns by using regular expressions.

Create a new DataFrame with the extracted data.

Convert the "contact_id" column to the integer type.

Split each "name" column value into a first and a last name, and place each in a new column.

Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.

--Create the Crowdfunding Database--

1. Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBDLinks to an external site..

2. Use the information from the ERD to create a table schema for each CSV file.

Note: Remember to specify the data types, primary keys, foreign keys, and other constraints.

3. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.

4. Create a new Postgres database, named crowdfunding_db.

5. Using the database schema, create the tables in the correct order to handle the foreign keys.

6. Verify the table creation by running a SELECT statement for each table.

7. Import each CSV file into its corresponding SQL table.

8. Verify that each table has the correct data by running a SELECT statement for each.

--Requirements--

A Category DataFrame is Created (15 points)

The DataFrame contains a "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories (5 points)

The DataFrame has a "category" column that contains only the category titles (5 points)

The category DataFrame is exported as category.csv (5 points)

A Subcategory DataFrame is Created (15 points)

The DataFrame contains a "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories (5 points)

The DataFrame contains a "subcategory" column that contains only the subcategory titles (5 points)

The subcategory DataFrame is exported as category.csv (5 points)

A Campaign DataFrame is Created (30 points)

The DataFrame has the following columns: (25 points)
A "cf_id" column
A "contact_id" column
A "company_name" column
A "description" column
A "goal" column that is a float data type
A "pledged" column that is a float data type
An "outcome" column
A "backers_count" column
A "country" column
A "currency" column
A "launch_date" with the time formatted as "YYYY-MM-DD"
An "end_date" with the time formatted as "YYYY-MM-DD"
A "category_id" column that contains the unique identification numbers matching those in the "category_id" column of the category DataFrame
A "subcategory_id" column that contains the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

The campaign DataFrame is exported as campaign.csv (5 points)

A Contacts DataFrame is Created (15 points)

The DataFrame has the following columns: (10 points)
A "contact_id" column
A "first_name" column
A "last_name" column
An "email" column

The contacts DataFrame is exported as contacts.csv (5 points)

A Crowdfunding Database is Created (25 points)

A database schema labeled, crowdfunding_db_schema.sql is created (5 points)

A crowdfunding_db is created using the crowdfunding_db_schema.sql file (5 points)

The database has the appropriate primary and foreign keys and relationships (5 points)

Each CSV file is imported into the appropriate table without errors (5 points)

The data from each table is displayed using a SELECT * statement (5 points)




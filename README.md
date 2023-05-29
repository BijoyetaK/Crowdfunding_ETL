# Crowdfunding_ETL - Project 2
### Contributors: Bijoyeta Kayal and Sophia Felix
### This project is a ETL mini project that involved:
  - ETL pipeline using Python, Pandas, and either using Python dictionary methods or regular expressions to extract and transform the data. 
  - Once the data was transformed, four CSV files got created.Data from those csv files were observed to create an ERD and a table schema. 
  - Finally import those CSV files to their respective tables that were created: contacts, category, subcategory, campaign.
  - 2 jupyter notebooks representing: Approach 1 and second approach. Notebooks are named accordingly. 

### Part 1: Create the Category and Subcategory DataFrames
  - Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
  - A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories.
  - A "category" column that contains only the category titles
  - The following image shows this category DataFrame:
  - ![image](https://github.com/BijoyetaK/Crowdfunding_ETL/assets/126313924/5bfa423c-f1e9-45ff-985f-2d1b929577dd)
  - Export the category DataFrame as category.csv and save it to GitHub repository under Resources folder.

  - Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
  - A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories.
  - A "subcategory" column that contains only the subcategory titles.
  - The following image shows this subcategory DataFrame:
  - ![image](https://github.com/BijoyetaK/Crowdfunding_ETL/assets/126313924/6301f284-c113-4703-ae40-e9fa7f6d4b69)
  - Export the subcategory DataFrame as subcategory.csv and save it to GitHub repository under Resources folder. 

### Part 2: Create the Campaign DataFrame
  - Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
  - "cf_id" column
  - "contact_id" column
  - "company_name" column
  - "blurb" column, renamed to "description"
  - "goal" column, converted to the float data type
  - "pledged" column, converted to the float data type
  - "outcome" column
  - "backers_count" column
  - "country" column
  - "currency" column
  - "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
  - "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
  - "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
  - "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
  - The following image shows this campaign DataFrame:
   ![image](https://github.com/BijoyetaK/Crowdfunding_ETL/assets/126313924/47b48c96-3446-4c0f-910f-3ea6b7091561)
  - Export the campaign DataFrame as campaign.csv and save it to  GitHub repository under Resources folder. 

### Part 3: Create the Contacts DataFrame
  - Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:
  - Option 1: Use Python dictionary methods.
  - Option 2: Use regular expressions.
  - Both the above options are used for practice to create the contacts dataframe and csv with contact ids, names and email addresses. 
  - For Option 1, following steps were followed:

    - Import the contacts.xlsx file into a DataFrame.
    - Iterate through the DataFrame, converting each row to a dictionary.
    - Iterate through each dictionary, doing the following:
    - Extract the dictionary values from the keys by using a Python list comprehension.
    - Add the values for each row to a new list.
    - Create a new DataFrame that contains the extracted data.
    - Split each "name" column value into a first and last name, and place each in a new column.
    - Clean and export the DataFrame as contacts.csv and save it to GitHub repository under Resources folder. 

  - For Option 2, following steps were followed:
  
    - Import the contacts.xlsx file into a DataFrame.
    - Extract the "contact_id", "name", and "email" columns by using regular expressions.
    - Create a new DataFrame with the extracted data.
    - Convert the "contact_id" column to the integer type.
    - Split each "name" column value into a first and a last name, and place each in a new column.
    - Clean and then export the DataFrame as contacts.csv and save it to GitHub repository under Resources folder.

   - Final DataFrame for contacts resembles the one in the following image:
     ![image](https://github.com/BijoyetaK/Crowdfunding_ETL/assets/126313924/6201a8b2-667d-4e37-b4bf-0782ba0198c5)
     
 ### Part 4: Create the Crowdfunding Database
   - Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBD: 
     ![image](https://github.com/BijoyetaK/Crowdfunding_ETL/assets/126313924/ad60d5fd-2dd7-40ca-8044-5b5450c27a64)
   - Using the DDL scripts from the ERD to create a table schema for each CSV file.Datatypes, primary keys, foreign keys and other constraints were specified.
   - 4 tables created in sequence: contacts, category, subcategory, and finally the campaign table containing all the foreign keys from contacts, category, subcategory.
   - Data from each csv were loaded in following sequence: 
   - contacts.csv to contacts 
   - category.csv to category
   - subcategory.csv to subcategory
   - campaign.csv to campaign
   - Once data is loaded into the tables, each table is read using select statements. 
     ![image](https://github.com/BijoyetaK/Crowdfunding_ETL/assets/126313924/a7e629c0-1027-43d3-93f8-3cc1752b63a2)
     
     ![image](https://github.com/BijoyetaK/Crowdfunding_ETL/assets/126313924/9a2285b5-957e-4f18-8e30-cc03506a69c1)
     
     
 ### references: 
   - module activities examples
   - https://www.guru99.com/python-regular-expressions-complete-tutorial.html
   - https://stackoverflow.com/questions/4770297/convert-utc-datetime-string-to-local-datetime
   - https://www.tutorialspoint.com/Extracting-email-addresses-using-regular-expressions-in-Python
   - https://www.tutorialspoint.com/Extracting-email-addresses-using-regular-expressions-in-Python


 










            
            

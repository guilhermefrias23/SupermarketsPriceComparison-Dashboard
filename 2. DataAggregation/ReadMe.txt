This script aims to piece together all the data obtained from the webscrapping tools to allow the correct production of the dashboard based on the defined template.

To do so this script will follow the following steps:
 - Import all the data from the three supermarkets and will store these data in different dataframes
 - Remove the first two rows (headers) and add the correct column names
 - Fill the missing data for each supermarket based on the supermarket and the category that they belong to
 - Replace the words that were changed regarding 'Bovino' to 'Vaca' as per the initial criteria
 - Fill the product category information based on the first availble value for each row
 - Left join each data frame with the original set of categories so that if there are missing products, all of them are placed on the DataFrame
 - Concatenate all dataframes into one in which each product is repeated three times and has 150 rows
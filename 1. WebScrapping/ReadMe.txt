This script allows to access the supermarket website and retrieve the data that is stored on the website specific tags.

Using the requests and the bs4 libraries was accessed the html code of the different webpages and retrieved the information regarding the name and the price of the products that were listed there.

The data that was obtained via this method was then transformed into a string and manipulated to get the product name and price on a readable format.

Based on the excel file _Categories.xlsx_, that was inputed, it was defined that the code would loop through the names of the products and would search for that name on the products webpage of the supermarket website.
 - the group opted to create a new url based on the "base url" of the webpage and replacing the words that had the search criteria for the ones on this file.

When accesing a url the data was stored on a data frame. This df will then be filtered using the function data_cleaning, which removes all searches that are out of scope for that search.
 - for example, when searching meat products is usual to have animal food on the search results, which is out of the scope of the search, therefore these items would be removed
Based on the removed results then the products would be narrowed for the top 10 products, that were selected based on the search preferences that each supermarket marked as more relevant.

These individual product dataframes were then concatenated into one dataframe that stores the information of this specific supermarket.

To this dataframe are then created new columns that have some summary statistics of the data on each row, detailing the minimum price, maximum and average price for each row, as well as the number of products that were passed onto the final dataframe for each product.

These data are to be then used on the next steps of the project
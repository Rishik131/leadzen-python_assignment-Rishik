# leadzen-python_assignment-Rishik
#### Part A
1. We first import the necessary Modules.
2. Request is sent to the required link for https request.
3. Function 'get_items()' extracts items from all 20 pages, with all the data, that is, with title, rating, discount etc.
4. Function 'get_titles()' extracts titles of all the items present in items list.
5. Function 'get_links()' extracts links of all the items present in items list.
6. Function 'get_price()' extracts prices of all the items present in items list.
7. Function 'get_rating()' extracts ratings out of 5 of all the items present in items list.
8. Function 'get_review()' extracts number of reviews of all the items present in items list.
9. All these data are stored in dataframe 'df'

#### Part B
1. Beautiful Soup fails to extract individual product's details. Whenever HTTP request is sent, Amazon website returns a CAPTCHA page. Amazon returns captcha to avoid scraping of its website by third party.
2. Hence we use Selenium for part B
3. Selenium Accesses the website via browser driver. Hence Amazon does not send CAPTCHA page to actual browser.
4. We create 3 functions:
    get_asin(): to extract ASIN of each product
    get_manufacturer: to extract manufacturer details of each product
    get_description: to extract product description
5. We iterate over dataframe 'df' row-wise and access each product's link one by one.
6. For each product, above mentioned 3 functions are called and stored into a list.
7. Finally these lists are appended to our original Datafram.
8. The Dataframe is exported as CSV file
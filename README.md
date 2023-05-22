# ETL Pipeline for Bookstore Data using Scrapy and MySQL
  
![ETL](https://github.com/MoohamedElsayed/Book-Scraper-MySQL-ETL./assets/108439954/886f9e7f-23a9-4a8e-921e-6cfa1ba2032f)
  


## Description :-
* In this project, I created an ETL (Extract, Transform, Load) pipeline using Scrapy to scrape data from a bookstore website. Then transform it, and load it into a MySQL database.
* The website use to scrape data from is "http://books.toscrape.com/"


## Steps of the project :-
### Step 1: Creating a Scrapy Spider
* I started by creating a Scrapy spider to crawl through the bookstore website and scrape data from each page.  
* To avoid getting blocked by the website while scraping, I used fake user-agents and headers.   
* The data columns I extracted were:
 <pre>
 1- url                                       2- title                                     3- upc
 4-product_type                               5- price_excl_tax                            6- price_incl_tax
 7- tax                                       8- availability                              9- num_reviews
 10- stars                                    11- category                                 12- description
 13- price
</pre>
### Step 2: Cleaning Data with Items & Item Pipelines    
After extracting the data, I used Scrapy’s Items and Item Pipelines to clean and process the data.    

### Step 3: Saving Data to CSV Files & MySQL Database    
Once the data was cleaned and processed, I saved it to CSV files and loaded it into a MySQL database.    


This project was a great learning experience in using Scrapy for web scraping and building an ETL pipeline.

## How to use :-

* Create a new environment and activate it using   
``` venv/scripts/activate ```

* Install the required python modules using    
``` pip install -r requirements.txt ```

* Add your ScrapeOps API key to the settings.py    
``` SCRAPEOPS_API_KEY = 'YOUR_API_KEY_HERE' ```

* Cd into the project spiders and Run the project using    
``` scrapy crawl bookspider ```

# Online Fashion Retail Web Scraper

This project utilizes Python to scrape product data (titles, prices, and hyperlinks) from an online fashion retail website and saves it to a CSV file.

## Project Description

This web scraper automates the collection of product information from an online fashion retailer. It uses the `requests` library to fetch HTML content and `BeautifulSoup` to parse and extract relevant data. The extracted data is then organized into a Pandas DataFrame and saved as a CSV file.

## Steps Performed

1.  **Import Libraries:**
    * Import necessary libraries: `requests`, `BeautifulSoup`, `pandas`.

2.  **Define Extraction Functions:**
    * Create functions `get_title(article)`, `get_price(article)`, and `get_href(article)` to extract product titles, prices (converted to float), and hyperlinks from each product's HTML `article` element.

3.  **Set User-Agent and Page Limit:**
    * Define a `headers` dictionary to simulate a browser request using a User-Agent.
    * Set a `limit` variable to control the number of pages to scrape.

4.  **Iterate Through Pages:**
    * Use a `for` loop to iterate through the specified number of pages.
    * Construct the URL for each page.
    * Use `requests.get()` to fetch the HTML content of the page.
    * Parse the HTML content using `BeautifulSoup`.

5.  **Extract Product Data:**
    * Locate the product list container (`ul` element with `data-elid='product-grid'`).
    * Iterate through each product item (`li` element).
    * Find the `article` element for each product.
    * Call the extraction functions (`get_title()`, `get_price()`, `get_href()`) to retrieve the data.
    * Append the extracted data to a dictionary (`scraped_data_dict`).

6.  **Create Pandas DataFrame:**
    * Convert the `scraped_data_dict` to a Pandas DataFrame using `pd.DataFrame.from_dict()`.

7.  **Save to CSV:**
    * Save the DataFrame to a CSV file named `Online_Fashion_Retail_Webscrape.csv` using `dataset.to_csv()`.

## Dependencies

* `requests`
* `beautifulsoup4`
* `pandas`

## Usage

1.  Clone the repository or copy the Python script.
2.  Install the required dependencies using `pip install requests beautifulsoup4 pandas`.
3.  Run the Python script.
4.  The scraped data will be saved in `Online_Fashion_Retail_Webscrape.csv`.

## Future Improvements

* Implement error handling for network requests and HTML parsing.
* Add functionality to handle pagination dynamically.
* Incorporate data cleaning and preprocessing steps.
* Add command-line arguments for URL and page limit.
* Implement data storage in a database.
* Add more features to extract additional product details.

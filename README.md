
# Amazon Product Scraper 🛒

## Overview

The **Amazon Product Scraper** is a versatile Python-based tool designed to extract detailed information from Amazon product pages using **Selenium**. This tool automates browsing through Amazon's website, gathering valuable data such as product names, prices, reviews, descriptions, ratings, and images. The extracted data can be saved in a structured format for further analysis or use in various applications.

## Features

- **Automated Data Extraction**: Efficiently scrapes multiple product details, including names, prices, reviews, descriptions, ratings, and images.
- **Handles Missing Data**: Robust error handling to manage missing or unavailable elements.
- **Flexible and Scalable**: Capable of scraping multiple pages across various product categories.
- **CSV Ready**: Extracted data is stored in lists that can be easily converted to a CSV file.

## Getting Started

### Prerequisites

- **Python 3.x** installed on your machine.
- **Selenium** library.
- A compatible **WebDriver** (e.g., ChromeDriver for Google Chrome).



### Usage

1. **Prepare the Script**:
   - Define a list of Amazon page URLs (`page_links`) that you want to scrape in your Python script.

2. **Run the Script**:

    ```bash
    python amazon_product_scraper.py
    ```

3. **Data Output**:
   - The script stores extracted data such as product names, prices, reviews, descriptions, and ratings in various Python lists. These can then be exported to a CSV file using the `pandas` library for further analysis.

### Code Workflow

- **Collect Links**: The script first gathers product links from the specified Amazon pages.
- **Extract Product Information**: For each product link, it extracts:
  - **Product Name**: Using `ID` or CSS selectors.
  - **Product Details**: Such as descriptions, specifications, or features, using various selectors.
  - **Reviews**: Scrapes customer reviews, cleans the text, and stores it.
  - **Prices**: Extracts current prices, discounts, and previous prices if available, handling dynamic content loading.
  - **Images**: Fetches URLs of main product images.
  - **Ratings**: Retrieves overall product ratings and the number of customer ratings.

- **Error Handling**: Uses robust exception handling (`try-except`) to manage scenarios where elements are missing, the page takes too long to load, or unexpected issues arise.

### Customization

You can modify the script to scrape different product categories or additional product details by adjusting the XPath, CSS selectors, or other scraping parameters.

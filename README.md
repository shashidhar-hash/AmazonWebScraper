# 🛒 Amazon Product Data Scraper using Python

## 📘 Project Overview
This project focuses on **extracting product information from Amazon** using **Python**, **BeautifulSoup**, and **Requests**.  
The goal was to collect data such as product titles, prices, ratings, and reviews — and store it in a structured format for analysis or comparison.

---

## 🧩 Tools and Technologies
- **Python 3** — core programming language  
- **Jupyter Notebook** — for code execution and data exploration  
- **BeautifulSoup (bs4)** — for parsing HTML content  
- **Requests** — for sending HTTP requests  
- **Pandas** — for data storage and manipulation  

---

## ⚙️ Project Workflow

### 1. Data Collection
- Selected Amazon product URLs for categories such as electronics, clothing, and accessories.  
- Used **HTTP GET requests** to fetch HTML content from Amazon product or search pages.

### 2. Data Extraction
- Parsed the HTML using **BeautifulSoup** to identify specific tags containing:
  - Product **title**
  - Product **price**
  - **Rating** and **review count**
  - **Availability** status
- Extracted text content using tag attributes and CSS selectors.

### 3. Data Cleaning
- Removed missing, duplicate, or null entries.  
- Converted prices and ratings to numerical values.  
- Formatted and standardized data for consistency.

### 4. Data Storage
- Structured extracted data into a **Pandas DataFrame**.  
- Exported the results into a **CSV file (`amazon_data.csv`)** for further analysis or visualization.

---

## 🧮 Example Code Snippet
```python
import requests
from bs4 import BeautifulSoup
import pandas as pd

url = "https://www.amazon.in/s?k=wireless+headphones"
headers = {"User-Agent": "Mozilla/5.0"}

response = requests.get(url, headers=headers)
soup = BeautifulSoup(response.content, "html.parser")

titles = [item.get_text(strip=True) for item in soup.select("h2 a span")]
prices = [item.get_text(strip=True) for item in soup.select(".a-price-whole")]

df = pd.DataFrame({"Title": titles, "Price": prices})
df.to_csv("amazon_data.csv", index=False)
df.head()

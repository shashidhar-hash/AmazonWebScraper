🛒 Amazon Web Scraper

A Python-based web scraping project that extracts product details from Amazon using BeautifulSoup and requests. This scraper collects data like product name, price, rating, and availability — perfect for analyzing pricing trends or product comparisons.

🚀 Features

Scrapes product information (title, price, rating, reviews, etc.)

Supports multiple product pages

Saves data into a structured CSV/Excel format

Handles request delays to avoid blocking

Easy to modify for different keywords or categories

🧠 Technologies Used

Python 3

BeautifulSoup4

Requests

Pandas

📁 Project Structure
AmazonWebScraper/
│
├── AmazonWebScraper.ipynb   # Main Jupyter Notebook
├── requirements.txt          # Dependencies (optional)
├── README.md                 # Project documentation
└── output.csv                # Sample output file (generated)

⚙️ Installation
git clone https://github.com/<your-username>/AmazonWebScraper.git
cd AmazonWebScraper

pip install -r requirements.txt

pip install requests beautifulsoup4 pandas

jupyter notebook AmazonWebScraper.ipynb

🧩 How It Works

Sends a request to Amazon’s search page with a product keyword.

Parses HTML using BeautifulSoup to extract details:

Product title

Price

Rating

Review count

Stores all results into a CSV for further analysis.

⚠️ Disclaimer

This project is for educational purposes only.
Amazon’s Terms of Service prohibit scraping without permission.
Use responsibly and avoid making frequent requests.

💡 Future Improvements

Add proxy rotation and user-agent randomization

Integrate with Selenium for dynamic content scraping

Build a small Flask or Streamlit dashboard for data visualization






















Jupyter Notebook


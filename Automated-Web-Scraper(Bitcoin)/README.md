# 📈 Crypto Scraper - Automated Bitcoin Web Scraper

This Python project is an **automated web scraper** that fetches **real-time Bitcoin prices** from [CoinMarketCap](https://coinmarketcap.com/currencies/bitcoin/) and logs them to a CSV file every 25 seconds.

## 🧠 Features

- Scrapes live Bitcoin prices using `requests` and `BeautifulSoup`
- Parses and stores data with a timestamp
- Saves the data into a CSV file (`Crypto_Automated_Pull.csv`)
- Appends new prices every 25 seconds automatically
- Automatically creates the CSV file if it doesn't exist

## 🛠️ Libraries Used

- `requests` – For sending HTTP requests  
- `BeautifulSoup` (from `bs4`) – For parsing HTML content  
- `pandas` – For handling tabular data  
- `datetime` – For generating timestamps  
- `os` – For checking file existence and handling file paths  
- `time` – For automating the periodic data pull

## 📁 File Structure

CryptoScraper/
│
├── crypto_scraper.py           # Main script to run the scraper  
├── Crypto_Automated_Pull.csv   # Output file (created automatically)  
└── README.md                   # Project documentation

## ▶️ How to Run

1. cInstall the required packages:**

pip install requests beautifulsoup4 pandas

2. **Update the CSV file path in the script:**

Replace `your file path` with your desired full path. For example:

```python
r'C:\Users\yourname\Documents\Crypto_Automated_Pull.csv'
```
3. **Run the script:**

python crypto_scraper.py


🧾 **Example Output:**
```python
  crypto Name     Price                TimeStamp
0     Bitcoin  68234.27  2025-06-12 12:34:56.789000

```
⚠️ **Note:**
- CoinMarketCap's HTML structure may change.
  If the script stops working, inspect the page again and update the class attributes in the BeautifulSoup selectors.

- Avoid sending too many requests in a short time to respect the website’s terms of service.
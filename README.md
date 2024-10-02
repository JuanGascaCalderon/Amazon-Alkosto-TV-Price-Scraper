# 📊 Amazon & Alkosto TV Price Scraper

This project performs **web scraping** on **Amazon** and **Alkosto** websites, extracting information about available TVs, their prices, and product images. Additionally, it converts prices from USD to COP using an exchange rate API.

## 🛠️ Technologies Used
- **Python** 🐍
- **Selenium** 🌐
- **Pandas** 🧮
- **Requests** 📡
- **Logging** 📝

## 🚀 Project Features
1. **Amazon & Alkosto Scraping** 🛒:
   - **Extracts** information about TVs, including name, price, and image link.
   - **Navigates** through multiple pages of results until all available products are collected.

2. **Data Cleaning** 🧹:
   - Converts non-numeric prices to `NaN` values for better manipulation.
   - Removes products without prices to improve data quality.

3. **Currency Conversion** 💱:
   - Uses an exchange rate API to convert TV prices from USD to COP.
   - Rounds prices to the local currency (Colombian pesos).

4. **CSV Storage** 💾:
   - Collected data is saved in CSV files for easier post-analysis.
  
## 🚀 How It Works

1. 🕵️‍♂️ **Scraping Amazon Data**  
   The script uses Selenium to navigate Amazon's product listings. It retrieves titles, prices, and images of TVs.

2. 🧹 **Cleaning Data**  
   The scraped prices are cleaned by replacing "no price" values with NaN. Any rows with NaN in the price column are dropped.

3. 💱 **Currency Conversion**  
   The script fetches the current exchange rate from USD to COP. Prices are converted from USD to COP and rounded to the nearest integer.

4. 💾 **Saving Data**  
   The cleaned and converted data is saved to a CSV file named `amazon_tvs.csv` and `alkosto_tvs.csv`.


## 📋 Installation and Setup

### 1. Clone the repository:
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```
### 2. Install the dependencies:
```bash
pip install -r requirements.txt
```
### 3. Run the Script:
```bash
python project.ipynb
```
### 4. Configure the exchange rate API:
 - You'll need an API key for the ExchangeRate-API or a similar service. Update the API URL in the code, replacing YOUR_API_KEY with your personal key.
```bash
api_url = "https://v6.exchangerate-api.com/v6/YOUR_API_KEY/latest/USD"
```

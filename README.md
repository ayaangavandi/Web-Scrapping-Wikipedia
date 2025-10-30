# 🌐 Web Scraping and Data Analysis using Python & Pandas  

## 🧠 Project Overview  
This project focuses on **extracting structured data from a website using Python’s web scraping techniques** and analyzing it with **Pandas**.  
The goal was to automate data collection, clean the scraped information, and transform it into a structured dataset ready for further insights and reporting.  

---

## 🎯 Objectives  
- Perform web scraping to collect tabular and structured data from a target website.  
- Parse and extract useful information such as product details, prices, or listings.  
- Clean, transform, and analyze the scraped data using **Pandas**.  
- Export the cleaned dataset for visualization or BI reporting.  

---

## ⚙️ Tools & Technologies  
- **Python** → Data extraction and cleaning  
- **Libraries Used:** `requests`, `BeautifulSoup`, `pandas`, `time`  
- **Environment:** Jupyter Notebook / Google Colab  

---

## 🧩 Process & Approach  

### 1️⃣ Web Scraping  
- Connected to the target website using the **`requests`** library.  
- Extracted HTML data from web pages.  
- Parsed HTML tags and extracted relevant information using **BeautifulSoup**.  

### 2️⃣ Data Cleaning (Pandas)  
- Created a **Pandas DataFrame** from the scraped data.  
- Removed duplicate and missing values.  
- Formatted column names and data types.  
- Sorted and filtered the data for further analysis.  

### 3️⃣ Data Analysis & Export  
- Used Pandas for quick summaries and exploratory analysis.  
- Calculated averages, totals, and frequency distributions.  
- Exported the cleaned dataset to CSV/Excel for further reporting.  

---

## 📈 Key Outcomes
  -✅ Successfully scraped data from multiple web pages.
  
  -✅ Cleaned and organized raw HTML data into a structured dataset.
  
  -✅ Demonstrated integration of BeautifulSoup with Pandas for seamless data handling.
  
  -✅ Exported final dataset to Excel/CSV for easy analysis and sharing.

---

## 🧠 Skills Demonstrated

🔹 Web Scraping with Python

🔹 HTML Parsing using BeautifulSoup

🔹 Data Cleaning & Structuring in Pandas

🔹 Exploratory Data Analysis (EDA)

🔹 Automation of Data Collection Workflows

---

## 🚀 Conclusion

This project showcases how Python’s web scraping and data manipulation libraries can work together to collect and transform real-world web data into clean, structured, and analysis-ready datasets essential for market research and business intelligence workflows.

---

## 🧰 Tools Used
| Tool             | Purpose                        |
| ---------------- | ------------------------------ |
| 🐍 Python        | Web Scraping & Data Cleaning   |
| 🌐 BeautifulSoup | HTML Parsing & Data Extraction |
| 📊 Pandas        | Data Structuring & Analysis    |

---

## 📫 Connect With Me  
🔗 [LinkedIn](https://www.linkedin.com/in/ayaan-gavandi-a16202218/)  
📧 [Email](mailto:ayaangavandi33@gmail.com)

---

## 📊 Example Code Snippet  

```python
import requests
from bs4 import BeautifulSoup
import pandas as pd

# Step 1: Fetch HTML
url = 'https://example.com'
response = requests.get(url)
soup = BeautifulSoup(response.text, 'html.parser')

# Step 2: Extract Data
items = soup.find_all('div', class_='item')
data = []
for item in items:
    name = item.find('h2').text.strip()
    price = item.find('span', class_='price').text.strip()
    data.append([name, price])

# Step 3: Convert to DataFrame
df = pd.DataFrame(data, columns=['Product Name', 'Price'])
df.head()

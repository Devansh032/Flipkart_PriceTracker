Here’s a more detailed and polished **README** for your **Flipkart Price Tracker** project. 🚀  

---

# 🛒 Flipkart Price Tracker  
A **Python-based automated price tracking system** that scrapes product prices from **Flipkart**, monitors price fluctuations over time, and **sends email alerts** when a product's price falls below a user-defined threshold.  

🔹 **Graphical User Interface (GUI)** for easy user input  
🔹 **Automated tracking every 30 minutes** using a scheduler  
🔹 **Stores price history** for analysis  
🔹 **Email notifications with price graphs**  

---

## 🚀 Features  

✅ **Automated Price Tracking** – Monitors prices every 30 minutes  
✅ **GUI for User Input** – Users can input product URLs and threshold prices  
✅ **Email Alerts** – Sends notifications when prices drop  
✅ **Graph Generation** – Saves price trends as images  
✅ **CSV Storage** – Stores scraped data for future reference  
✅ **Efficient Data Cleaning** – Removes unwanted text from product names  

---

## 🏗️ Project Structure  

```
📂 Flipkart_PriceTracker  
├── 📄 init.py              # Initial scraper to fetch product data  
├── 📄 tracker.py           # Core price tracking logic  
├── 📄 scheduler.py         # Automates tracking every 30 minutes  
├── 📄 send_email.py        # Sends price drop alerts via email  
├── 📄 gui.py               # User interface (Tkinter)  
├── 📄 graph.py             # Generates price trend graphs  
├── 📄 spaceremover.py      # Cleans up scraped product names  
├── 📄 FlipkartWebScraperDataset.csv  # Stores price history  
├── 📄 data.csv             # Stores user preferences (URLs, thresholds, emails)  
```

---

## 🛠️ Installation & Setup  

### 1️⃣ Clone the Repository  
```sh
git clone https://github.com/Devansh032/Flipkart_PriceTracker.git  
cd Flipkart_PriceTracker
```

### 2️⃣ Install Required Dependencies  
```sh
pip install -r requirements.txt
```

### 3️⃣ Run the GUI (For User Input)  
```sh
python gui.py
```
- Enter **Flipkart product URL**, **Threshold Price**, and **Email**  
- Click **Submit** to store the details  

### 4️⃣ Start Automated Price Tracking  
```sh
python scheduler.py
```
- Runs **every 30 minutes** to check prices  
- Sends **email alerts** when the price is below the threshold  

---

## 📊 How It Works  

### 1️⃣ **Scraping Flipkart Prices**  
- The script (`tracker.py`) **fetches real-time prices** using **BeautifulSoup**  
- Product details are extracted and **stored in CSV files**  

### 2️⃣ **Threshold Price Comparison**  
- If the **current price** ≤ **user-defined threshold**, an **email is sent**  
- The `send_email.py` script **sends an email with the latest price & a graph**  

### 3️⃣ **Price History Graphs**  
- The `graph.py` script **plots a price history graph**  
- Uses **Matplotlib** to visualize price trends  
- Graph is **attached to the email alert**  

### 4️⃣ **Automated Tracking Every 30 Minutes**  
- The `scheduler.py` **automatically runs the tracker**  
- Runs every **30 minutes** to check for price updates  

---

## 📧 Email Notification Example  

💡 **When a price drop occurs**, users receive an email like this:  

📩 **Subject:** *Exciting News: Price Drop Alert for [Product Name]*  

✉️ **Message:**  
> The price of **[Product Name]** has dropped below ₹[Threshold]!  
> New price: ₹[Current Price]  
> Click here to buy: [Flipkart Product URL]  

📎 **Attachment:** *A price history graph*  

---

## 💻 Technologies Used  

- **Python** 🐍  
- **BeautifulSoup** (for web scraping)  
- **Requests** (to fetch webpage data)  
- **Matplotlib** (for generating graphs)  
- **SMTP (smtplib)** (to send email alerts)  
- **Tkinter** (for GUI)  
- **Schedule** (for automation)  

---

## 📌 Future Enhancements  

✅ **Support for multiple e-commerce platforms** (Amazon, Myntra, etc.)  
✅ **Mobile App Integration** for real-time alerts  
✅ **Push Notifications instead of Email**  
✅ **Database Integration** instead of CSV storage  

---


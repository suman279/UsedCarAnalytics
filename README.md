# UsedCarAnalytics

Web Scraping | MySQL | Power BI Reports

Project Overview
This project automates the extraction, storage, and visualization of used car data. It scrapes data from Cardekho, saves it into MySQL, and generates insightful reports using Power BI.

Features
✅ Web Scraping: Extracts car details (name, price, kilometers_driven, fuel_type, transmission_type, location, Car_type, model, Mileage  )
✅ MySQL Storage: Organizes and maintains structured data
✅ Power BI Reports: Provides visual insights into car pricing trends and market dynamics

⚙️ Tech Stack
Python 🐍 (Selenium, Requests, Pandas) for Web Scraping
MySQL 🗄️ for Data Storage
Power BI 📊 for Report Generation

Project Structure
📦 UsedCarAnalytics
├── 📂 data                # Contains scraped data before inserting into MySQL
├── 📂 sql                 # MySQL database schema and queries
├── 📂 reports             # Power BI reports and dashboards
├── 📂 python              # Web scraping script using BeautifulSoup
├── 📜 requirements.txt    # Python dependencies
└── 📜 README.md           # Project documentation

🛠️ Setup & Installation
1️⃣ Install Dependencies
Ensure Python and MySQL are installed, then install required Python libraries:
pip install -r requirements.txt

2️⃣ Database Setup
CREATE SCHEMA `car_details` ;
CREATE TABLE `used_cars` (
  `name` varchar(255) NOT NULL,
  `price` int DEFAULT NULL,
  `kilometers_driven` int DEFAULT NULL,
  `fuel_type` varchar(50) DEFAULT NULL,
  `transmission_type` varchar(50) DEFAULT NULL,
  `location` varchar(255) DEFAULT NULL,
  `car_type` varchar(255) DEFAULT NULL,
  `model` varchar(255) DEFAULT NULL,
  `mileage` int DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

3️⃣ Run the Web Scraper

python cardekho_scrapper.py
This script fetches used car data from Cardekho and inserts it into MySQL.

4️⃣ Connect Power BI to MySQL
Open Power BI Desktop
Click Get Data → MySQL Database
Enter your MySQL server details and select the used_cars table
Load data and build visualizations
📈 Sample Reports
✔️ Price trends across fuel types
✔️ Popular car transmission types
✔️ Mileage vs. price analysis


📜 Future Enhancements
🔹 Automate data updates with a scheduled job
🔹 Integrate Machine Learning for price predictions
🔹 Build an interactive web dashboard

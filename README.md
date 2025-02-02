# UsedCarAnalytics

Web Scraping | MySQL | Power BI Reports

Project Overview
This project automates the extraction, storage, and visualization of used car data. It scrapes data from Cardekho, saves it into MySQL, and generates insightful reports using Power BI.

🚀 Features
✅ Web Scraping: Extracts car details (name, price, kilometers driven, fuel type, transmission)
✅ MySQL Storage: Organizes and maintains structured data
✅ Power BI Reports: Provides visual insights into car pricing trends and market dynamics

⚙️ Tech Stack
Python 🐍 (BeautifulSoup, Requests, Pandas) for Web Scraping
MySQL 🗄️ for Data Storage
Power BI 📊 for Report Generation

Project Structure
📦 cardekhodataanalytics
├── 📂 data                # Contains scraped data before inserting into MySQL
├── 📂 sql                 # MySQL database schema and queries
├── 📂 reports             # Power BI reports and dashboards
├── 📜 scraper.py          # Web scraping script using BeautifulSoup
├── 📜 database.py         # MySQL database connection and operations
├── 📜 requirements.txt    # Python dependencies
└── 📜 README.md           # Project documentation
🛠️ Setup & Installation
1️⃣ Install Dependencies
Ensure Python and MySQL are installed, then install required Python libraries:

sh
Copy
Edit
pip install -r requirements.txt
2️⃣ Database Setup
Create a MySQL database:
sql
Copy
Edit
CREATE DATABASE car_data;
Create the used_cars table:
sql
Copy
Edit
CREATE TABLE used_cars (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255),
    price VARCHAR(50),
    kilometer_driven VARCHAR(50),
    fuel_type VARCHAR(50),
    transmission_type VARCHAR(50)
);
3️⃣ Run the Web Scraper
sh
Copy
Edit
python scraper.py
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

👨‍💻 Contributing
Feel free to fork this repository and create pull requests! Contributions are always welcome.

📄 License
This project is licensed under the MIT License.
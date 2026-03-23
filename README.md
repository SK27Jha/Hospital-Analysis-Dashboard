🏥 Hospital Management Analytics System

Power BI + MySQL + Python Flask

An end-to-end Hospital Data Analytics project that integrates Excel → MySQL → Flask → Power BI to analyze hospital operations, patient data, doctor performance, and financial insights through interactive dashboards.

📌 Project Overview

This project demonstrates a complete data analytics pipeline, starting from raw Excel data to database storage and interactive Power BI dashboards for business insights.

The system allows users to upload hospital Excel datasets through a Flask web application, store them in a MySQL database, and visualize insights in Power BI dashboards connected to the database.

🧱 Project Architecture
Data Flow
Excel Files → Flask Web App → MySQL Database → Power BI Dashboard
Workflow
Hospital data stored in Excel files
Flask web application uploads Excel data
Data inserted into MySQL database
Power BI connects to MySQL
Dashboards update automatically with latest data

This represents a real-world ETL + Data Visualization pipeline.

📂 Project Structure
Hospital-Management-Analytics/
│
├── Mysql/
│   └── hospital_data.sql
│
├── dataset/
│   ├── patients.xlsx
│   ├── doctors.xlsx
│   ├── billing.xlsx
│   ├── medicines.xlsx
│
├── excel_uploader/
│   ├── app.py
│   ├── templates/
│   │   ├── index.html
│   │   └── upload.html
│
├── Result/
│   ├── Home.png
│   ├── Overview.png
│   ├── Patient.png
│   ├── Doctor.png
│   ├── Hospital.png
│   └── Finance.png
│
├── hospital_dashboard.pbix
└── README.md
⚙️ Installation & Setup

1️⃣ MySQL Setup

Install MySQL Community Server and import the database:

mysql -u root -p < Mysql/hospital_data.sql

Verify database:

hospital_data
2️⃣ Flask Web App Setup

Navigate to Flask folder:

cd excel_uploader

Create virtual environment:

python -m venv venv
venv\Scripts\activate

Install dependencies:

pip install flask pandas mysql-connector-python openpyxl

Run the Flask application:

python app.py

Open browser:

http://127.0.0.1:5000/

Upload Excel files from dataset folder.

3️⃣ Power BI Dashboard Setup
Open hospital_dashboard.pbix
Go to Transform Data → Data Source Settings
Update MySQL credentials
Click Refresh
Dashboards will load live data
📊 Dashboards
Dashboard Modules
Dashboard	Description
Home Dashboard	Navigation and summary
Overview Dashboard	Hospital KPIs and performance
Patient Dashboard	Patient demographics and visits
Doctor Dashboard	Doctor performance and workload
Hospital Dashboard	Department and bed utilization
Finance Dashboard	Revenue, expenses, and profit
📈 Key Business Insights

The dashboard provides insights such as:

Total Patients and Appointments
Revenue and Expense Analysis
Doctor Performance Metrics
Department Workload Distribution
Bed Occupancy Rate
Patient Demographics
Disease Trends
Medicine Inventory Analysis
Monthly Revenue Trends
Discount and Billing Analysis
🛠️ Tools & Technologies Used
Tool	Purpose
Excel	Raw Data
MySQL	Database
Python	Data Processing
Flask	Web Upload System
Pandas	Data Cleaning
Power BI	Dashboard & Visualization
SQL	Data Queries
DAX	KPI Calculations
🧠 Skills Demonstrated
Data Cleaning
ETL Pipeline
Database Design
SQL Joins
Data Modeling
Power BI Dashboard Development
DAX Measures
Python Automation
Flask Web Development
Business Data Analysis
KPI Development
🚀 Future Improvements
Appointment No-Show Prediction
Revenue Forecasting
Patient Readmission Analysis
Doctor Utilization Rate
Medicine Stock Alerts
Department Profitability Analysis
Machine Learning Integration
👨‍💻 Author

Saket Kumar Jha
Data Analyst | Power BI | SQL | Python | Data Analytics

LinkedIn: (www.linkedin.com/in/saket1502)


⭐ If you like this project

Please star ⭐ the repository and share feedback!

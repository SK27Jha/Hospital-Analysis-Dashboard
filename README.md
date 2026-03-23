Hospital Management Analytics Project (Power BI + MySQL + Flask)
A complete Hospital Management Data Analytics project that integrates MySQL, Power BI, and a Flask-based web uploader for end-to-end hospital data analysis and visualization.

Home Dashboard Overview Dashboard Patient Dashboard *Doctor Dashboard Hospital Dashboard Finance Dashboard

📋 Overview
This project demonstrates a real-world data analytics workflow:

🗄️ Data Source: Multiple Excel files containing patient, doctor, billing, and medicine data
💾 Database Layer: MySQL database storing cleaned & structured hospital data
🌐 Web Application: Flask-based uploader to insert Excel data directly into MySQL
📊 Visualization Layer: Power BI dashboard that connects to MySQL for live insights
🧱 Project Structure
Folder / File	Description
Mysql/	Contains the MySQL dump file (hospital_data.sql) to create the database
dataset/	Contains all Excel dataset files used for data import
excel_uploader/	Flask web app for uploading Excel data into MySQL
Output/	Contains Power BI dashboard screenshots for preview
hospital_dashboard.pbix	Power BI dashboard file
README.md	Project documentation (this file)
⚙️ Setup Guide
1️⃣ MySQL Setup
Install MySQL Community Server
Import the provided SQL file:
mysql -u root -p < Mysql/hospital_data.sql
Verify that the database hospital_data is created successfully.
2️⃣ Flask Web App Setup
Navigate to the excel_uploader folder:

cd excel_uploader
Create a virtual environment (optional but recommended):

python -m venv venv
venv\Scripts\activate
Install dependencies:

pip install flask pandas mysql-connector-python openpyxl
Run the Flask app:

python app.py
Open your browser and go to:

http://127.0.0.1:5000/
Upload Excel files from the /dataset folder using the interface.

🧩 Flask app files:

templates/index.html → Main upload page
templates/upload.html → Upload confirmation page
3️⃣ Power BI Dashboard Setup
Open hospital_dashboard.pbix in Power BI Desktop
Navigate to Transform Data → Data Source Settings
Update the MySQL connection credentials (host, username, password)
Click Refresh to load live data
📸 Dashboard Preview
All visualizations are located in the Output folder.

#	Visualization	File	Description
1	Home Dashboard	Output/Home.png	High-level overview and navigation hub
2	Overview Dashboard	Output/Overview.png	Hospital performance summary and KPIs
3	Patient Dashboard	Ouput/Patient.png	Patient visits, demographics, and analysis
4	Doctor Dashboard	Output/Doctor.png	Doctor performance, specialization, and efficiency
5	Hospital Dashboard	Output/Hospital.png	Department-level and resource utilization analysis
6	Finance Dashboard	Output/Finance.png	Billing, revenue, and cost analysis
🧠 Key Insights
📅 Appointment trends by doctor, department, and date
💰 Revenue and expense tracking with discount analysis
🧍‍♂️ Patient demographics and diagnostic insights
🧑‍⚕️ Doctor performance, experience, and workload metrics
🏨 Bed occupancy, availability, and department load distribution
💊 Medicine inventory and supplier-level performance
🧑‍💻 Author
Saket Kumar Jha 🎓 Data Analytics Enthusiast | 📊 Power BI | 🐍 Python | 🗄️ SQL 🔗 LinkedIn Profile

🪪 License
This project is open-source and available under the MIT License.

⭐ Support
If you found this project helpful or inspiring, please star 🌟 this repository and connect with me on LinkedIn! Your feedback helps me improve and build more real-world data analytics projects.

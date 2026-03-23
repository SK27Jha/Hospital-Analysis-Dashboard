# Hospital-Analysis-Dashboard

# 🏥 Hospital Management Analytics Dashboard

> A full-stack data analytics project integrating **MySQL**, **Power BI**, and a **Flask** web application for end-to-end hospital data management and visualization.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Project Structure](#-project-structure)
- [Dashboard Preview](#-dashboard-preview)
- [Setup Guide](#%EF%B8%8F-setup-guide)
  - [MySQL Setup](#1%EF%B8%8F⃣-mysql-setup)
  - [Flask Web App Setup](#2%EF%B8%8F⃣-flask-web-app-setup)
  - [Power BI Dashboard Setup](#3%EF%B8%8F⃣-power-bi-dashboard-setup)
- [Key Insights](#-key-insights)
- [Tech Stack](#-tech-stack)
- [Author](#-author)
- [License](#-license)

---

## 🔍 Overview

This project demonstrates a complete, real-world **hospital data analytics workflow** — from raw Excel files to interactive Power BI dashboards. It covers:

- 🗄️ **Data Source** — Multiple Excel files containing patient, doctor, billing, and medicine data
- 💾 **Database Layer** — A structured MySQL database storing cleaned hospital records
- 🌐 **Web Application** — A Flask-based uploader to load Excel files directly into MySQL
- 📊 **Visualization Layer** — A Power BI dashboard connected live to the MySQL database

---

## 🗂️ Project Structure

```
hospital-management-analytics/
│
├── 📁 Mysql/
│   └── hospital_data.sql          # MySQL dump to recreate the database
│
├── 📁 dataset/
│   └── *.xlsx                     # Excel files: patients, doctors, billing, medicines
│
├── 📁 excel_uploader/
│   ├── app.py                     # Flask application entry point
│   └── templates/
│       ├── index.html             # Main upload interface
│       └── upload.html            # Upload confirmation page
│
├── 📁 Output/
│   ├── Home.png
│   ├── Overview.png
│   ├── Patient.png
│   ├── Doctor.png
│   ├── Hospital.png
│   └── Finance.png
│
├── hospital_dashboard.pbix        # Power BI dashboard file
└── README.md
```

---

## 📸 Dashboard Preview

| # | Dashboard | Description |
|---|-----------|-------------|
| 1 | **Home** | High-level overview and navigation hub |
| 2 | **Overview** | Hospital performance summary and KPIs |
| 3 | **Patient** | Patient visits, demographics, and diagnostics |
| 4 | **Doctor** | Doctor performance, specialization, and efficiency |
| 5 | **Hospital** | Department-level and resource utilization |
| 6 | **Finance** | Billing, revenue, discounts, and cost analysis |

> 📁 All screenshots are available in the [`Output/`](./Output/) folder.

---

## ⚙️ Setup Guide

### 1️⃣ MySQL Setup

1. Install [MySQL Community Server](https://dev.mysql.com/downloads/mysql/)
2. Import the provided SQL dump file:

```bash
mysql -u root -p < Mysql/hospital_data.sql
```

3. Verify the database was created:

```sql
SHOW DATABASES;
-- You should see: hospital_data
```

---

### 2️⃣ Flask Web App Setup

1. Navigate to the uploader folder:

```bash
cd excel_uploader
```

2. *(Optional but recommended)* Create and activate a virtual environment:

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python -m venv venv
source venv/bin/activate
```

3. Install required dependencies:

```bash
pip install flask pandas mysql-connector-python openpyxl
```

4. Run the Flask application:

```bash
python app.py
```

5. Open your browser and visit:

```
http://127.0.0.1:5000/
```

6. Use the interface to upload Excel files from the `/dataset` folder into MySQL.

---

### 3️⃣ Power BI Dashboard Setup

1. Open `hospital_dashboard.pbix` in **Power BI Desktop**
2. Go to **Transform Data → Data Source Settings**
3. Update the MySQL connection with your credentials:

| Field | Value |
|-------|-------|
| Host | `localhost` |
| Database | `hospital_data` |
| Username | `root` (or your MySQL user) |
| Password | *(your password)* |

4. Click **Refresh** to load live data from MySQL into the dashboard

> ⚠️ Make sure the MySQL server is running before refreshing the dashboard.

---

## 🧠 Key Insights

The dashboard uncovers the following analytics across 6 views:

- 📅 **Appointment Trends** — by doctor, department, and time period
- 💰 **Revenue & Expenses** — billing breakdown with discount analysis
- 🧍 **Patient Demographics** — age groups, visit frequency, and diagnoses
- 🧑‍⚕️ **Doctor Performance** — experience, workload, and specialization metrics
- 🏨 **Bed Occupancy** — availability, utilization rate, and department load
- 💊 **Medicine Inventory** — stock levels and supplier performance

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Data Storage | MySQL 8.x |
| Backend | Python, Flask |
| Data Processing | Pandas, OpenPyXL |
| Visualization | Microsoft Power BI |
| Data Format | Excel (.xlsx) |

---

## 🧑‍💻 Author

**Saket Kumar Jha**  
🎓 Data Analytics Enthusiast &nbsp;|&nbsp; 📊 Power BI &nbsp;|&nbsp; 🐍 Python &nbsp;|&nbsp; 🗄️ SQL

[![LinkedIn] (www.linkedin.com/in/saket1502)
---

## 🪪 License

This project is open-source and available under the [MIT License](LICENSE).

---

## ⭐ Support

If you found this project helpful or inspiring:

- ⭐ **Star** this repository
- 🔗 **Connect** with me on LinkedIn
- 🐛 **Open an issue** if you spot a bug or have a suggestion

Your feedback helps me build better, more impactful data analytics projects! 🙌

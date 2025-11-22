📘 AdTech Analytics Pipeline — End-to-End Data Analysis [Python + SQL + BI Project]

A full-stack data workflow using Python, SQL Server, and Power BI

📌 Overview

This project demonstrates a complete AdTech Analytics pipeline, starting from large-scale raw CSV data ingestion, followed by SQL-based data cleaning, and finally Power BI modeling, DAX measures, and dashboard creation.

It simulates a real enterprise environment where raw marketing data flows through:

Python Automation → Upload raw CSV files to SQL Server

SQL Cleaning & Validation Layer → Standardize and clean 120,000+ ad impressions

Power BI Semantic Model → Build advanced dashboards with ROI, CTR, CVR, ROAS, Fraud %, Time Intelligence, and Rankings

🏗️ End-to-End Architecture
📂 Raw CSV Files (120K+ rows)
        │
        ▼
🐍 Python Automation (Pandas + SQLAlchemy)
        │
        ▼
🗄️ SQL Server
  - Staging Tables
  - Data Cleaning
  - Standardization
  - Fraud Rules
  - Views (vw_Adtech_Cleaned)
        │
        ▼
📊 Power BI
  - Modeling (Star Schema)
  - DAX Measures
  - Time Intelligence
  - Dashboard

🎯 Project Goals

✔ Load & manage large AdTech datasets efficiently
✔ Clean messy marketing & web-tracking data using SQL
✔ Build a robust analytical data model in Power BI
✔ Implement 25+ DAX measures including:

CTR, CVR, CPC, eCPM, ROI, ROAS

Revenue MTD/YTD

Fraud detection metrics

Time-to-conversion & Click-to-view KPIs

Top N Ranking (RANKX)
✔ Build a professional BI dashboard for campaign performance

🚀 Phase 0 — Project Setup

Created project folder, README, and version tracking

Loaded raw CSVs (120K rows)

Followed naming conventions:

Raw_* → original tables

Clean_* → cleaned tables

Opened Power BI → Transform Data → Power Query

🐍 Phase 1 — Python Automation (Load CSV → SQL Server)

Python script automatically loads all CSV files to SQL Server.

Key Achievements

Imported 2 CSV files totaling 120,000+ records

Automated upload using SQLAlchemy + PyODBC

Tables created automatically using Pandas .to_sql()

Eliminated manual SQL inserts

✔ Time Saved: ~90%
✔ Fully automated ingestion

🗄️ Phase 2 — SQL-Based Data Cleaning

Performed 26+ cleaning transformations, including:

🔧 Column Standardization

CampaignName → remove spaces, tabs, NBSP, punctuations

PublisherName, AdvertiserName → unified naming (ACME CORP, BLUESKY, MARKETIFY)

DeviceType → normalized to Mobile / Desktop / Other

Browser → spell-checking (CHR0ME → CHROME)

CreativeID, CreativeSize, AdFormat → Trim + UPPER

🕒 Date Cleaning

Supported 5 date formats

Converted epoch → datetime

Extracted:

EventYear

EventMonth

EventWeek

EventHour

EventDate

🛑 Fraud Rules

Duplicate ImpressionID detection

Flagging suspicious behavior (IsFraud = 1)

🌐 URL Standardization

Lowercase

Remove invalid prefixes (htp:// → http://)

🧱 Final SQL View

Created vw_Adtech_Cleaned as the final consumption layer for Power BI.

📊 Phase 3 — Power BI Analytics & Visualization
✔ Data Model

Fact table → Cleaned events

Dimensions → Campaign, Device, Publisher, Time

Relationships & star schema optimized

✔ 25+ DAX Measures Implemented

Includes:

CTR = Click-Through-Rate

CVR = Conversion Rate

eCPM = Revenue per 1000 impressions

CPC = Cost per Click

ROI & ROAS

Revenue MTD / YTD / Last 30 Days

TopN using RANKX

Fraud Percentage

Avg Click-to-View & Time-to-Conversion

✔ EDA Covered

Device & Browser performance

Publisher ROI

Campaign revenue trend

Conversion funnel

Time-of-day performance (DayPart analysis)

Fraud vs Non-fraud behavior

📈 Final Power BI Dashboards

Campaign Performance Overview

Time Intelligence Breakdown (MTD/YTD/Weekly Trends)

Publisher & Device Insights

Fraud Detection Report

Engagement Metrics: Click-to-View, Time-to-Conversion

ROI / ROAS Executive Summary

(Images were generated separately in the conversation)

📌 Technologies Used
Layer	Tools
Programming	Python (Pandas, SQLAlchemy, OS)
Database	SQL Server (Views, CASE, TRY_CONVERT, DATEADD, Window Functions)
BI	Power BI Desktop
Languages	Python, SQL, DAX
Modeling	Star Schema, Fact/Dim Tables
📈 Key Metrics Achieved
Metric	Result
Total Rows Processed	120,000+
Fraud Impressions	591
Fraud Percentage	0.49%
Total DAX Measures Created	25+
Duplicate IDs Cleaned	Detected using COUNT() OVER()
Time to Convert SQL + Python Pipeline	~8 minutes
📂 Project Structure
AdTech-Analytics-Project/
│
├── python/
│   └── upload_to_sql.py
│
├── sql/
│   ├── cleaning_scripts.sql
│   ├── eventtime_standardization.sql
│   └── vw_Adtech_Cleaned.sql
│
├── powerbi/
│   ├── dashboard.pbix
│   └── theme.json
│
└── README.md

🔮 Future Enhancements

Build automated pipeline using Airflow

Integrate Azure SQL + Fabric Lakehouse

Add anomaly detection using Python ML

Build real-time dashboard version

🏁 Conclusion

This project showcases an end-to-end enterprise-grade ETL + BI workflow, demonstrating:

✔ Strong Data Analysis skills (Python + SQL)
✔ BI Modeling & Visualization (Power BI)
✔ Analytical storytelling
✔ Ability to handle large messy datasets
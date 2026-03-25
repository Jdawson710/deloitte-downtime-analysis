# 📊 Manufacturing Downtime Analysis (Deloitte Forage Simulation)

## 📌 Project Overview
This project analyzes machine telemetry data from multiple global manufacturing facilities to identify operational inefficiencies and root causes of machine downtime.

The dataset contains one month of telemetry data (May 2021) collected from 4 factories, with machines reporting status updates every 10 minutes.

The objective of this analysis was to answer two key business questions:
- Which factory experienced the most machine breakdowns?
- Which machines contributed most to downtime in that factory?

---

## 🛠 Tools & Technologies
- Tableau (Data Visualization & Dashboarding)
- JSON Data Processing
- Data Analysis & Aggregation
- Business Intelligence Techniques

---

## 📂 Dataset
- Source: Deloitte Forage Data Analytics Simulation  
- Format: JSON  
- Records: ~160,000+ telemetry entries  

### Key Fields:
- Factory  
- Device Type  
- Status (healthy/unhealthy)  
- Timestamp  
- Temperature  

---

## 🔍 Data Preparation
The dataset was loaded into Tableau and prepared for analysis.

A calculated field was created to quantify downtime:

```sql
IF [Status] = "unhealthy" THEN 10 ELSE 0 END

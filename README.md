# ShrimpGuard-IoT-Monitor
# 🦐 ShrimpGuard: IoT Water Quality Monitoring System

**Project Challenge #9:** Shrimp Pond Water-Quality Monitor  
**Team:** [Your Name] & [Partner Name]

## 📌 Project Overview
ShrimpGuard is an end-to-end monitoring system designed to predict shrimp mortality events 48 hours in advance. By analyzing the correlation between Ammonia (NH3) spikes, Dissolved Oxygen (DO) drops, and mortality rates, this system provides actionable "Toxic Event" alerts to farmers.

---

## 🎯 CLO Proofs (Course Learning Objectives)

### ✅ CLO-1: Computational Thinking & Problem Solving
**Problem:** Shrimp mortality is a "lagging indicator"—by the time shrimp die, the water quality has often returned to normal, hiding the root cause.
**Solution:**
* **Abstraction:** We ignored hourly noise and focused on daily maximums.
* **Pattern Recognition:** We identified a consistent **48-hour lag** between toxic spikes and mortality.
* **Algorithm:** Developed the `Origin_Cause` algorithm that scans historical data (T-2 days) to flag "Toxic Events" even when current water conditions look safe.

### ✅ CLO-2: Data Wrangling & Analysis (Power BI)
**ETL Pipeline:**
* Ingested >5,000 rows of simulated sensor data.
* Cleaned date formats to ensure precise time-matching.
* Modeled a **Star Schema** linking `Clean_Sensors` and `Clean_Mortality` via a dynamic `MasterDate` dimension.

**Key DAX Measures:**
* **Anchor Evidence:** `Avg_Ammonia_Level` (Cited from Book Fig 9.3).
* **Intelligence:** `Origin_Cause` logic to categorize daily risk.
* **Visuals:** Decomposition Tree (Root Cause Analysis) & Time-Series Chart (Correlation Proof).

### ✅ CLO-3: Web Development & Cloud Integration
**System Architecture:**
* **Frontend:** Responsive HTML5/CSS3 dashboard hosting the embedded Power BI report.
* **Backend:** Google Firebase (Firestore) for real-time data ingestion.
* **IoT Simulation:** JS-based input form that simulates live sensor readings and triggers "Critical Risk" alerts in the cloud.

---

## 🛠️ Tech Stack
* **Analysis:** Microsoft Power BI, Power Query, DAX
* **Web:** HTML, JavaScript, CSS Grid
* **Database:** Google Firebase (NoSQL)
* **Version Control:** GitHub

---

## 📸 Screenshots
*(You can upload screenshots of your Dashboard and Firebase Console here later)*

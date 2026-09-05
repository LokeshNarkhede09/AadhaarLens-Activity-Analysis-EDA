# AadhaarLens-Activity-Analysis-EDA

AadhaarLens: Where Does Aadhaar Activity Actually Happen? 🔍
📌 Project Overview

AadhaarLens is a data analytics project that analyzes UIDAI Aadhaar enrolment and update data to understand service demand patterns across age groups, geography, and time. The project focuses on identifying where Aadhaar activity is concentrated and understanding the difference between enrolment and update-related demand.

🎯 Problem Statement

Aadhaar service demand is not the same everywhere. Some locations still show high new enrolment, while others mostly generate demographic or biometric update activity.

This project identifies Aadhaar service demand patterns across time, age groups, and geography — and uses them to classify districts as still-growing (need enrolment camps) or already-mature (need update/maintenance camps), with a scan for unusual activity days worth investigating.

📂 Dataset
Source: UIDAI — Aadhaar Enrolment & Update Records
Rows: 94,955
Columns: date, state, district, pincode, age-band enrolment counts (0–5, 5–17, 18+), and age-band demographic/biometric update counts

🛠️ Tools Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook

🔄 Project Workflow
1. Data Understanding
Examined dataset structure and columns
Checked data types
Understood enrolment and update-related variables

3. Data Cleaning
Removed unnecessary columns
Standardized inconsistent state name spellings (e.g. Orissa → Odisha, Pondicherry → Puducherry)
Checked missing values
Checked duplicate records
Converted date column to datetime format
Examined outliers (IQR method)

4. Feature Engineering
Created the following new features:
Total Enrolment
Total Demographic Updates
Total Biometric Updates
Total Updates
Total Aadhaar Activity

5. Exploratory Data Analysis

Univariate Analysis

Analysed overall Aadhaar service demand (enrolment vs demo update vs bio update)
Analysed enrolment across different age groups

Bivariate Analysis

Identified states with the highest Aadhaar activity
Compared enrolment and update demand across states
Analysed Aadhaar activity patterns over time

Multivariate Analysis

Used a correlation heatmap to understand relationships between different Aadhaar enrolment and update activities
📊 Key Insights
Adult (18+) new enrolment is minimal in most records — most adult-related activity today is updates, not new registrations.
A small number of states account for a disproportionately large share of total Aadhaar activity.
Enrolment-heavy states and update-heavy states are not always the same — the two needs are geographically distinct.
Certain dates show unusual spikes/drops in total activity, worth investigating as camps, drives, or possible data issues.


✅ Recommendation

Districts should not be treated uniformly. States/districts still showing strong new-enrolment activity should be prioritized for new enrolment camps, while update-dominated districts should be prioritized for biometric/demographic update camps — making resource planning more targeted and efficient.

📁 Project Structure
text
AadhaarLens/
│
├── data/
│   └── UIDAI_DATASET.csv
│
├── notebooks/
│   └── AadhaarLens_EDA.ipynb
│
└── README.md

▶️ How to Run
Clone this repository
Install dependencies:
   pip install pandas numpy matplotlib seaborn
Open notebooks/AadhaarLens_EDA.ipynb in Jupyter Notebook
Update the dataset path in the pd.read_csv() cell to point to data/UIDAI_DATASET.csv
Run all cells in order

👤 Author
Lokesh Narkhede
Project: AadhaarLens-Activity-Analysis-EDA

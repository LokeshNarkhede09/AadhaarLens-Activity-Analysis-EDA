# AadhaarLens – Aadhaar Activity Analysis & EDA

**Where Does Aadhaar Activity Actually Happen? 🔍**

## 📌 Project Overview

**AadhaarLens** is a data analytics and Exploratory Data Analysis (EDA) project based on UIDAI Aadhaar enrolment and update data.

The project analyzes Aadhaar activity across **age groups, states, districts, and time** to understand where service demand is concentrated.

The analysis focuses on understanding the difference between **new Aadhaar enrolment** and **demographic/biometric update activity**.

---

## 🎯 Problem Statement

Aadhaar service demand is not the same everywhere.

Some locations still have significant **new enrolment activity**, while others mainly generate **demographic and biometric update activity**.

This project aims to:

- Identify Aadhaar activity patterns across different regions.
- Compare enrolment and update demand.
- Analyze Aadhaar activity across different age groups.
- Understand how Aadhaar activity changes over time.
- Identify states and districts with higher service demand.
- Detect unusual spikes or drops in Aadhaar activity.

The analysis can help classify areas as:

- **Growing Areas** – Higher new enrolment activity and potential need for enrolment services.
- **Mature Areas** – Higher update activity and potential need for demographic or biometric update services.

---

## 📂 Dataset

**Source:** UIDAI – Aadhaar Enrolment & Update Records

### Dataset Information

- **Rows:** 94,955
- **Columns:** Aadhaar enrolment and update-related attributes
- **Date:** Date of activity
- **State:** State name
- **District:** District name
- **Pincode:** Location pincode
- **Age Groups:** 0–5, 5–17, 18+
- **Enrolment:** Age-wise Aadhaar enrolment counts
- **Demographic Updates:** Age-wise demographic update counts
- **Biometric Updates:** Age-wise biometric update counts

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 🔄 Project Workflow

### 1. Data Understanding

- Examined the dataset structure.
- Reviewed the available columns.
- Checked data types.
- Understood enrolment and update-related variables.

### 2. Data Cleaning

The dataset was prepared for analysis by:

- Removing unnecessary columns.
- Standardizing inconsistent state names.
- Correcting state name variations such as:
  - Orissa → Odisha
  - Pondicherry → Puducherry
- Checking missing values.
- Checking duplicate records.
- Converting the date column into datetime format.
- Identifying potential outliers using the IQR method.

### 3. Feature Engineering

New features were created to make the analysis easier:

- **Total Enrolment**
- **Total Demographic Updates**
- **Total Biometric Updates**
- **Total Updates**
- **Total Aadhaar Activity**

### 4. Exploratory Data Analysis

#### Univariate Analysis

Analyzed:

- Overall Aadhaar service demand.
- Enrolment activity by age group.
- Demographic update activity.
- Biometric update activity.
- Distribution of Aadhaar activity.

#### Bivariate Analysis

Analyzed relationships between:

- Aadhaar activity and states.
- Enrolment and update activity.
- Aadhaar activity and time.
- Different age groups and enrolment activity.

#### Multivariate Analysis

A **correlation heatmap** was used to understand relationships between:

- Enrolment activity.
- Demographic updates.
- Biometric updates.
- Total updates.
- Total Aadhaar activity.

---

## 📊 Key Insights

### 1. Adult Enrolment Activity

Adult **18+ new enrolment activity is relatively low** in most records.

This suggests that a large portion of adult Aadhaar-related activity is associated with **updates rather than new enrolment**.

### 2. Regional Concentration

A relatively small number of states account for a significant share of total Aadhaar activity.

This shows that Aadhaar service demand is not evenly distributed geographically.

### 3. Enrolment vs Update Demand

States with higher enrolment activity are not always the same states with higher update activity.

This indicates that different regions may require different types of Aadhaar services.

### 4. Activity Over Time

The analysis identified certain dates with unusually high or low Aadhaar activity.

These unusual patterns could potentially be associated with:

- Special enrolment drives
- Update camps
- Government initiatives
- Seasonal activity
- Possible data-quality issues

Such dates can be investigated further to understand the reason behind the unusual activity.

---

## 💡 Recommendations

Aadhaar services should not be planned uniformly across all locations.

### For Enrolment-Heavy Areas

Areas with higher new enrolment activity can be prioritized for:

- New enrolment camps
- Additional enrolment facilities
- Enrolment support staff

### For Update-Heavy Areas

Areas dominated by update activity can be prioritized for:

- Biometric update camps
- Demographic update services
- Update support facilities

This type of targeted planning can help allocate resources more efficiently.

---

## 📁 Project Structure

```text
AadhaarLens/
│
├── data/
│   └── UIDAI_DATASET.csv
│
├── notebooks/
│   └── AadhaarLens_EDA.ipynb
│
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/AadhaarLens-Activity-Analysis-EDA.git
```

### 2. Open the Project Folder

```bash
cd AadhaarLens-Activity-Analysis-EDA
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
notebooks/AadhaarLens_EDA.ipynb
```

### 5. Dataset Path

Make sure the dataset is available at:

```text
data/UIDAI_DATASET.csv
```

If required, update the dataset path in the `pd.read_csv()` cell.

### 6. Run the Notebook

Run all cells in order to reproduce the analysis.

---

## 📌 Key Skills Demonstrated

- Python
- Pandas
- NumPy
- Exploratory Data Analysis
- Data Cleaning
- Feature Engineering
- Data Visualization
- Statistical Analysis
- Outlier Detection
- Correlation Analysis
- Business Insight Generation

---

## 👤 Author

**Lokesh Narkhede**

B.Tech Student | Aspiring Data Analyst

**Project:** AadhaarLens – Aadhaar Activity Analysis & EDA

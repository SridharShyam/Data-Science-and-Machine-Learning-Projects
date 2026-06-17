# 🏥 Health Analytics Dashboard — Power BI

An interactive 2-page business intelligence dashboard analyzing body metric distributions across gender and age groups, built on a 10,000-record health dataset.

📊 **[View Dashboard File →](Health%20Analytics%20Dashboard%20-%20Power%20BI.pbix)**

![Dashboard Screenshot](Health%20Overview.png)
![Dashboard Screenshot](Detailed%20Analysis.png)

---

## 📌 Business Problem

A wellness organization needs to understand how body metrics — height, weight, and BMI — vary across gender and age demographics, in order to design targeted fitness programs and flag high-risk population segments.

---

## 📁 Dataset

| Field | Type | Description |
|---|---|---|
| gender | Text | Male / Female |
| height | Decimal | Height in centimeters |
| weight | Decimal | Weight in kilograms |
| age | Integer | Age in years (18–69) |

- **Records:** 10,000
- **Missing values:** None
- **Gender split:** 50% Male / 50% Female

---

## ⚙️ What I Built

### Power Query (Data Transformation)
- Renamed columns for readability
- Added **BMI** as a calculated column: `Weight / (Height/100)²`
- Added **Age Group** buckets: 18–29, 30–44, 45–59, 60+
- Added **BMI Category**: Normal / Overweight / Obese
- Capitalized gender values for clean labeling

### DAX Measures
```
Avg BMI          = AVERAGE('Table'[BMI])
Total People     = COUNTROWS('Table')
Avg BMI Male     = CALCULATE(AVERAGE('Table'[BMI]), 'Table'[gender] = "Male")
Avg BMI Female   = CALCULATE(AVERAGE('Table'[BMI]), 'Table'[gender] = "Female")
BMI Threshold    = 36.50
High BMI Count   = CALCULATE(COUNTROWS('Table'), 'Table'[BMI] > 36.50)
```

### Dashboard — Page 1: Overview
- 📦 **KPI Card** — Overall Avg BMI (24.75)
- 📊 **Clustered Bar Chart** — Total Height & Weight by Gender
- 🔵 **Scatter Plot** — Height vs Weight distribution by Gender
- 🍩 **Donut Chart** — Population split by Age Group
- 🔢 **Matrix Table** — Avg BMI cross-tabbed by Gender × Age Group
- 🎛️ **Gender Slicer** — filters all visuals simultaneously

### Dashboard — Page 2: Deep Dive
- 📊 **Stacked Bar Chart** — People by Gender and BMI Category (Normal / Overweight / Obese)
- 📈 **Line Chart** — Avg BMI trend by Age and Gender
- 📉 **Histogram** — Height distribution by Gender
- 📦 **KPI Card** — BMI Threshold (36.50)
- 📦 **KPI Card** — High BMI Count (21 people flagged)

---

## 🔍 Key Insights

- 📌 **Females have consistently higher BMI** than males across every age group (25.89 vs 23.61 overall)
- 📌 **60+ females show the highest BMI** at 26.03 — the peak risk segment in the dataset
- 📌 **30–44 males have the lowest BMI** at 23.48 — the fittest demographic group
- 📌 **Overall average BMI is 24.75** — within the healthy Normal range (18.5–24.9)
- 📌 **Only 21 individuals** (< 0.2% of 10,000) exceed the high BMI threshold of 36.50

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Power BI Desktop | Report building, visuals, layout |
| Power Query (M) | Data cleaning, feature engineering |
| DAX | Dynamic measures, threshold flagging |

---

## 📂 Files

| File | Description |
|---|---|
| `Health Analytics Dashboard - Power BI.pbix` | Power BI project file — contains full data, visuals, and DAX measures |
| `Health Analytics Dashboard - Power BI.pbit` | Power BI template — open with the CSV to load full dashboard |
| `Gender_Classification_Data.csv` | Source dataset (10,000 records) |
| `Health Overview.png` | Dashboard Page 1 preview |
| `Detailed Analysis.png` | Dashboard Page 2 preview |
| `README.md` | Project documentation |

> 💡 To open the `.pbit` file: download both the `.pbit` and the CSV → open the `.pbit` in Power BI Desktop → point it to the CSV when prompted.

---

## Credits

Dataset provided by [Sameh Raouf on Kaggle](https://www.kaggle.com/datasets/samehraouf/gender-classification-dataset).

# GLOBAL-CANCER-DASHBOARD
# 🌍 Global Cancer Patient Analytics Dashboard (Power BI)

## 📌 Project Overview
Cancer is one of the leading global health challenges affecting millions of people every year. This project presents a Power BI dashboard that analyzes global cancer patient data to uncover meaningful insights related to survival rates, demographics, treatment costs, and geographic distribution.

The dashboard transforms raw healthcare data into interactive visualizations, enabling better understanding and data-driven decision-making.

---

## 🎯 Objectives
- Analyze global cancer patient data
- Study survival trends and patient outcomes
- Perform age-wise and gender-wise analysis
- Visualize cancer distribution across countries
- Analyze treatment cost patterns
- Identify key risk factors affecting patients
- Demonstrate the use of DAX in data analytics

---

## 📊 Dataset Information

The dataset contains detailed information about cancer patients across different countries.

Attributes included:
- Patient ID
- Age
- Gender
- Country
- Cancer Type
- Cancer Stage
- Survival Years
- Treatment Cost

---

## 🛠 Tools & Technologies
- Microsoft Power BI
- Microsoft Excel
- DAX (Data Analysis Expressions)
- Data Modeling

---

## ⚙️ DAX Formulas Used

### Age Group Classification
AGE WISE = 
IF(global_cancer_patients_2015_2024[Age]<18,"CHILDREN",
IF(global_cancer_patients_2015_2024[Age]<30,"TEENAGE",
IF(global_cancer_patients_2015_2024[Age]<71,"MIDDLE_AGE",
IF(global_cancer_patients_2015_2024[Age]>=70,"SENIOR"))))

### Cancer Type Count
CANCER TYPE = DISTINCTCOUNT(global_cancer_patients_2015_2024[Cancer_Type])

### Survival Rate Classification
SURVIVAL_RATE = 
IF(global_cancer_patients_2015_2024[Survival_Years]<4,"LOW SURVIVAL CHANCE",
IF(global_cancer_patients_2015_2024[Survival_Years]<7,"MEDIUM_LEVEL OF SURVIVAL",
IF(global_cancer_patients_2015_2024[Survival_Years]>=7,"HIGH RATE OF CHANCE")))

### Average Survival Years
SUVIVAL YEARS AVG average per Year 2 = 
AVERAGE(global_cancer_patients_2015_2024[Survival_Years])

### Total Treatment Cost
TOTAL_COST = SUM(global_cancer_patients_2015_2024[Treatment_Cost_USD])

### Total Patient Count
TOTAL_PATIENT = COUNTA(global_cancer_patients_2015_2024[Patient_ID])

---

## 📈 Dashboard Features

### KPI Metrics
- Total Patients
- Total Treatment Cost
- Cancer Types Count
- Countries Covered

### Age-wise Analysis
Patients are categorized into:
- Children
- Teenage
- Middle Age
- Senior

### Cancer Type Distribution
Displays distribution of cancer types using charts.

### Cancer Stage Analysis
Shows patient distribution across Stage I, II, III, IV.

### Survival Analysis
Displays average survival years and survival categories.

### Risk Factor Analysis
Includes:
- Smoking
- Air Pollution
- Genetic Risk
- Obesity
- Alcohol

### Geographic Analysis
Map visualization showing cancer distribution across countries.

### Cost Analysis
Analyzes treatment costs across regions and stages.

---

## 🔍 Key Insights
- Middle-aged population is most affected
- Survival rates decrease with age
- Cancer types are evenly distributed
- Treatment costs are significantly high
- Geographic trends highlight high-risk regions
- Lifestyle factors play a major role

---

## 📸 Dashboard Preview
(Add your screenshots here after uploading images to repository)

---

## 🚀 Future Enhancements
- AI-based cancer prediction models
- Real-time data integration
- Advanced drill-through dashboards
- Patient risk scoring system

---


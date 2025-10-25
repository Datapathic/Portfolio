# 🩺 Medical Insurance Analysis — Power BI Dashboard

### 📘 Objective
Analyze how demographic and behavioral factors (age, BMI, smoking, gender, region) influence U.S. medical insurance charges, using a clean, interactive Power BI dashboard.

---

## 📊 Dataset
- **Source:** Codecademy BI Path / Kaggle Medical Insurance dataset  
- **Rows:** 1,338  
- **Fields:** `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`  
- **Data Model:** Star schema (FactClaims + Dim tables)  
- **Transformations:** Performed in Power Query (age bands, BMI categories, smoker label)

---

## ⚙️ Process Overview
1. **Data Cleaning & Enrichment**
   - Created derived columns for Age Band (`18–25`, `26–35`, …) and BMI Class (`Underweight`, `Normal`, `Overweight`, `Obese`)
   - Added `Smoker Label` (“Smoker” / “Non-Smoker”) and `Risk Group` (Low / Moderate / High)
2. **Data Modeling**
   - Star schema with `FactClaims` (charges) and dimension tables.
   - DAX measures for:
     - `Total Charges`
     - `Avg Charge`
     - `% Smokers`
     - `% Charges from Smokers`
3. **Visualization Design**
   - Built KPI cards and insight-driven charts.
   - Implemented page navigators, bookmarks, and dynamic titles.
   - Consistent theme and UI layout across all pages.

---

## 📈 Dashboard Pages

### 🏠 **Home Page**
Elegant navigation hub guiding users through:
- **Cost Overview**
- **Demographics**
- **Risk Segments**

---

### 💰 **Page 1 – Cost Overview**
**Objective:** Provide an executive summary of overall medical spending.

**Highlights**
- **KPIs:** Total Charges \$17.76M | Avg Charge \$13.27K | % Smokers 20.5% | % Charges from Smokers 49.5%
- **Charts:**
  - Avg Charge by Age Band → *Patients aged 56+ have nearly double the charges of those under 25.*
  - Avg Charge by BMI Class → *Obese patients generate ~50% higher costs than normal-weight individuals.*
  - Share of Charges by Smoking Status & Region → *Smokers contribute nearly half of total expenses.*

---

### 👥 **Page 2 – Demographics**
**Objective:** Analyze how age, BMI, and gender affect medical costs.

**Highlights**
- Line Chart: *Medical charges rise sharply with BMI and age, especially among males.*
- Bar Chart: *Males incur \$1.7K higher average charges than females.*
- Matrix Table: *Obese patients aged 46+ form the costliest demographic group.*

---

### ⚠️ **Page 3 – Risk Segments**
**Objective:** Understand how risk profiles and smoking behavior drive total charges.

**Highlights**
- Stacked Bar: *Smokers show ~25% higher share of charges from obese patients.*
- Treemap: *High and moderate-risk groups account for ~75% of all spending.*

---

## 💡 Key Insights
- **Age & BMI** are the primary cost drivers — charges nearly double after age 50.  
- **Smoking** significantly amplifies costs, responsible for ~50% of total medical charges.  
- **Obese smokers** represent the highest-cost population segment.  
- **Moderate and high-risk groups** account for ~¾ of total healthcare spending.  

---

## 🧰 Tech Stack
- **Tool:** Power BI Desktop  
- **Language / Models:** DAX, Power Query (M)  
- **Visualization:** KPI Cards, Line Charts, Bar Charts, Treemap, Matrix  
- **Design:** Custom color theme, minimal UI with page navigators & dynamic titles  

---

## 📂 Repository Structure
📦 medical-insurance-powerbi
┣ 📂 data
┃ ┗ 📄 insurance.csv
┣ 📂 docs
┃ ┣ 📄 Home_Navigation.png
┃ ┣ 📄 Cost_Overview.png
┃ ┣ 📄 Demographics.png
┃ ┗ 📄 Risk_Segments.png
┣ 📂 pbix
┃ ┗ 📄 Medical_Insurance.pbix
┗ 📄 README.md

---

## 🔗 Links
- **📊 Power BI Dashboard:** [View on Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiZjY5ZWJlODEtNzY4MS00MDFiLTlmZDMtNzY0NTE2YWViZjVhIiwidCI6IjE0MzVkNzQxLTFiYjAtNGE4Ny1hNGIwLWQ0NzIyODY5NDQyNiJ9)
- **📁 Dataset:** [Kaggle – Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)

---

## 🧠 Summary
This project demonstrates advanced Power BI capabilities:
- End-to-end ETL using Power Query and DAX.
- Dynamic storytelling through page navigators and insight-based titles.
- Clear narrative: **From total cost → demographic trends → risk segmentation.**

> 🎓 *Ideal for showcasing analytical storytelling, DAX proficiency, and UI design in a professional Power BI portfolio.*

---


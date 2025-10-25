# 🩺 **Medical Insurance Analysis — Power BI Dashboard**

![Medical Insurance Dashboard](docs/Home_Navigation.png)

> Built with advanced **DAX measures**, optimized **Power Query transformations**, and professional **UI/UX design principles** in Power BI.

---

### 📘 **Objective**
Analyze how demographic and behavioral factors — **age, BMI, smoking, gender, region** — influence U.S. medical insurance charges through an interactive, insight-driven Power BI dashboard.

---

## 📊 **Dataset**
- **Source:** Codecademy BI Path / Kaggle *Medical Insurance Dataset*  
- **Rows:** 1,338  
- **Fields:** `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`  
- **Data Model:** Star schema (`FactClaims` + Dim tables)  
- **Transformations:** Performed in Power Query (age bands, BMI categories, smoker label)

---

## ⚙️ **Process Overview**

### 1️⃣ Data Cleaning & Enrichment
- Created derived columns:  
  - **Age Band:** `18–25`, `26–35`, `36–45`, `46–55`, `56+`  
  - **BMI Class:** `Underweight`, `Normal`, `Overweight`, `Obese`  
- Added:  
  - `Smoker Label` → *Smoker / Non-Smoker*  
  - `Risk Group` → *Low / Moderate / High*  

### 2️⃣ Data Modeling
- Star schema design with **FactClaims** (charges) + Dim tables.
- Key **DAX Measures**:
  - `Total Charges`
  - `Avg Charge`
  - `% Smokers`
  - `% Charges from Smokers`

### 3️⃣ Visualization Design
- Consistent layout and theme across pages.
- Dynamic titles and KPI-based storytelling.
- Custom navigation buttons & icons for intuitive flow.

---

## 📈 **Dashboard Pages**

### 🏠 **Home Page**
Elegant landing page that guides users to:
- **Cost Overview**
- **Demographics**
- **Risk Segments**

---

### 💰 **Page 1 – Cost Overview**
**Objective:** Provide a high-level view of national medical spending.

**Highlights**
- **KPIs:**  
  - Total Charges → **$17.76M**  
  - Avg Charge → **$13.27K**  
  - % Smokers → **20.5%**  
  - % Charges from Smokers → **49.5%**
- **Charts:**
  - *Avg Charge by Age Band:* Patients aged **56+** have nearly **double** the charges of those under 25.  
  - *Avg Charge by BMI Class:* Obese patients generate **~50% higher costs** than normal-weight individuals.  
  - *Charges by Smoking & Region:* Smokers contribute **almost half** of total regional expenses.

---

### 👥 **Page 2 – Demographics**
**Objective:** Explore how **age**, **BMI**, and **gender** impact costs.

**Highlights**
- 📈 *Line Chart:* Medical charges **rise sharply** with age and BMI, especially among males.  
- 📊 *Bar Chart:* Males incur **$1.7K higher** average charges than females.  
- 🧮 *Matrix Table:* Obese patients aged **46+** form the **costliest** demographic segment.

---

### ⚠️ **Page 3 – Risk Segments**
**Objective:** Reveal how **smoking** and **risk profiles** drive total charges.

**Highlights**
- 🟩 *Stacked Bar:* Smokers show **~25% higher** charge share from obese patients.  
- 🟧 *Treemap:* High + Moderate risk groups account for **~75%** of all spending.

---

## 💡 **Key Insights**
**Top Cost Drivers**
- 🧓 **Age:** Charges nearly double after 50.  
- 🚬 **Smoking:** Responsible for ~50% of total medical charges.  
- ⚖️ **BMI:** Obese patients incur ~50% more costs vs. normal-weight.  
- 💰 **High-risk groups:** Account for ~¾ of total healthcare spending.  

---

## 🧰 **Tech Stack**
- **Tool:** Power BI Desktop  
- **Languages / Models:** DAX, Power Query (M)  
- **Visuals Used:** KPI Cards, Line Charts, Bar Charts, Treemaps, Matrices  
- **Design:** Custom theme, dynamic titles, and minimal UI with page navigators  

---

## 📂 Repository Structure

📦 **medical-insurance-powerbi**  
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
- **📊 Power BI Dashboard:** [View on Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiYTM2MGFkMzAtZWNiMS00ZmQyLThmZmYtZjBiNWE5NGQ0YjM3IiwidCI6IjE0MzVkNzQxLTFiYjAtNGE4Ny1hNGIwLWQ0NzIyODY5NDQyNiIsImMiOjl9)
- **📁 Dataset:** [Kaggle – Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **📥 PBIX File:** [Medical_Insurance.pbix](pbix/Medical_Insurance.pbix)

---

## 👤 Author
**Enrique**  
📧 [LinkedIn](https://www.linkedin.com/in/enrique-ardelean-816837394/) | 
[GitHub](https://github.com/Datapathic/Portfolio)  
🎯 *Focus: Data Analysis • Power BI • DAX • Storytelling Dashboards*

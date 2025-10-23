# Medical Insurance Costs — Power BI

## 🎯 Objective
Analyze how age, BMI, and smoking status impact medical insurance charges.

## 🗂️ Dataset
- Source: Codecademy BI Path / Kaggle Insurance dataset  
- Rows: 1,338  
- Fields: age, sex, bmi, children, smoker, region, charges

## ⚙️ Process
1. Cleaned in Power Query (age bands, BMI categories)
2. Built star schema (FactClaims + Dim tables)
3. Created DAX measures for Avg Charge, Smoker vs Non-Smoker %, etc.
4. Designed dashboards with region + demographic filters.

## 📈 KPIs
- Average Charge  
- Avg Charge by Smoker Status  
- Avg BMI  
- Charges per Child  

## 📊 Insights
- Smokers pay ~60 % more on average.  
- BMI > 30 group drives highest costs.  
- Southeast region shows largest average charges.

## 🔗 Links
- [Power BI dashboard](#)  
- [Data Source](#)

## 📎 Files
- `/pbix/insurance_analysis.pbix`
- `/data/insurance.csv`
- `/docs/` screenshots

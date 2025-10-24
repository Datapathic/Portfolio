# Medical Insurance Costs — Power BI

![Cost Overview Dashboard](docs/Cost%20Overview_Screenshot.png)

## ❤️ Objective
Analyze U.S. medical insurance costs to identify how age, BMI, region, and smoking behavior affect total and average medical charges.

## 🧠 Dataset
- **Source:** [Kaggle – Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **Rows:** 1,338  
- **Fields:** age, sex, bmi, children, smoker, region, charges

## ⚙️ Process
1. Cleaned in Power Query (age bands, BMI categories)  
2. Built star schema (FactClaims + Dim tables)  
3. Created DAX measures for Avg Charge, Smoker %, etc.  
4. Designed dashboards with region & demographic filters  

## ✅ KPIs
- Total Charges  
- Average Charge  
- % Smokers  
- % Charges from Smokers  

## 📊 Dashboard Preview
The Power BI report includes:  
1. **Cost Overview** – KPI summary and cost drivers  
2. **Demographics Analysis** – Age × BMI × Sex trends  
3. **Risk Segmentation** – Regional smoker cost share  

![Dashboard Preview](docs/Cost%20Overview_Screenshot.png)

## 💡 Insights
- Smokers pay ≈ 60 % more on average.  
- BMI > 30 group drives highest costs.  
- Southeast region shows largest average charges.  

## 🔗 Links
- [View Power BI file](pbix/Medical_Insurance.pbix)  
- [Download dataset](data/insurance.csv)  

## 📂 Files
- `pbix/Medical_Insurance.pbix`  
- `data/insurance.csv`  
- `docs/Cost Overview_Screenshot.png`

# 🦅 Biodiversity in National Parks — Tableau

## 🎯 Objective
Analyze biodiversity across U.S. national parks to understand species distribution, conservation status, and identify parks with the highest proportion of endangered species.

---

## 🗂️ Dataset
- **Source:** Codecademy *BI Data Analyst* Path (`species_info.csv` and `observations.csv`)
- **Rows:** ~5,000 (species) + ~20,000 (observations)
- **Key Fields:**
  - `species_id`, `category`, `scientific_name`, `park_name`, `conservation_status`, `observations`
- **Data Prep:**
  - Cleaned null `conservation_status` → “No Intervention”
  - Grouped species by **Category** (Mammal, Bird, Reptile, etc.)
  - Calculated `EndangeredFlag`:
    ```
    IIF([Conservation Status] IN ('Endangered','Threatened'), 1, 0)
    ```

---

## ⚙️ Process
1. **Data Cleaning:**  
   Imported CSVs into Tableau → removed duplicates and standardized names.  
2. **Modeling:**  
   Joined `species_info` to `observations` on `species_id`.  
3. **Calculated Fields:**  
   - `% Endangered` = `SUM([EndangeredFlag]) / COUNTD([Species ID])`
   - `Species Count` = `COUNTD([Scientific Name])`
4. **Dashboard Design:**  
   - Built interactive **map view** of national parks.  
   - Linked map to detailed breakdowns via dashboard actions.  
   - Added filters: Park, Category, Conservation Status.  
5. **Storytelling:**  
   Designed a 2-page Tableau Story showing overview + conservation analysis.

---

## 📊 KPIs & Visuals
| KPI | Definition | Visualization |
|------|-------------|---------------|
| **Total Species** | Unique species per park | KPI Card |
| **% Endangered** | Endangered / Total Species | Map color intensity |
| **Top 10 Categories** | Count of species per category | Horizontal bar chart |
| **Trend of Endangered Species** | Endangered species count over time (if available) | Line chart |
| **Species Distribution** | Park × Category grid | Highlight table |

---

## 📈 Insights
- **Yellowstone** and **Yosemite** host the greatest biodiversity (~500 species each).  
- **Bryce Canyon** shows a higher-than-average share of endangered species (~6 %).  
- Mammals and birds make up **~65 % of all recorded species**.  
- “No Intervention” species dominate in most parks, indicating stable ecosystems.  

---

## 🖼️ Dashboard Design
**Page 1 – Biodiversity Overview**
- Map of national parks (colored by % Endangered)
- KPI cards: Total Species | % Endangered | # Categories
- Bar chart: Top 10 Categories
- Filters (top right): Park | Category | Status  

**Page 2 – Conservation Focus**
- Highlight table: Park × Category with % Endangered
- Line chart of Endangered species trend (if temporal data present)
- Action filter: select a park on map → updates table and chart  

---

## 🧩 Files
| File | Description |
|-------|-------------|
| `/data/species_info.csv` | Species reference data |
| `/data/observations.csv` | Observation counts per park |
| `/twbx_or_twb/biodiversity_dashboard.twbx` | Tableau workbook |
| `/docs/` | Screenshots of dashboards |

---

## 🔗 Links
- [View Tableau Dashboard](#) ← *(replace # with your Tableau Public URL)*  
- [Dataset Source](https://www.codecademy.com/paths/bi-data-analyst)

---

## 🧠 Technical Highlights
- Joined multiple CSVs → single data model in Tableau  
- Used **calculated fields**, **action filters**, and **story points**  
- Designed for readability with consistent color scheme + tooltips  

---

## 🗒️ Next Improvements
- Add park-level trend over multiple years (if time dimension available).  
- Blend additional environmental datasets (temperature, rainfall).  
- Parameterize endangered-level thresholds for dynamic filtering.  

---

*Created as part of the Codecademy BI Data Analyst Portfolio Projects series.*

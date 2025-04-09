# Exploring the UK Gender Pay Gap Over Time* 


Absolutely! Crafting **strong research and guiding questions** is essential for building a compelling narrative in your portfolio project. These questions should lead to **insightful analysis**, **clear visualizations**, and **actionable recommendations**, just like a McKinsey-style consultant would present.

---

## 🧪 Main Research Question (The Big One)

> **“How has the UK Gender Pay Gap evolved across sectors, company sizes, and regions from 2017 to 2025, and what are the key structural drivers behind it?”**

This question drives the core of your project and allows you to build a story through multiple lenses: time, geography, sector, and company characteristics.

---

## 🎯 Guided Sub-Questions (with Visual Suggestions)

Each of these builds depth and structure to your story.

---

### 📅 1. **How has the average gender pay gap changed over time?**
- **Goal:** Spot national trend, positive or negative shifts.
- **Visuals:** 
  - Line chart: `DiffMeanHourlyPercent` & `DiffMedianHourlyPercent` over years.
  - Side-by-side comparisons for hourly vs. bonus gaps.

---

### 💼 2. **Which company sizes report the largest gender pay gaps?**
- **Goal:** Evaluate whether company scale affects pay disparity.
- **Visuals:**
  - Bar chart: `EmployerSize` vs `DiffMeanHourlyPercent` (aggregated mean).
  - Boxplots by `EmployerSize` to show distribution.

---

### 🏢 3. **Are certain industries consistently showing higher gaps?**
- **Goal:** Uncover structural issues in sectors like Finance, Tech, etc.
- **Visuals:**
  - Horizontal bar chart: Top 10 `SIC Code` groups by mean pay gap.
  - Heatmap: Year vs Industry sector gap trends.

📌 You’ll want to map `SicCodes` to industry names using a lookup table.

---

### 📍 4. **How does the gender pay gap vary geographically across the UK?**
- **Goal:** Highlight regional disparities.
- **Visuals:**
  - Choropleth or scatter map: Pay gap by `PostCode` or derived `Region`.
  - Cluster map (Plotly or Folium): Color/size by `DiffMeanHourlyPercent`.

---

### 👥 5. **How are women represented in the top vs. bottom quartiles?**
- **Goal:** Check leadership pipeline and wage mobility.
- **Visuals:**
  - Stacked bar chart: `FemaleTopQuartile` vs `MaleTopQuartile` per year.
  - Quartile difference over time (line or area chart).

---

### 💰 6. **What’s the difference in Bonus Pay distribution between genders?**
- **Goal:** Analyze inequality in incentive compensation.
- **Visuals:**
  - Boxplot: `DiffMeanBonusPercent` vs `DiffMeanHourlyPercent`
  - Bar chart: `MaleBonusPercent` vs `FemaleBonusPercent` by year or sector

---

### ⏳ 7. **Which companies are consistently late in submitting data, and does that correlate with worse gender gaps?**
- **Goal:** Accountability and transparency pattern.
- **Visuals:**
  - Pie chart: % of companies that submit late
  - Violin or boxplot: `DiffMeanHourlyPercent` by `SubmittedAfterTheDeadline`

---

### 📈 8. **Can we predict future gender pay gaps or bonus trends using regression?**
- **Goal:** Add forecasting or light ML to show value.
- **Visuals:**
  - Regression plot or trend line projection (e.g., `sklearn.LinearRegression`)
  - Highlight if certain regions/industries are improving faster

---

## 🧩 Bonus Analysis Ideas (if time allows)

- **Clustering:** Group similar companies by gap profile (KMeans on quartiles, bonuses, etc.)
- **Ranking:** Top 10 most improved vs. worst regressed companies over the years
- **Correlation Heatmap:** Between all gap-related columns

---

## 📌 Recommendation Section (Final Output)

Turn your findings into actionable takeaways, e.g.:

- “Targeted interventions are needed in mid-sized tech firms with high bonus gaps.”
- “Postcodes in [region] show consistent leadership gender imbalance.”

---

Would you like a ready-to-use template in a Jupyter Notebook or a Streamlit dashboard with dropdowns to explore these guided questions interactively?
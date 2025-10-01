# Multi-Modal Skin Disease Analysis Power BI Dashboard
## Project Objective
This project utilizes Power BI to analyze a multi-modal dataset for skin disease diagnosis and intervention planning. The dashboard provides a comprehensive view of **disease and death rate trends** (2018–2023), identifies **high-risk demographics** by age and gender, and breaks down the **average patient cost** across multiple skin conditions to support data-driven decisions in healthcare resource allocation.

## Key Questions Answered
This dashboard was designed to answer the following critical questions related to skin disease analysis:

* What are the **mortality and incidence rate trends** for various skin diseases over the 2018–2023 period?
* Which specific skin diseases have the **highest average cost per patient**, making them candidates for cost-efficiency reviews?
* What is the **demographic breakdown** of disease incidence by gender and age group?
* Which patient group (e.g., **age 60+**) is disproportionately affected by the total disease rate?

## Dashboard Preview
<img width="1279" height="712" alt="image" src="https://github.com/user-attachments/assets/7d2956f6-9912-4464-80d2-dd401dc048d8" />

## Analysis Process
This section outlines the technical steps taken in Power BI to transform the raw data into the final dashboard:

### 1. Data Connection & Transformation (Power Query)
* **Source Connection:** Connected to the two source files: `synthetic_skin_disease_dataset.csv` and `skin_disease_awareness_dataset.xlsx`.
* **Data Cleaning:** Performed standardization of columns, ensured date fields were correctly typed, and handled null/missing values.
* **Data Reshaping:** Transformed some columns from wide format to long format (unpivoting) to facilitate easier calculation of rates and trends in DAX.

### 2. Data Modeling & DAX
* **Relationships:** A simple star schema (or equivalent) was established to relate the main metrics table to any lookup tables (if applicable).
* **Key Measures (DAX):** Created explicit measures to calculate the key metrics displayed on the dashboard:
    * `Sum of Death_Rate_per_100k`
    * `Sum of Disease_Rate_per_100k_or_pct`
    * `Sum of Avg_Cost_per_Patient_USD`

### 3. Report Design
* Visualizations were chosen to clearly represent trends (Line Charts for time series) and distribution (Bar Charts for demographics, Pie/Donut Chart for cost distribution).

## Key Findings & Insights
Based on the visual analysis, the following are the primary insights:

* **Overall Disease Trend:** The total skin disease rate shows a volatile trend, with notable dips in 2020 and 2022 and a significant peak in 2023, suggesting recent increases in reported cases.
* **Cost Drivers:** Fungal Skin Diseases and Rosacea represent the highest average patient cost, at $491.59K (14.27%) and $478.28K (13.86%) respectively, highlighting them as critical areas for cost efficiency review.
* **Most Affected Demographic:** The 60+ age group shows the highest disease rate across all conditions combined, underscoring the necessity of targeted interventions for older adults.
* **Gender Distribution:** While gender percentages are relatively balanced overall, specific conditions like Rosacea and Psoriasis show a slightly higher rate in one gender versus others, which may warrant further investigation.
* **Mortality Trend:** The death rate per 100K peaked across most skin diseases around 2021 and has generally maintained a high, albeit slightly declining, trend since then.

## Final Conclusion & Recommendations
The analysis provides clear direction for healthcare stakeholders, translating data insights into actionable strategies:

1.  **Cost Efficiency Review:** Immediate investigation is recommended for the treatment protocols of **Fungal Skin Diseases** and **Rosacea** to identify opportunities for cost reduction, as they are the highest-cost drivers.
2.  **Targeted Campaigns:** Given the significantly higher incidence rate in the **60+ age group**, public health and awareness campaigns should be specifically targeted toward this demographic.
3.  **Resource Allocation:** The volatile nature of the disease rate (spiking in 2023) and the high mortality rates (peaking in 2021) suggest a need for continuous monitoring and flexible resource allocation to handle sudden increases in demand.

## 🔗 Live Interactive Dashboard
You can view and interact with the full, live report here:
**https://app.powerbi.com/reportEmbed?reportId=0fce1c3e-18da-447c-ba5c-00757d3574b2&autoAuth=true&ctid=70de1992-07c6-480f-a318-a1afcba03983**



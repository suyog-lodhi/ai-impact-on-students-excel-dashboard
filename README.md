# AI Impact on Students
📊 *2026 Excel Project*

## 📌 Project Overview
A single-page Excel dashboard analyzing how Generative AI tools
affect academic performance, burnout risk, and skill retention
among 50,000 students across multiple majors and academic years.

## 📜 Problem Statement
Does AI adoption genuinely help students academically — or does
it come at a hidden cost to their long-term learning and wellbeing?

## 🗃️ Dataset
- **Source:** Kaggle — AI Impact on Students Dataset
- **Coverage:** 50,000 Students | 5 Major Categories | 5 Academic Years
- **Columns analyzed:** 16 raw variables + 7 calculated columns

## 🛠️ Tools Used
| Tool | Purpose |
|---|---|
| Microsoft Excel | Single-page dashboard, pivot tables, pivot charts |
| Power Query | Data cleaning, 7 calculated columns (ETL layer) |
| Power Pivot | Data Model setup, DAX measures |
| DAX | 5 KPI measures for dynamic KPI cards |

## ✅ Key Findings

**1️⃣ The Retention Trap**
Skill retention drops sharply as AI usage intensifies —
Severe users score 65.7 vs 76.6 for Moderate users,
a 10.9 point decline. More AI hours = better grades
short term, worse learning long term.

**2️⃣ Burnout Crisis Among AI-Dependent Learners**
AI-Dependent Learners show 51% high burnout rate vs
just 11% for Traditional Learners — nearly 5x higher.
Heavy AI reliance amplifies academic stress rather
than reducing it.

**3️⃣ 1 in 6 Students Are in Critical Risk Zone**
17.3% of students (8,650 out of 50,000) simultaneously
show High burnout AND high AI dependency. More than half
the student population shows some level of AI-related risk
when Watch category (18,532) is included.

**4️⃣ Most Students Are Not Benefiting Meaningfully**
73% of students are Stable — GPA neither improved nor
declined significantly. Only 22% are genuine Improvers.
AI effectiveness depends heavily on HOW it is used,
not just THAT it is used.

**5️⃣ Students Use AI for Tasks, Not Learning**
Debugging/Troubleshooting (25%) and Copywriting/Drafting (24%)
account for nearly 49% of all AI usage. Students are
optimizing for output, not understanding — directly
explaining the skill retention decline.

**6️⃣ GPA Improvement Is Real But Modest**
Overall average GPA Gap is +0.20 points at 8.4 hrs/week
average AI usage. The risk-reward ratio worsens significantly
as usage crosses into High/Severe territory.

## 📊 Dashboard Preview

### Single Page Dashboard
<img width="1872" height="801" alt="Screenshot 2026-06-20 141813" src="https://github.com/user-attachments/assets/e4771adf-68a9-4c68-944d-d7de882696cb" />


## 🧮 Calculated Columns (Power Query)

| Column | Logic |
|---|---|
| GPA_Gap | Post_Semester_GPA − Pre_Semester_GPA |
| AI_Intensity | Buckets Weekly_GenAI_Hours → Low / Moderate / High / Severe |
| Performance_Tag | GPA_Gap > 0.1 → Improver / < -0.1 → Decliner / else Stable |
| Risk_Profile | Burnout=High AND Dependency≥4 → Critical / either → Watch / else Safe |
| Study_Balance_Ratio | AI Hours / (AI Hours + Traditional Hours) × 100 |
| Learners | Traditional / Hybrid / AI-Dependent / Low Engagement based on dataset averages (8.42 AI hrs, 11.2 traditional hrs) |
| IsHighBurnout | 1 if Burnout_Risk_Level = High, else 0 (DAX flag column) |

## 📐 DAX Measures (Power Pivot)

| Measure | Purpose |
|---|---|
| Avg GPA Gap | Core outcome metric |
| Avg Weekly AI Hours | Usage intensity benchmark |
| Critical Risk % | % students with High burnout AND high dependency |
| Avg Skill Retention | Long-term learning quality score |
| High Burnout % | % students at High burnout risk |

---

# 📂 Repository Structure
```
├── 01_Data
│   └── 01_Raw_data
│   └── 02_Working_data
│
├── 02_Dashboard
│   └── AI_Impact_Students.xlsx
│
├── 03_Images
│   └── Dashboard_preview.png
│
└── README.md
```

## 🧮 Analytical Approach
- Data cleaning and type standardization via Power Query
- 7 calculated columns engineered from raw variables
- Data Model built in Power Pivot with 5 DAX KPI measures
- Single-page dashboard with 5 KPI cards, 6 pivot charts,
  3 interactive slicers (Major, Year of Study, AI Intensity)
- Data Dictionary sheet documenting all 23 columns
- Insights sheet with 6 key findings and recommendations

## ❗ Data Limitations
- Dataset is synthetic/Kaggle-sourced — findings are
  analytical in nature, not from a real institutional study
- Burnout and dependency scores are self-reported —
  subject to perception bias
- GPA Gap reflects one semester only — long-term trends
  may differ

---

# 👨‍💻 Author

**Suyog Lodhi**<br/>Aspiring Data Analyst | Excel | SQL | Power BI

🔗 LinkedIn: www.linkedin.com/in/suyog-lodhi-94a45825a

# California Community College Enrollment Trends (2016–2024)

## Overview  
This exploratory data analysis (EDA) examines enrollment trends across California Community Colleges (CCC) from 2016 to 2024 using publicly available data from the California Community Colleges Chancellor’s Office (CCCCO) [Data Mart](https://datamart.cccco.edu/datamart.aspx).  

The analysis examines how total enrollment changed before, during, and after the COVID-19 pandemic while tracking shifts across student demographics such as age, gender, and ethnicity. It also looks at enrollment type differences—full-time versus part-time students—to understand how learning preferences and participation patterns evolved over time.

Through visualizations and year-over-year comparisons, this project highlights recovery trends, demographic shifts, and possible implications for statewide access to higher education. The goal is to provide clear insights that can inform strategies around student engagement, retention, and targeted access across California’s community college system.

### Objectives  
- Observe enrollment trends over eight academic years to identify overall growth or decline  
- Assess the impact of the COVID-19 pandemic on statewide enrollment and recovery patterns  
- Compare demographic changes by age, gender, and ethnicity  
- Explore differences in enrollment types (full-time vs. part-time)  
- Provide insights that can inform strategies to improve access, engagement, and retention  

## Table of Contents  
- [Project Background](#project-background)
- [Data Structure Overview](#data-structure-overview)
- [Executive Summary](#executive-summary)
- [Insights Deep Dive](#insights-deep-dive)
- [Recommendations](#recommendations)

## Project Background  
The California Community Colleges Chancellor’s Office (CCCCO) provides detailed statewide data on students, faculty, staff, and institutional outcomes. The dataset includes information on student demographics, enrollment status, academic programs, and course participation across all 116 community colleges.  

This project draws on Data Mart’s term-level enrollment data to analyze academic years 2016–2017 through 2023–2024. 

### Data Structure Overview  
**Source**: CCCCO [Data Mart](https://datamart.cccco.edu/datamart.aspx).  
**Period Covered**: 2016–2017 to 2023–2024 academic years  
**Format**: CSV file containing term-level and demographic-level enrollment data  

**Key Fields**:  
- Academic Year  
- Term  
- College  
- Gender  
- Age Group  
- Ethnicity  
- Full-/Part-Time Status  
- Headcount  

**Tools and Techniques**:  
- **Python Libraries:** Pandas, NumPy, Matplotlib, Seaborn  
- **Data Cleaning:** Handling missing values, correcting data types, and normalizing demographic categories  
- **Visualization:** Time series plots, demographic distributions, and heatmaps for enrollment shifts  


 
## Executive Summary

### Systemwide Trends  
- Total statewide enrollment fell from about **4.01 million students in 2019** to **3.42 million in 2021**, a **14.7% decline** during the height of the COVID-19 disruption.  
- By **2024**, enrollment climbed back to roughly **3.90 million**, a **13.8% increase** from the 2021 low point but still about **2.8% below** the 2019 baseline.

### Year-over-Year Observations  
- Enrollment decreased from **2019–2022 (-0.9%, -6.1%, -9.1%, -2.7%)** and then rebounded with **+9.6% (2023)** and **+6.8% (2024)**.  
- Year-over-year change turned positive in **2023 (+9.6%)** and remained strong in **2024 (+6.8%)**, showing clear recovery momentum.

### Term-Level Patterns  
- **Fall** and **Spring** saw the sharpest declines between 2020–2022, followed by steady growth through 2024.  
- **Spring 2022** was the lowest enrollment point (1.27M), while **Fall 2023–2024** show the strongest recovery.  
- **Summer** remained stable throughout the pandemic, consistently making up **~19–21%** of yearly enrollment.  

### Student Status Overview  
- Enrollment by student status shows that **Continuing Students** remain the largest group but also experienced the steepest pandemic-related decline. Their enrollment fell from **2.41 million (2019)** to **1.96 million (2021)** (–18.8%) and has only partially recovered to **2.07 million in 2024**, still **14% below** pre-pandemic levels.

In contrast, **First-Time**, **First-Time Transfer**, and **Returning Students** recovered much faster.  
- First-Time and Transfer student counts in 2024 are within **2%** of 2019 levels.  
- Returning Students nearly fully rebounded to **424,985 (2024)**, matching 2019 levels.  
- **Special Admit Students** (dual enrollment) grew continuously, rising **63%** from **2019 to 2024**, the strongest increase of any status category.

The **ratio of new students to continuing students** increased from **0.31 (2019)** to **0.36 (2022–2024)**, indicating that new student enrollment has become a relatively larger contributor to systemwide recovery.

### Demographic Insights  
- **Hispanic/Latino students** remain the largest group, rising from **46.7% (2019–2020)** to **48.3% (2023–2024)**.  
- Headcount fell from **1,027,693** to **861,713** between 2019–2020 and 2021–2022 (**-16.2%**) before rebounding above **1.02 million**.  
- **Asian students** declined around **16.8%** from 2019–2020 to 2021–2022, and **White Non-Hispanic students** declined **14.4%** over the same period.  
- **Female students** consistently make up the largest gender group, followed by **Male**; **Non-Binary** and **Unknown** categories remain small but are slowly increasing.  

### Age-Group Patterns  
- Students **19 or younger** surpassed pre-pandemic levels, rising **6.2%** from 2019–2020 to 2023–2024.  
- Students aged **20–24** and **25–29** remain **17–18% below** pre-pandemic levels even by 2023–2024.  
- Students **50+** experienced the steepest pandemic drop (**-27.7%** by 2021–2022) and remain about **9% below** 2019–2020 levels.  

### Top 5 Colleges by 2024 Enrollment  
Based on systemwide totals combined across Fall, Spring, and Summer terms:  

1. **Mt. San Antonio College** – **115,270** students *(+7.64% YoY)*  
2. **Santa Ana College** – **102,073** students *(+9.92% YoY)*  
3. **East Los Angeles College** – **91,786** students *(+7.55% YoY)*  
4. **Bakersfield College** – **81,232** students *(+6.30% YoY)*  
5. **American River College** – **74,710** students *(+6.66% YoY)*  

These colleges collectively represent about **11.9% of the statewide total (465,071 out of 3.89 million in 2024)**.  


### Conclusion  
Although California’s community college system has not fully returned to pre-pandemic levels, **younger students and large urban colleges are driving recovery**, while **adult learners and returning students continue to decline**. Ongoing recovery will depend on targeted outreach, flexible learning options, and equity-driven strategies that address demographic and regional disparities.  



---
## Insights Deep Dive  

### 1. Pandemic Shock and Recovery Trajectory  
The statewide dataset shows a clear before-, during-, and after-pandemic pattern. Total enrollment declined from **4.01 million in 2019** to **3.42 million in 2021**, a loss of **585,000 students** (–14.7%). The steepest single-year decline occurred between **2020 → 2021**, when enrollment dropped another **9.1%**.

Recovery followed immediately after the 2021 low point:  
- **2022:** 3.33M → 3.36M (slight stabilization)  
- **2023:** Jump to **3.68M** (+9.6%)  
- **2024:** Further increase to **3.90M** (+6.8%)  

By 2024, enrollment regained **about 460,000 students** from the low point, but total headcount remains **2.8% below 2019**.

### Key Takeaways  
- Pandemic losses were deep and concentrated in 2020–2021.  
- The rebound from 2021–2024 is strong but not complete.  
- Recovery is uneven across different student demographics and statuses. 

---

### 2. Seasonal Trends Across Fall, Spring, and Summer  .

### Fall  
- **Fall 2019:** 1.51M students  
- **Fall 2020:** 1.41M (–6.6%)  
- **Fall 2021:** 1.36M (–3.7%)  
- **Fall 2024:** **1.58M** (highest value in the post-pandemic period)  

### Spring  
- **Spring 2020:** 1.41M  
- **Spring 2021:** 1.37M  
- **Spring 2022:** **1.27M** (lowest point of any major term)  
- **Spring 2024:** **1.52M**, surpassing pre-pandemic levels  

### Summer  
- **Summer 2019:** 786,000  
- **Summer 2022:** **680,407** (lowest summer value)  
- **Summer 2024:** **832,000**, returning to growth  

Summer terms stayed the **most stable**, consistently making up about **19–21%** of annual enrollment, suggesting flexible sessions helped students stay engaged even during the pandemic.

### Key Takeaways  
- Fall and Spring experienced the most significant disruptions.  
- Summer demonstrated resilience and maintained consistent.  
- By 2024, all three terms show strong recovery, with Spring rebounding the fastest (**1.52M**).  


---

### 3. New vs. Continuing Student   
Using First-Time + First-Time Transfer students compared to Continuing Students:

#### Annual Totals (selected years)
- **2019:**  
  - New Students: 749,891  
  - Continuing Students: 2,408,908  
  - Ratio = **0.31**

- **2021 (pandemic low):**  
  - New Students: 648,559  
  - Continuing Students: 1,956,506  
  - Ratio = **0.33**

- **2024:**  
  - New Students: 735,279  
  - Continuing Students: 2,065,625  
  - Ratio = **0.356**

Across all years, the system averages **about 3 new students for every 10 continuing students**.

The rise from **0.31 → 0.36** after the pandemic shows the **new student enrollment recovered faster than continuing student persistence**.

#### Key Takeaways  
- New student volumes (first-time + transfers) recovered quickly.  
- Continuing student losses drive most of the systemwide decline.  
- Improving persistence will be essential to full enrollment restoration.  


---

### 4. Ethnicity Trends and Equity Patterns  
Demographic analysis shows both disparities in the pandemic decline and differences in the recovery trajectory.

#### Hispanic/Latino  
- **2019–2020:** 1,027,693 students  
- **2021–2022:** 861,713 (–16.2%)  
- **2023–2024:** ~1.02M (full recovery)  
- Share of statewide enrollment grew from **46.7% → 48.3%**

#### White (Non-Hispanic)  
- Fell from **~514,000 → ~440,000** between 2019–2021 (–14%).  
- Recovery modest; still below pre-pandemic levels.

#### Asian  
- Fell **~17%** during the pandemic low; recovery ongoing but not fully restored.  

#### African-American  
- Declines persisted longer, with only partial recovery by 2024.  

#### Key Takeaways  
- Hispanic/Latino students rebounded fastest and now form nearly half the system.  
- White, Asian, and African-American students remain below pre-pandemic levels.  
- Demographic recovery is uneven and tied to broader equity challenges.  


---

### 5. Age Structure and Adult Learner Dynamics  
Age-based trends highlight which groups returned to college — and which didn’t.

#### Age 19 or Younger  
- Increased **+6.2%** from 2019–2024  
- Fully above pre-pandemic levels  

#### Age 20–24  
- Dropped sharply in 2020–2021 (20%+ declines)  
- Still **~17% below** 2019–2020 levels  

#### Age 25–29  
- Similar pattern to 20–24  
- Remains **~18% below** pre-pandemic participation  

#### Ages 30–49  
- Moderate declines with steady recovery  
- Not yet fully restored but trending upward  

#### Age 50+  
- Largest proportional decline (–27.7% at the low point)  
- Still **~9% below** pre-pandemic levels in 2024  
- Represents the most challenging group to re-engage  

#### Key Takeaways  
- Youth enrollment is leading the system’s recovery.  
- Working-age adults (20–49) remain significantly below their pre-pandemic levels.  
- Adult and older adult learners (50+) face the steepest re-entry barriers.  

---

## Recommendations

### 1. Re-Engage Adult and Working-Age Learners  
- Prioritize outreach to students in the **20–29** and **50+** groups since they’ve had the slowest recovery.  
- Offer more evening, weekend, short-term, and non-credit courses that fit around work and family schedules.  

### 2. Strengthen Recruitment for New Students  
- Keep building on the growth in new students by supporting dual enrollment and first-year onboarding programs.  
- Make sure new students get early advising and support so they’re more likely to stay enrolled.  

### 3. Support Persistence with Early Intervention  
- Use early-alert tools and predictive indicators to catch students who may be close to dropping out.
- Connect students to financial aid help, academic counseling, and basic-needs resources before issues escalate.  

### 4. Improve Equity for Hispanic/Latino and Underrepresented Students  
- Use more culturally responsive outreach and support strategies that reflect the needs of the communities being served.  
- Work with local organizations to help students get access to aid, tutoring, transfer guidance, and other support.  

### 5. Direct Resources Where They’re Needed Most  
- Focus support on colleges and districts that are recovering the slowest.  
- Look at what high-recovery colleges (like Mt. SAC, Santa Ana, and East LA) are doing well and see what practices can be applied statewide.  





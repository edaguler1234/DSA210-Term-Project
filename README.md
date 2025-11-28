# DSA210-Term-Project
**Topic:** **Screen Time Analysis**  
**Course:** DSA210 - Introduction to Data Science (Fall 2025)  
**Student:** Eda Güler

#Project Motivation

Digital devices occupy a large part of our daily lives. Understanding how and why our screen usage changes can provide valuable insight into productivity, attention, and well-being.  

This project aims to **analyze my daily screen time data** collected from my digital devices using Screen Time.  
By combining this data with contextual variables (such as exam days, trips, or social activities), I aim to identify if there are routines and build a **machine learning model** that can predict future screen time behavior (after data collection phase, I will continue to record my daily data to see if predictions are going to match with the real data).

The ultimate goal is to evaluate how accurately such a machine can estimate my real-world screen habits and what factors most influence digital usage.

## Objectives   
- Collect and organize daily screen time data from my iPhone (iPad may also be added).  
- Perform **data cleaning** and **exploratory data analysis (EDA)** to identify behavior trends.  
- Enrich the dataset with **contextual variables** like exams, trips, and activity days etc..  
- Apply **hypothesis testing** to analyze differences across contexts.  
- Apply **machine learning models** to predict daily screen time.  
- Compare **predicted vs actual values** and interpret influencing factors.

## Data Collection  
### Data Source  
All data will be collected manually from **Apple Screen Time** on my iPhone (Settings/ Screen Time/ See All Activity).  
Since Apple does not allow direct exports, data will be recorded daily in a CSV file following a structured format. 

### Data Structure
The .CSV file will contain this format:

| Variable | Description | Type |
|-----------|-------------|------|
| date | Observation date | Date |
| total_minutes | Total screen time in minutes | Numerical |
| social_minutes | Time spent on social apps | Numerical |
| productivity&finance_minutes | Time spent on productivity or finance apps | Numerical |
| entertainment_minutes | Time spent on entertainment apps | Numerical |
| creativty_minutes | Time spent on creativity apps | Numerical |
| travel_minutes | Time spent on travel apps | Numerical |
| shopping&food_minutes | Time spent on shopping or food apps | Numerical |
| reading_minutes | Time spent on reading apps | Numerical |
| games_minutes | Time spent on game apps | Numerical |
| other_minutes | Time spent on apps which belong to other areas | Numerical |
| notifications | Number of notifications received | Numerical | 
| pickups | Number of device pickups | Numerical |
| exam day | 1 if exam day, else 0 | Binary |
| activity | 1 if exercise/social activity day, else 0 | Binary |
| weekend | 1 if weekend, 0 otherwise | Binary |

## Methods
### 1. Exploratory Data Analysis (EDA)

The EDA explores my daily screen time patterns across different categories such as social media, productivity, entertainment, creativity, games, and others. The goal of this section was to understand the general behavior of my screen usage and identify early patterns that could support later hypothesis testing and modeling.

#### Key Findings

1. **Daily Screen Time Trends**  
   A line plot of total screen time across the recording period shows fluctuations from day to day, with certain peaks likely related to weekends or days without academic responsibilities.

2. **Category-Level Behavior**  
   Different categories (social, productivity, entertainment, creativity, games, etc.) show distinct usage patterns. Productivity and social categories tend to make up most of the total screen time, while categories like creativity and reading remain relatively low.

3. **Notifications and Pickups**  
   Scatter plots reveal a weak but noticeable positive relationship between:  
   - notifications and total screen time  
   - device pickups and total screen time  
   This suggests that more frequent phone interactions are associated with higher usage, although the correlation is not very strong.

4. **Correlation Analysis**  
   A correlation heatmap shows meaningful relationships among screen time categories. Productivity minutes negatively correlate with social and entertainment minutes, while total screen time is strongly influenced by categories like productivity, games, and other usage.

5. **Normal vs Special Days**  
   Days labeled as Normal Days (no exam and no activity) show higher usage in several categories compared to Special Days (exam or activity days). Special Days generally show lower screen time, especially in productivity and social categories.

6. **Category Comparison Around Exams**  
   By examining screen time categories separately, patterns emerge that align with later hypothesis testing. Productivity appears higher before exams, which supports the idea of increased study behavior.

#### Summary

The EDA provides a clear overview of my screen time habits and highlights several important behavioral patterns. These insights motivated the hypothesis that productivity usage changes around exam periods and guided the development of the statistical tests performed in the next section.

### 2. **Hypothesis Testing**

This section analyzes whether productivity-related screen time changes around exam days. Since productivity apps often reflect study activity, I expected productivity to increase before exams and decrease afterward.

#### Hypotheses
- **H₀ (Null Hypothesis):**  
  There is no difference in productivity screen time between *Before Exam*, *Exam Day*, and *After Exam* days.

- **H₁ (Alternative Hypothesis):**  
  Productivity screen time is higher before an exam and lower on the exam day and the day after.


#### Methodology

1. Each day in the dataset was labeled as one of the following based on exam timing:
   - Before Exam  
   - Exam Day  
   - After Exam  

2. The mean productivity screen time was compared across these three groups.

3. Two statistical tests were applied:
   - **One-Way ANOVA** to test for overall differences among the groups.
   - **Tukey HSD Post-Hoc Test** to identify which specific pairs of groups differ.

These steps follow the hypothesis testing methods introduced in the DSA210 course.


#### Results

##### One-Way ANOVA
- F-statistic: 8.56  
- p-value: 0.000744  

Since the p-value is below 0.05, the null hypothesis is rejected.  
This indicates that the groups differ significantly.

##### Tukey HSD Post-Hoc Test
The Tukey analysis shows statistically significant differences between:

- Before Exam vs Exam Day  
- Before Exam vs After Exam  
- Exam Day vs After Exam  

## Conclusion

The results support the alternative hypothesis. Productivity screen time is higher before an exam, likely due to increased study activity, and decreases both on the exam day and on the day after. This suggests a clear behavioral pattern in how productivity-related screen time shifts around exam periods.

### 3. **ML Model**  
- **Goal:** Predict daily total minutes and how it is spent (e.g. 1 hour fot entartainment, 30 minutes for productivity etc.)
- **Features:** notifications, pickups, sleep hours, exam day, trip day, activity day, weekend etc.
- **Evaluation:**  Errors are going to be evaluated with predicted vs actual data.

## Expected Results  
- Cleaned dataset (data/screen_time_log.csv)  
- EDA and correlation visuals (various plots)  
- Statistical test results
- ML model accuracy/performance 
- Visualization of **actual vs predicted screen time**  
- Discussion of factors that influence daily screen usage  

## Project Timeline  
| Phase | Description | Deadline |
|-------|--------------|-----------|
| **Phase 1** | Project proposal | **Oct 31, 2025** |
| **Phase 2** | Data collection & EDA | **Nov 28, 2025** |
| **Phase 3** | ML implementation | **Jan 2, 2026** |
| **Phase 4** | Final report & submission | **Jan 9, 2026** |







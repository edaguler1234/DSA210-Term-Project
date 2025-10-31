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
| total minutes | Total screen time in minutes | Numerical |
| social minutes | Time spent on social apps | Numerical |
| productivity minutes | Time spent on productivity apps | Numerical |
| entertainment minutes | Time spent on entertainment apps | Numerical |
| notifications | Number of notifications received | Numerical |
| pickups | Number of device pickups | Numerical |
| sleep hours | Total sleep hours (from Apple Health) | Numerical |
| exam day | 1 if exam day, else 0 | Binary |
| trip | 1 if travel/vacation day, else 0 | Binary |
| activity | 1 if exercise/social activity day, else 0 | Binary |
| weekend | 1 if weekend, 0 otherwise | Binary |
| phase | Control (normal) or experiment (e.g., notification limit) | Categorical |

## Methodology  
### 1. **Exploratory Data Analysis (EDA)**  
- Visualize screen time distribution and weekly patterns.  
- Compute correlations between screen time and contextual variables.  
- Examine behavioral differences between control and experimental phases.  
- Identify outliers and trends in daily activity.  

### 2. **Hypothesis Testing**  
- Example:  
  - H₀: Average screen time on exam days equals average screen time on regular days.  
  - H₁: Average screen time on exam days is lower.  
- Apply hypothesis tests where appropriate.

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




  






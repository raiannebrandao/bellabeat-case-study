# bellabeat-case-study
Google Data Analytics Capstone: Fitbit data analysis and insights for Bellabeat

## 📌 Project Overview
This case study is part of the **Google Data Analytics Capstone project**.  
The goal is to analyze **Fitbit smart device data** to identify user behavior patterns and provide insights that could be applied to **Bellabeat’s Time smart watch**.  

Bellabeat wants to understand how consumers use non-Bellabeat smart devices and leverage these insights to shape its **marketing strategy**.

---

## 🎯 Business Task
1. Identify trends in smart device usage.  
2. Apply these trends to Bellabeat customers.  
3. Recommend marketing strategies for Bellabeat based on the findings.

---

## 📂 Data Source
- Dataset: [Fitbit Fitness Tracker Data (Kaggle)](https://www.kaggle.com/datasets/arashnic/fitbit)
- 30 users, tracked daily activity, sleep, weight, and heart rate.  
- Limitation: Small sample size, missing stress and menstrual cycle data, ~40% missing timestamps in sleep logs.

---

## 🛠️ Tools Used
- **Google BigQuery** → SQL queries & data cleaning  
- **Google Sheets** → Data exploration  summary stats & Visualization 
- **PowerPoint** → Final presentation slides  

---

## 🔄 Process

### 1. Data Cleaning & Preparation
- Converted timestamps from `MM/DD/YYYY hh:mm:ss` to `YYYY-MM-DD hh:mm:ss`.
- Handled missing values in sleep logs (~40% missing timestamps).
- Uploaded cleaned datasets to BigQuery.

### 2. Queries & Analysis
- Calculated average **steps, calories, sedentary minutes**.  
- Aggregated **sleep data per user/day**.  
- Classified sleep patterns into categories:  
  - Short sleep (<6h)  
  - Normal sleep (6–9h)  
  - Long sleep (>9h)  
- Compared patterns across **days of the week**.  

*(See full SQL queries [here](queries.md))*

---

## 📊 Key Findings

### 🔹 Sleep
- Average sleep: **6h33min** (below recommended 7–9h).  
- ~25% of nights classified as **short sleep (<6h)**.  
- More sleep on Sundays (7h34), less on Mondays (6h36).  
- **Insight**: Sleep is inconsistent, worse at the start of the week.

### 🔹 Physical Activity
- Average steps: **6,547** → below recommended **7,000–8,000**.  
- Sedentary minutes: ~16h30/day (!!).  
- Most activity is **light** (~170 min/day); very little moderate/intense exercise.  
- **Insight**: Users are highly sedentary, with insufficient vigorous activity.

### 🔹 Weekly Patterns
- **Best day**: Wednesday → highest steps & reasonable sleep.  
- **Worst day**: Tuesday → lowest steps & poor sleep.  
- **Sunday**: longest sleep, but lowest activity.  
- **Insight**: Clear weekly cycle → struggles at start of week, recovery mid-week.

---

## 💡 Business Insights & Marketing Recommendations
- **Position Bellabeat Time as a lifestyle coach**:  
  Not just tracking, but motivating consistent habits.  

- **Target sleep & activity consistency**:  
  - Push notifications on Mondays (“Recover your sleep”)  
  - Movement reminders on Thursdays/Fridays (“Stand up & stretch!”)  

- **Gamification & challenges**:  
  Weekly challenges like “8,000 steps on Wednesday” or “7h of sleep on Monday night”.  

- **Highlight automatic tracking**:  
  Users rarely log activities manually → emphasize effortless tracking as a product feature.  

---

## 🎥 Presentation Slides
👉 [See my presentation here](./Fitbit%20Data%20Analysis.odp)  

---

## ✨ Key Takeaways
- Smart device data reveals **clear trends** in sleep and activity.  
- Bellabeat can use these patterns to design **personalized interventions**.  
- Marketing should focus on **consistency, motivation, and education**.  

---

## 🤝 Acknowledgments
This project was guided by the **Google Data Analytics Capstone** framework.  
I also leveraged resources such as **ChatGPT** to brainstorm insights and refine queries, reflecting real-world usage of AI tools in data analysis.  

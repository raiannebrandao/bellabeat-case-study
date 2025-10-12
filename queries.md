# SQL Queries – Bellabeat Case Study

This file contains the SQL queries used for analyzing Fitbit data in the **Google Data Analytics Capstone Project**.  
The queries were run in **BigQuery** to clean, explore, and generate insights from the dataset.  

---

## 1. Checking the number of distinct users
```sql
SELECT DISTINCT Id
FROM `fitbit_data.daily_activity`;
````

## 2. Total number of distinct users
```sql
SELECT COUNT(DISTINCT Id) AS total_users
FROM `fitbit_data.daily_activity`;
````

## 3. Checking duplicates
```sql
SELECT Id, ActivityDate, COUNT(*) AS record_count
FROM `fitbit_data.daily_activity`
GROUP BY Id, ActivityDate
HAVING COUNT(*) > 1;
````

## 4. Average daily steps
```sql
SELECT ROUND(AVG(TotalSteps), 0) AS avg_daily_steps
FROM `fitbit_data.daily_activity`;
````

## 5. Average daily minutes asleep
```sql
SELECT ROUND(AVG(TotalMinutesAsleep), 0) AS avg_sleep_minutes
FROM `fitbit_data.sleep_day`;
````

## 6. Average daily sedentary minutes
```sql
SELECT ROUND(AVG(SedentaryMinutes), 0) AS avg_sedentary_minutes
FROM `fitbit_data.daily_activity`;
````

## 7. Average daily active minutes (light, fairly, very active)
```sql
SELECT 
  ROUND(AVG(LightlyActiveMinutes), 0) AS avg_light_active,
  ROUND(AVG(FairlyActiveMinutes), 0) AS avg_fairly_active,
  ROUND(AVG(VeryActiveMinutes), 0) AS avg_very_active
FROM `fitbit_data.daily_activity`;
````

## 8. Average daily calories burned
```sql
SELECT ROUND(AVG(Calories), 0) AS avg_calories
FROM `fitbit_data.daily_activity`;
````

## 9. Average steps per day of the week
```sql
SELECT 
  FORMAT_DATE('%A', ActivityDate) AS day_of_week,
  ROUND(AVG(TotalSteps), 0) AS avg_steps
FROM `fitbit_data.daily_activity`
GROUP BY day_of_week
ORDER BY avg_steps DESC;
````

## 10. Average sleep minutes per day of the week
```sql
SELECT 
  FORMAT_DATE('%A', SleepDay) AS day_of_week,
  ROUND(AVG(TotalMinutesAsleep), 0) AS avg_sleep
FROM `fitbit_data.sleep_day`
GROUP BY day_of_week
ORDER BY avg_sleep DESC;
````

## 11. Average sedentary minutes per day of the week
```sql
SELECT 
  FORMAT_DATE('%A', ActivityDate) AS day_of_week,
  ROUND(AVG(SedentaryMinutes), 0) AS avg_sedentary
FROM `fitbit_data.daily_activity`
GROUP BY day_of_week
ORDER BY avg_sedentary DESC;
````

## 12. Active minutes per day of the week
```sql
SELECT 
  FORMAT_DATE('%A', ActivityDate) AS day_of_week,
  ROUND(AVG(LightlyActiveMinutes), 0) AS avg_light_active,
  ROUND(AVG(FairlyActiveMinutes), 0) AS avg_fairly_active,
  ROUND(AVG(VeryActiveMinutes), 0) AS avg_very_active
FROM `fitbit_data.daily_activity`
GROUP BY day_of_week
ORDER BY day_of_week;
````

✅ These queries supported the analysis of sleep, physical activity, and sedentary behavior patterns, which were later used to generate insights for Bellabeat’s marketing strategy.



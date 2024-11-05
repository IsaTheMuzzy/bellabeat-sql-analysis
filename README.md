# Bellabeat SQL Analysis

This repository contains SQL queries used to analyze Bellabeat's daily activity data.

## Project Overview
- **Goal**: Analyze user activity data to uncover trends in steps, calories burned, and activity levels.
- **Skills**: SQL queries, data aggregation, and segmentation.

## SQL Files
- `activity_analysis.sql`: Contains queries for daily step counts, calories burned, activity level segmentation, and more.

## Example Queries
- **Daily Steps Calculation**:
  ```sql
  SELECT ActivityDate, SUM(TotalSteps) AS daily_steps
  FROM daily_activity
  GROUP BY ActivityDate;
# Activity Level Segmentation:
```sql
  SELECT UserID, 
       CASE 
         WHEN TotalSteps < 5000 THEN 'Low'
         WHEN TotalSteps BETWEEN 5000 AND 10000 THEN 'Moderate'
         ELSE 'High'
       END AS activity_level
FROM daily_activity;
```
# Results

Here are some key insights derived from the SQL analysis:

- **Average Daily Steps**: Users averaged around 7,000 steps per day, with fluctuations based on activity level.
- **Calorie Expenditure**: There is a noticeable correlation between higher step counts and increased calories burned, especially on days with over 10,000 steps.
- **User Segmentation**: Users were segmented into three groups:
  - **Low Activity** (less than 5,000 steps): Represented a small portion of users who burned fewer calories on average.
  - **Moderate Activity** (5,000 to 10,000 steps): The largest user group, with moderate calorie expenditure.
  - **High Activity** (over 10,000 steps): These users consistently showed higher calorie burn, highlighting their engagement with physical activity.

These findings provide a foundation for targeted recommendations to Bellabeat, aimed at encouraging activity and calorie expenditure through customized goals and reminders.

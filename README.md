# Churn-Prediction-Model
Objective: Predict which users are likely to leave the platform.  Task Deliverables:  Analyze user behavior (login frequency, course engagement). Use Random Forest or Gradient Boosting for prediction. Outcome: Reduce churn by offering personalized support. 📊 Data Source: LMS engagement logs and user activity.

# LMS User Churn Prediction: Data Engineering & Logic

## Project Overview
This project was developed for an internship task at **Internee.pk**. The goal was to build a data generation pipeline and a logic-based labeling system to predict user churn within a Learning Management System (LMS). By simulating user behavior, this project creates a foundation for training predictive Machine Learning models.

## Key Features
* **Synthetic Data Generation:** Simulates 1,000 unique users with realistic metrics such as login frequency, course engagement, and quiz scores.
* **Feature Engineering:** Creates key indicators like `last_login_days_ago` and `course_engagement_rate` to quantify user activity.
* **Churn Logic Implementation:** Developed a multi-factor labeling system to identify "at-risk" users based on inactivity and low performance.
* **Data Reproducibility:** Uses `np.random.seed(42)` to ensure the dataset remains consistent across different environments.

## Churn Criteria (The Logic)
A user is labeled as **Churned (1)** if they meet any of the following conditions:
1. **High Inactivity:** Has not logged in for more than 25 days.
2. **Low Engagement:** Has completed less than 25% of their course content.
3. **Low Performance + Low Activity:** An average quiz score below 55 combined with fewer than 5 monthly logins.

## Tech Stack
* **Python 3.x**
* **Pandas:** For data manipulation and CSV export.
* **NumPy:** For statistical data generation and randomization.

# Predictive Maintenance Optimization
### 
---
Kyle Anderson
---


![image](https://github.com/user-attachments/assets/795701a7-b73b-4485-8d2c-cb51adb0ad32)



## Problem Statement

Maintenance scheduling challenges often result in unplanned downtime and inefficient resource use. The project's goals include:

* Create weekly actionables for Swire
* Workload Prediction: Accurately forecast the time required for future work in minutes.
* Maintenance Forecasting: Predict the next planned maintenance date based on historical patterns and expected workloads.
* Optimization: Minimize disruptions by integrating workload and maintenance forecasting into actionable schedules.

---

## EDA
The dataset contains various features with significant missing data, as 80% of the entries are missing or null. Features such as "Execution Start Date" and "Execution Finish Date" had a narrow range, with means close to 2020-12-20 and 2020-12-21, showing a focus on recent operations. Categorical variables like "Maintenance Activity Type" (unplanned) and "Functional Area Node 1 Modified" (COTA Production) show high frequency in certain values, but further data cleaning and exploration are required due to the substantial missing values.

---

## Modeling

### Maintenane Date Prediction
This model looked at each equipment for each equipment and predicted its next maintenance date
The goal was to achieve an MAE within 5 days, this was achieved

![image](https://github.com/user-attachments/assets/cd0f1556-4508-4ede-a248-4dfdd415e33c)


---
### Time Series Forecasting:

Accurate Workload Predictions: Provided granular forecasts for workload in minutes, aiding in resource planning.
Scheduled Maintenance: Generated actionable insights to determine when to perform maintenance before critical thresholds are reached.
Batching Logic: Introduced a 7-day rolling window for grouped maintenance, minimizing disruption and cost.

![image](https://github.com/user-attachments/assets/acbb6401-6bad-43f4-8919-afd3ee477cad)

---

###Future Enhancements
Integration with Real-Time Data: Add live workload data for adaptive maintenance planning.
Machine-Specific Models: Customize predictions based on individual equipment characteristics.
Dashboards: Provide stakeholders with interactive dashboards for better decision-making.


Predict work durations using Prophet’s yhat values.
Simulate changes under planned maintenance conditions (yhat_planned).
Maintenance Scheduling:

Predict the optimal date for next maintenance tasks.
Prioritize high-impact tasks based on workload metrics.














![image](https://github.com/user-attachments/assets/c3f868a1-af51-40b5-a966-27ce70808331)

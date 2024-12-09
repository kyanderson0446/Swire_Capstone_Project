# Predictive Maintenance Optimization
### 
---
Kyle Anderson
---


![image](https://github.com/user-attachments/assets/795701a7-b73b-4485-8d2c-cb51adb0ad32)

## Introduction: 

Swire Coca-Cola is a major bottling partner of The Coca-Cola Company in the Western United States. Swire operates 6 production plants across 13 states which support distribution, marketing and production of Coca-Cola products. 

## Problem Statement
As it stands, Swire is the source of Coca-Cola in the Western United States. Any changes made cause a ripple effect across the distribution network. One of those ripples is manufacturing maintenance downtime. This translates to Swire meeting 94% of demand. The lack of predictive maintenance and part inventory are leading causes to the downtime, which translates to $60M dollars lost in uncaptured revenue.  

### Groups Solution
This project utilizes the Facebook Prophet model and Python to forecast maintenance time trends, enabling more informed decision-making. By applying advanced time series forecasting techniques, the goal is to minimize downtime, optimize resource allocation, and effectively prioritize critical tasks.

### Contribution
I focused heavily in the EDA and line-by-line details. This produced findings on Equipment groupings and maintenance distribution. This was a time-series focused project and identifying maintenance over time would show us where we needed to pull data. The main goal quickly turned away from breakdowns to reducing unplanned maintenance.

### Business Context
Increasing planned maintenance helps reduce costly unplanned downtime, lowers critical repair expenses, and improves equipment lifespan. By forecasting and scheduling maintenance, the company can better allocate resources, avoid disruptions, and increase efficiency, ultimately saving dollars lost on downtime.

### Trials
Deciding on using Prophet for predicting maintenance and the next maintenance date was challenging due to varying opinions on model options within the group. While Prophet’s ability to handle time series data and trends was beneficial, there were concerns about its integration of categorical variables and handling of sparse data, leading to uncertainty about its predictive accuracy. Although the R2 was low, Prophet proved interpretable and more suitable for long-term use with live data.

### Takeaways
* The importance of selecting the right model for real-world, imperfect data.
* The challenges of balancing predictive accuracy with interpretability.
* Understanding how to handle sparse, irregular data and integrating categorical variables.
* The need to consider varying stakeholder needs when the end-users are unclear.
* The value of iterative testing and refinement for improving model performance.

---
---

## Maintenance scheduling challenges often result in unplanned downtime and inefficient resource use. The project's goals include:

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

#### Location: MONZA
* MAE (Days +-): 3.75
* RMSE: 7.196754716522867
* R2: 0.18678322162821415


![image](https://github.com/user-attachments/assets/cd0f1556-4508-4ede-a248-4dfdd415e33c)


---

### Time Series Forecasting:

![image](https://github.com/user-attachments/assets/4c18c383-1d6d-45a2-8cc7-2537fc38c7d2)

Accurate Workload Predictions: Provided granular forecasts for workload in minutes, aiding in resource planning.
Scheduled Maintenance: Generated actionable insights to determine when to perform maintenance before critical thresholds are reached.

### Maintenance Scheduling:
Predict the optimal date for next maintenance tasks.
Prioritize high-impact tasks based on workload metrics.


#### For optimization for weekly actionables
Batching Logic: Introduced a 7-day rolling window for grouped maintenance, minimizing disruption and cost.

![image](https://github.com/user-attachments/assets/acbb6401-6bad-43f4-8919-afd3ee477cad)

---

### Future Enhancements
* Integration with Real-Time Data: Add live workload data for adaptive maintenance planning.
* Machine-Specific Models: Customize predictions based on individual equipment characteristics.
* Dashboards: Provide stakeholders with interactive dashboards for better decision-making.







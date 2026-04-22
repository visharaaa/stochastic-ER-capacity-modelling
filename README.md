# Emergency Room Queue Simulation (M/M/c Model)

This project presents a **discrete-event simulation** of an Emergency Room (ER) triage system using an **M/M/c queueing model**. The objective is to evaluate whether current staffing levels meet the hospital’s waiting time requirements and to assess the impact of adding an additional triage doctor.

---

## Problem Overview

The hospital is experiencing **overcrowding in its Emergency Room**, particularly during weekend shifts. Patients report excessive waiting times before receiving triage.

The hospital has established the following requirement:

> Average patient waiting time must not exceed **10 minutes**

---

## Model Description

The system is modelled as an **M/M/c queue**, with:

- **Arrival Process**: Poisson distribution  
  - λ = 12 patients/hour  
- **Service Process**: Exponential distribution  
  - Mean service time = 12 minutes per patient  
- **Queue Discipline**: First-Come, First-Served (FCFS)  
- **Simulation Size**: 500 patients  

---

## Scenarios Simulated

### Scenario 1: Current System
- 3 Triage Doctors  
- Evaluates whether existing staffing meets the required performance threshold  

### Scenario 2: Enhanced System
- 4 Triage Doctors  
- Assesses the impact of increasing system capacity  

---

## Key Performance Metrics

The simulation evaluates:

- Average Waiting Time  
- Average System Time  
- Average Queue Length (via Little’s Law)  
- Percentage of patients waiting longer than 10 minutes  

---

## Results Summary

| Metric | 3 Doctors | 4 Doctors |
|------|----------|----------|
| Mean Waiting Time (min) | ~8.82 | ~1.85 |
| Average Queue Length | ~1.37 | ~0.25 |
| Threshold Met (≤10 min) | Yes | Yes |

---

## Key Findings

- The **3-doctor system satisfies the required waiting time constraint**, but operates close to its capacity limit.  
- The **4-doctor system significantly reduces waiting time and queue length**, improving overall system performance.  
- Increasing the number of servers enhances system stability and reduces the impact of variability in patient arrivals.

---

## Technologies Used

- R  
- R Markdown  
- `knitr`  

---

## How to Run

1. Open the `.Rmd` file in RStudio  
2. Click **Knit** to generate the report  
3. Review simulation outputs and analysis  

---

## Conclusion

Although the current system meets the minimum requirement, the addition of a fourth triage doctor provides a more efficient and robust solution, reducing congestion and improving patient experience.

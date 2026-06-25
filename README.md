## Project Name : Manufacturing Downtime

# Project Idea :
A Manufacturing Downtime Analysis Project focuses on collecting and analyzing machine downtime data in a factory to identify the causes of production interruptions and improve operational efficiency. The goal is to reduce downtime, increase productivity, and optimize maintenance strategies.

The project analyzes historical production and machine data to determine when, why, and how often machines stop operating. Using data cleaning, analysis, and visualization, the project identifies patterns and root causes of downtime so managers can make data-driven decisions.

# KPIs (Key Performance Indicators): 

1. Availability Rate: The percentage of time the line was actually running vs. standing still.
2. Performance Efficiency: Measures if the operator is running the machine at the target speed.
3. Human Error Impact: The percentage of downtime caused by operator mistakes.
4. Average Recovery Time: How long it takes, on average, to fix a stop and get back to work.


# Metrics for project success:  

1. Gross Production Time: The full time recorded for a single batch (Clock time).
2. Total Downtime (Lost Minutes): The total minutes lost due to machine stops or delays.
3. Stop Frequency: A count of how many times the line actually stopped during a batch.
4. Batch Count: The total number of batches completed by the team.
   
## 🗃️ Dataset Summary
* **Raw Data:** 4 sheets (`Line productivity`, `Products`, `Downtime factors`, `Line downtime`).
* **Processed Data:** Cleaned, denormalized long-format flat table containing **64 rows and 15 columns** covering 38 unique batches.
* **Preservation Status:** Retained all 61 non-null downtime entries and 3 zero-downtime batches.

## 🔧 Data Transformation & Quality Fixes
1. **Wide-to-Long Melting:** Converted a sparse 12-column downtime matrix into an event-level database to enable granular root-cause analytics.
2. **Midnight Crossing Resolution:** Implemented logic to add $+1$ day to `End Time` when it occurs past midnight relative to `Start Time`.
3. **Metrics Protection:** Employed distinct batch-level aggregation rules to avoid overcounting `Production Duration` or `Batch Count` due to unpivoting duplicate rows.
4. 
## 📊 Key Insights & Dashboard Architecture
The project transitions findings into an interactive BI dashboard built across 5 dedicated areas:
* **Overview:** High-level KPIs tracking Availability Rate, Performance Efficiency, and Human Error Impact.
* **Downtime Root Causes:** Pareto ranking of time lost by machine and operator errors.
* **Operator Performance:** Process analysis comparing duration and error rates (backed by ANOVA testing).
* **Product Performance:** Benchmarking cycle metrics against minimum expected targets.
* **Trend View:** Day-over-day tracking to flag anomalous event spikes.
  
# Team Members 
1.Shams Ahmed Abdo.
2.Shahd Hussein Hassan.	  
3.Mennatullah Samer Maged.
4.Malak Ahmed Sayed.
5.Ali Fathy Ali.

# Instructor: 
 Yasser A.Rahman
 
# Project Files: 
You can find the full project files here: 
https://drive.google.com/drive/folders/1G_uLDXxVe6CJVVbjNDoWaBOlvi9189EV?usp=sharing


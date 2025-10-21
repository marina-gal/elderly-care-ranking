# Sheet 1 – Descriptive Statistics & Initial Data Review

This sheet provides a descriptive statistical analysis of the main variables in the dataset before data cleaning and scoring. The goal was to understand data distribution, detect missing values, and identify potential outliers.

<img width="708" height="596" alt="image" src="https://github.com/user-attachments/assets/34921510-97b1-4605-b43c-4613cfc1177d" />

Variables analyzed:

Staffing Level – Staff-to-resident ratio (0–1 scale)

Avg Waiting Time – Average waiting time (days)

Infection Rate – Percentage of residents affected

IT Readiness Score – Digital infrastructure and readiness

Satisfaction Index – Resident satisfaction (1–5 scale)

Key steps and findings:

Calculated key descriptive metrics: mean, median, quartiles (Q1–Q3), IQR, min, max, and standard deviation.

Detected 1 missing value in Avg Waiting Time and Infection Rate.

Identified possible outliers:

Staffing Level: Slightly high maximum (1.5) compared to Q3 (0.83).

Avg Waiting Time: Wide spread (SD = 18.5), most values between 42–69.

Infection Rate: Potential high outlier at 6.23%.

IT Readiness and Satisfaction showed no missing values or extreme outliers.

Added interpretative notes below the table to summarize data quality and variability per variable.

Purpose:
This analysis guided later steps in cleaning, normalization, and scoring, ensuring that the data used for ranking was consistent and reliable.

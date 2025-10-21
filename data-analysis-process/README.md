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
Avg Waiting Time: Wide spread (SD = 18.5), most values (by density) between 42–69.

Infection Rate: Potential high outlier at 6.23%.
IT Readiness and Satisfaction showed no missing values or extreme outliers.
Added interpretative notes below the table to summarize data quality and variability per variable.

# Sheet 2 – Data Cleaning & Outlier Validation
<img width="1308" height="248" alt="image" src="https://github.com/user-attachments/assets/b4e5dff9-b0fa-4bb1-a820-6dc034a3d2bf" />

This sheet focuses on validating the consistency of input data and identifying possible outliers detected during the descriptive analysis.
Key actions:

Re-checked all variables for missing values and outliers using the IQR (Interquartile Range) method.

Created “Checking” columns to verify whether each observation was within acceptable bounds.

Marked each record as:

✅ OK — within range

⚠️ Outlier — above or below the calculated fences

🟠 Empty — missing values

Detailed checks performed:

Staffing Level: Confirmed one high outlier (1.5) but retained it since it is still a plausible value in context.

Avg Waiting Time: One missing value was detected and replaced with the mean (57.33).

Infection Rate: One lower and one higher outlier identified (1.79, 6.23), both considered valid since variability may reflect real differences between homes.

IT Readiness & Satisfaction: All values within the expected range (no missing or outlier cases).

# Sheet 3 – Scoring, Ranking & Visualization
<img width="945" height="495" alt="image" src="https://github.com/user-attachments/assets/d477f0a5-f936-4553-a695-ab8d9dedc0c2" />

This sheet presents the final stage of the project: normalization, scoring, and visual analysis of elderly care home performance.

Score Calculation

Each variable (Staffing Level, Avg Waiting Time, Infection Rate, IT Readiness, and Satisfaction) was normalized to a 0–100 scale, where higher scores indicate better performance.
A Total Score was computed as the average of all dimension scores for each care home.

Key results:

Highest-performing home: Care Home 3 (Total Score ≈ 73.9)

Lowest-performing home: Care Home 5 (Total Score ≈ 28.9)

Most homes scored between 40–60, showing moderate overall performance.

*Graph 1 – Bar Chart “Score per Care Home”*

This horizontal bar chart visualizes the overall ranking of each home.
Insights:

Care Home 3 and Care Home 7 clearly outperform the others, scoring above 60.

Care Home 5 and Care Home 10 underperform significantly compared to the group average.

The mid-tier homes (e.g., Care Home 2, 6, 9) cluster around 45–55 points.

This visualization provides a clear comparative overview of institutional performance.

<img width="529" height="296" alt="image" src="https://github.com/user-attachments/assets/cb779546-909c-4c01-9b02-640985cceb3a" />

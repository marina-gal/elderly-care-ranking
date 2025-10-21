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
<img width="589" height="128" alt="image" src="https://github.com/user-attachments/assets/5f147e10-979a-4d7e-8fd1-afd39e42375f" />

All cleaned variables were converted to a **0–100 scale** (higher = better).  
A **Total Score** was computed as the average of all dimension scores per home.

**Top performers:**
- 🥇 *Care Home 3* — Total Score: **73.86**
- 🥈 *Care Home 7* — Total Score: **61.95**
- 🥉 *Care Home 2* — Total Score: **53.47**

**Lowest performers:**
- *Care Home 5* — Total Score: **28.85**
- *Care Home 10* — Total Score: **32.33**

Visual Analysis

###  Score per Care Home (Bar Chart)
Shows the total performance score for each home.  
- *Care Home 3* and *Care Home 7* clearly outperform others.  
- *Care Home 5* and *Care Home 10* are below average.  
- Most institutions cluster between 40–60 points.
<img width="424" height="300" alt="image" src="https://github.com/user-attachments/assets/fd438e32-2442-47da-be7a-347360e406b3" />

### Satisfaction vs Other Dimensions (Scatter Plots)
Explored relationships between **Satisfaction** and key metrics:

<img width="524" height="319" alt="image" src="https://github.com/user-attachments/assets/43f86446-a7c5-447d-881b-0ae5d8975e75" />

| Comparison | Correlation | Interpretation |
|-------------|-------------|----------------|
| Satisfaction vs Staffing | -0.39 | Moderate negative — higher staffing does not necessarily lead to higher satisfaction |
| Satisfaction vs Waiting Time | -0.35 | Moderate negative — longer waiting times tend to lower satisfaction |
| Satisfaction vs Infection Rate | -0.03 | Very weak to none — infection rate appears unrelated to satisfaction in this dataset |
| Satisfaction vs IT Readiness | -0.25 | Weak negative — IT readiness has a limited direct influence on satisfaction |

Resident satisfaction is most affected by waiting time and staffing levels, while infection rate and IT readiness show little to no direct correlation in this dataset.

### Dimensional Analysis (Radar / Spider Chart)
Displays the five dimension scores for each home.

**Highlights:**
- *Care Home 3:* High and balanced across all categories (top performer).  
- *Care Home 7:* Strong in IT and waiting time, moderate elsewhere.  
- *Care Home 5:* Weak across all dimensions.  
- *Care Home 6* & *Care Home 9:* Average and consistent performance.


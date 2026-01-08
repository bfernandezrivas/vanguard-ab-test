# vanguard-ab-test
# Vanguard A/B Test – Digital CX Experiment (2017)

## Project Overview
Vanguard’s CX team ran an A/B test from **2017-03-15 to 2017-06-20** to evaluate whether a redesigned digital interface improves the **process completion rate** compared to the traditional experience.

- **Control (A):** Traditional online process  
- **Test (B):** New redesigned interface  
- **Primary KPI:** Process completion rate

## Business Question
**Does the new digital experience lead to a higher client completion rate?**

## Hypotheses
- **H0:** Completion rate(Test) = Completion rate(Control)  
- **H1:** Completion rate(Test) > Completion rate(Control)

Additional questions explored:
1. Does the uplift differ by client segment (e.g., age/tenure)?
2. Does the new UI reduce drop-offs or steps/time to completion?
3. Are there behavioral differences in session patterns between groups?

## Data Sources (Links)
- Demographics: https://github.com/data-bootcamp-v4/lessons/blob/main/5_6_eda_inf_stats_tableau/project/files_for_project/df_final_demo.txt  
- Experiment assignment: https://github.com/data-bootcamp-v4/lessons/blob/main/5_6_eda_inf_stats_tableau/project/files_for_project/df_final_experiment_clients.txt  
- Web activity (Part 1): https://github.com/data-bootcamp-v4/lessons/blob/main/5_6_eda_inf_stats_tableau/project/files_for_project/df_final_web_data_pt_1.txt  
- Web activity (Part 2): https://github.com/data-bootcamp-v4/lessons/blob/main/5_6_eda_inf_stats_tableau/project/files_for_project/df_final_web_data_pt_2.txt  

## Tools
- Python (pandas, numpy, matplotlib/seaborn, scipy/statsmodels)
- Tableau (dashboard + story)
- GitHub (version control)
- Trello (project management)

## Methodology
### Data Preparation
- Merged web data parts (pt_1 + pt_2)
- Joined datasets on `client_id`
- Filtered records to experiment window (2017-03-15 → 2017-06-20)
- Handled missing values, duplicates, and inconsistent formatting
- Built analysis features (completion flag, session metrics, etc.)

### Exploratory Data Analysis
- Compared completion rates by group (A vs B)
- Checked sample balance and key distributions
- Segment analysis (demographics/behavior)
- Visualized drop-off behavior and engagement patterns

### Statistical Testing
- Two-proportion z-test (or chi-square test) for completion rate difference
- Reported uplift, confidence interval, and p-value

## Key Results (Summary)
- Completion rate (Control): **[X%]**
- Completion rate (Test): **[Y%]**
- Uplift: **[Δ%]**
- Statistical significance: **p = [value]**
- Decision recommendation: **[Roll out / Iterate / Do not roll out]**

## Tableau Dashboard
- Tableau file: `tableau/vanguard_ab_test.twbx`
- Dashboard highlights:
  - Completion rate comparison
  - Segment performance
  - Drop-off analysis
  - Engagement patterns

## Repository Structure

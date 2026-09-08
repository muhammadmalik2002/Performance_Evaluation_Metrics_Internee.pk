# Performance Evaluation Metrics

**Internee.pk — Data Analyst Domain — Task 6**

## Objective
Evaluate and track intern performance through a metrics-based system.

## What this project does
- Designs 3 KPIs: task completion time, project quality score, and mentor feedback
- Automates data extraction and aggregation using **SQL** (via sqlite3, joining task and feedback tables)
- Computes a weighted composite performance score per intern per month
- Generates monthly reports ranking interns for supervisors

## Data note
No real dataset was provided, so `task_metrics_raw.csv` and `mentor_feedback_raw.csv` were generated synthetically (30 interns, 3 months, fixed random seed).

## Files
| File | Description |
|---|---|
| `intern_kpi_summary.csv` | All interns' KPIs and performance scores, all 3 months |
| `monthly_report_2026-07.csv` / `-08` / `-09` | Ranked monthly reports for supervisors |
| `performance_trend.png` | Team average performance score over time |

## KPI weighting
- 40% project quality score
- 30% mentor feedback
- 30% task completion speed

(Quality weighted highest — a fast but sloppy intern shouldn't outrank a careful one.)

## Key findings
- Team average performance rose from **6.09 (July) to 6.19 (Aug/Sep)** and held steady
- **INT004 was the lowest performer in both July and August** — a repeated pattern worth flagging for mentor follow-up
- Top performer varied by month, indicating distributed rather than single-intern-driven performance
- **Recommendation:** flag interns who repeat as bottom performers across multiple months for proactive mentor outreach

## Tools
Python (pandas, numpy, sqlite3, matplotlib) in Google Colab.

## Author
Muhammad Ahmad — Data Analyst Intern, Internee.pk

# Educational Platform Analytics: SQL & Pandas

## Project Overview
Analyzed user behavior patterns from an educational platform's database (250k+ records) to measure the impact of a new "Newsfeed" feature using SQL and Pandas. Delivered data-driven insights that informed product decisions.

## Key Results
- **27% increase** in early submissions after Newsfeed implementation
- Identified **peak engagement hours** (14:00-17:00 on weekdays)
- Reduced query execution time by **40%** through optimization
- Automated **daily reports** used by 10+ instructors

## Technical Implementation

### SQL Expertise
```sql
-- Example: Complex join with time delta calculation
SELECT 
    u.user_id,
    AVG(julianday(d.deadline) - julianday(c.first_commit)) AS avg_lead_time
FROM users u
JOIN commits c ON u.user_id = c.user_id
JOIN deadlines d ON c.lab_id = d.lab_id
WHERE c.status = 'ready'
GROUP BY u.user_id
HAVING COUNT(c.commit_id) > 3;
```
## Pandas Analysis

# A/B Test Analysis
test_group = df[df['newsfeed_views'] > 0]
control_group = df[df['newsfeed_views'].isna()]

print(f"Mean improvement: {test_group['lead_time'].mean() - control_group['lead_time'].mean():.1f} hours")

# 🛠️ Technical Stack  

| Component       | Technologies Used                |
|----------------|----------------------------------|
| **Database**   | SQLite, SQLAlchemy               |
| **Analysis**   | Pandas, NumPy, Jupyter           |
| **Visualization** | Matplotlib, Seaborn           |
| **Optimization** | Query planning, Indexing      |

# Key Insights

## Behavioral Patterns
- **Frequent Newsfeed Checkers**: Students who checked the newsfeed **3+ times/week** submitted labs **1.2 days earlier** on average.  
- **Weekend Engagement**: Weekend activity showed **15% lower completion rates** compared to weekdays.  

## Technical Achievements
- **Automated Data Validation Pipeline**: Ensures data consistency and accuracy.  
- **Incremental Data Loading**: Optimizes performance by processing only new or updated data.  
- **Reusable Query Templates**: Standardizes and speeds up database interactions.  

# How to Use
1. Clone repository
2. Install requirements: pip install -r requirements.txt
3. Run Jupyter notebooks in order (ex00-ex05)

This project showcases comprehensive data analysis skills from basic SQL operations through advanced experimental analysis.
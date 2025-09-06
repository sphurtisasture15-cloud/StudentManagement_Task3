SQL Developer - Task 3

• Objective
Use subqueries and aggregations to analyze student performance.

• Database Setup
Students table with fields:
  - student_id (Primary Key)
  - name
  - math_score
  - science_score
  - english_score
 
• Tasks
1. Top Students by Total Score
```sql
SELECT name, (math_score + science_score + english_score) AS total_score
FROM Students
ORDER BY total_score DESC
LIMIT 5;

2.Averages Based on Conditions
• Average Math Score (>70)
• Average Total Score (200–250)
• Group students by total score ranges

3.Second Highest Math Score
SELECT MAX(math_score)
FROM Students
WHERE math_score < (SELECT MAX(math_score) FROM Students);

• Conclusion
Subqueries and aggregations were used to:
  -Find top students
  - Calculate averages with conditions
  -Identify the second-highest math score

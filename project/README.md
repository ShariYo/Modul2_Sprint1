
# Project: Mental Health in the Tech Industry

Survey on Mental Health in the Tech Workplace in 2014, 2016, 2017, 2018, 2019 has been taken as a dataset for a project. Each survey measures and attitudes towards mental health and frequency of mental health disorders in the workplace.  
The raw data was processed using Python and SQL for cleaning and manipulation.  
Steps involved in cleaning were:  
- Similar questions were grouped together;  
- Unclear answers of survey were removed;  
- Spelling errors were fixed.


## Data source

Data srouce is given in a database file "mental_health.sqlite"

```bash
  https://www.kaggle.com/datasets/anth7310/mental-health-in-the-tech-industry
```
    
## SQL tables, main functions and libraries used for analysis:

SQLite database contains of 3 tables. Survey, Question, Answer:  
- Survey (PRIMARY KEY INT SurveyID, TEXT Description);  
- Question (PRIMARY KEY QuestionID, TEXT QuestionText);  
- Answer (PRIMARY/FOREIGN KEY SurveyID, PRIMARY KEY UserID, PRIMARY/FOREIGN KEY QuestionID, TEXT AnswerText).  
Some main SQLite functions:  
SELECT, FROM, COUNT, DISTINCT, GROUP BY, ORDER BY, WHERE, CASE, JOIN, ON, etc.  

Queries where written in tripple quoutes and read with pd.read_sql_query() fucntion.  
Special local data cleaning function was used.  
  
For this particular project, to visualize results, mainly sns.barplot and sns.lineplot were used.
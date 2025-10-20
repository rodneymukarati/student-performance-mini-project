# Student Performance Analysis — Mini Project

**Short description**
A small exploratory data analysis on student scores using pandas and SQL-like queries with pandasql.

## Contents
- `notebooks/student_performance_analysis.ipynb` — the main notebook (narrative + results)
- `src/analysis.py` — reproducible script to generate figures
- `data/` — dataset or link to dataset
- `figures/` — output images used in README

## How to run locally
1. Create and activate venv:
 python -m venv venv
venv\Scripts\activate

2. Install:
pip install -r requirements.txt

3. Start the notebook:
jupyter notebook notebooks/student_performance_analysis.ipynb
//not really necessary because 

or run script:
python src/analysis.py



## Key finding (example)
- Average math score tends to increase with age for students with ScienceScore > 60.

## SQL note (fix applied)
Originally I grouped incorrectly using `GROUP BY AvgMath DESC`. I fixed it to:
```sql
SELECT Age, AVG(MathScore) AS AvgMath
FROM df
WHERE ScienceScore > 60
GROUP BY Age
ORDER BY AvgMath DESC;

![Average Math by Age](figures/avg_math_by_age.png)

What I learned

How to run SQL-like queries on pandas DataFrames with pandasql.

Importance of correct GROUP BY vs ORDER BY usage.

How to clean/structure a reproducible mini project.


### `LICENSE` (MIT — replace YEAR and YOUR NAME)
```text
MIT License

Copyright (c) YEAR YOUR NAME

Permission is hereby granted, free of charge, to any person obtaining a copy...
[standard MIT text — you can copy full MIT license from choosealicense.com]



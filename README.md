# 📊 Data Cleaning & Application Scoring Project

A practical data cleaning and scoring project based on a real-world homework assignment.
The task: clean and process application data, merge additional industry information, and calculate a custom rating for each applicant.

# 🧩 Project Overview
In this project, I was given two CSV files:

- applications.csv — list of user applications
- industries.csv — industry-level scoring information

My goal was to:
1.Clean the application data
2.Enrich it with industry ratings
3.Calculate a rating from 0 to 100 based on a set of conditions
4.Filter valid applications
5.Group accepted applications by submission week and analyze the weekly average score

# ✅ Step-by-Step Logic
## 1. Data Cleaning
- Removed duplicates based on applicant_id
- Filled missing values in External Rating with 0
- Replaced missing Education level with "Середня"

## 2. Merging
- Merged the applications with industries.csv on the Industry column

## 3. Rating Logic The rating was calculated as a sum of scores from the following criteria:
Criterion	Points
Age between 35–55	+20
Application on weekday	+20
Marital status = Married	+20
Location = Київ чи область	+10
Industry Score (from merge)	+0 to +20
External Rating ≥ 7	+20
External Rating ≤ 2	-20
If Amount is missing or External Rating = 0, the score is automatically set to 0

## 4. Filtering
- Only applications with rating > 0 are considered accepted

## 5. Weekly Aggregation
- The final DataFrame includes a Week column based on ISO calendar
- Aggregated by week to calculate the average rating of accepted applications

#🧪 Tech Stack
- Python
- Pandas
- Jupyter Notebook

## 🧠 This project reflects my hands-on experience with data cleaning, custom business logic implementation, and data analysis workflows in Python.



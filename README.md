# CaseStudy2DDS
Data Analysis of Employee Attrition - A Case Study

## Purpose

To address the challenge of retaining talented employees, the leadership team of Frito Lay have engaged DDS Analytics to conduct an in-depth analysis aimed at uncovering the underlying factors behind employee turnover within their organization. This study, leveraging data from 870 employees across 36 distinct variables, is designed to yield actionable insights to inform decision-making processes. By employing a combination of visualizations, statistical methodologies, and the creation of predictive models, the objective is to provide strategic guidance and practical tools to enhance future strategies and organizational policies.

* **Analyst:** Kristin Henderson
* **Analytics Firm:** DDS Analytics
* **Stakeholders:** Frito Lay CEO and CFO


## Repository structure

### Root directory

* `README.md`: Readme file detailing purpose, contents and usage.
* `Analysis_of_Employee_Attrition_and_Income.Rmd`: Rmarkdown file with introduction, objectives, all code to interact with the data and build the plots, written explanations, links to the video presentation and R Shiny interactive app and conclusion.
* `Analysis_of_Employee_Attrition_and_Income.html`: HTML file knitted with the above and with embedded data and visualizations.
* `Presentation_Attrition.ppt`: Powerpoint slides for the analysis with link to seven-minute YouTube video presentation.

### Data directory containing five data files.

* **`Case2PredictionsHenderson Attrition.csv`**
* **`Case2PredictionsHenderson Salary.csv`**
* `CaseStudy2-data.csv`
* `CaseStudy2CompSet No Attrition.csv`
* `CaseStudy2CompSet No Salary.csv`


## Codebook

### Data dictionary

The original dataset, `CaseStudy2-data.csv` was obtained from "https://s3.us-east-2.amazonaws.com/msdsds6306/CaseStudy2-data.csv".  

Below are the variables and the information I have and/or assumptions I make about them.

- `CaseStudy2-data.csv`: dataset of employee data with 870 observations of 36 variables.  
  - `ID`: The row of the observation, a unique number from 1 to 870; numerical/continuous.
  - `Age`: The employee's age (between 18 and 60); numerical/continuous.
  - `Attrition`: Whether the employee left, "No" or "Yes"; categorical with 2 levels.
  - `BusinessTravel`: Amount of business travel, "Non-Travel", "Travel_Frequently", or "Travel_Rarely; categorical with 3 levels.
  - `DailyRate`: No specific information provided; integer from 103 to 1499, numerical/continuous.
  - `Department`: I assume this is the employee's department, either "Human Resources", "Research & Development", or "Sales"; categorical with 3 levels.
  - `DistanceFromHome`:  Relative distance low or high, no specific information provided regarding unit of distance; integer from 1 to 29; numerical/continuous.
  - `Education`: An employee's level of education, 1-Below College, 2-College, 3-Bachelor, 4-Master, 5-Doctor; numerical/categorical.
  - `EducationField`: I assume this is the employee's educational field, either "Human Resources", "Life Sciences", "Marketing", "Medical", "Other" or "Technical Degree"; categorical with 6 levels.
  - `EmployeeCount`: Perhaps a counter in the data set, all values are 1 (numerical).
  - `EmployeeNumber`: I assume this is a unique identifying employee number. I do not know if low numbers are earlier hires and high numbers later, or perhaps low numbers are more important positions; numerical/continuous.
  - `EnvironmentSatisfaction`: No specific information beyond 1-Low, 2-Medium, 3-High, 4-Very High; numerical/categorical.
  - `Gender`: An employee's gender, "Female" or "Male"; categorical with 2 levels.
  - `HourlyRate`: No specific information provided; integer from 30 to 100, numerical/continuous.
  - `JobInvolvement`: No specific information beyond 1-Low, 2-Medium, 3-High, 4-Very High; numerical/categorical.
  - `JobLevel`: No specific information provided other than 1 is low and 5 is high; numerical/categorical.
  - `JobRole`: I assume this is the employee's job role, either "Heathcare Representative", Human Resources", "Laboratory Technician", "Manager", "Manufacturing Director", "Research Director", "Research Scientist", "Sales Executive", or "Sales Representative"; categorical with 9 levels.
  - `JobSatisfaction`: No specific information beyond 1-Low, 2-Medium, 3-High, 4-Very High; numerical/categorical.
  - `MaritalStatus`: An employee's marital status, "Divorced", "Married", or "Single"; categorical with 3 levels.   
  - `MonthlyIncome`: I assume this is monthly income in dollars; numerical/categorical.
  - `MonthlyRate`: No specific information provided; integer from 2094 to 26997, numerical/continuous.
  - `NumCompaniesWorked`: I assume this is number of companies an employee has worked for in total; numerical/continuous.
  - `Over18`: Yes, if the employee is over 18 years of age. All employees are "Yes".
  - `OverTime`: Only earned by non-exempt/hourly employees, "No" or "Yes"; categorical with 2 levels.
  - `PercentSalaryHike`: I assume this is percent of salary increase at some unknown time point; numerical/continuous.
  - `PerformanceRating`: No specific information beyond 1-Low, 2-Good, 3-Excellent, 4-Outstanding. Data is self-reported, and only 3 and 4 exist in data set; numerical/categorical.
  - `RelationshipSatisfaction`: Relationship satisfaction with manager, either 1-Low, 2-Medium, 3-High, 4-Very High; numerical/categorical.
  - `StandardHours`: No specific information provided. Perhaps hours per two week period. All values are 80 (numerical).
  - `StockOptionLevel`: I assume this is 0-None/Low to 3-High; numerical/categorical (0,1,2,3).
  - `TotalWorkingYears`: I assume this is number of years working in total; numerical/continuous.
  - `TrainingTimesLastYear`: Number of training sessions attended by the employee in the last year; numerical/continuous.
  - `WorkLifeBalance`: No specific information provided beyond 1-Bad, 2-Good, 3-Better, 4-Best; numerical/categorical.
  - `YearsAtCompany`: I assume this is number of years working at the company; numerical/continuous.
  - `YearsInCurrentRole`: I assume this is number of years working in current role; numerical/continuous.
  - `YearsSinceLastPromotion`: I assume this is number of years since last promotion; numerical/continuous.
  - `YearsWithCurrManager`: I assume this is number of years working for current manager; numerical/continuous.


### Data transformation

Here is the description of the two primary dataframes used in the analysis.

In the code, the primary dataset (`CaseStudy2-data.csv`) is imported as `cs2`. The numerical variables that are Likert scale responses are converted to factors, creating a new data frame, `cs2_conv`. There are various other data frames created, but this is the primary one used in most of the analysis.


### Usage

* Clone this repository
`git clone https://github.com/kdhenderson/CaseStudy2DDS.git`
* The files were created with RStudio version 2023.12.1+402. (Machine: MacBook Pro, OS: macOS Monterey 12.7.1)
* All required libraries are listed and loaded in the Rmarkdown file in one of the first code chunks. If not already installed, run `install.packages("package_name")` substituting the needed package for `package_name`, prior to loading the libraries.
* R and package versions are provided in the appendix of the Rmd file.





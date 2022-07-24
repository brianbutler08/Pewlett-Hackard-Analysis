# Pewlett Hackard Analysis

# Overview

For this project, we worked with Pewlett_Hackard, a large company with thousands of employees. They were facing the possibility in the near future of a significant personnel exodus as their older employees reached retirement age. In order to prepare for this inevitability, two main initiatives were being discussed. Firstly, they were planning on offering retirement packages to those employees that met certain criteria. Secondly, they wanted to look at the vacancies that would be open to begin planning on how to fill them.

We worked with company HR to analyze their available employee and departmental data in order to help them address these two initiatives. Up to this point, they had primarily relied on Excel and VBA to maintain and analyze employee data, but we utilzed PostgreSQL to create a database and PgAdmin to query appropriate data to answer some of HR's questions.

All of Pewlett_Hackard's HR related information was spread across six csv files, which we brought into PgAdmin in order to access the needed information.

1. Departments: names and codes of PH departments
2. Employees: personal information on employees
3. Department/Employees: department that each employee works in, in addition to start and end dates
4. Department/Managers: managers of each department 
5. Titles: Current and historic title of each employee
6. Salaries: Employee salaries

# Results

For the overall project, we created about a dozen different csv files for company leadership, each responding to different questions that they had regarding potential employee retirement and the possibility of establishing a mentorship program. The final two products, however, provided potentially the most insight. 

## Number of Retiring Employees by Title

Looking at employees by title was crucial to determine the general type of employee that was looking at retirement (and how many there were). This will enable PH to determine the best course of action in filling these poitions in the future (i.e. promoting from within or hiring externally). 

### Major Findings

- A total of 72,458 employees meet the criteria that the company has set for retirement in the near future. This is an incredibly large number of people and an coordinated effort to replace them is a necessity.
- Seventy percent of these employees are in just two title categories. The largest category is Senior Engineer (35.8% of retirees), followed by Senior Staff (34.4%). Addressin vacancies in these two groups should be a priority.

## Employees Eligible for the Mentorship Program

In order to mitigate disruption caused by a wave of retirements, PH is looking at installing a mentorship program involving experienced employees. Using their criteria for involvement in the program, we generated a list of potential participants.

### Major Findings

- Only 1,549 employees meet the criteria for the mentorship program. While this may seem like a large number on its own, it is woefully short of the number required to successfully mentor colleagues intended to replace such a large number of retirees.
- Employees targeted for the mentorship program are spread fairly evenly across title categories, at least in the top four categories. The distribution of employees (by percentage) is: Senior Staff (27.8%), Engineer (25.6%), Senior Engineer (19.0%), Staff (19.0%), Technique Leader (5.0%) and Assistant Engineer (3.7%). While a fairly even distribution could be desirable, it is significantly misaligned with those that will be retiring.

# Summary

## Primary Questions

After our analysis, we were asked to answer two primary questions.

1. How many roles will need to be filled as the "silver tsunami" begins to make an impact? 

The wave of potential retirements facing the company is massive. Baby Boomers make up a significant proportion of their workforce and there will be significant business consequences if their absences are not adequately planned for. Even if retirements are spread out over severla years, replacing more than 72,000 experienced, senior personel will be a major challenege. Addionally, it is unclear whether there are enough existing junior employees already at PH to step into those roles. Getting the balance of internal promotion and external recruitment correct will be crucial.

2. Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

In short, no. Mentorships are successful when the mentor has strong and meaningful relationships with those that they are working with. It is unrealistic for a mere 1,500 individuals to effectively mentor the *enormous* number of personnel stepping up into those roles. Each mentor would be working with many, many junior employees and there would not be enough hours in the day to remotely prepare them for their future roles.

## Additional Queries

After conducting this analysis, I have a recommendation for two additional queries that would help to shed light on the situation. These queries answer two key questions:

1. Are there enough junior staff employees to replace the retiring senior staff employees? Our original query looked at a five year range of potential retirement, finding a large number of Senior Engineers and Senior Staff 

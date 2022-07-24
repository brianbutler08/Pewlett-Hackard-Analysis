# Pewlett Hackard Analysis

# Overview

For this project, we worked with Pewlett Hackard (PH), a large, established company with thousands of employees. They were facing the possibility in the near future of a significant personnel exodus as their older employees reached retirement age. In order to prepare for this inevitability, two main initiatives were being discussed. Firstly, they were planning on offering retirement packages to those employees that met certain criteria. Secondly, they wanted to look at the vacancies that would be open to begin planning on how to fill them.

We worked with company HR to analyze their available employee and departmental data in order to help them address these two initiatives. Up to this point, they had primarily relied on Excel and VBA to maintain and analyze employee data, but we utilzed PostgreSQL to create a database and PgAdmin to query appropriate data to answer some of HR's questions.

All of Pewlett Hackard's HR related information was spread across six csv files, which we brought into PgAdmin in order to access the needed information.

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

![1](https://github.com/brianbutler08/Pewlett-Hackard-Analysis/blob/main/PH%20images%20for%20README/PH%20retirement%20by%20title.png)

### Major Findings

- A total of 72,458 employees meet the criteria that the company has set for retirement in the near future. This is an incredibly large number of people and an coordinated effort to replace them is a necessity.
- Seventy percent of these employees are in just two title categories. The largest category is Senior Engineer (35.8% of retirees), followed by Senior Staff (34.4%). Addressing vacancies in these two groups should be a priority.

## Employees Eligible for the Mentorship Program

In order to mitigate disruption caused by a wave of retirements, PH is looking at installing a mentorship program involving experienced employees. Using their criteria for involvement in the program, we generated a list of potential participants.

![2](https://github.com/brianbutler08/Pewlett-Hackard-Analysis/blob/main/PH%20images%20for%20README/PH%20mentorship%20original.png)

### Major Findings

- Only 1,549 employees meet the criteria for the mentorship program. While this may seem like a large number on its own, it is woefully short of the number required to successfully mentor colleagues intended to replace such a large number of retirees.
- Employees targeted for the mentorship program are spread fairly evenly across title categories, at least in the four biggest groups. The distribution of employees (by percentage) is: Senior Staff (27.8%), Engineer (25.6%), Senior Engineer (19.0%), Staff (19.0%), Technique Leader (5.0%) and Assistant Engineer (3.7%). While a fairly even distribution could be desirable, it is significantly misaligned with those that will be retiring.

# Summary

## Primary Questions

After our analysis, we were asked to answer two primary questions.

1. How many roles will need to be filled as the "silver tsunami" begins to make an impact? 

The wave of potential retirements facing the company is massive. Baby Boomers make up a significant proportion of their workforce and there will be major business consequences if their absences are not adequately planned for. Even if retirements are spread out over several years, replacing more than 72,000 experienced, senior personnel will be a major challenege. Addionally, it is unclear whether there are enough existing junior employees already at PH to step into those roles. Getting the balance of internal promotion and external recruitment correct will be crucial.

2. Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

In short, no. Mentorships are successful when the mentor has strong and meaningful relationships with those that they are working with. It is unrealistic for a mere 1,500 individuals to effectively mentor the *enormous* number of personnel stepping up into those roles. Each mentor would be working with many, many junior employees and there would not be enough hours in the day to remotely prepare them for their future roles.

## Additional Queries

After conducting this analysis, I have a recommendation for two additional queries that would help to shed light on the situation. These queries answer two key questions:

1. Are there enough junior staff employees to replace the retiring senior staff employees? Our original query looked at a five year range of potential retirement, finding a large number of Senior Engineers and Senior Staff that were on the verge of leaving PH. One likely source of professionals to fill these vacant positions would be the junior Engineers and Staff already at PH, who have extensive experience and may be candidates for promotion. To explore 
this possibility, I created a query that looked at current employees born in the decade after our retirees.

![3](https://github.com/brianbutler08/Pewlett-Hackard-Analysis/blob/main/PH%20images%20for%20README/PH%20non-retirees.png)

In addition to the expected senior employees, there are 21,698 Engineers and 17,890 Staff that could be good candidates to fill those soon to be vacant "senior" roles. These employees were born between 1956 and 1965, meaning that they will not retire soon, but are likely expereinced enough to be a senior member of staff.

2. How do we fill the wide gap between potential mentors and the numbers of mentors needed to be effective? The simple answer is to expand the criteria for participation in the mentorship program. Originally, PH targeted mentors born in only 1965, which did not yield enough participants. I created a query that expanded eligibility to those also born in 1964. 

![4](https://github.com/brianbutler08/Pewlett-Hackard-Analysis/blob/main/PH%20images%20for%20README/PH%20query%20for%20expanded%20mentorship.png)

By simply including another birth year of employees, the number of mentors increased from 1,549 to 19,905, making the prospect of a successful mentorship program much more likely. 

![5](https://github.com/brianbutler08/Pewlett-Hackard-Analysis/blob/main/PH%20images%20for%20README/PH%20expanded%20mentorship.png)

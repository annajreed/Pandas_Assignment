# PyCity Schools Assignment
## Pandas Challenge
In this assignment, you’ll create and manipulate Pandas DataFrames to analyze school and standardized test data.

### Instructions
### Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

****District Summary****

Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.
     
Include the following:
 + Total number of unique schools
 + Total students
 + Total budget
 + Average math score
 + Average reading score
 + % passing math (the percentage of students who passed math)
 + % passing reading (the percentage of students who passed reading)
 + % overall passing (the percentage of students who passed math AND reading)

**School Summary**
     Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:
- School name
- School type
- Total students
- Total school budget
- Per student budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

**Highest-Performing Schools (by % Overall Passing)**
     Sort the schools by % Overall Passing in descending order and display the top 5 rows.
     Save the results in a DataFrame called "top_schools".

**Lowest-Performing Schools (by % Overall Passing)**
     Sort the schools by % Overall Passing in ascending order and display the top 5 rows.
     Save the results in a DataFrame called "bottom_schools".

**Math Scores by Grade**
     Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

**Reading Scores by Grade**
     Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

**Scores by School Spending**
     Create a table that breaks down school performance based on average spending ranges (per student).
     Use the code provided below to create four bins with reasonable cutoff values to group school spending.
     Use pd.cut to categorize spending based on the bins then calculate mean scores per spending range.
     
          spending_bins = [0, 585, 630, 645, 680]
          labels = ["<$585", "$585-630", "$630-645", "$645-680"]
     
Include the following metrics in the table:

- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
 % overall passing (the percentage of students who passed math AND reading)

**Scores by School Size**
     Use the following code to bin the per_school_summary.
     Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.
          
          size_bins = [0, 1000, 2000, 5000]
          labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]

Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

**Scores by School Type**
     Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.
     This new DataFrame should show school performance based on the "School Type".


## Analysis
Once combining the two data sets, we can see all high school students in the PyCity district and their math and reading numeric grades as well as the total budget for each high school. From there, I made an initial summary table separated by individual schools, to get a overview of the entire district. Then went further and did tables for both reading scores and math scores by grade for each school. The final three tables were average mathand reading scores and passing percentages based off of the school’s budget per student, the school size and the school type. These three tables are what you can draw a betterconclusion from.  You can see that the budget per student table actually shows that the schools that were given a higher budget per student actually have lower math and reading score averages than the schools that were given a lower budget per student. That alone doesn’t mean much though because there is a wide range of school sizes within this district. Looking at the school size table you can clearly see that the large schools with over 2,000 students, had a much lower passing rate for math, reading and overall than schools with less than 2,000 students. Even further than that, in the averages by school type, it is clear that charter schools outperform district schools. Their overall passing rate is almost 40 percentage points higher than district schools. Overall, from this data set wecan see that charter schools perform better than district schools, schools with less than 2,000 students perform better than schools with more than 2,000 students and budget per student is an unreliable metric to base school performance on. In order to get a more in-depth reason behind these conclusions, we would need to base it off of size as well as type of school and also look into the methods of teaching for individual schools. I think it would also be beneficial to know whether the student has an outside-of-school tutor which of course can greatly skew the results. I would also like to compare the socio-economic standings of the students that attend each school, as we know that affects resources available to students and in turn their grades. 

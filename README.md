# School_District_Analysis

## Project Overview
A Chief Data Scientist for a city school district is tasked with preparing all standardized test data for analysis, reporting, and presentation to provide insights about performance trends and patterns. These insights are used to inform discussions and strategic discussions at the school and district level. Data from students standardized math and reading scores as well as various information on the schools they attend was aggregated with each school's performance showcased.  

1) The district summary
2) The school summary
3) The top 5 and bottom 5 performing schools, based on the overall passing rate
4) The average math score for each grade level from each school
5) The average reading score for each grade level from each school
6) The scores by school spending per student, by school size, and by school type

## Resources
- Data Source: schools_complete.csv, students_complete.csv
- Software:Python 3.7.6, jupyter-notebook 6.0.3, Anaconda 4.13.0, Pandas, Numpy

## Challenge Overview
The school board identified evidence of academic dishonesty in altered test scores for math and reading test score, specifically, for the 9th graders at Thomas High School. The school board requested the suspect grades to be replaced by NaNs and for the results to be reassessed and the changed results to be compared and analyzed. 

## Challenge Summary
- How is the district summary affected?
The removal of the THS 9th grade scores showed a reduced Average Math Score for the district by 0.1, % Passing Math by 0.2, % Passing Reading by 0.1, and a reduction in % Overall Passing by 0.3

This is the Original district Summary
<img src="https://github.com/mcgibbenyd1/   width="450" height="500" />
This is the New district Summary
<img src="https://github.com/mcgibbenyd1/   width="450" height="500" />                                                                   
                                                                    

- How is the school summary affected?
The major affected values were the percentages for Thomas High School were affected by replacing the 9th grade student grades with NaN as the original method used the student name to calculate the denomintors. This resulted in drastically low percentages being shown as the incorrect number of student scores were being reported. To correct this the .loc method was used to filter out the 9th grade scores and only count the student names from the 10th, 11th, & 12th grades. The summary was the recalculated to accomodate only the 3 grades. No other values were affected for the other schools. 

This is the Original School Summary
<img src="https://github.com/mcgibbenyd1/   width="450" height="500" />
This is the Updated School Summary with the .value_counts affecting the percentage values
<img src="https://github.com/mcgibbenyd1/   width="450" height="500" />
This is the New Revised School Summary accomodating only to Thomas High School 10th, 11th, & 12th.
<img src="https://github.com/mcgibbenyd1/   width="450" height="500" />

- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
- How does replacing the ninth-grade scores affect the following:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type 
   

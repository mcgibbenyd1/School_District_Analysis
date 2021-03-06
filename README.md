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
   - The removal of the Thomas High School 9th grade scores showed a reduced Average Math Score for the district by 0.1, % Passing Math by 0.2, % Passing Reading by 0.1, and a reduction in % Overall Passing by 0.3

<p align="center">
Original District Summary
</p>

<p align="center">  
<img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/Original_District_Summary.png" width="85%"/>
</p>

<p align="center">
Revised District Summary
</p>

<p align="center">
<img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/New_District_Summary.png" width="80%"/>
</p>                                                                   

- How is the school summary affected?
  - The major affected values were the percentages for Thomas High School were affected by replacing the 9th grade student grades with NaN as the original method used the student name to calculate the denomintors. This resulted in drastically low percentages being shown as the incorrect number of student scores were being reported. To correct this the .loc method was used to filter out the 9th grade scores and only count the student names from the 10th, 11th, & 12th grades. The summary was the recalculated to accomodate only the 3 grades. No other values were affected for the other schools. 

<p align="center">
Original School Summary
</p>
  
<p align="center">  
<img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/Original_School_Summary.png"/>
</p>
  
<p align="center"> 
Updated School Summary with the .value_counts affecting the percentage values
</p>
  
<p align="center">
<img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/New_School_Summary.png"/>
</p>

<p align="center"> 
New Revised School Summary accomodating only to Thomas High School 10th, 11th, & 12th.
</p>
  
<p align="center">
<img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/New_Revised_School_Summary.png"/>
</p>
  
- How does replacing the ninth graders??? math and reading scores affect Thomas High School???s performance relative to the other schools?
  - Relative to the other schools Thomas was in second top school based on the overall Passing % prior to the replacement of the scores and was not a drastic enough of a change to alter the rank of the school after the change. After the change Thomas High School remained in second place with a reduction in overall passing % of 0.31% that was not enough to drop below the ranking of the next school.


- How does replacing the ninth-grade scores affect the following:
1. Math & reading scores by grade

<p align="center">
  <img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/New_Math%20Scores%20by%20Grade.png" width="41%">
&nbsp; &nbsp;
  <img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/New_Reading%20Scores%20by%20Grade.png" width="40%">
</p>

  2. Scores by school spending

<p align="center">
  <img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/School%20Spending.png" width="75%"/>
</p>
 
  3. Scores by school size

<p align="center">
  <img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/School%20Size%20Summary.png" width="90%"/>
</p>  
  
  4. Scores by school type

<p align="center">
  <img src="https://github.com/mcgibbenyd1/School_District_Analysis/blob/main/Resources/School_Type_Summary.png" width="75%"/>
</p> 
  
  
 All five summaries shown were unaffected by the removal of the suspect test scores from Thomas High school 9th grade.
 
## Overall Summary
Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
  
- Replacing the test scores with NaNs had the following outcomes:
  1. Math & reading scores by grade Dataframe shows the NaNs in the summary for 9th graders at Thomas High School
  2. The student count calculation code needed to be rewritten due to conditional of excluding the 9th grade scores to correct the percentages for Thomas High School that were reported
  3. Math average and the passing % values were reduced in the District Summary
  4. Thomas High School reading average increased slightly but the reading pass rate decreased along with the other math and overall pass %
  

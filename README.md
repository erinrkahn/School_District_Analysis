# School District Analysis

## Background

### Purpose
The purpose of this analysis is to report district and schoool metrics, utilizing two data sets (school and student data). Reports include math and reading performance scores, as well as budget and site-based metrics for schools in the district. With questions surrounding the accuracy of scores for 9th graders at Thomas High School, their math and reading scores have been removed from the overall analysis. The analysis summary includes implications of removing these scores. Data Frame summaries are included for all Thomas High School students (with 9th grade scores removed and replaced with NaN, district and school summaries, top and bottom performing schools, performance on math and reading exams by grade level, and a comparison of testing scores against budget, school size and type). The 9th grade student scores from Thomas High School were replaced by using the .loc method and the conditions ["school_name"] == "Thomas High School" and ["grade"] == "9th". The function np.nan was used to replace the scores with NaN.

###### Code Replacing 9th Grade Scores at THS 
>

## Results

### Summary of Findings

- __How is the district summary affected?__
  - The overall district summary was largely uneffected by removing the scores of 9th grade students at Thomas High School. The average math score was 79.0 and changed to 78.9, the average reading score was unchanged, % Passing went from 75 to 74.8 for math and 86 to 85.7 for reading, and the overall passing percentage changed minimally from 65 to 64.9. None of these metrics had a significant shift that warranted additional analyses or explanation.

###### District Summary with 9th Graders from THS
> 
###### District Summary with 9th Graders from THS Removed
> 

- __How is the school summary affected?__
  - Similar to the District Summary, the school summary for Thomas High School was not significantly impacted by removing the math and reading scores for the 9th grade students and all other school site summaries remained unchanged as the data for THS was the only one that was altered. The metrics that had the largest shift were "% Passing Reading" and "% Overall Passing", but with a change of 0.3 each, this was not a significant changed that impacted the integrity of the report. 

###### Thomas High School Summary with 9th Graders
> 
>
###### Thomas High School Summary with 9th Graders Removed
> 
>

- __How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?__
  - Replacing the ninth graders' math and reading scores did not impact Thomas High School's performance relative to the other schools. THS remained the 2nd top school in the district with the newly reported % Passing Math, % Passing Reading and % Overall Passing only decreasing slightly from 93.3 to 93.2, 97.3 to 97.0 and 90.9 to 90.6 respectively. 

###### Top 5 Performing Schools (with THS 9th grader data)
> 

###### Top 5 Performing Schools (without THS 9th grader data)
> 

- __How does replacing the ninth-grade scores affect the following:__
  - _Math and reading scores by grade_
    - The only impact to the math and reading scores by grade is that in the newly reported scores do not include a score for 9th graders at Thomas     Hight school (replaced with nan). All other reported scores remained unchanged.
    ###### Average Math Scores by Grade (with THS 9th grader data)
    > 
    ###### Average Math Scores by Grade (without THS 9th grader data)
    > 
    ###### Average Reading Scores by Grade (with THS 9th grader data)
    > 
    ###### Average Reading Scores by Grade (without THS 9th grader data)
    > 

  - _Scores by school spending_
    - Scores by school spending were not impacted by removing the 9th graders at Thomas High School. All reported scores are the same, given that the scores are an average of all schools within the spending range and THS average scores did not change significantly to impact the Scores by school spending in the $630-$644 range. To generate the School Spending data frame, bins were established and named and .groupby and .mean were utilized to pull and average the "Spending Range (Per Student)".
    ###### Scores by School Spending (with THS 9th grader data)
    > 
    ###### Scores by School Spending (without THS 9th grader data)
    > 
    ###### Scores by School Spending Code
    >

  - _Scores by school size_
    - Scores by school size were not impacted by removing the 9th graders at Thomas High School. All reported scores are the same, given that the scores are an average of all schools within the size range and THS average scores did not change significantly to impact the Scores by school size in the medium (1000-2000) range. To generate the School Size data frame, bins were established and named and .groupby and .mean were utilized to pull and average the "School Size".
    ###### Scores by School Size (with THS 9th grader data)
    > 
    ###### Scores by School Size (without THS 9th grader data)
    > 
    ###### Scores by School Size Code
    >

  - _Scores by school type_
    - Scores by school type were not impacted by removing the 9th graders at Thomas High School. All reported scores are the same, given that the scores are an average of all Charter schools and THS average scores did not change significantly to impact the Scores by school type for Charter Schools.
    ###### Scores by School Type (with THS 9th grader data)
    > 
    ###### Scores by School Type (without THS 9th grader data)
    > 

## Summary

### Major Changes in the Updated School District Analysis

Four major changes to the school district analysis after reading and math scores have been replaced for 9th graders at Thomas High School are;
1. 9th grade THS student scores are no longer reported in the student data and therefore cannot be included in future analyses utilizing this DataFrame. 
2. While % Math Passing, % Reading Passing, and % Overall Passing only changed slightly, the reported numbers did decrease for Thomas High School. 
3. Math and reading average scores per grade per school no longer include 9th grade students and therefore their progress cannot be tracked over the course of the year or multiples years. This may impact the interventions or services 9th grade students receive. 
4. With the 9th grade math and reading scores not reported, with could impact state funding for Thomas High School or raise concerns with incoming 9th grade families who are choosing between schools. 

# School District Analysis

## Background

### Purpose
The purpose of this analysis is to report district and school metrics, utilizing two data sets (school and student data). Reports include math and reading performance scores, as well as budget and site-based metrics for schools in the district. With questions surrounding the accuracy of scores for 9th graders at Thomas High School, their math and reading scores have been removed from the overall analysis. The analysis summary includes implications of removing these scores. Data Frame summaries are included for all Thomas High School students (with 9th grade scores removed and replaced with NaN, district and school summaries, top and bottom performing schools, performance on math and reading exams by grade level, and a comparison of testing scores against budget, school size and type). The 9th grade student scores from Thomas High School were replaced by using the .loc method and the conditions ["school_name"] == "Thomas High School" and ["grade"] == "9th". The function np.nan was used to replace the scores with NaN.

###### Code Replacing 9th Grade Scores at THS 
>![NaN Code](https://user-images.githubusercontent.com/77405273/108896742-26384e80-75ca-11eb-8b38-657ae0feb446.png)

## Results

### Summary of Findings

- __How is the district summary affected?__
  - The overall district summary was largely unaffected by removing the scores of 9th grade students at Thomas High School. The average math score was 79.0 and changed to 78.9, the average reading score was unchanged, % Passing went from 75 to 74.8 for math and 86 to 85.7 for reading, and the overall passing percentage changed minimally from 65 to 64.9. None of these metrics had a significant shift that warranted additional analyses or explanation.

###### District Summary with 9th Graders from THS
>![DSO](https://user-images.githubusercontent.com/77405273/108896734-25072180-75ca-11eb-9a66-e6aaeb26f97f.png)
###### District Summary with 9th Graders from THS Removed
>![DSN](https://user-images.githubusercontent.com/77405273/108896740-26384e80-75ca-11eb-99f7-8787372231f9.png)

- __How is the school summary affected?__
  - Similar to the District Summary, the school summary for Thomas High School was not significantly impacted by removing the math and reading scores for the 9th grade students and all other school site summaries remained unchanged as the data for THS was the only one that was altered. The metrics that had the largest shift were "% Passing Reading" and "% Overall Passing", but with a change of 0.3 each, this was not a significant changed that impacted the integrity of the report. 

###### Thomas High School Summary with 9th Graders
>![THS SO](https://user-images.githubusercontent.com/77405273/108896757-289aa880-75ca-11eb-8ee5-d368aa05e7b1.png)
>![THS SO 2](https://user-images.githubusercontent.com/77405273/108896752-28021200-75ca-11eb-93aa-c62a2d7d806d.png)
###### Thomas High School Summary with 9th Graders Removed
>![THS SN](https://user-images.githubusercontent.com/77405273/108896763-29333f00-75ca-11eb-9750-57145584f9a4.png)
>![THS SN 2](https://user-images.githubusercontent.com/77405273/108896747-26d0e500-75ca-11eb-9a62-8386f607fcc4.png)

- __How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?__
  - Replacing the ninth graders' math and reading scores did not impact Thomas High School's performance relative to the other schools. THS remained the 2nd top school in the district with the newly reported % Passing Math, % Passing Reading and % Overall Passing only decreasing slightly from 93.3 to 93.2, 97.3 to 97.0 and 90.9 to 90.6 respectively. 

###### Top 5 Performing Schools (with THS 9th grader data)
>![Top Schools O](https://user-images.githubusercontent.com/77405273/108896733-25072180-75ca-11eb-80c2-8eb419b6d589.png)

###### Top 5 Performing Schools (without THS 9th grader data)
>![Top Schools N](https://user-images.githubusercontent.com/77405273/108896738-259fb800-75ca-11eb-9e5a-a4a98db7b25b.png)

- __How does replacing the ninth-grade scores affect the following:__
  - _Math and reading scores by grade_
    - The only impact to the math and reading scores by grade is that in the newly reported scores do not include a score for 9th graders at Thomas     Hight school (replaced with nan). All other reported scores remained unchanged.
    ###### Average Math Scores by Grade (with THS 9th grader data)
    >![Math Grade O](https://user-images.githubusercontent.com/77405273/108896745-26d0e500-75ca-11eb-9d2b-8ad2bc1006d6.png)
    ###### Average Math Scores by Grade (without THS 9th grader data)
    >![Math Grade N](https://user-images.githubusercontent.com/77405273/108896754-289aa880-75ca-11eb-9680-98663afe15d3.png)
    ###### Average Reading Scores by Grade (with THS 9th grader data)
    >![Reading Grade O](https://user-images.githubusercontent.com/77405273/108896751-28021200-75ca-11eb-821b-1bd9ac5d6a33.png)
    ###### Average Reading Scores by Grade (without THS 9th grader data)
    >![Reading Grade N](https://user-images.githubusercontent.com/77405273/108896749-27697b80-75ca-11eb-8fb3-3973df3dc0fb.png)

  - _Scores by school spending_
    - Scores by school spending were not impacted by removing the 9th graders at Thomas High School. All reported scores are the same, given that the scores are an average of all schools within the spending range and THS average scores did not change significantly to impact the Scores by school spending in the $630-$644 range. To generate the School Spending data frame, bins were established and named and .groupby and .mean were utilized to pull and average the "Spending Range (Per Student)".
    ###### Scores by School Spending (with THS 9th grader data)
    >![School Spending O](https://user-images.githubusercontent.com/77405273/108896729-23d5f480-75ca-11eb-90f5-9d0cae1fa44d.png)
    ###### Scores by School Spending (without THS 9th grader data)
    >![School Spending N](https://user-images.githubusercontent.com/77405273/108896737-259fb800-75ca-11eb-9a85-278b53c423e1.png)
    ###### Scores by School Spending Code
    >![Spending code](https://user-images.githubusercontent.com/77405273/108896759-29333f00-75ca-11eb-911f-0b8e33fbbd6b.png)

  - _Scores by school size_
    - Scores by school size were not impacted by removing the 9th graders at Thomas High School. All reported scores are the same, given that the scores are an average of all schools within the size range and THS average scores did not change significantly to impact the Scores by school size in the medium (1000-2000) range. To generate the School Size data frame, bins were established and named and .groupby and .mean were utilized to pull and average the "School Size".
    ###### Scores by School Size (with THS 9th grader data)
    >![School Size O](https://user-images.githubusercontent.com/77405273/108896748-27697b80-75ca-11eb-994c-bf6c2c390f11.png)
    ###### Scores by School Size (without THS 9th grader data)
    >![School Size N](https://user-images.githubusercontent.com/77405273/108896753-28021200-75ca-11eb-8ad0-46518b166201.png)
    ###### Scores by School Size Code
    >![Size Code](https://user-images.githubusercontent.com/77405273/108896730-246e8b00-75ca-11eb-8ddc-5ae94ab8b891.png)

  - _Scores by school type_
    - Scores by school type were not impacted by removing the 9th graders at Thomas High School. All reported scores are the same, given that the scores are an average of all Charter schools and THS average scores did not change significantly to impact the Scores by school type for Charter Schools.
    ###### Scores by School Type (with THS 9th grader data)
    >![School Type O](https://user-images.githubusercontent.com/77405273/108896755-289aa880-75ca-11eb-8c87-c2c88249ba04.png)
    ###### Scores by School Type (without THS 9th grader data)
    >![School Type N](https://user-images.githubusercontent.com/77405273/108896761-29333f00-75ca-11eb-8797-f4345248e64a.png)

## Summary

### Major Changes in the Updated School District Analysis

Four major changes to the school district analysis after reading and math scores have been replaced for 9th graders at Thomas High School are;
1. 9th grade THS student scores are no longer reported in the student data and therefore cannot be included in future analyses utilizing this DataFrame. 
2. While % Math Passing, % Reading Passing, and % Overall Passing only changed slightly, the reported numbers did decrease for Thomas High School. 
3. Math and reading average scores per grade per school no longer include 9th grade students and therefore their progress cannot be tracked over the course of the year or multiples years. This may impact the interventions or services 9th grade students receive. 
4. With the 9th grade math and reading scores not reported, with could impact state funding for Thomas High School or raise concerns with incoming 9th grade families who are choosing between schools. 

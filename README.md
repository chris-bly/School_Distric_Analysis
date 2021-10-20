# School_District_Analysis
Module 4

## Overview of the School District Analysis
The purpose of developing the district-level analysis of math and reading standardized test scores for all students across the 15 high schools in the district was to provide key decision-makers with key performance trends and patterns based on school and/or student characteristics that may help drive future decision-making when allocating school funding in the future. With a limited budget, it is important that dollars spent are allocated as efficiently as possible, while also ensuring that particular groups of students of need receive additional support to raise overall standardized test scores.

Upon final analysis of the data, it is clear that both math and reading scores for the 9th grade students at Thomas High School appear to have been altered, rendering their scores unusable in a validated dataset. **The specific objective of the challenge analysis was to remove the 9th grade scores from Thomas High School for both math and meading so that updated student- and school-level data could be analyzed without the presence of inaccurate values.** In addition, comparisons between the original data and the corrected dataset should provide insight on the impact of the academically dishonest actions of the students and/or educators on the overall findings from this analysis.

To remove all the questionable data in the dataframe, it was important to change all Thomas High School 9th grade math and reading scores from the present values to "not a number". Setting the values to zero would have left the students in the dataset with inaccurate scores of 0 as opposed to being completely removed from the calculation of percent passing and average score. To perform this, the following code was utilized to change all the relevant math and reading scores to "not a number"

'''

  student_data_df.loc[(student_data_df["school_name"]==("Thomas High School")) & (student_data_df["grade"]==("9th")),   ["reading_score"]] = np.nan
  student_data_df.loc[(student_data_df["school_name"]==("Thomas High School")) & (student_data_df["grade"]==("9th")), ["math_score"]] = np.nan
  #student_data_df.tail(10)

'''
The resulting output is represented in this dataframe:
![Thomas 9th Grade Scores Adjusted](resources/sc-res_replaced_nan.png)

## Results
- How is the district summary affected?
  - a

- How is the school summary affected?
  - 

- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
  - b

- How does replacing the ninth-grade scores affect the following:
   - Math and reading scores by grade
    - c
   - Scores by school spending
    - d
   - Scores by school size
    - e
   - Scores by school type
    - f

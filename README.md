# School_District_Analysis.
## Overview of the school district analysis:
 Maria, the chief data scientist for city school districts is responsibe for analyzing information from a varieity of sources and in a variety of formats. Currently, she is tasked with presenting imsights in to  City Schools Testing Proficiency for reading and math in different high schools. These insights are used to inform discussions and strategic decisions at the school and distict level. The current analysis involves helping Maria to analyze data on student funding and student standardized test scores. The analyzed data results will help the school board regarding the decison of school budget allotment. 

First part analysis was done on the school district data to get the district summary of school such as Total schools in the district, Total students, Total Budget for all schools in the district, Average Math score, Reading score, % of students passing Math, reading, both math and reading. 

<img width="247" alt="image" src="https://user-images.githubusercontent.com/94877067/150442531-0a4f09b2-0d04-4144-8085-a117604d414a.png">



The second part of the analysis was focused on providing seven key metrics
1) A school summary which had information for each school on school type, total students in each school, total budget for each school, per school capita, average math score, reading score, % of students passing math, reading and both.

<img width="709" alt="image" src="https://user-images.githubusercontent.com/94877067/150461353-ad586b3a-05f4-4e20-ae0b-77dd537bbd08.png">


2) Identify the Top 5 and bottom 5 performing schools, based on the overall passing rate
 Top 5 Schools:
 
 <img width="689" alt="image" src="https://user-images.githubusercontent.com/94877067/150461445-f05b65ef-b816-43eb-8f92-5b3c34bb1599.png">
 
Bottom Five Schools:

<img width="701" alt="image" src="https://user-images.githubusercontent.com/94877067/150461485-ddfa3a8c-c294-4f96-b2b7-e7b2bc55f795.png">


3) The average Reading score received by students in each grade level at each school

<img width="179" alt="image" src="https://user-images.githubusercontent.com/94877067/150462821-95a8005c-3493-42a7-95a1-0214fb5a90de.png">


4) The average Math score received by students in each grade level at each school

<img width="197" alt="image" src="https://user-images.githubusercontent.com/94877067/150462740-b97a5bea-3dd9-4f1d-a62f-ad9db66601f8.png">


5) School performance based on the budget per student

<img width="495" alt="image" src="https://user-images.githubusercontent.com/94877067/150462630-d0ad4032-01f1-4cd6-b90e-2a49d5fafae5.png">


6) School performance based on the school size 

<img width="452" alt="image" src="https://user-images.githubusercontent.com/94877067/150462381-db95c08b-8b88-4fe1-9762-098a2ea951f6.png">

7) School performance based on the type of school

<img width="444" alt="image" src="https://user-images.githubusercontent.com/94877067/150462423-4c9a0a79-5940-4acd-b74a-dffd5b529f40.png">


After the analysis, the school board notified maria and her team that the student data file shows evidence of academic dishonesty, specifically, the reading and math grades for Thomas High School. So the school board has decided to uphold the state testing standards and wants us to reanalyze the data for the above metrics after replacing the math and reading scores for ninth grade in Thomas High school wth NaNs. Rest of the data will be intact and the school distirct analysis was repeated to discuss if these changes affected the over all analysis.

### Declaration: Data protected under FERPA (Family Educational Rights and Privacy Act)

## Resources:
##### schools_complete.csv - This file holds data about the schools such as type, size, budget.
##### students_complete.csv - This file hold information on students from 9th - 12 th grade in 15 different highschools in the district. We have access to which school they went to and their math and reading scores

## Results: 
##### Cleaning the Data:
Initial step in the cleaning process is to convert the ninth grade Math and reading scores in Thomas High School to NaN.
<img width="619" alt="image" src="https://user-images.githubusercontent.com/94877067/150463221-1d4e49f6-a01f-4d67-868c-d3ba523bdb1b.png">

Result was as shown below:
<img width="379" alt="image" src="https://user-images.githubusercontent.com/94877067/150463302-facfe56c-9a06-4a6a-85c6-b34fc2531c2d.png">

 The updates data frame was then used for further analysis to see if this change made affects the result of the analysis.


### District Summary Analysis

##### District Summary results before Changes:

<img width="546" alt="image" src="https://user-images.githubusercontent.com/94877067/150443079-ef56462a-5d2f-46f2-8ff9-55db3aef13e8.png">

##### District Summary results after Changes: 

<img width="569" alt="image" src="https://user-images.githubusercontent.com/94877067/150443148-5ad3d7f3-07cd-4b78-9617-74f03f0c0c43.png">

#### Effect of change in district summary:
The District summary results were not afffected by the changes. The changes applied was only for the ninth grade Math and Reading scores in Thomas High school. This shows that the ninth grade scores from Thomas high school did not have any impact on the overall numbers of math and reading scores from all the high schools.

### Per School Summary 
##### Per School Summary results before Changes:

<img width="595" alt="image" src="https://user-images.githubusercontent.com/94877067/150443914-5354148e-28c4-4c6e-b4e6-9d1e02dee2f9.png">


The above image shows the results from all the high school. As changes made were only for Thomas High School, below shown image highlights the results from Thomas High School. 

<img width="509" alt="image" src="https://user-images.githubusercontent.com/94877067/150444777-7678a557-6635-42e9-b88e-9c4c4474af84.png">
<img width="593" alt="image" src="https://user-images.githubusercontent.com/94877067/150444162-50c4d896-dc1a-4280-a351-359723ad8830.png">


##### Per School Summary results after Changes:

<img width="590" alt="image" src="https://user-images.githubusercontent.com/94877067/150444052-71b8e2e5-46c3-47ce-8b0d-8bc4bc91e1ec.png">


#### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

Thomas High School summary after Changes:

<img width="509" alt="image" src="https://user-images.githubusercontent.com/94877067/150444823-175dc833-3752-4ac0-ad20-9525a06c17ba.png">
<img width="599" alt="image" src="https://user-images.githubusercontent.com/94877067/150444556-67fda9a6-db7c-4437-beb0-092493a5d8d7.png">


From the above images before and after changes we can see  that the mean math and reading scores were not affected but there was a huge drop in the % of students passing math, reading and both for Thomas High School students. This is because the math and reading scores for the ninth grade students was made NaN and later replaced with Zero for percentage calculations. This does not reflect the correct true value as mean was claculated with total students in the high school and we have intentionally replaced Ninth grade values.

So, further analysis was performed to calculated the total number of students in each grade. From this we calculated total number of students in 10th - 12th grade.

<img width="445" alt="image" src="https://user-images.githubusercontent.com/94877067/150464402-bfafc3ec-8b62-4d60-8748-730eaf0fe18b.png">


Results show that the % passing math, reading and both increased back to that the origical data analysis (before changing Thomas High School 9th grade scores)

<img width="692" alt="image" src="https://user-images.githubusercontent.com/94877067/150464591-3b459765-d21f-4630-9bf9-69d74e3e8311.png">

Thomas High school still remianined in the list of top high schools.

<img width="563" alt="image" src="https://user-images.githubusercontent.com/94877067/150465506-abf079bd-a816-42c0-b522-ec61f0b00750.png">


#### Effect of replacing the ninth-grade scores on Math and reading scores by grade
MATH SCORES:
<img width="242" alt="image" src="https://user-images.githubusercontent.com/94877067/150466235-92b115ca-dd67-4025-baeb-30962fefe633.png">

READING SCORES: 
<img width="182" alt="image" src="https://user-images.githubusercontent.com/94877067/150466303-d62fff33-de2b-46d3-a666-188465503892.png">

The changes were obviously reflected for the ninth grade values for Thomas High School as NaN


#### Effect of replacing the ninth-grade scores on Scores by school spending

<img width="446" alt="image" src="https://user-images.githubusercontent.com/94877067/150466618-ef7c9928-2246-49d4-b656-c2805f756fe0.png">

 The changes in ninth grade THomas High School scores did not have an effect on scores by school spending.

#### Effect of replacing the ninth-grade scores on Scores by school size

<img width="451" alt="image" src="https://user-images.githubusercontent.com/94877067/150466873-3d0a1c4c-3b4b-4b45-ab70-ebe98947d660.png">



#### Effect of replacing the ninth-grade scores on Scores by school type


<img width="412" alt="image" src="https://user-images.githubusercontent.com/94877067/150466993-e2447795-7878-4266-8671-2b1197c31fa5.png">
There was no effect due to changes in the ninth grade scores at Thomas HIgh School




Summary:

There is a statement summarizing four changes to the school district analysis after reading and math scores have been replaced (5 pt).
Submission

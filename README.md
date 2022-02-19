# **School_District_Analysis**
Analysis of Reading and Math standatized testing score data from various high schools in a school distict using python.
## **Overview**
The goal of this analysis is to help the school board take an insightful decison of school budget allotment for the school district.
### **Resources**
**schools_complete.csv**

This CSV file has data about the name of high schools, School ID, School type (Distict/Charter), total size and the budget alloted for each school

**students_complete.csv**

This CSV file has data about the name of students, Student ID, Gender, Grade, School name, each student's reading and math scores

The analysis was done using the pandas (Python Data Analysis Library)

### **Deliverables**
1) A high-level snapshot of the district's key metrics, presented in a table format
2) An overview of the key metrics for each school, presented in a table format
Tables presenting each of the following metrics:
3) Top 5 and bottom 5 performing schools, based on the overall passing rate
4) The average math score received by students in each grade level at each school
5) The average reading score received by students in each grade level at each school
6) School performance based on the budget per student
7) School performance based on the school size 
8) School performance based on the type of school

### **Results and Analysis**
The very first step before analysis was to inspect and clean the dataset. The csv files were converted to data frame.
- Number of rows and columns were looked using df.shape 
Both the files were inspected for null values using the df.isnull().sum method or the df.notnull.sum() method. There was no missing values in both the data. 
- As we will be getting key metrics from the dataset which involved getting sums, averages and percentages, we want to check if the numbers in these datasets are the correct datatype. This was done using df.dtypes
- Few student names had professional prefixes and suffixes  like "Dr.","Miss", etc. The student names were split and a separte list with few of the common prefixes and suffixes was made.Each student name  was iterated over and checked for prefix and suffix. Any prefix or suffix found from the list was replaced with space (")

#### **Deliverable 1:A high-level snapshot of the district's key metrics, presented in a table format - "School District Summary"
 The school district summary will be a high-level snapshot of the district's key metrics with :
Total number of students,
Total number of schools,
Total budget,
Average math score,
Average reading score,
Percentage of students who passed math,
Percentage of students who passed reading,
Overall passing percentage
Each of these values were calculated and assigned to a variable.
These were used to create the district_summary_df dataframe. The columns were then also formated using df[column name].map() to adjust decimal places, add $ sign, add coma and percentage.

<img width="569" alt="image" src="https://user-images.githubusercontent.com/94877067/154780740-5b8f377c-4170-4f21-936c-ecd47c0bdecf.png">

#### **Deliverable 2: An overview of the key metrics for each school, presented in a table format**
school_name is set as index for this dataframe using set_index function. Key Metrics for the dataframe are:
School name,
School type,
Total students,
Total school budget,
Per student budget/per school capita - which is per school budget/per school counts,
Average math score,
Average reading score,
% passing math  with passing grade >=70,
% passing reading with passing grade >=70,
% overall passing with passing grade >=70
All the columns were then formatted to include decimal places, comma and $ where needed.

<img width="726" alt="image" src="https://user-images.githubusercontent.com/94877067/154781005-b7550131-df8c-4bdb-80ac-d8a8b06b9078.png">

- The total number of students are high in district schools than the charter schools.
- Though there was no big difference in the average math and reading score between schools 
- The result shows that there is a huge difference in the % of student passing both reading and math between charter and disrict schools with district schools having a low percentage.



#### **Top 5 and bottom 5 performing schools, based on the overall passing rate**





# School_District_Analysis

## **Overview** ##

##### **Background** ##### 

Analysis performed by request of the School District on the results of the High Schools State Board of Education Standardized Tests within the district. The analyzed data contained Mathematics and Reading test results of every student along with their High Schools information and the budget each school received for the year. The student information was managed with confidentiality following the requirements of the Family Educational Rights and Privacy Act (FERPA). Evaluation of the data was done in order to provide insights about performance, trends and patterns that could facilitate strategic decisions at the school and district level. 

##### **Methodology** #####

The students result on Mathematics and Reading were aggregated in order to generate the performance statistics for every High School.  The metric for passing each test was set to a score of 70 or higher and was utilized to calculate the passing percentage of every school by comparing it to the total amount of students. Finally, the passing scores were compared with the budget allocated to each school. The raw data was provided by the School District and was processed utilizing Jupyter Notebook with Python as programming language. 

	Data Consideration
  
1.	Errors in Data
    -	The data was reviewed prior to analysis, and it was found that some student names contained prefixes and suffixes that were incorrect. They were removed with no impact to the integrity of the data. 
2.	Removal of Data
    -	Initially, the data contained information for every High School student in the district. By request of the School Board, the information for the 9th grade students from Thomas High School was removed and is not present in the final result. This impacted the integrity of the data.  


## **Results** ##
The results of the following data analysis was performed with the information removed of the 9th grade students from Thomas High School (THS). 

	District Summary
  
![District Summary - Revised](https://user-images.githubusercontent.com/85839235/126593642-f26b005d-f3f3-4f21-a4f0-f351ad26995b.png)

This summary of the Distrcit presents a high-level overview of the data. The 39,170 students who reported test results from the 15 schools show a higher competence with Reading compared to the Mathematics test. It also shows a significant number of students being able to pass one of the test subjects but not both. 


	Per School Summary
  
![Per School Summary - Revised](https://user-images.githubusercontent.com/85839235/126593658-200e3506-0d48-42f7-afe7-2a4dea221ffa.png)

Zooming in on the data and looking at the statistics by school provides insights in certain areas that are worth investigating. 

 -	**First**, there is less variation between the scores of the schools in the Reading Test (79% - 97% passing score) compared to Mathematics (65% - 94% passing score). This contrast can be further exemplified by comparing the scores of the Top 5 and Bottom 5 schools. 


###### Top 5 Schools ######
![Top 5 Schools - Revised](https://user-images.githubusercontent.com/85839235/126593704-8280b4c6-1808-4d2e-8522-50da481d737e.png)

###### Bottom 5 Schools ######
![Bottom 5 Schools - Revised](https://user-images.githubusercontent.com/85839235/126593783-c3ca0c14-dc6f-4d83-b0ad-f78fa660d291.png)

While the Top 5 schools show variations of 2% – 4% between their Math and Reading passing percentages, the bottom 5 schools reveal a difference between 14% – 15%. 


-	**Second**, the relationship between school budgets and test results may be worthy of consideration. The Bottom 5 schools shows a higher budget for the year compared to the Top 5. That data, by itself, could be misconstrued to find an inverse relationship between school budget and their scores. Building a relationship between school budget and the amount of students, produced a Per Student Budget column. The difference between the Top 5 and Bottom 5 schools budgets shows a slight overall variation, but considerably less than comparing the budgets between schools by themselves. 

###### Performance by Spending ######
![Performance by Spending](https://user-images.githubusercontent.com/85839235/126593806-0a87ee74-b39b-48a6-9ecc-5494483b4b56.png)

To further inspect this relationship the data was sorted in different spending brackets by student and compared to the passing percentages. It illustrates that the schools that fall within the higher spending ranges per student have a lower Overall Passing percentage. While analyzing this trend further, the source of the school budget was evaluated. The budget assigned to the schools seem to have a relative direct relationship with the amounts of students. The higher the amounts of students, the higher the budget amount. Between schools of similar total students, their budgets were similar as well. This led to looking at the relationship between the number of students each school has, their budget and their performance on the tests. 
  
###### Performance by School Size ######
![Performance by School Size](https://user-images.githubusercontent.com/85839235/126593852-a9f40aa6-5725-45e4-92fc-9756d326e781.png)

The fewer number of students at the school, the smaller the budget. The apparent relationship between school budget and test results seems more reasonable if interpreted instead as a negative relationship between the amount per students the school has and test results. The higher budget seems to be an effect of the number of students and not a direct negative relationship with the test results. 

-	**Third**, there may be an influential relationship between the type of school, Charter or District, and the test results of the students.

###### Performance by School Type ######
![Performance by School Type](https://user-images.githubusercontent.com/85839235/126593940-901980b4-886c-4db0-998c-8f0198b645ff.png)

The Charter schools performed distinctively superior in all Passing Metrics in comparison with District schools. 


-	**Fourth**, a comparison between the Test Scores and the Schools by Grade was performed. 

###### Reading Score by Grade ######
![Reading_Score by Grade](https://user-images.githubusercontent.com/85839235/126593983-7b935122-d5e4-482b-a600-47367d83f8c1.png)


###### Math Score by Grade ######
![Math_Score by Grade](https://user-images.githubusercontent.com/85839235/126593991-3f1166f9-e11c-472a-9f14-00607e01a160.png)

The data gathered illustrates a consistent pattern of performance of the students within their schools. There seems to be very little variance on students performance, in both Math and Reading, in relation to their school peers. 

## **Results and Relationship with the removal of data from 9th Grade Students from THS** ##

-	All previous analysis were performed without the data of THS 9th grade students. In order to measure what possible impact this could have in the overall trends or insights, some of analysis was also performed including the 9th Grade THS Students Scores.
  
###### District Summary with the test results THS 9th Graders ######
![District Summary - Original](https://user-images.githubusercontent.com/85839235/126594042-aa60edfd-a47f-421e-8b1c-a8ee9480eb61.png)

###### District Summary without the test results THS 9th Graders ######
![District Summary - Revised](https://user-images.githubusercontent.com/85839235/126594108-9b23130a-c935-4376-adb2-dbda099ac0bd.png)

The 3 metrics for passing percentages decreased slightly when the data was removed. It would be reasonable to expect this decrease since THS students are in the Top 5 Schools by performance and seems to usually perform well. Taking in consideration the trends observed in the Fourth area of the School Summary (Test Scores and the Schools by Grade), it would be sensible to expect the results of the 9th grade students would remain similar to the scores THS 10th, 11th and 12th grades students.

-	While removing data from an analysis will almost certainly have an effect in the resulting statistics, attempts were made in order to minimize the effect on the data. When we removed the data from the 9th graders, we used an adjusted average of the passing percentage from the 10th, 11th and 12th graders. With this new passing percentage, the effect of the 9th graders passing percentage removal was minized as much as possible. Without this adjustment, the total numbers of students from the 9th grade would have show as not passing. This would have skewed the data giving THS a considerably lower passing percentage which in turn would have affected the District data.  

###### School Summary with 9th Grade THS Scores ######
![Per School Summary - Original](https://user-images.githubusercontent.com/85839235/126594164-38a45011-7d69-4337-a533-7e21e1328b8b.png)

###### School Summary without 9th Grade THS Scores – Non Adjusted ######
![Per School Summary  - THS - Omitted](https://user-images.githubusercontent.com/85839235/126594219-f03369a2-cf96-4eff-9a5e-1ccb55fe6689.png)

When THS 9th grade students data was removed, it heavily impacted the metrics for THS overall. If let uncorrected, it would have skewed all the subsequent assessment.
-	The Per School Summary shows a considerable effect on THS metrics. It would have become the lowest performing Charter School. 
-	If the data would not have been adjusted, both the Top 5 and Bottom 5 Schools would be different. THS would be removed from the Top 5 and be included in the Bottom 5.
-	Scores by School Spending, Type and Size would have been negatively impacted since it would have showed an outlier relationship of considerable lower scores when compared by those 3 metrics.   	

The metrics for the Per Student Budget remain unaffected since the 9th grade students number was still used for the statistic calculations. 

###### School Summary without 9th Grade THS Scores ######
![Per School Summary  - THS - Revised](https://user-images.githubusercontent.com/85839235/126594252-06ecd0a7-fd9e-4342-97aa-889e14e43477.png)

Utilizing the adjusted scores for THS yielded a more consistent data and minimized the effect of the removal of the 9th grade students data. As long as the final 9th grade students data doesn’t deviate from the patter of THS students in other grade, the impact of the data could be reasonably accepted and the data insights remain similar.  


## **Conclusions** ##
-	From the insights gathered it seems School Size and the Type of School (District vs Charter) may be influential in the students passing performance for the School District Standardized Tests. 
	-	Charter Schools have been know to advertise that smaller classrooms sizes are one of their benefits1️⃣. 
	-	Charter Schools are also able to set a threshold for the amount of students they accept for the school year while District Schools cannot. 
	-	The Top 5 Schools are Charter while Bottom 5 are Districts.  
-	Reading is a subject that students consistently show more proficiency. The results for Mathematics tests fluctuates greater between schools.
	 

##### Further Analysis Recommendations #####
-	School size. 
	-	Relationship between classroom density (students per teacher) and their school test results. 
	-	Relationship between school density (structural size) and number of students.

-	Analysis of spending by school.
	-	Possible budget efficiency of Charter Schools. 
	-	Identify if District schools have operating costs that Charter Schools do not have. 


#### Links ####
1️⃣ https://rhodesschools.org/differences-between-charter-and-public-schools/

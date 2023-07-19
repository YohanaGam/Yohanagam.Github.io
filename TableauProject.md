## The Education Project.

**Introduction:** 

This project is part of the Data Analytics Accelerator program that I am taking to improve and practice my Data Skills. 


Therefore, I am acting as recently hired Data Analyst with the purpose to analyze the education data from the State of Massachusetts. The Department of Education Superintendent is looking for the following:


- A report to show the school board the state of the school system 

- How does class size affect college admission?

- What are the top math schools in the state?

- What schools are struggling the most?



###  The data set


The data set is REAL data taken from Massachusetts Department of Education Website from the year 2017. It is actually a combination of multiple reports with information about  Enrollment by Grade, Enrollment by Selected Population, Enrollment by Race/Gender and etc. 


The reports can be found here. [Link](https://profiles.doe.mass.edu/statereport/)


###  Analyses


Once the data was connected to Tableau. I started to analyze the information to see how and where to go to cross information. 


Totals are important to have a sense of the big picture and to further test the analyses comparing aggregations. 


So, in the first place the total number of schools and total number of students enrolled were calculated by simply counting the schools' names and summing the students:


- Number of Schools = 1,861
- Number of Students = 943,748
- Wich means an average of  507,118 students per school
  

**1. What schools need extra attention? Thus, has lowest graduation rates?**


   A bar chart with the bottom 10 high schools in terms of graduation% is the best option to illustrate the rank. So, the % Graduated metric was crossed with the school’s names:


<img src="images/LowGrad_1.jpg?raw=true"/> 


To emphasize the numerical rates a bit more so they stand out, it was added numerical labels and to have a better view of the differences in graduation the bar colors were customized to show the worst schools in red.


<img src="images/LowGrad_2.jpg?raw=true"/>


Since it was discovered what schools are underperorming in graduation rates, the next suggested step would be to explore more and ask why those particularly schools are presenting these numbers. Some factors to consider:


- Is it the personal situation or school’s poor administration that keep students get to graduation? 
- Is there a survey from the teachers that could give a rinch in how they are feeling about the work environment?
- Do the teachers feel motivated to really help students? Do they have the basics resources for that?
- Do students and teachers feel safe in the school environment?
- Is there a annual psychological assessment to know if the students have some sort of disability and if so, are they being adressed?
- What are the specilaizations of the teachers, or methods that are being applied?
- Are there any psychological relevant constraints like racism, bullying, criminality, family, misoginy that are affecting students?


It would be very important to cross data with census data, police records, drug cases rates, air quality and/or environmental rates and so on. There are several ways to find out the root cause and even better address an effective solution. However, for now, this project is focusing in one data source.


**2. How does class size affect college admission? Or How college attendance could be increased?**


_My personal though: It was shown that almost 50% of students are not even graduating from high school, but the superintended wants to know about college admission? Maybe we could also cross political data as well, to see why the schooll administration intentions are more in college numbers than addressing the problem of the students that are not even graduating. Politics is also important to know when data analysing._


Since the graduation rate is lower investing in building more schools with the aim of lowering the average class size to hopefully increase the percentage attending college is the generic ideia that was brain stomerd from the college board. 


Furthermore, to test the hipothesis  the metric “Average Class Size” and “% Attending College” were crossed in a sclatter plot:



<img src="images/CollegevsClassSize_1.jpg?raw=true"/>


It looks like the AVG class size does not significantly impact in College admission. Common sense would believe that the less students better grades, but it is not quite what the data shows, the orange square shows the opposite. 


For example a class with 13 students (pink arrow) has 50% of college admission rate, and a class with 19 students (orange arrow) has 90% of college admission. 13 to 19 is not a very relevant range to consider, wich means does not tell much. So, there is no significantly correlation between the two metrics.


Next step was to add a 3rd metric: "% of Economically Disadvantaged" but in color formatt as shown below: 


<img src="images/CollegevsClassSize_2.jpg?raw=true"/>



The color scale shows that the darker dots are the most  Economically Disadvantaged, the lighter dots are the opposite. 


So it’s possible to see that the majority of the lighter dots are above of the line 80% Attendance College, wich means that the students that has a steady financial situation are more keen to go to college.

The solution would not be build more schools, but again analyze deeper and to understand the impacts of lower income on students. Factors to consider:


- Students need to work while studying to help their families?
- Students has the resources to learn and progress in order to have better grades?
- If student have good grades do they have the intention to apply for college? If not why? Do they have the means to pay for college? Are they motivated enough to do so?
- What are the immediately impacts on going to college for a lower income student? Or are there only after graduation benefits?
- 

**2. What are the top math schools in the state?**


The superintendent believes that 4th grade math is key to a student's feature & would like to focus on improving the state's MCAS 4thGrade Math P value (P stands for passing). 
They want to know which districts are above the desired threshold of 50% and would like to collect the names of these districts to invite some of these teachers to train the rest of the state on how they improve math scores. 


In order to do that the metric "% MCAS 4thGrade Math P" was analyzed with the metric "District Name". 


<img src="images/4thGradeMath.jpg?raw=true"/>


Since not all districts have elementary school MCAS scores, a filter was added to only allow non-null MCAS 4thGrade Math P scores. To know the top scholls the data was sorted by the math percentage descending order and the reference line and shaded colors emphasizes the 50% threshold.  In blue are the scholls with above 50% passing score and grey are the scholls needing some work.


**Conclusion**

This is a relative small project that answered 4 questions but it can trigger a lot of more questions: 
How does class size affect college admission?
What are the top math schools in the state?
What schools are struggling the most?


<img src="images/Final Dashboard.jpg?raw=true"/>





## The Education Project.

**Introduction:** This project is part of the Data Analytics Accelerator program that I am taking to improve and practice my Data Skills. 

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


<img src="images/LowGrad%_1.jpg?raw=true"/> 


To emphasize the numerical rates a bit more so they stand out, it was added numerical labels and to have a better view of the differences in graduation the bar colors were customized to show the worst schools in red.

<img src="images/LowGrad%_2.jpg?raw=true"/>

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















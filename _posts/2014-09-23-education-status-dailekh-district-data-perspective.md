---
layout: post
title: Education status in Dailekh district from data perspective
---

Crossposted from [OpenNepal.net](http://opennepal.net/blog/education-status-dailekh-district-data-perspective)

TL;DR

How open data could help get insights from the data? This blog goes through the process of finding the story of education, trapped inside the pdf document using just excel. 

<hr>

How should we go about finding the status of education? I don’t know but thought that going through the flash reports from Ministry of Education and getting the data from those reports, might give some insights. It was no easy activity. The flash report is more than 100 pages with all the data in tabular format in pdf, compressing data as much as possible.
 
![Data from Flash Report](/public/education-status-dailekh/data-pdf.png "Data from flash report")
 
It gives comprehensive data on the districts and on various indicators. Personally i don’t see the utility of those data in the report. We ventured out to see the process of getting data for one district and chose Dailekh and see if anything useful what could be produced. For ease, we just collected enrolment data for all grades, segregated by gender and ethnic group (Dalit, Janajati and others). 
 
We extracted data from annual flash reports from 2064 to 2069 and used Microsoft Excel for the analysis and charting. 
 
We simply plotted the students enrolment for grades 1 to 10 for 6 years. The dropout is seen high in Grade 2 based on the enrolment numbers only. Though the gap is higher in the beginning years, it tapers towards the later years. Could it be that the families moved out of districts after the grade 1? Or could it be that the policy focus is on grade 1 enrolment only and not on the promotion to grade 2. What could be other explanations? We are here to present what the data shows and not why it shows. If anyone decides to further delve into the why question, please let us know. 
 
![Trend of students in different growth](/public/education-status-dailekh/class-1-10-trend.png "Trend of students in different growth")
 
Gender is also an interesting aspect to see the gender distribution. We simply plotted the boys and girls total for each year. The results looks impressive. Six years aggregate data shows there’s perfect balance of 50-50 boys and girls. Can we say that gender equality is somehow maintained in Dailekh? Maybe not so fast. Lets get into more details. 
 
![Boys girls distribution in different years](/public/education-status-dailekh/boys-girls-total.png "Boys girls distribution in different years")
 
The next plot is to break down the gender distribution in different grades. For simplicity, we took the average of 6 years for each grade and the plot is an eye-opener. Female students steadily dropped to almost 41% from 50% when they reached grade 10. There could be different reasons for this trend - early marriage, helping family at home, preferring sons over daughters. Or could it that boys are better than girls in schools? I think not. Infact the other way round seems plausible as reported by [theatlantic](http://www.theatlantic.com/education/archive/2014/09/why-girls-get-better-grades-than-boys-do/380318/) - "Girls succeed over boys in school because they are more apt to plan ahead, set academic goals and put efforts into achieving those goals." 
 
![Boys girls gradewise](/public/education-status-dailekh/boys-girls-gradewise.png "Boys girls gradewise")

Looking from inclusion perspective, we can see the distribution of students among different ethnic groups. It seems that the dalit students are well represented. However deeper inspection on the distribution among different grades shows different perspective. 
 
![Distribution of students ethnicity in years](/public/education-status-dailekh/students-ethnicity-yearwise.png "Ethnicity of student in years")
 
The dalits students dropped at alarming rate on their way to grade 10. The overall students are also dropping, however dalits students seem to be affected the most. There could be more richer ways to look into the data. I leave it upto you to get deep and mash up with other data sources.
 
![Ethnicity of student distribution in different grades](/public/education-status-dailekh/ethnicity-gradewise.png "Ethnicity of student distribution in different grades")
 
Education is the top priority sector of Nepal with almost 17% of budget allocated to this sector in 2013-14. Simple analysis raises fundamental questions like whether the budget allocation is done based on the data or not and whether the budget attempts to hit the areas of concern or not. 
 
The bigger question is when will such data of national interest be available in open format so that we put our effort in the analysis for better decisions and planning than in the data cleaning process. [The New York Times has rightly pointed](http://www.nytimes.com/2014/08/18/technology/for-big-data-scientists-hurdle-to-insights-is-janitor-work.html) out that the "Janitor Work is key hurdle to insights”. We had to go through the whole extracting and cleaning process two times because the totals didn’t match when we tried to reconcile in the end. Most of our effort went into getting the data in structured form - roughly 60% of the time spent in the data cleaning and the other 40% in the analysis and writing. 
 
I don’t claim that the results presented in this blog are all correct. They are true to the data we extracted and verified. Please do not use this analysis for any purpose. We spent only 4 days for the whole process that leads to this writing. 
 
Please find the [excel file](/public/education-status-dailekh/Dailekh-education-data-analysis.xlsx) with the data and analysis.
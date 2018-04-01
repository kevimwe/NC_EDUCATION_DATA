# North Carolina Eduation 

North Carolina students continue to make gains on most measures of student learning, according to school accountability data released (News Release School-Year 2016-2017) to the State Board of Education, with more than 75 percent of public schools overall earning grades of C or better in the third year of the state’s A-F grading system.

School grades, required by state law, continue to correlate closely with the poverty levels of schools. Among all schools last year that received a D or F, 93 percent had enrollments with at least 50 percent of students from low-income families. Conversely, among schools that received at least a B, 75.7 percent had enrollments with less than 50 percent of students from low-income families.

In terms of growth achieved by schools this past year, 27.5 percent exceeded expected growth, virtually unchanged from 2014-15; 46.1 percent of schools met their expected performance, up from 44.7 percent in the previous year; and 26.4 percent fell short of their expected result, down from 27.7 percent the year before. The percentages of schools falling into the three growth categories have remained constant since 2012-13, with slight annual fluctuations up and down.

Full News Release Article http://www.ncpublicschools.org/newsroom/news/2016-17/20160901-01

### Data Source
For this project we'll be using the North Carolina Schools education data set. The data we use is a combination of multiple data tables publicly available by the North Carolina Department of Public Instruction (NCDPI) which is charged with implementing the state's public-school laws and the State Board of Education's policies and procedures governing pre-kindergarten through 12th grade public education. You can learn more about the data by visiting http://www.ncpublicschools.org/data/reports/

Our starting datasets [All_Data_By_School_Final] and [1516_Test_Scores] were taken from Dr. Drews GitHub https://github.com/jakemdrew/EducationDataNC where he combines multiple datasets from North Carolina Schools education data, preprocesses them and cleans them for Machine learning.

### Repository Organization
##### 1. *EDA/Visualization* 

In this repositiory, initial data exploration and preprocessing is performed. Features with missing data are either dropped or logically computed based on the data type. New features are also created and explored based on the data.
>>https://github.com/kevimwe/NC_EDUCATION_DATA/blob/master/NC_EDUC_Visualization_Data_Processing/NC_Graduation_Rates_Project_Combined_Notebook_Final.ipynb

##### 2. *Classification*

To gauge the health of the education system in the state of North Carolina, our team is going to focus on building models to classify the four-year graduation rate Graduation_Rate4_Yr on High school data.

Our team will build classification models to classify schools based on graduation rate of High Schools. We will begin by creating a categorical feature "Above_Avg_Graduation_Rate4_Yr" based Graduation_Rate4_Yr. "Above_Avg_Graduation_Rate4_Yr" is a binary feature binning schools as 1 if their Graduation_Rate4_Yr is above North Carolina (NC) four-year average High school graduation rate (85.4%) per http://www.dpi.state.nc.us/newsroom/news/2015-16/20150902-01 or 0 if the school’s Graduation_Rate4_Yr is below the NC State Average graduation rate. We will look at ROC curves, AUC, confusion matrix to see how well our classifiers fit our data perform.

For both cases our team hopes to measure the accuracy and performance of our models by leveraging Stratified 10-Fold Cross Validation which will be discussed in detail in our results section of this report.

##### 3. *Clustering*

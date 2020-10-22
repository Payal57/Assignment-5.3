# Assignment-5.3


4.1 A student evaluation of a teacher is on a 1-5 Leichert scale. Suppose the answers to the first 3 questions are
given in this table
Student
Enter in the data for question 1 and 2 using c(), scan(), read.table or data.entry()
q1=c(3,3,3,4,3,4,3,4,3,4)
> q2=c(5,2,5,5,2,2,5,5,4,2)
> q3=c(1,3,1,1,1,3,1,1,1,1)
1. Make a table of the results of question 1 and question 2 separately.


table(q1,q2)
> 


2. Make a contingency table of questions 1 and 2.

tmp=table(q1,q2)
> old.digits = options("digits")
> options(digits=3)
> prop.table(tmp,1)
> prop.table(tmp,2)
> prop.table(tmp)

3. Make a stacked barplot of questions 2 and 3.


>barplot(table(q2,q3))



4. Make a side-by-side barplot of all 3 questions.

boxplot(q2,q3)


!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
4.2 In the library MASS is a dataset UScereal which contains information about popular breakfast cereals. Attach
the data set as follows
> library(’MASS’)
> data(’UScereal’)
> attach(UScereal)
> names(UScereal)
Now, investigate the following relationships, and make comments on what you see. You can use tables, barplots,
scatterplots etc. to do you investigation.

[1] "mfr"       "calories"  "protein"   "fat"       "sodium"    "fibre"     "carbo"     "sugars"    "shelf"    
[10] "potassium" "vitamins"

1. The relationship between manufacturer and shelf


   shelf
mfr     1

2. The relationship between fat and vitamins

t

3. the relationship between fat and shelf

table("fat","vitamins")

vitamins
fat        1


4. the relationship between carbohydrates and sugars


table("carbohydrates","sugars")

sugars
carbohydrates        1



5. the relationship between fibre and manufacturer

table("fibres","mfr")

mfr
fibres   1



6. the relationship between sodium and sugars
table("sodium","sugars")

sugars
sodium      1


Are there other relationships you can predict and investigate?
  
  
  
  4.3The built-in data set mammals contains data on body weight versus brain weight. Use the cor to find the
Pearson and Spearman correlation coefficients. Are they similar? Plot the data using the plot command and
see if you expect them to be similar. You should be unsatisfied with this plot. Next, plot the logarithm (log)
of each variable and see if that makes a difference.

data("mammals")
> attach(mammals)
> names(mammals)
boxplot(scale(body),scale(brain))
plot(scale(body),scale(brain))

YEs same.





4.4 For the data set on housing prices, homedata , investigate the relationship between old assessed value and new.
Use old as the predictor variable. Does the data suggest a linear relationship?Are there any outliers? What
may have caused these outliers? What is the predicted new assessed value for a $75,000 house in 1970.


data("housing")
attach(housing)
names(housing)





4.5 For the florida dataset of Bush vs. Buchanan, there is another obvious outlier that indicated Buchanan
received fewer votes than expected. If you remove both the outliers, what is the predicted value for the number
of votes Buchanan would get in Miami-Dade county based on the number of Bush votes?
  

 
  
  
  4.6 For the data set emissions plot the per-Capita GDP (gross domestic product) as a predictor for the response
variable CO2 emissions. Identify the outlier and find the regression lines with this point, and without this point.
4.7 Attach the data set babies :
  > library("Simple")
> data("babies")
> attach(babies)
This data set contains much information about babies and their mothers for 1236 observations. Find the
correlation coefficient (both Pearson and Spearman) between age and weight. Repeat for the relationship
between height and weight. Make scatter plots of each pair and see if your answer makes sense.




4.8 Find a dataset that is a candidate for linear regression (you need two numeric variables, one a predictor and
                                                              one a response.) Make a scatterplot with regression line



4.9 The built-in data set mtcars contains information about cars from a 1974 Motor Trend issue. Load the data
set (data(mtcars)) and try to answer the following:
  1. What are the variable names? (Try names.)

[1] "mpg"  "cyl"  "disp" "hp"   "drat" "wt"   "qsec" "vs"   "am"   "gear" "carb"

2. what is the maximum mpg
33.9

3. Which car has this?
Toyota Corolla 

  4. What are the first 5 cars listed?
    
    head(mtcars,5)
    
  5. What horsepower (hp) does the “Valiant” have?

    
    105
  6. What are all the values for the Mercedes 450slc (Merc 450SLC)?
    
    
  7. Make a scatterplot of cylinders (cyl) vs. miles per gallon (mpg). Fit a regression line. Is this a good
candidate for linear regression?
  
  data(mtcars)
attach(mtcars)
> plot(cyl,mpg)


  Yes,it is not a good candidate for linear regression.
  

A Little Book for R for Biomedical Statistics 
=============================================

Introduction to R
-----------------

This little booklet has some information on how to use R for biomedical statistics.

R (`www.r-project.org <http://www.r-project.org/>`_) is a commonly used
free Statistics software. R allows you to carry out statistical
analyses in an interactive mode, as well as allowing simple programming.

How to check if R is installed on a Windows PC
----------------------------------------------

To use R, you first need to install the R program on your computer.

These instructions are for installing R on a Windows PC.

Before you install R on your computer, the first thing to do is to check whether
R is already installed on your computer (for example, by a previous user). To do this,
click on the "Start" menu at the bottom left of your Windows desktop, and then move your 
mouse over "All Programs" in the menu that pops up. See if "R" appears in the list
of programs that pops up. If it does, it means that R is already installed on your
computer, and you can start R by selecting "R"  (or R X.X.X, where X.X.X gives the version of R, 
eg. R 2.10.0) from the list.

|image1|

If there is an old version of R installed on the Windows PC that you are using,
it is worth installing the latest version of R, to make sure that you have all the
latest R functions available to you to use.


Installing R on a Windows PC
----------------------------

To install R on your Windows computer, follow these steps:

1. Go to `http://ftp.heanet.ie/mirrors/cran.r-project.org <http://ftp.heanet.ie/mirrors/cran.r-project.org>`_.
2. Under "Download and Install R", click on the "Windows" link.
3. Under "Subdirectories", click on the "base" link.
4. On the next page, you should see a link saying something like "Download R 2.10.1 for Windows" (or R X.X.X, where X.X.X gives the version of R, eg. R 2.11.1). 
   Click on this link.
5. You may be asked if you want to save or run a file "R-2.10.1-win32.exe". Choose "Save" and
   save the file on the Desktop. Then double-click on the icon for the file to run it.
6. You will be asked what language to install it in - choose English.
7. The R Setup Wizard will appear in a window. Click "Next" at the bottom of the R Setup wizard 
   window.
8. The next page says "Information" at the top. Click "Next" again.
9. The next page says "Information" at the top. Click "Next" again.
10. The next page says "Select Destination Location" at the top. 
    By default, it will suggest to install R in "C:\\Program Files" on your computer. 
11. Click "Next" at the bottom of the R Setup wizard window.
12. The next page says "Select components" at the top. Click "Next" again.
13. The next page says "Startup options" at the top. Click "Next" again.
14. The next page says "Select start menu folder" at the top. Click "Next" again.
15. The next page says "Select additional tasks" at the top. Click "Next" again.
16. R should now be installed. This will take about a minute. When R has finished, you will 
    see "Completing the R for Windows Setup Wizard" appear. Click "Finish".
17. If you click on the "Start" button at the bottom left of your computer screen, and then 
    choose "All programs", you can start R by selecting "R"  (or R X.X.X, where 
    X.X.X gives the version of R, eg. R 2.10.0) from the menu of programs. 
    The R console (a rectangle) should pop up:

|image3|

How to install an R library
---------------------------

R comes with some standard libraries that are installed when you install R. However, in this 
booklet I will also tell you how to use some additional R libraries that are useful, for example,
the "rmeta" library. These additional libraries do not come with the standard installation of R,
so you need to install them yourself.

Once you have installed R on a Windows computer (following the steps above), you can install 
an additional library by following the steps below:

1. Start R by clicking on the "Start" button at the bottom left of your computer screen, 
   choosing "All programs", and starting R by selecting "R" (or R X.X.X, where
   X.X.X gives the version of R, eg. R 2.10.0) from the menu of programs. 
   The R console (a rectangle) should pop up.
2. Once you have started R, you can now install an R library (eg. the "rmeta" library) by 
   using the install.packages() R function. For example, to install the "rmeta" library, type in
   the R console:

::

    > install.packages("rmeta")

3. This will ask you what website you want to download the package from, you should choose 
   "Ireland" (or another country, if you prefer). This will install the "rmeta" package.
4. The "rmeta" package is now installed. Whenever you want to use the "rmeta" package after this, 
   after starting R, you first have to load the package by typing into the R console:

::

    > library("rmeta")

Running R
-----------

To use R, you first need to start the R program on your computer.
You should have already installed R on your computer (see above). 
To start R, click on the "Start" menu at the bottom left of your
Windows desktop, and then move your mouse over "All Programs" in
the menu that pops up, and then click on 'R' (or R X.X.X, where
X.X.X gives the version of R, eg. R 2.10.0) in the list of programs
that pops up. This should bring up a new window, which is the
*R console*.

A brief introduction to R
-------------------------

You will type R commands into the R console in order to carry out
analyses in R. In the R console you will see:

.. highlight:: r

::

    >

This is the R prompt. We type the commands needed for a particular
task after this prompt. The command is carried out after you hit
the Return key.

Once you have started R, you can start typing in commands, and the
results will be calculated immediately, for example:

::

    > 2*3
    [1] 6
    > 10-3
    [1] 7

All variables (scalars, vectors, matrices, etc.) created by R are
called *objects*. In R, we assign values to variables using an
arrow. For example, we can assign the value 2\*3 to the variable
*x* using the command:

::

    > x <- 2*3 

To view the contents of any R object, just type its name, and the
contents of that R object will be displayed:

::

    > x
    [1] 6

There are several possible different types of objects in R,
including scalars, vectors, matrices, arrays, data frames, tables,
and lists. The scalar variable *x* above is one example of an R
object. While a scalar variable such as *x* has just one element, a
vector consists of several elements. The elements in a vector are
all of the same type (eg. numeric or characters), while lists may
include elements such as characters as well as numeric quantities.

To create a vector, we can use the c() (combine) function. For
example, to create a vector called *myvector* that has elements
with values 8, 6, 9, 10, and 5, we type:

::

    > myvector <- c(8, 6, 9, 10, 5)

To see the contents of the variable *myvector*, we can just type
its name:

::

    > myvector
    [1]  8  6  9 10  5

The [1] is the index of the first element in the vector. We can
extract any element of the vector by typing the vector name with
the index of that element given in square brackets. For example, to
get the value of the 4th element in the vector *myvector*, we
type:

::

    > myvector[4]
    [1] 10

In contrast to a vector, a list can contain elements of different
types, for example, both numeric and character elements. A list can
also include other variables such as a vector. The list() function
is used to create a list. For example, we could create a list
*mylist* by typing:

::

    > mylist <- list(name="Fred", wife="Mary", myvector)

We can then print out the contents of the list *mylist* by typing
its name:

::

    > mylist
    $name
    [1] "Fred"
    
    $wife
    [1] "Mary"
    
    [[3]]
    [1]  8  6  9 10  5

The elements in a list are numbered, and can be referred to using
indices. We can extract an element of a list by typing the list
name with the index of the element given in double square brackets
(in contrast to a vector, where we only use single square
brackets). Thus, we can extract the second and third elements from
*mylist* by typing:

::

    > mylist[[2]]
    [1] "Mary"
    > mylist[[3]]
    [1]  8  6  9 10  5

Elements of lists may also be named, and in this case the elements
may be referred to by giving the list name, followed by "$",
followed by the element name. For example, *mylist$name* is the
same as *mylist[[1]]* and *mylist$wife* is the same as
*mylist[[2]]*:

::

    > mylist$wife
    [1] "Mary"

We can find out the names of the named elements in a list by using
the attributes() function, for example:

::

    > attributes(mylist)
    $names
    [1] "name" "wife" ""    

When you use the attributes() function to find the named elements
of a list variable, the named elements are always listed under a
heading "$names". Therefore, we see that the named elements of the
list variable *mylist* are called "name" and "wife", and we can
retrieve their values by typing *mylist$name* and *mylist$wife*,
respectively.

Another type of object that you will encounter in R is a *table*
variable. For example, if we made a vector variable *mynames*
containing the names of children in a class, we can use the table()
function to produce a table variable that contains the number of
children with each possible name:

::

    > mynames <- c("Mary", "John", "Ann", "Sinead", "Joe", "Mary", "Jim", "John", "Simon")
    > table(mynames)
    mynames
       Ann    Jim    Joe   John   Mary  Simon Sinead 
         1      1      1      2      2      1      1 

We can store the table variable produced by the function table(),
and call the stored table "mytable", by typing:

::

    > mytable <- table(mynames)

To access elements in a table variable, you need to use double
square brackets, just like accessing elements in a list. For
example, to access the fourth element in the table *mytable* (the
number of children called "John"), we type:

::

    > mytable[[4]]
    [1] 2

Alternatively, you can use the name of the fourth element in
the table ("John") to find the value of that table element:

::

    > mytable[["John"]]
    [1] 2

Functions in R usually require *arguments*, which are input
variables (ie. objects) that are passed to them, which they then
carry out some operation on. For example, the log10() function is
passed a number, and it then calculates the log to the base 10 of
that number:

::

    > log10(100)
    2

In R, you can get help about a particular function by using the
help() function. For example, if you want help about the log10()
function, you can type:

::

    > help("log10")

When you use the help() function, a box or webpage will pop up with
information about the function that you asked for help with.

If you are not sure of the name of a function, but think you know
part of its name, you can search for the function name using the
help.search() function. For example, if you want to know if there
is a function to calculate the standard deviation of a set of
numbers, you can search for the names of all functions containing
the word "deviation" in their description by typing:

::

    > help.search("deviation")
    Help files with alias or concept or title matching
    'deviation' using fuzzy matching:
    
    genefilter::rowSds
                        Row variance and standard deviation of
                        a numeric array
    nlme::pooledSD      Extract Pooled Standard Deviation
    stats::mad          Median Absolute Deviation
    stats::sd           Standard Deviation
    vsn::meanSdPlot     Plot row standard deviations versus row

Among the functions that were found, is the function sd() in the
"stats" library (an R library that comes with the standard R
installation), which is used for calculating the standard deviation.

We can perform computations with R using objects such as scalars
and vectors. For example, to calculate the average of the values in
the vector *myvector* (ie. the average of 8, 6, 9, 10 and 5), we
can use the mean() function:

::

    > mean(myvector)
    [1] 7.6

We have been using built-in R functions such as mean(),
length(), print(), plot(), etc. We can also create our own
functions in R to do calculations that you want to carry out very
often on different input data sets. For example, we can create a
function to calculate the value of 20 plus square of some input
number:

::

    > myfunction <- function(x) { return(20 + (x*x)) }

This function will calculate the square of a number (*x*), and then
add 20 to that value. The return() statement returns the calculated
value. Once you have typed in this function, the function is then
available for use. For example, we can use the function for
different input numbers (eg. 10, 25):

::

    > myfunction(10)
    [1] 120
    > myfunction(25) 
    [1] 645

To quit R, type:

::

    > q()

Calculating Relative Risks for a Cohort Study
---------------------------------------------

One very common type of data set in biomedical statistics is a cohort study, where you have
information on people who were exposed to some treatment or environment (for example, people
who took a certain drug, or people who smoke) and also on whether the same people have a 
particular disease or not. Your data set would look something like this:

+------------+------------+-----------+
|            | Disease    | Control   |  
+============+============+===========+
| Exposed    | 156        | 9421      |
+------------+------------+-----------+
| Unexposed  | 1531       | 14797     |
+------------+------------+-----------+

You can enter the data in R by typing:

::

    > mymatrix <- matrix(c(156,9421,1531,14797),nrow=2,byrow=TRUE)
    > colnames(mymatrix) <- c("Disease","Control")
    > rownames(mymatrix) <- c("Exposed","Unexposed")
    > print(mymatrix)
               Disease Control
    Exposed       156    9421
    Unexposed    1531   14797
    
You can calculate the relative risk of having the disease given exposure in R, by using a
function calcRelativeRisk(). To be able to use this function, just copy the following code and paste
it into R:

::

    > calcRelativeRisk <- function(mymatrix,alpha=0.05,referencerow=2)
      {
         numrow <- nrow(mymatrix) 
         myrownames <- rownames(mymatrix)
         for (i in 1:numrow)
      	 {
    	    rowname <- myrownames[i]
            DiseaseUnexposed <- mymatrix[referencerow,1]
            ControlUnexposed <- mymatrix[referencerow,2]
    	    if (i != referencerow)
	    {
	       DiseaseExposed <- mymatrix[i,1]
	       ControlExposed <- mymatrix[i,2]
	       totExposed <- DiseaseExposed + ControlExposed
	       totUnexposed <- DiseaseUnexposed + ControlUnexposed
	       probDiseaseGivenExposed <- DiseaseExposed/totExposed
	       probDiseaseGivenUnexposed <- DiseaseUnexposed/totUnexposed
		
               # calculate the relative risk 
	       relativeRisk <- probDiseaseGivenExposed/probDiseaseGivenUnexposed
	       print(paste("category =", rowname, ", relative risk = ",relativeRisk))
			
	       # calculate a confidence interval
	       confidenceLevel <- (1 - alpha)*100
	       sigma <- sqrt((1/DiseaseExposed) - (1/totExposed) + (1/DiseaseUnexposed) - (1/totUnexposed)) 
	       # sigma is the standard error of estimate of log of relative risk
	       z <- qnorm(1-(alpha/2))         
	       lowervalue <- relativeRisk * exp(-z * sigma)
	       uppervalue <- relativeRisk * exp( z * sigma)
	       print(paste("category =", rowname, ", ", confidenceLevel,"% confidence interval = [",lowervalue,",",uppervalue,"]"))	
	    }
         }
      }

You can now use the function calcRelativeRisk() to calculate the relative risk of having the
disease given exposure, and a confidence interval for that relative risk. For example, to
calculate a 99% confidence interval, type:

::

    > calcRelativeRisk(mymatrix,alpha=0.01)
   [1] "category = Exposed , relative risk =  0.173721236521721"
   [1] "category = Exposed ,  99 % confidence interval = [ 0.140263410926649 , 0.215159946697844 ]"

This tells you that the estimate of the relative risk is about 0.174, and that a 99% confidence interval is [0.140, 0.215].
A relative risk of 0.174 means that the risk of disease in people who are exposed (to the treatment or environmental
factor etc. that we are examining) is 0.174 times the risk of disease of people who are not exposed. 

If the relative risk is 1 (ie. if the confidence interval includes 1), it means there is no evidence for an association between exposure and disease.
Otherwise, if the relative risk > 1, there is evidence of a positive association between exposure and disease; while
if the relative risk < 1, there is evidence of a negative association. The relative risk can be estimated for a
cohort study but not for a case-control study.

Note that we can also use the calcRelativeRisk() function in the case where we have more than
one exposure category (eg. smoking cigarettes versus smoking cigars, compared to non-smoking).
For this purpose it is used similarly to the calcOddsRatio() function (see below).

Calculating Odds Ratios for a Cohort or Case-Control Study
----------------------------------------------------------

As well as the relative risk of disease given exposure (to some treatment or environmental factor eg. smoking or some drug),
you can also calculate the odds ratio in a cohort study. The odds ratio is also commonly calculated in a case-control
study. Again, for either a cohort study or case-control study, your data will look something like this:

Your data set would look something like this:

+------------+------------+-----------+
|            | Disease    | Control   |  
+============+============+===========+
| Exposed    | 156        | 9421      |
+------------+------------+-----------+
| Unexposed  | 1531       | 14797     |
+------------+------------+-----------+

You can enter the data in R by typing:

::

    > mymatrix <- matrix(c(156,9421,1531,14797),nrow=2,byrow=TRUE)
    > colnames(mymatrix) <- c("Disease","Control")
    > rownames(mymatrix) <- c("Exposed","Unexposed")
    > print(mymatrix)
               Disease Control
    Exposed       156    9421
    Unexposed    1531   14797

You can use the following R function, calcOddsRatio() to calculate the odds ratio. You will need to copy
and paste the function into R before you can use it:

::

   > calcOddsRatio <- function(mymatrix,alpha=0.05,referencerow=2,quiet=FALSE)
   {
      numrow <- nrow(mymatrix) 
      myrownames <- rownames(mymatrix)
	
      for (i in 1:numrow)
      {
         rowname <- myrownames[i]
	 DiseaseUnexposed <- mymatrix[referencerow,1]
	 ControlUnexposed <- mymatrix[referencerow,2]
	 if (i != referencerow)
	 {
  	    DiseaseExposed <- mymatrix[i,1]
	    ControlExposed <- mymatrix[i,2]
			
   	    totExposed <- DiseaseExposed + ControlExposed
  	    totUnexposed <- DiseaseUnexposed + ControlUnexposed
			
	    probDiseaseGivenExposed <- DiseaseExposed/totExposed
	    probDiseaseGivenUnexposed <- DiseaseUnexposed/totUnexposed
	    probControlGivenExposed <- ControlExposed/totExposed
	    probControlGivenUnexposed <- ControlUnexposed/totUnexposed
	
            # calculate the odds ratio            
	    oddsRatio <- (probDiseaseGivenExposed*probControlGivenUnexposed)/(probControlGivenExposed*probDiseaseGivenUnexposed)
	    if (quiet == FALSE)
	    {
	       print(paste("category =", rowname, ", odds ratio = ",oddsRatio))
	    }
			
	    # calculate a confidence interval
	    confidenceLevel <- (1 - alpha)*100
	    sigma <- sqrt((1/DiseaseExposed)+(1/ControlExposed)+(1/DiseaseUnexposed)+(1/ControlUnexposed)) 
            # sigma is the standard error of our estimate of the log of the odds ratio
	    z <- qnorm(1-(alpha/2)) 
   	    lowervalue <- oddsRatio * exp(-z * sigma)
	    uppervalue <- oddsRatio * exp( z * sigma)
	    if (quiet == FALSE)
	    {
	       print(paste("category =", rowname, ", ", confidenceLevel,"% confidence interval = [",lowervalue,",",uppervalue,"]"))	
	    }
	 }
      }
      if (quiet == TRUE && numrow == 2) # If there are just two treatments (exposed/nonexposed)
      {
         return(oddsRatio)
      }
   } 

You can then use the function to calculate the odds ratio, and a confidence interval for the odds ratio.
For example, to calculate the odds ratio and a 95% confidence interval for the odds ratio:

::

   > calcOddsRatio(mymatrix,alpha=0.05)
   [1] "category = Exposed , odds ratio =  0.160039091621751"
   [1] "category = Exposed ,  95 % confidence interval = [ 0.135460641900536 , 0.189077140693912 ]"

This tells us that our estimate of the odds ratio is about 0.160, and a 95% confidence interval
for the odds ratio is [0.135, 0.189].

If the odds ratio is 1 (ie. if the confidence interval includes 1), it means there is no evidence for an association between exposure and disease.
Otherwise, if the odds ratio > 1, there is evidence of a positive association between exposure and disease; while
if the odds ratio < 1, there is evidence of a negative association. The odds ratio can be estimated for either a cohort
study or a case-control study.

We may also have several different exposures (for example, smoking cigarettes versus smoking cigars, compared to
no smoking). In that case, our data will look like this:

+------------+------------+-----------+
|            | Disease    | Control   |  
+============+============+===========+
| Exposure1  | 30         | 24        |
+------------+------------+-----------+
| Exposure2  | 76         | 241       |
+------------+------------+-----------+
| Unexposed  | 82         | 509       |
+------------+------------+-----------+

You can enter the data in R by typing (notice that you need to type "nrow=3" now to have 3 rows):

::

    > mymatrix <- matrix(c(30,24,76,241,82,509),nrow=3,byrow=TRUE)
    > colnames(mymatrix) <- c("Disease","Control")
    > rownames(mymatrix) <- c("Exposure1","Exposure2","Unexposed")
    > print(mymatrix)
               Disease Control
     Exposure1      30      24
     Exposure2      76     241
     Unexposed      82     509

We can again use the function calcOddsRatio() to calculate the odds ratio for each exposure category
relative to lack of exposure. We need to tell the calcOddsRatio() which row in our data matrix contains
the data for lack of exposure (row 3 here), by using the "referencerow=" argument:

::

    > calcOddsRatio(mymatrix, referencerow=3)
    [1] "category = Exposure1 , odds ratio =  7.75914634146342"
    [1] "category = Exposure1 ,  95 % confidence interval = [ 4.32163714854064 , 13.9309131884372 ]"
    [1] "category = Exposure2 , odds ratio =  1.95749418075094"
    [1] "category = Exposure2 ,  95 % confidence interval = [ 1.38263094540732 , 2.77137111707344 ]"

If your data comes from a cohort study (but not from a case-control study), you can also calculate
the relative risk for each exposure category:

::

   > calcRelativeRisk(mymatrix, referencerow=3)
   [1] "category = Exposure1 , relative risk =  4.00406504065041"
   [1] "category = Exposure1 ,  95 % confidence interval = [ 2.93130744422409 , 5.46941498113737 ]"
   [1] "category = Exposure2 , relative risk =  1.72793721628068"
   [1] "category = Exposure2 ,  95 % confidence interval = [ 1.30507489771431 , 2.2878127750653 ]"


Testing for an Association Between Disease and Exposure, in a Cohort or Case-Control Study
------------------------------------------------------------------------------------------

In a case-control or cohort study, it is interesting to do a statistical test for association
between having the disease and being exposed to some treatment or environment (for example,
smoking or taking a certain drug). 

In R, you can test for an association using the Chi-squared test, or Fisher's exact test.
For example, using our data from the example above:

::

   > print(mymatrix)
             Disease Control
   Exposure1      30      24
   Exposure2      76     241
   Unexposed      82     509
   > chisq.test(mymatrix)
        Pearson's Chi-squared test

    data:  mymatrix 
    X-squared = 60.5762, df = 2, p-value = 7.015e-14
   
   > fisher.test(mymatrix) 
       Fisher's Exact Test for Count Data

    data:  mymatrix 
    p-value = 5.263e-12
    alternative hypothesis: two.sided 
    
Here the P-value for the Chi-squared test is about 7e-14, and the P-value for Fisher's exact
test is about 5e-12. Both are very tiny (<0.05), indicating a significant association between
exposure and disease. 

Calculating the (Mantel-Haenszel) Odds Ratio when there is a Stratifying Variable 
---------------------------------------------------------------------------------

You may have data from a cohort study or case-control study that is stratified, for example,
the data may be separated (stratified) by the sex of the people studied. For example, we may
have two different tables giving information on the relationship between exposure (eg. to
a certain drug or smoking cigarettes) and having a particular disease. One of the tables
may given information for women, and the other give information for men.

Data for women:

+------------+------------+-----------+
|            | Disease    | Control   |  
+============+============+===========+
| Exposure   | 4          | 5         |
+------------+------------+-----------+
| Unexposed  | 5          | 103       |
+------------+------------+-----------+

Data for men:

+------------+------------+-----------+
|            | Disease    | Control   |  
+============+============+===========+
| Exposure   | 10         | 3         |
+------------+------------+-----------+
| Unexposed  | 5          | 43        |
+------------+------------+-----------+

We can enter our data into R as follows:

::

    > mymatrix1 <- matrix(c(4,5,5,103),nrow=2,byrow=TRUE)
    > colnames(mymatrix1) <- c("Disease","Control")
    > rownames(mymatrix1) <- c("Exposure","Unexposed")
    > print(mymatrix1)
              Disease Control
    Exposure        4       5
    Unexposed       5     103
    
    > mymatrix2 <- matrix(c(10,3,5,43),nrow=2,byrow=TRUE)
    > colnames(mymatrix2) <- c("Disease","Control")
    > rownames(mymatrix2) <- c("Exposure","Unexposed")
    > print(mymatrix2)
              Disease Control
    Exposure       10       3
    Unexposed       5      43

The Mantel-Haenszel odds ratio estimates the odds ratio for association between the exposure and disease, controlling
for the possible confounding effects of the stratifying variable (gender here). There is an R library
called "lawstat" that contains a function "cmh.test()" for calculating the Mantel-Haenszel odds ratio.
To use this function, we first need to install and load the "lawstat" R library by typing:

::

    > install.packages("lawstat")
    > library("lawstat")

You can then use the "cmh.test()" function to calculate the Mantel-Haenszel odds ratio:

::

    > myarray <- array(c(mymatrix1,mymatrix2),dim=c(2,2,2))
    > cmh.test(myarray)
        Cochran-Mantel-Haenszel Chi-square Test

      data:  myarray 
      CMH statistic = 40.512, df = 1.000, p-value = 0.000, 
      MH Estimate = 23.001, 
      Pooled Odd Ratio = 25.550, 
      Odd Ratio of level 1 = 16.480, 
      Odd Ratio of level 2 = 28.667
   
This tells you that the odds ratio for the first stratum (women) is 16.480, the
odds ratio for the second stratum (men) is 28.667, and the aggregate odds ratio that
we would get if we pooled the data for men and women is 25.550. 
The Mantel-Haenszel odds ratio is estimated to be 23.001. 

The cmh.test() function also gives you the output of the Cochran-Mantel-Haenszel Chi-squared,
which is a test for association between the disease and exposure, which controls for the
stratifying variable (gender here). In this case, the p-value for the test is given as 0.000,
indicating a significant association between disease and exposure.

Note that if the we see very different odds ratios for the two strata, it suggests that the variable 
used to separate the data into strata (gender here) is a confounder, and we should not use
the Mantel-Haenszel odds ratio. To test whether the odds ratios in the different 
strata are different, we can use a test called Tarone's test. To calculate Tarone's test,
we can use functions from the "metafor" library. We first need to install and
load the "metafor" R library:

::

    > install.packages("metafor")
    > library("metafor")

We can then use the function calcTaronesTest() below to perform Tarone's test. You will need
to copy and paste this function into R to use it:

::

    > calcTaronesTest <- function(mylist,referencerow=2)
    {
       numstrata <- length(mylist)
       # make an array "ntrt" of the number of people in the exposed group, in each stratum
       # make an array "nctrl" of the number of people in the unexposed group, in each stratum
       # make an array "ptrt" of the number of people in the exposed group that have the disease, in each stratum
       # make an array "pctrl" of the number of people in the unexposed group that have the disease, in each stratum
       # make an array "htrt" of the number of people in the exposed group that don't have the disease, in each stratum
       # make an array "hctrl" of the number of people in the unexposed group that don't have the disease, in each stratum
       ntrt <- vector()
       nctrl <- vector()
       ptrt <- vector()
       pctrl <- vector()
       htrt <- vector()
       hctrl <- vector()
       if (referencerow == 1) { nonreferencerow <- 2 }
       else                   { nonreferencerow <- 1 }
       for (i in 1:numstrata)
       {
          mymatrix <- mylist[[i]]
	  DiseaseUnexposed <- mymatrix[referencerow,1]
	  ControlUnexposed <- mymatrix[referencerow,2]
	  totUnexposed <- DiseaseUnexposed + ControlUnexposed
	  nctrl[i] <- totUnexposed
	  pctrl[i] <- DiseaseUnexposed
	  hctrl[i] <- ControlUnexposed
	  DiseaseExposed <- mymatrix[nonreferencerow,1]
	  ControlExposed <- mymatrix[nonreferencerow,2]
	  totExposed <- DiseaseExposed + ControlExposed
	  ntrt[i] <- totExposed 
	  ptrt[i] <- DiseaseExposed
	  htrt[i] <- ControlExposed
       }
       # calculate Tarone's test of homogeneity, using the rma.mh function from the "metafor" library
       tarone <- rma.mh(ptrt, htrt, pctrl, hctrl, ntrt, nctrl)
       pvalue <- tarone$TAp
       print(paste("Pvalue for Tarone's test =", pvalue))
   }


We can then use the "calcTaronesTest()" function to perform Tarone's test:
 
::

    > mylist <- list(mymatrix1,mymatrix2)
    > calcTaronesTest(mylist)
    [1] "Pvalue for Tarone's test = 0.627420741721689"
    
Here the p-value for Tarone's test is greater than 0.05, indicating that there is no
evidence for a significant difference in the odds ratio between the different strata
(between males and females, in this example).

Testing for an Association Between Exposure and Disease in a Matched Case-Control Study
---------------------------------------------------------------------------------------

In a 1-1 matched case-control study, there is a control individual who is matched to
each person who has the disease. The matched control individual has the same age, race, sex, etc.
as the person who has the disease. Then we look to see whether the control individuals and
individuals with the disease were exposed to some factor (eg. if they smoked, or took a certain
drug). The data would look something like this:

+---------------------+---------------------+----------------------+
|                     | Control, Exposed    | Control, Unexposed   |  
+=====================+=====================+======================+
| Disease, Exposed    | 10                  | 57                   |
+---------------------+---------------------+----------------------+
| Disease, Unexposed  | 13                  | 95                   |
+---------------------+---------------------+----------------------+

We can enter our data into R as follows:

::

    > mymatrix <- matrix(c(10,57,13,95),nrow=2,byrow=TRUE)
    > colnames(mymatrix) <- c("Control-Exposed","Control-Unexposed")
    > rownames(mymatrix) <- c("Disease-Exposed","Disease-Unexposed")
    > print(mymatrix)


Links and Further Reading
-------------------------

Some links are included here for further reading.

For a more in-depth introduction to R, a good online tutorial is
available on the "Kickstarting R" website,
`cran.r-project.org/doc/contrib/Lemon-kickstart <http://cran.r-project.org/doc/contrib/Lemon-kickstart/>`_.

There is another nice (slightly more in-depth) tutorial to R
available on the "Introduction to R" website,
`cran.r-project.org/doc/manuals/R-intro.html <http://cran.r-project.org/doc/manuals/R-intro.html>`_.

Acknowledgements
----------------

Thank you to Noel O'Boyle for helping in using Sphinx, `http://sphinx.pocoo.org <http://sphinx.pocoo.org>`_, to create
this document, and github, `https://github.com/ <https://github.com/>`_, to store different versions of the document
as I was writing it.

.. |image1| image:: ../_static/P0_image1.png
.. |image3| image:: ../_static/P0_image3.png
.. |image4| image:: ../_static/P0_image4.png



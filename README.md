# CRPW3_Quiz_My_Answers
 Coursera R Programming Week 3 Quiz Answer
# Coursera R programming Week 3 - Quiz Answers 
# 1- Q1 - Answer : The mean f 'Sepal.Length' for the species virginica? Please round your answer to the nearest whole number.

library(datasets)
data("iris")
?iris
mean(iris[iris$Species=="virginica",]$Sepal.Length)
[1] 7

# Q2 - Answer: The R code returns a vector of the means of the variables 'Sepal.Length', 'Sepal.Width', 'Petal.Length', and 'Petal.Width'?
apply(iris[, 1:4], 2, mean)

# Q3- Answer: Load the 'mtcars' dataset in R with the following code
library(datasets)
data("mtcars")
?mtcars

with(mtcars, tapply(mpg, cyl, mean)) # correct
sapply(split(mtcars$mpg, mtcars$cyl), mean) # correct
tapply(mtcars$mpg, mtcars$cyl, mean) # correct

# Q5- what is the absolute difference between the average horsepower 
# of 4-cylinder cars and the average horsepower of 8-cylinder cars (Round the nearest whole number) 

mean(mtcars[mtcars$cyl == "8",]$hp) - mean(mtcars[mtcars$cyl == "4",]$hp)
127

# Q6 - If you run
debug(ls)
> Execution of ‘ls’ will suspend at the beginning of the function and you will be in the browser.



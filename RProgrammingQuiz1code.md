Set WD to the one I want
  setwd("/Users/PrePhDCarolina/Desktop/DataScience/R ProgrammingQuiz1")
Make sure file exists > file.exists("rprog_data_quiz1_data.zip")
[1] TRUE
> file.exists("hw1_data.csv")
[1] TRUE
Imported data using Tools.
###Subset first 2 rows of data ( I created a new variable called Q4 )Q4 <- hw1_data[c(1,2),]
Print to console: type Q4
###How many rows and column: it s right there written on the data
Last 2 rows of dataset and print them
Q4 <- hw1_data[c(152,153),]
Q4
What is the value Ozone row 47 Q15 <- hw1_data[47,]
  Q15 <- hw1_data[47,1] ( adds an L as answer that I don't know where it comes from)

###Q16 Find how many NA values in Ozone column
    get Ozone column into new dataset Q16.2 <- hw1_data[,(1)]
    get NA values from Q16.2 into new logical vector Q16.3 <- is.na(Q16.2)
    sum TRUE or FALSE in Q 16.3 to see how many equals NA, how many TRUE, sum of sum(Q16.3)

    Try to paste all of this into one function sum(is.na(hw1_data[,(1)]))

###Q17 Mean of values in Ozone column,excluding NA
  extract all NA values ( using function from previous question) Q17.1 <- Q16.2[!is.na(Q16.2)]
  mean of Q17.1 mean(Q17.1)

or   mean(hw1_data[!is.na(hw1_data[,(1)])]) DOESNT'T WORK, dont know why

###Q18
Found answer online on a forum teaching how to do this
colMeans(subset(hw1_data,Ozone>31&Temp>90))

###Q19
colMeans(subset(hw1_data,Month==6),na.rm =TRUE) (answer is 79.1) NOTE na.rm =TRUE to ignore NA values

###Q20
  Got function from the web colMax <- function(data) sapply(data, max, na.rm = TRUE)
  then used subset colMax(subset(hw1_data,Month==5))

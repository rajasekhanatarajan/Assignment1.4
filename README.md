# Assignment1.4
Read multiple JSON files into a directory to convert into a dataset.I have files text1, text2, text3 in the directory JSON.
getwd()

Load the package required to read JSON files.
library("rjson")

Give the input file name to the function.
result <- fromJSON(file = "input.json")

Print the result.
print(result)

Load the package required to read JSON files.
library("rjson")

Give the input file name to the function.
result <- fromJSON(file = "input.json")

Convert JSON file to a data frame.
json_data_frame <- as.data.frame(result)

print(json_data_frame)

Parse the following JSON into a data frame.
js<-'{

"name": null, "release_date_local": null, "title": "3 (2011)",

"opening_weekend_take": 1234, "year": 2011,

"release_date_wide": "2011-09-16", "gross": 59954

}'

ans:

library(rjson)

data.frame(t(unlist(fromJSON(js))))

title opening_weekend_take year release_date_wide gross 3 (2011) 1234 2011 2011-09-16 59954

Write a script for Variable Binning using R.
ans:

x <- c(0,1,3,4,2,4,2,5,43,432,34,2,34,2,342,3,4,2) binned.x <- as.factor(ifelse(x > 10,"10+",x))

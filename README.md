# D-is-for-dummy_cols

The details of the codeset and plots are included in the attached Microsoft Word Document (.docx) file in this repository. 
You need to view the file in "Read Mode" to see the contents properly after downloading the same.

A Brief Introduction
======================

For the letter D, I’m going to talk about the dummy_cols functions, which isn’t actually part of the tidyverse, but hey: my posts, my rules. This function is incredibly useful for creating dummy variables, which are used in a variety of ways, including multiple regression with categorical variables. When conducting linear regression, the assumption is that both the predictor and outcome variables are numeric. To include categorical variables, you need to convert them to numeric variables. If they aren’t strictly continuous, then you instead create dummy variables to represent the different categories. If I had three levels on a categorical variable, I’d need 2 dummy variables: one to delineate category 1 from the other 2, and another to delineate category 2 (with the third category being represented by 0s on the other two variables).

There are, of course, other uses for dummy variables. For instance, at work, I was examining unique users of our testing system by time of day. Our system creates a row for every action by the user, with a time stamp. If I simply generated counts of these rows during spans of time, I would get a count of actions per hour by users (clicks, highlights, etc.), rather than individual users logged in during a given hour. So I created dummy codes by hour of day, then aggregated by unique user identifier. This was how I could generate accurate counts of how many users were online during a given hour.

To apply this procedure to the reading dataset, I used the dummy_cols function to create dummy variables (or flags) for genre. I created a long-form dataset of the top genres for each title, which you can download here. For simplicity, this file only contains Book.ID, title, and genre (with a separate entry for each genre, so some books have a single row, for one genre, and others have multiple rows, to reflect multiple genres).

DataSet as attached on this repository: reads2019_long.csv

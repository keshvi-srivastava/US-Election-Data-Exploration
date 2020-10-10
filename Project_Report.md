# Project Report
## Course - CS 418 (Introduction to Data Science)
## Term - Fall 2020

## Team - 
- Saurabh Sangwan
- Rakshitha Jayarame Gowda
- Keshvi Srivastava

## Tasks - 
#### 1. Reshape dataset election_train from long format to wide format. Hint: the reshaped dataset should contain 1205 rows and 6 columns.
#### 2. Merge reshaped dataset election_train with dataset demographics_train. Make sure that you address all inconsistencies in the names of the states and the counties before merging.
#### 3. Explore the merged dataset. How many variables does the dataset have? What is the type of these variables? Are there any irrelevant or redundant variables? If so, how will you deal with these variables?
- The dataset has 19 variables. Following are the datatypes for each variable - 

![](images/data_types.png)

- Further, the number of variables for each data types are as follows -
  
![](images/count_data_types.png)

- There are two columns - 'Year' and 'Office' which have only a single value 
for all observations which are '2018' and 'US Senator' respectively. Since these
  variables are constant for all the observations we will drop these columns from our dataset.

#### 4. Search the merged dataset for missing values. Are there any missing values? If so, how will you deal with these values?
There are 2 and 3 missing values for columns 'Republican Votes' and 'Democratic Votes' 
respectively. <br>
For the column 'Citizen Voting-Age Population' we have 56.67 % of values equal to
zero. With this large percentage of missing values we decide to drop the column/variable 
as we do not believe that it adds much value to our dataset/

#### 8. Compare Democratic counties and Republican counties in terms of age, gender, race and ethnicity, and education by computing descriptive statistics and creating plots to visualize the results. What conclusions do you make for each variable from the descriptive statistics and the plots?
Blue - 1- Democratic
Red - 0 - Republic

#### AGE
Percent of people with age between 29 and 65 are more in number for voting. Lesser percentage of people of age 65 and older are noted.  
Also we note that the age 65 and older people have voted more for Democratic

![](images/Age1.png)  ![](images/Age2.png) ![](images/Age3.png)

#### GENDER
The percentage of female and male voters are consistant,short boxes indicate that there is consistancy in the distribution of the data.
There are outliers 1.5 times the interquartile range, lower quartile for female and upper quartile for male

![](images/Gender1.png)  ![](images/Gender2.png)

#### RACE
The percentage of white, not hispanic or Latino are majority of voters, also there is likely difference between the two party voters.

![](images/Race1.png)  ![](images/Race2.png) ![](images/Race3.png)

#### ETHNICITY
The percentage of foreign born have more voting for Republic where as the percentage of non foreign born have more vote for Democratic.

![](images/Ethnicity1.png)  ![](images/Ethnicity2.png) 

#### EDUCATION
There are less percentage of voters who have not taken high shool degree .This can also infer that the voters are educated with minimun of batchelors degree.

![](images/Education1.png)  ![](images/Education2.png) 

#### 9. Based on your results for tasks 6-8, which variables in the dataset do you think are more important to determine whether a county is labeled as Democratic or Republican? Justify your answer.
We reject the null hypothesis for <b>mean median household income</b> <br>
There no is sufficient evidence to conclude that mean median household income of Democratic counties is higher or Republican counties.
But there is sufficient evidence to conclue that mean median household income may not be equal for both the party. <br>

We reject the null hypothesis <b>mean population</b> <br>
There no is sufficient evidence to conclude that mean population of Democratic counties is higher or Republican counties.
But there is sufficient evidence to conclue that mean population may not be equal for both the party. <br>

Since, we do not have sufficient evidence from the testing, we can refer to the Age, Race, Ethnicity and education of the voters determine whether a county is labeled as Democratic or Republican. <br>
<b>Justification</b>
AGE: The polulation with age 65 and older are supporters of Democratic, where as the rest of the lower age group people have moslty votes for Republic <br>
GENDER: There is no significant inference with the polulation classified as female as male <br>
RACE: The majority voters (white, not hispanic or Latino) have voting for Republic where as the minority have there preference as Democratic<br>
ETHNICITY: Here we can note that foreign born people have more than average voters for Democratic where compared to the non foreign born population <br>
EDUCATION: Here we can make conclusion on just the population without bachelors degree. Both the population with less than high school degree and bachelors degree have more support for Democratic


#### 10. Create a map of Democratic counties and Republican counties using the counties’ FIPS codes and Python’s Plotly library (plot.ly/python/county-choropleth/). Note that this dataset does not include all United States counties
![](images/newplot.png) 



# Tech Report

### Covid Data<br>
We collected the COVID-19 data from [The Covid Tracking Project](https://covidtracking.com/), a reputable and reliable volunteer organization launched from The Atlantic that is dedicated to collecting and publishing the data required to understand the COVID-19 outbreak in the United States. <br>
Our COVID-19 sample on the increase in positive case(positiveIncrease) and daily increase in total test results(totalTestResultsIncrease) is comprehensively large, as it includes all 50 US states + Washington DC from Jan 2020 to Feb 2021. Given that The Covid Tracking Project cross-check and compile racial and ethnic demographic information via [The COVID Racial Data Tracker](https://covidtracking.com/race), and long-term-care facilities via the [Long-Term-Care tracker](https://covidtracking.com/nursing-homes-long-term-care-facilities), we are confident that our sample is representative in terms of the COVID-19 patients' demography. However there are some challenges associated with the data: <br>
- Ideally COVID-19 cases in the dataset should represent unique individuals, but depending on how states "deduplicate" data of individuals who received multiple tests, duplicates might be included; 
- Lacking federal data standards, states and territories have been reporting test results in different ways, using different units, and often with unclear definitions and documentation. Over time The Covid Project have developed data definitions that are comparable between states, but discrepancies may still exists. 

The purpose of the COVID-19 US State Policy Database for this project is provide policy contexts of each state that may affect individuals' mobility going in and out of states(quarantines, state of emergency etc.). It is also developed and maintained by a reliable source, the Boston University School of Public Health. Since information that we draw from this database is mainly factual dates, we do not think that bias is a concern. Although it can be argued that many, if not all, of the state policies collected in this database are likely to influence state Covid-19 impact, but we decided to select specific policies that relate to individuals’ capacities to travel in and out of their states and drop the other columns of the database to simplify our analysis and hopefully avoid overfitting. However we may reconsider the relevance of other state policies as our analysis progresses. 




### How Clean is the Data<br>
Combining the aviation and Covid-19 data, we have approximately data points, which we can divide into the months ranging from Jan 2020 to July 2021. 


### Challenges or Observations since Data Collection<br>
1. **Minimizing residuals of our regression models**: It is clear that many other variables(mask mandates, public health information etc.) that are correlated with our dependent variable(increase in positive case) are also possibly correlated with our independent variable(stronger institutional response of a place might make people more inclined to fly there). 
2. **Estimating the infection weights of passengers from different** 

# Data Spec

## COVID-19 Data
**all-states-history.csv**  
This csv file is sourced from [The Covid Tracking Project](https://covidtracking.com/data), which collects and stores historical COVID information from all fifty states + DC. For the purpose of this project we will use the following data:  
- Date(datetime64): Date on which data was collected by The COVID Tracking Project 
- State(text): Initials of 50 US states + Washington DC
- positiveIncrease(integer): The daily increase in API field positive, which measures Cases (confirmed plus probable) calculated based on the previous day’s value
- totalTestResultsIncrease(integer): Daily increase in totalTestResults, calculated from the previous day’s value. This calculation includes all the caveats associated with Total tests/totalTestResults, and we recommend against using it at the state/territory level

**COVID-19-us-state-policy-database-2_17_2021.xlsx**  
The COVID-19 US State Policy Database tracks the dates when each US state implemented new social safety net, economic, and physical distancing policies in response to the COVID-19 pandemic, combined with data on existing health and social policies and information on state characteristics. This database is developed and maintained by researchers at the Boston University School of Public Health, and is updated at least biweekly.
For this purpose of this project we will use the following data:
- State(text): Initials of 50 US states + Washington DC
- state_of_emergency(datetime64)
- stay_at_home(datetime64)
- stay_at_home_end(datetime64)
- business_closure(datetime64)
- business_closure_end(datetime64)
- facemask_mandate(datetime64)
- facemask_mandate_end(datetime64)
- quaratine_mandate(datetime64)
- quaratine_mandate_end(datetime64)
- population_density(integer)
- population(integer) 

The data stated above are stored in covid.db, which has two tables - covid_history and covid_policy. 

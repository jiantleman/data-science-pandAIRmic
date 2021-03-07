# Data Spec

## covid table
The data in this table is sourced from [The COVID Tracking Project](https://covidtracking.com/data), which collects and stores historical COVID-19 information from all 50 states + DC. For the purpose of this project we will use the following data:  
- Date(datetime64): Date on which data was reported
- State(text): Initials of 50 US states + Washington DC
- positiveIncrease(integer): Daily increase in the number of confirmed plus probable cases of COVID-19 reported by the state or territory
- totalTestResultsIncrease(integer): Daily increase in the estimated number of viral (PCR) tests conducted

## policy table
The data in this table is sourced from the [COVID-19 US State Policy Database](https://github.com/USCOVIDpolicy/COVID-19-US-State-Policy-Database), which tracks the dates when each US state implemented new social safety net, economic, and physical distancing policies in response to the COVID-19 pandemic, combined with data on existing health and social policies and information on state characteristics. This database is developed and maintained by researchers at the Boston University School of Public Health, and is updated at least biweekly. For this purpose of this project we will use the following data:
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

## flight table

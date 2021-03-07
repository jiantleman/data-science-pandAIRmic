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
- state_of_emergency(datetime64): The date a state first issued any type of emergency declaration
- stay_at_home(datetime64): The date a state's stay at home/shelter in place order went into effect. Only included directives/orders. Did not include guidance or recommendations. Order must apply to entire state
- stay_at_home_end(datetime64): The date a state ended their stay at home/shelter in place order or allowed it to expire. Order must apply to entire state
- business_closure(datetime64): The date a state closed non-essential businesses statewide. Only included directives/orders. Did not include guidance or recommendations. Order must apply to entire state
- business_closure_end(datetime64): The date a state began to reopen businesses that were previously closed due to COVID-19 statewide. Order must apply to entire state.
- facemask_mandate(datetime64): The date a state mandated face mask use in public spaces by all individuals statewide.The order does not have to apply to all public spaces, but must apply state wide. Only included directives/orders. Did not include guidance or recommendations. Order must apply to entire state
- facemask_mandate_end(datetime64): Whether a face mask mandate is enforced through fines. Must apply to entire state.
- quaratine_mandate(datetime64): The date a state first mandated that individuals arriving in their state from any state must undergo quarantine.  Did not include guidance or recommendations. Order must apply to entire state. Quarantine order must apply to visitors using all forms of transportation to enter the state (not just air travel)
- quaratine_mandate_end(datetime64): The date a state ended all mandated quarantines for individuals arriving from out of state. If any statewide quarantines for out of state individuals is still  in effect or if the state never had a quarantine in effect  the column will bear a 0.
- population_density(integer): The population density of the state in square miles
- population(integer): The total 2018 populatio

## flight table
We downloaded two databases directly from the U.S. Department of Transportation’s Bureau of Transportation Statistics. From these databases, we collected information on the airports involved, month, and total passengers. After cleaning and organizing the data as explained in the tech report, we placed our flight data in the table flight_data in covid.db. Based on the data from USDOT, we list the total number of passengers flying between two states in every month from January until September 2020. All fields are required, and the STATE column will be used to connect aviation data with the COVID infection and policy data. We assumed that all states will have standard abbreviations, timescales will be reported in the month number, and that total passengers are reported as integers (since fractions of people cannot fly).

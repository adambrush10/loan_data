# loan_data

ETL project linking loan data and NFP data in a mySQL database

We used two sources of data, both being csv files. Source 1 was the nonfarm payroll data showing us the weekly and monthly average salary categorized by state. Source2 was a list of loan data from Q1 of 2016 on the website LendingClub. 

The NFP data required some basic cleaning and removal of null values, some aggregation to create a new yearly salary average field and a state abbreviations column was also added. This was done primarily in Python.

The LendingClub data required significant cleaning and removal of irrelevant columns and the member id column was populated with unique id’s via Python.



Our final productional database was loaded into a relational database (MySQL) 

Tables created include the following:
1.	loans
2.	NonfarmPayroll


A foreign key was created linking the following:
1.	addr_state from the loans table and abbrev from the NonfarmPayroll table.


Views we created include the following:
1.	Total Loan amount by state (total_by_state)
2.	Total delinquency rate and amount by state along with the yearly average salary growth by state (delinquencies)
3.  Total YoY growth rate by state (earnings_growth)

* additional changes included removing spaces from all names, editing the state abbreviation for Connecticut 

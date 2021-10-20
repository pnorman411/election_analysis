# Election Analysis

## Overview of the Election Audit

The Colorado Board of Elections has requested an audit of the election results for the U.S. Congressional Precinct in Colorado. The Board would like to automate the process so the script can be used to audit other elections, such as senatorial districts and local elections. The use of Python functionality including dictionaries, for loops, and writing to a text file will be used for this project. 


## Election Audit Results

The audit returned the following results:

###    Total Votes: <span style="color:red">369,711</span> 

###     County Votes and Percentage of Total Votes:

            * Jefferson: 38,855 votes / 10.5%

            * Denver: 306,055 votes / 82.8%

            * Arapahoe: 24,801 votes / 6.7%

###     Largest County Turnout: <span style="color:red">Denver</span>


###     Candidate Votes and Percentage of Total Votes:

           * Charles Casper Stockham: 85,213 votes / 23.0%

           * Diana DeGette: 272,892 votes / 73.8%

           * Raymon Anthony Doane: 11,606 votes / 3.1%

###     Winning Candidate Information:

           * Winner: Diana DeGette

           * Winning Vote Count: 272,892

           * Winning Percentage: 73.8%


## Election Audit Summary

The election audit project successfully tallied the county votes, percentage of votes, and identified Denver as the county with the largest turnout. The project also tallied each candidate's votes, percentage of total votes, and confirmed Diana DeGette as the winning candidate.

I propose that this script be modified for future elections.  Not only could this script be used for future congressional elections but other local and senatorial elections.

### Modification Examples to the Script

Some simple modifications to the script would allow for easy tallying of any election data.

#### Pulling Data from a Different CSV

To pull data for a different election, the path in line 6 of the code would need to be modified to list the correct folder, referenced here as "Resources" and the correct CSV, listed here as "election_results.csv"

    file_to_load = os.path.join("Resources", "election_results.csv")

#### Verify Candidate and County Information

To retrieve the candidate and county in each row, lines 32 & 35 of the code would need to be verified or adjusted according to the new CSV holding the election data.  "row[2]" is pulling the 3rd column of information from each row of the CSV because the list index starts with 0.

        candidate_name = row[2]

        county_name = row[1]

With the proper modifications, this script can be used to pull and calculate election data from any CSV.

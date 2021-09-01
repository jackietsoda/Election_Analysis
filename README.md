# Election Analysis

## Project Overview
The election commission has requested some additional data to complete the audit of a recent local congressional election. I have found the voter turnout for each county, the percentage of votes from each county out of the total count, and the county with the highest turnout. I have also included the number of votes and the percentage of the total votes each candidate received.

## Election Audit Results 
**1. How many votes were cast in this congressional election?** 

369,711

**2. Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.**
  
County Votes:
  
Jefferson: 10.5% (38,855)
  
Denver: 82.8% (306,055)
  
Arapahoe: 6.7% (24,801)

**3. Which county had the largest number of votes?** 

Denver

**4. Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.**

Candidate Votes:

Charles Casper Stockham: 23.0% (85,213)

Diana DeGette: 73.8% (272,892)

Raymon Anthony Doane: 3.1% (11,606)

**5. Which candidate won the election, what was their vote count, and what was their percentage of the total votes?**

Winner: Diana DeGette

Winning Vote Count: 272,892

Winning Percentage: 73.8%

## Summary
Prepared for the Election Commission:

This script is extremely useful for calculating the number of votes and percentage for each candidate and county in this election. This script can be modified to be used for other elections as well.

Two things I would modify is including which politcal party each candidate is running for and another thing is adding important dates during the election like speeches from the candidates or deadlines for ballots.

- We can modify the script by adding another column in the file named "Political Party." We can add in the political party in the original 'for loop' to find the candidate name so that the script will look like this:

        for row in reader:
        
        # Add to the total vote count
        total_votes = total_votes + 1

        # Get the candidate name from each row.
        candidate_name = row[2]

        # Extract the county name from each row.
        county_name = row[1]
        
        # Extract the political party from each row
        political_party = row[3]

- Another way to modify the script is to track the important dates in chronological order. You can do this by including this script: 
        
        from datetime import datetime
        A=['4/21/2015', '10/14/2014', '9/16/2014', '7/10/2014', '8/11/2014', '8/3/2014', '7/20/2014', '7/6/2014', '4/21/2015', '4/21/2015']
        
        # create a list of sorted datetime objects
        sorted_dates = sorted([datetime.strptime(d, FORMAT) for d in A])

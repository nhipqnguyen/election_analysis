# Election_Analysis

# Project Overview
A Colorado Board of Elections has given us the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Challenge Overview
After getting the results of the election, the election commission would like some additional data to complete the audit. Our additional tasks are:

6. Get a complete list of counties where voters were from.
8. Calculate the voter turnout for each county
9. Calculate the percentage of votes from each counties out of the total count.
10. Determine the county with the higest turnout.

## Resources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code, 1.56.2

## Election-Audit Results
Below is a screeenshot of the results text file after running our Python script:

![Results Text File](https://github.com/nhipqnguyen/election_analysis/blob/main/analysis/election_analysis_screenshot.png)

The analysis of the election shows that:
- There were 369,711 votes cast in this congressional election.
- The voters were from 3 counties and here is the number and percentage of votes for each county:
  - 10.5% of the votes and 38,855 number of votes were from Jefferson County.
  - 82.8% of the votes and 306,055 number of votes were from Denver County.
  - 6.7% of the votes and 24,801 number of votes were from Arapahoe County.
- The county that had the largest number of votes was: Denver County.
- The candidates were:
  - Charles Casper Stockham
  - Diana DeGette
  - Raymon Anthony Doane
- The candidate results were:
  - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
  - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
  - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
- The winner of the election was:
  - Diana DeGette who received 73.8% of the vote and 272,892 number of votes.

## Election-Audit Summary
To generate the results of this election, we've written a Python script that has the following function: 
- It goes though each row in the given text file,
  - gets the candidate name and puts it in a list of candidates if it's not already in there, then increments the vote count for that candidate by 1,
  - gets the county name and puts it in a list of counties if it's not already in there, then increments the vote count for that county by 1,
  - increments the total count of votes by 1.
- Then it uses the vote count for each county and each candidate to calculate the percentage out of the total number of votes.
- The last step is to determine the winner (the candidate with the most votes) and the county with the largest number of votes.

With its function to read data from a text file, retrieve the important attributes, do mathematical calculations, and return the requested results, this script can be used to analyze not just this election, but any election. Here are 2 examples:
 - For a federal election by state or district, we can replace all the county variables in our current script to state or district variables.
 - For the U.S. Presidential election which is based on the Electoral College system, instead of determining the winner by the popular votes, we can modify the script to calculate the number of votes each candidate wins in a state, from there we decide whether the state is red or blue, then add the number of electoral votes of that state to the vote count of the winning candidate. We then calculate the percentage out of 538 electoral votes for each candidate and whoever has the higher percentage wins the election.

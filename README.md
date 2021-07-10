# Election_Analysis
## Project Overview
Helping Tom and Seth for the election audit cast in Colorado. Performing analysis for election result with Python, we completed the task below:
  1. Calculate the total number of votes cast
  2. Find out the voter turnout for each county
  3. Find out the percentage of votes from each county out of the total count
  4. Find out the county with the highest turnout
  5. Find out the percentage of votes each candidate won
  6. Find out the total number of votes each candidate won
  7. Giving out the Summary of the winner of the election based on popular vote.
  
## Election-Audit Results
![Election_Results](https://github.com/rykiprince/Election_Analysis/blob/main/analysis/Election_Results.png)

- There were total 369,711 votes cast in the election.
- The county results were:
  - Jefferson County received **10.5%** of the vote and **38,855** number of votes.
  - Denver County received **82.8%** of the vote and **306,055** number of votes.
  - Arapahoe County received **6.7%** of the vote and **24,801** number of votes.
- Denver County had the largest number of votes, **306,055**.
- The candidate results were:
  - Charles Casper Stockham received **23.0%** of the vote and **85,213** number of votes.
  - Diana DeGette received **73.8%** of the vote and **272,892** number of votes.
  - Raymon Anthony Doane received **3.1%** of the vote and **11,606** number of votes.
- **Diana DeGette**, who received **73.8%** of the vote and **272,892** number of votes. 

## Election-Audit Summary
The script we created for this election audit will fit furthur election as long as they have the same format for the data sources, with Ballot ID, County, and Candidate as headers. If there is additional information category, it's easily to be modified as well.
Let say we are now modifying this script for a election that also contain the political party information
- Now, we might have additional factor for the ballot such as "political party". While we declare all the variables in this script, we use the `for` loop to go through the whole data set, e.g.:
  ```
  with open(file_to_load) as election_data:
      reader = csv.reader(election_data)
      header = next(reader)
      for row in reader:

          total_votes = total_votes + 1

          candidate_name = row[2]

          county_name = row[1]
    ```
  So the new data column will be easily add within the `for` loop, and the script will read it through out the file. We can extract the political party from each row by declare is as `row[#]`. Also, ensure the index is correctly indicating the column.
  
- Besides, we used well-named variables indicating all the list, and dict

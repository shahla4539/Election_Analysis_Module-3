# Election_Analysis_Module-3

# Overview of Election Audit
I am assisting **Tom**,Colorado Board of Election employee to **Audit** congressional election results. For this I will be using Python as Python can be very helpful to automate the process with simplfied codes. I am given task of reporting 
* The total numbers of votes cast,
* The total number of votes for each candidate,
* The percentage of votes for each candidate and
* The **Winner** of the Election based on the popular votes. 

After the completion of vote count my job is to generate a vote count report **Election Analysis** based on the final Election results. With successfully coding and creating an Election Analysis, Tom`s manager wants to utilize these codes not only for other congressinal district elections but also for sanatorial and local elections.

# Election-Audit Results


### Total number of votes cast in this congressional election:
I created a vaiable to initialize the total vote count 

        # Initialize a total vote counter 
        total_votes = 0

Later I ran the FOR loop to to read each row in the CSV file
   
        #For each row in the CSV file.
        for row in reader:
      
        # Add to the total vote count
        total_votes = total_votes + 1
        

![image](https://user-images.githubusercontent.com/105535250/176986469-ef8c697b-e3c6-4adc-bb73-5448dde126c7.png)


### Breakdown of the number of votes and the percentage of total votes for each county in the precinct:
Following are the code I used to find the percentage and total vote for each county:

       # 6a: Write a for loop to get the county from the county dictionary.
        for county in county_votes:

        # 6b: Retrieve the county vote count.
        vote_count=county_votes[county]

        # 6c: Calculate the percentage of votes for the county.
        percentage_vote=(vote_count/total_votes)*100.0

        # 6d: Print the county results to the terminal.
        county_results = (
            f"{county}: {percentage_vote:.1f}% ({vote_count:,})\n")
        print(county_results)
       
    
* Name of county which has the largest number of votes

* Provided is a breakdown of the number of votes and the percentage of the total votes each candidate received.

* Which candidate won the election, what was their vote count, and what was their percentage of the total votes?

* Winner of the election, their vote count, the percentage of the total votes



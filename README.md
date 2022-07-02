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
    Initialize a total vote counter 
                total_votes = 0
Later I ran the FOR loop to to read each row in the CSV file
    For each row in the CSV file.
    for row in reader:
      
        # Add to the total vote count
        total_votes = total_votes + 1

* Provided is a breakdown of the number of votes and the percentage of total votes for each county in the precinct.

* Name of county which has the largest number of votes

* Provided is a breakdown of the number of votes and the percentage of the total votes each candidate received.

* Which candidate won the election, what was their vote count, and what was their percentage of the total votes?

* Winner of the election, their vote count, the percentage of the total votes



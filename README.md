# Election_Analysis_Module-3

# Overview of Election Audit
I am assisting **Tom**,Colorado Board of Election employee to **Audit** congressional election results. For this I will be using Python as Python can be very helpful to automate the process with simplfied codes. I am given task of reporting 
* The total numbers of votes cast,
* The total number of votes for each candidate,
* The percentage of votes for each candidate and
* The **Winner** of the Election based on the popular votes. 

After the completion of vote count my job is to generate a vote count report **Election Analysis** based on the final Election results. With successfully coding and creating an Election Analysis, Tom`s manager wants to utilize these codes not only for other congressinal district elections but also for sanatorial and local elections.

# Election-Audit Results


* **Total number of votes cast in this congressional election:**
I created a vaiable to initialize the total vote count 

        # Initialize a total vote counter 
        total_votes = 0

Later I ran the FOR loop to to read each row in the CSV file
   
        #For each row in the CSV file.
        for row in reader:
      
        # Add to the total vote count
        total_votes = total_votes + 1
        

![image](https://user-images.githubusercontent.com/105535250/176986469-ef8c697b-e3c6-4adc-bb73-5448dde126c7.png)


* **Breakdown of the number of votes and the percentage of total votes for each county in the precinct:**
Following are the code I used to find the percentage and total vote for each county:

First I created a county list and a vote dictionary,

        # 1: Create a county list and county votes dictionary.
        county_options=[]
        county_votes={}
        
 Then ran the following if statement:
 
        # 4a: Write an if statement that checks that the
        # county does not match any existing county in the county list.
        if county_name not in county_options:

            # 4b: Add the existing county to the list of counties.
            county_options.append(county_name)

            # 4c: Begin tracking the county's vote count.
            county_votes[county_name]=0

        # 5: Add a vote to that county's vote count.
        county_votes[county_name]+=1
        
  Added for loop to do the county vote count also applied percentage formula as follows:     

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
       
![image](https://user-images.githubusercontent.com/105535250/176986833-af83017f-7ac3-41ef-91e8-06dac75416bd.png)

    
* **Name of county which has the largest number of votes:**
Created variable then utilized the following codes:

        # 2: Track the largest county and county voter turnout.
        largest_county = ""
        largest_county_count = 0
        largest_county_percentage = 0
        
        # 6f: Write an if statement to determine the winning county and get its vote count.
        if largest_county_count<vote_count:
            largest_county = county
            largest_county_count = vote_count
            largest_county_percentage = percentage_vote
            
  ![image](https://user-images.githubusercontent.com/105535250/176987270-03336bd5-3f94-4355-9925-0638c0ea9a29.png)



* **Breakdown of the number of votes and the percentage of the total votes each candidate received:**

        # Candidate Options and candidate votes.
        candidate_options = []
        candidate_votes = {}

        # Get the candidate name from each row.
        candidate_name = row[2]

If statement:
        # If the candidate does not match any existing candidate add it to
        # the candidate list
        if candidate_name not in candidate_options:

        # Add the candidate name to the candidate list.
        candidate_options.append(candidate_name)

        # And begin tracking that candidate's voter count.
        candidate_votes[candidate_name] = 0

        # Add a vote to that candidate's count
        candidate_votes[candidate_name] += 1
       
For loop:       
        # Save the final candidate vote count to the text file.
        for candidate_name in candidate_votes:

        # Retrieve vote count and percentage
        votes = candidate_votes.get(candidate_name)
        vote_percentage = float(votes) / float(total_votes) * 100
        candidate_results = (
            f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")
            
![image](https://user-images.githubusercontent.com/105535250/176987795-865b1ab0-dafd-453e-a78a-8be910fcf2a3.png)

* **Winner of the election, their vote count, the percentage of the total votes:**

        # Determine winning vote count, winning percentage, and candidate.
        if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage

![image](https://user-images.githubusercontent.com/105535250/176987836-313753a9-fcd5-406e-9acf-17906cb6cb05.png)

## Election-Audit Summary: 



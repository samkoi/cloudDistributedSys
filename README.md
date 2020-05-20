Assignment 2 DSAM
============================

The following functionalities have been implemented in the assignment:

/candidate =Only accessible after sign in. 
			This allows you to create candidates for election. A candidate can participate in multiple elections.

/election = Only accessible after sign in.
			Gives you the option to create multiple election.
			Assign start date/time.
			Assign end date/time.
			Upload voter email ids (should be comma-separated-value file (.csv))
			Select candidates participating in the election.
			

/vote?electionID={id}  = "id" is the election id sent to voters through mail.
						If the election hasn't started or already ended, error message is shown.
						Check is implemented on "doPost" method as well.
						Imitates ballot box to select one candidate and enter token.

/result      = Gives the list of completed election whose results are now visible.
				Gives record of total no. of voters, votes cast and individual candidates' votes.
				
/reminder   = CRON job triggers this URL and all the voters with election in next 24 hours are sent a reminder email.
			

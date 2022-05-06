# Go-Lang-IPL-Project-20280056

Attachments area
/*
Fantasy Points IPL Project Description
--------------------------------------
This project consist of 6 services categorized into 2 services. They are Player-Services and Fantasy-Services.
1. Player services:
   There are 4 player services which are used to manupulate data related to players in DB.
	1.1. Posting Player details.
	1.2. Posting Player scores.
	1.3. Getting Player details.
	1.4. Getting Player scores.

2. Fantasy services:
   There are 2 fantasy services which are uses player services to get fantasy scores and populate cap-holders.
	2.1. Getting Fantasy scores.
	2.2. Getting cap-holder players based on their performance.
===================================================================
Code Description
----------------
*** This project is designed without database with the help of slices. I considered slice as DB in this project.***

*** Virat and Dhoni data are added intially to the DB(slice) for reference.***

*** All the inputs and output of the 6 services created in this project are designed in a format as per the document shared.***

*** Basic authorization is added to this code so that authorized people can able to access the data provide by the API services. Refer code for authorization details like username and password.***

PlayerService is the main slice which contains the details of player like ID, Name, Team along with there score details like Match Number, Runs, Wickets secured in the matches played.

1. "postPlayer" is a function used to post the player details like ID, Name, Team to the DB(slice) through Rest API with POST method.

2. "postPlayerScore" is a function used to post the player score details like Matchnumber, Runs, Wickets to the DB(slice) by considering the player ID as a parameter through Rest API with POST method.

3. "getPlayers" is a function used to get all player details like ID, Name, Team from the DB(slice), accessed using Rest API with GET method.

4. "getPlayerScore" is a function used to get all player score details like Matchnumber, Runs, Wickets of all the matches along with ID of the player from the DB(slice), accessed using Rest API with GET method.

5. "fantasyScoreCal" is a function that calculates the fantasy-score of all the players based on their individual performance from the matches they played by considering their scores present in DB(slice), accessed using Rest API with GET method.
*** Fantasy score is calculated as per the logic mentioned in the document.***

6. "capHolders" is a function that generates cap-holders based on their performance taken from DB(silce), accessed using Rest API with GET method.
*** Cap-Holders are generated as per the logic mentioned in the document.***
============================================================================
Response Codes
--------------
200 OK 			- represents, API request is made successfully.
403 Unauthorized 	- represents, API request is denied due to invalid username or password or both.
405 Method Not Allowed 	- represents, ID or Name or both the details of player given while posting is invalid.

Validations
-----------
Username and password in authorization need to be given properly. Otherwise request will be failed.
ID or Name of the player should be sent properly while posting the player details. 
==============================================================================================================
ReadMe of IPL Project.txt
Displaying ReadMe of IPL Project.txt.

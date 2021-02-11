Installations:
pip3 install sqlite3
pip3 install python3

1) The way to run this code is to use the following command from terminal:
$Python3 egenv2.py

** Incase you need to schedule a cron job please refer the document steps_for_scheduling_cronjob

Note : I have scheduled the cron job for 12:15 AM everyday everymonth as the  data in the link gets updated everyday at 12:00 AM
Please refer the screenshot for the same. 


Explanation of the code:
1) First get the data from URL using get_data method.We retrieve the data using key 'data'.
2) Then we use set_data method to use those data which is a list and put it into dataframe.
3) Then we have created create_database and load_datbase to load the dataframe into sqlite3 based on each county.
Each County belongs to one table in the database.
   

For testing if the data has been loaded into the SQL DB
please uncomment the print result under main function which will call the test_results method and test the database only for "Bronx" county.


Ways I can work forward to make this code better:
1) Use Multi-threading using concurrent.futures and can decrease the time taken to pull data from URL.
2) Work on Unit Testing using Pytest Library make a function using county name as input parameter check the output result if it is present in sqlite\db\pythonsqlite.db.



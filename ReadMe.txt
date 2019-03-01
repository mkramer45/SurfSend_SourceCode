


Package Summary:

1.) routes.py file is our routes file (Flask framework) ... this file needs to be running on the server at all times for our web app to function.

2.) SurfScraper.py is our web-scraping script that runs each morning at 6:00AM EST. Responsible for updating our SQLite database with data that the web app consists of.

3.) DailyDBTruncateScript is responsible for wiping our database clean of all data pertaining to surf information. This runs every day BEFORE SurfScraper.py - in order to give us a nice, clean database to start fresh with everyday. This script does NOT touch anything relating to our User database (info we need to save).

4.) DailyEmailScripts directory contains beach-specific scripts that are responsible for sending email alerts to registered users ONLY IF their beach satisfies all of the requirements for good surf conditions. No email alert will be sent if the conditions aren't deemed proper by SurfSend standards. These are scheduled to be run everyday at 6:15.

4.) DailySMS_Scripts directory contains beach-specific scripts that are responsible for sending SMS text message alerts to registered users ONLY IF their beach satisfies all of the requirements for good surf conditions. No SMS text message alert will be sent if the conditions aren't deemed proper by SurfSend standards. These are scheduled to be run everyday at 6:15.

5.) templates directory contains all of our HTML pages & static images used throughout the website (flask framework).

Any questions, please email mkramer789@gmail.com
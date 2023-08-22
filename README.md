# google-cal-working-locations
Tool to display working locations for the last financial year - ATO (Australia)

## Requirements
- Python 3.8
- Python Package Installer (Pip)

## About
This tool is designed to export the working locations value
from a Google calendar. I created this as i noticed there's
currently no way to export the 'Location' event from your
Google calendar. As it happens, I keep this value up to date
throughout the year, so that I know which days I work from 
home. The ATO decided they needed evidence of when you
worked from home. But until I created this tool there was
no way of getting the values.

## Setup
Follow the steps below to get set up.

### 1) Get a client secret for the API
See the Google Developer link, (https://developers.google.com/calendar/quickstart/python).
Just follow the steps which lead to a credentials.json file being downloaded. Once done,
place that file in the root of this repository directory.

### 2) Setup the virtualenv
Create a virtual environment:

        python3 -m venv exportcal
        
        source exportcal/bin/activate

Install the requirements:

        pip3 install -r pip3-requirements.txt

### 3) Execute the script

        python3 export-working-locations.py

When you execute this, a browser window will launch asking you to login
to your Google account. You must then click Approve to allow access to 
your calendar.

Once approved, this tool will output the daily working locations from your
Calendar between 1st July 2022 and 30th June 2023
(you can adjust the dates in the code accordingly).


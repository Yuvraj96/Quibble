# Quibble
Quibble is a marks entering software which automates the process of Internal Assessment Tests mapping with course outcome mapping and various marks calculations. It makes use of a database to store all details required, allowing the user to pickup their work from where they left-off. It does various sanity checks and validations to avoid potential mistakes. The software automatically generates attainment for each Course outcome dependent on given criteria.

## Technologies used
Electron
Material Design Lite
Firebase
Web Technologies (HTML, CSS, JavaScript) 

## Minimum Requirements
Processor: 1 gigahertz (GHz) or faster processor
OS: Windows 7 or above
RAM: 1GB or above
Space: 160MB free
Internet Connection

## Implementation Details
-In order to use the application teachers will have to register with their official SFIT email ID (@sfitengg.org). The registration details will be stored in the firebase auth database.
-These registration details will be their login credentials whenever they have to use the software.
-After login, teachers will enter the details like class, year, etc. for which they want to enter the marks and/or mapping.
-There will be a lookup in the database to see if the student list of that class for that year already exists else teachers will have to upload the excel sheet consisting of student name, PID no and roll no.
-After details, teachers will enter CO of each question unless already entered.
-The CO mapping is stored in the Firebase Realtime database.
-Teachers will then start entering marks of each student. If the teachers already have entered marks in an excel file (for previous years), the marks can be entered directly by uploading the excel file.
-They can also resume the marks entering as the data will be stored in the realtime database.
-A tick will appear next to the names of students whose marks have been entered.
-After entering marks of all the required students, teacher can generate the CO mapping table with all marks and attainments automatically generated.
-The PDF of this table can be saved automatically to the desktop.

## Key features

### Web based Software
-Being a web based software means we get to enjoy the ease of development usually associated with web projects.
-Not running it in a browser as a website allows us to control flow of the software and prevent certain user actions (jumping to pages, back, forward, etc).
-We also get access to some lower level system functions not easily available through browser (like directly saving pdf to desktop).

### Restricted access
-The login, registration and related functions are all handled through the firebase auth database
-This keeps us from having to re-invent the wheel and provides us with all new and advanced security features from google.
-Only users with confirmed-email @sfitengg.org can use the software.
-Even if someone somehow gets access with another email id, the database read and write rules would prevent them from getting or modifying any data.

### Read student list from excel
-The college has data of all students of a class for a particular year stored in an excel file.
-This file can directly be parsed by Quibble to get the required student info and store it in the database so that teachers won’t have to repeatedly add it.

### Read previous marks from excel
-Before Quibble, the college manually did all the work and stored all data in an excel file.
-Quibble can read these old excel files and automatically store all required data in the database.

### Automatic computations and color Coding
-Following important calculations are automated by Quibble: + Top 5 scorers + Total marks obtained and attempted per CO for each student + Total marks scored by each student + Attainment value for each CO for every student + Total attainment for each CO Quibble also automatically color-codes: + Attainment of each CO for every student + Total attainment of each CO

### All data in database
-All required data is collected and stored using Firebase Realtime database.
-FRD stores all data in JSON format.
-Storing data allows us to provide open-and-resume functionality as well as to prevent unnecessary repetitions.
-The stored data will further be used for advanced data analytics and visualization.

# Hospital-Management-Web_Application
# Description :point_left:
It's a web application for managing hospitals rooms and determining the patient's priority for isolation. The app provides a centralised hub for managing the patients and planning their distribution across hospital’s rooms. 

It allows nurses to keep track of the patients and their diseases in real time and to have an overview over the patients and rooms, and better manage the rooms assignment across patients.

# Live demo :rocket:
* username: admin
* password: admin

# Prerequisites
- [x] Node.js 6.9.1 or later - install from https://nodejs.org/

# Installing - easy :electric_plug:
1.	Download the repository
```
2.	Open the Terminal (Linux & MacOS) or PowerShell (Windows) and change directory to the project folder.
3.	Type ‘npm install’ in the Terminal (PowerShell) and press Enter. All the dependencies would be installed.
4.	Go back to the Terminal (PowerShell) and be sure that you are pointing inside the project folder. To open the application, type ‘node app.js’ and press Enter.
5.	The application should be live on the local port 3000.  
6.	Type http://localhost:3000/ into a browser.
7.	To login use the username: admin  and the password: admin
8.	Now you should be inside the application


### Add patient page

You can add a new patient in the system with his personal details and his diseases. The application automatically computes the score of the patient based on the entered diseases


### Patient page

Double click on a patient name on the dashboard to get here.'

### System settings

The control center of the application. It allows users to manage the diseases & rooms of the Hospital and create new accounts



# App Modules and Code organisation
### Modules

Module|Core	|Patients|Diseases|Rooms 
------|-----|--------|--------|----
Functionality	|- login system | - add / delete patients | - add / delete diseases | 	- assign rooms to patients
.|- add users | - update patient's diagnosis | - assign disease to patients | - add / remove rooms
.|- view dashboard	| - view patient’s page | 
.|.| - retrieve patient's information	

### Code organisation :open_file_folder:

Folder | Content | Responsability
------|-----|--------
/public	| |	Contains the public files, such as CSS, fonts and scripts.
/routes	| |	Manage the HTTP requests. Is divided into smaller modules responsible for disjoint tasks.
.	|/app.js| 	Renders dashboard page
.	|/disease.js| 	Responsible for diseases
.	|/login.js|	Responsible for logging in
.	|/patients.js|	Responsible for patients
.	|/rooms.js|	Responsible for rooms
.	|/settings.js|	Renders settings page
.	|/users.js|	Add new users and logout
/server	| |	Defines the database and Schemas
.	|/db/mongoose.js| 	Database settings
.	|/models| 	Defines Schemas
/views		| |Render pages
.	|/layouts|	The core layout; each page is rendered inside the layout
.	|/(other files)|	Contains specific visual changes for every page



**The available application is connected to a MongoDB database online.** If you want to change the database to another one, you need to go: NHS app folder -> server -> db -> mongoose.js



# REST Apis
The backend and frontend communicate through REST Apis. On the frontend, we make Ajax requests using jQuery to the following routes: 

URI |	Returns
----|----
/app/getdiseases |	returns information about all diseases in the system
/app/getpatients |       	returns information about all patients in the system
/app/getpatient/:hospitalNumber |	returns information about a specific patient
/app/getrooms	| returns information about the rooms in the system

# Known bugs :bug:
1. On some mobiles devices (iPhone, iPad) assigning rooms to patients is not working because mobile browsers doesn’t interpret the double-click. Also, the user can’t enter the patient's page because of the same reason. However, on LG mobile devices this feature works. 







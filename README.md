**HHA504 / Cloud Computing / Assignment 7 / Patient Self Service Portal - Admin View**


**This repo aims to:**
- practice CRUD (CREATE, READ, UPDATE, DELETE): 4 essential operations for creating and managing persistent data elements, mainly in relational databases

# TASKS:
1. Create a new github repo called PssP in your github  

2. Copy the code (files, folders, subfolders) from Part6_CRUD in our HHA-504-2022 repo (https://github.com/hantswilliams/HHA-504-2022/tree/main/Part6_CRUD) 

3. Re-create your own cloud-managed mysql database (either in GCP or Azure) or re-use one if you already have one running, and execute the scripts located in Part5_DBs to create some testing data (https://github.com/hantswilliams/HHA-504-2022/tree/main/Part5_DBs)   

4. Then create your .ENV file with the proper credentials/keys so the flask PssP app nows how to connect to the database 

5. Then update the PssP code in the following ways: 
Include in at least 3 additional patient demographic fields that are displayed in the /patients and patient details views (note, you may need to update your SQL schema depending on what you decide to use or not use)  
Update the EDIT functionality to include the ability to also edit the 3 new fields in the edit modal window dialogue 
Update the NEW PATIENT functionality to include the ability to also include the 3 new fields in the new patient modal window dialogue 
OPTIONAL: attempt to replicate the 'EDIT' functionality within the medications detail view; I have provided the code currently within conditions, try and create a similar process 
6. Include a new folder in the repo called IMAGES - this folder should contain the following screen shots: 
Screen shot of the app running on your browser on the /patients list page, showing dummy patients with the newly added demographics
Screen shot of the app running on your browser on one of the patient details pages - showing some dummy patient details with the newly added demographics  
Screen shot of the updated modal window for EDITING a patient from the /patients list view 
Screen shot of the updated modal window for the NEW PATIENT action from the /patients list view
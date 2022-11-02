**HHA504 / Cloud Computing / Assignment 7 / Patient Self Service Portal - Admin View**


**This repo aims to:**
- practice CRUD (CREATE, READ, UPDATE, DELETE): 4 essential operations for creating and managing persistent data elements, mainly in relational databases
- continue using a MySQL instance I previously created in: **mysql-cloudmanaged** to create and style a patient self-service portal


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


# app.py
- app.secret_key = random number/ dummy variable for when flask starts a new instance, the secret key ensures there's a unique idenitfier associated with it
- class Patients(db.Model): db.Model allows me to tell Flask what's the PRIMARY KEY and string field, and map out what was previously created in the patient_portal DB created in mysql-cloudmanaged assignment 
- Under ## Models##: No longer doing db design, list table name, and its existing columns 
- Edit table names and column to exactly match the table schema created in mysql-cloudmanaged 
- render_template('file.html) = references specific .html file for the page


# Procedures to test run on local machine:
1. Copy files from Part6_CRUD
2. Copy mysql credentials into .env file (store in root directory):
        MYSQL_USERNAME = "user"
        MYSQL_PASSWORD = "pass"
        MYSQL_HOST = "host"
3. In terminal:
-       pip install flask-mysqlalchemy
        pip install mysqlclient
4. In terminal: Run Flask app using app.py script
-       python Part6_CRUD/app.py
5. Click "Running on: hostname" to view page
6. Make sure table names and column names match exactly to schema
7. Revise app.py to your previously created DB schema
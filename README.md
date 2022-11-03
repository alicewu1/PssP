**HHA504 / Cloud Computing / Assignment 7 / Patient Self Service Portal - Admin View**


**This repo aims to:**
- practice CRUD (CREATE, READ, UPDATE, DELETE): 4 essential operations for creating and managing persistent data elements, mainly in relational databases
- Re-create a new MYSQL DB by following my **mysql-cloudmanaged** setup in Azure instead of GCP due to diminshed GCP credits
- Create and style a patient self-service portal using the dummy data from **mysql-cloudmanaged** repo


# TASKS:
1. Re-create my own cloud-managed MySql database in Azure (as seen in mysql-cloudmanaged)
2. Reference code from Part6_CRUD in our HHA-504-2022 repo (https://github.com/hantswilliams/HHA-504-2022/tree/main/Part6_CRUD) 
3. Create .ENV file in the root directory with new AZURE credentials/keys so the flask PssP app nows how to connect to the database 
4. Update app.py to:
- Include 3 new patient demographic fields to display in /patients and patient details page: dob, contact_mobile, contact_home
- Update EDIT patient function to allow ability to edit 3 new demographic fields in the new edit modal window dialogue
- Update the NEW patient function to allow ability to edit 3 new demographic fields in the new patient modal window dialogue
 
5. OPTIONAL [COMPLETED]: Create an 'EDIT' functionality within the patients_details.html page - medications view
- Edited patients_details.html to create the buttons and modal window
- Edited app.py to create a endpoint for medications modal window 

6. Create an IMAGES folder containing screenshots of:
        - the app running on your browser on the /patients list page, showing dummy patients with the newly added demographics
        - the app running on your browser on one of the patient details pages - showing some dummy patient details with the newly added demographics  
        - the updated modal window for EDITING a patient from the /patients list view 
        - the updated modal window for the NEW PATIENT action from the /patients list view


# setup_azure.md
- contains instructions for how I setup a MySQL database in Azure


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
-       python CRUD/app.py
5. Click "Running on: hostname" to view page
6. Make sure table names and column names match exactly to schema
7. Revise app.py to your previously created DB schema


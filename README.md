**HHA504 / Cloud Computing / Assignment 7 / Patient Self Service Portal - Admin View**


**This repo aims to:**
- Practice CRUD *(CREATE, READ, UPDATE, DELETE)*: 4 essential operations for creating and managing persistent data elements, mainly in relational databases
- Create a new MYSQL DB, table schemas, and dummy data by following my [mysql-cloudmanaged](https://github.com/alicewu1/mysql-cloudmanaged) repo setup in Azure due to diminshed GCP credits
- Create and style a patient self-service portal

<br>

## 1. Re-create a cloud-managed MySQL db in Azure
- Using my repo: [mysql-cloudmanaged](https://github.com/alicewu1/mysql-cloudmanaged)

## 2. Set Up the MySQL DB
- **setup_azure.md:** contains instructions for how I setup and configured the Azure MySQL db
- Create .ENV file in the root directory with new AZURE credentials/keys so the flask PssP app nows how to connect to the database 

## 3. Deploying Flask
- In terminal:
-       pip install flask-mysqlalchemy
        pip install mysqlclient
        
        python app.py


## 4. Edit app.py to customize and stylize a patient self-service portal according to the schema you previously created and:
- Include 3 new patient demographic fields to display in /patients and patient details page: dob, contact_mobile, contact_home
- Update EDIT patient function to allow ability to edit 3 new demographic fields in the new edit modal window dialogue
- Update the NEW patient function to allow ability to edit 3 new demographic fields in the new patient modal window dialogue
     - ***Note**: Make sure table names and column names match exactly your previously created table schemas*

## 5. Create an 'EDIT' functionality within the patients details page in medications view (Optional - Completed)
- Edited **patients_details.html** to create the buttons and modal window
- Edited **app.py** to create an endpoint for medications modal window 

## 6. Create an IMAGES folder containing screenshots of:
-      - the app running on your browser on the /patients list page, showing dummy patients with the newly added demographics
       - the app running on your browser on one of the patient details pages - showing some dummy patient details with the newly added demographics  
       - the updated modal window for EDITING a patient from the /patients list view 
       - the updated modal window for the NEW PATIENT action from the /patients list view


# CRUD FILES:
- **static:** folder containing CSS scripts used to style pages
- **templates**: folder containing HTML scripts 
- **setup_azure:** instructions for how I setup a MySQL database in Azure
- **images**: folder containing screenshots of my patient portal
- **data:** folder containing the .csv file I used to pull LOINC codes for the social determinants table
- **sql_table_creation.py:** script I used to create table schemas
- **sql_dummy_data.py:** script I used to create realistic patient dummy data and insert into patients





# Setting Up: Azure Database for MySQL flexible servers

1. Server Name: mysql-pssp
Region: East US
MySQL Version: 5.7
Workload Type: For development or hobby projects 
Compute + storage: Burstable, B1ms (1 vCores, 2 GB RAM, 20 GB storage, 360 IOPS)
Geo-redundancy: Disabled

Admin username: user
password: pass

2. Network: 
Connectivity Method: Public access
Firewall Rules: Add current client IP address (173.68.135.133)

3. Deploying Server:
Sever_Parameters: Turn off Require_Secure_transport
To allow local IPs to connect to server


4. In terminal:
-       mysql -u alice -h [copy server name to clipboard] -p


DO NOT NEED TO DO THE FOLLOWING. USE OWN TERMINAL:
- install sudo apt-get update
- sudo apt install mysql-server mysql-client
- sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
- change 'bind-address' to 0.0.0.0
- pip install python-dotenv


5. Back to Networking:
- Add Firewall rule: 0.0.0.0 - 255.255.255.255


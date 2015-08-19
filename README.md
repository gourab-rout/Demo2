# SFTP FILE POLL USECASE

Purpose
=======

The sftp-file-poll project polls file from a read only folder.

Prerequisites
=============

1. CRUSHFTP SERVER
2. Anypoint Studio
3. mule-ee-distribution-standalone-3.7.1
4. apache-maven-3.3.3-bin

Project setup
==============

### Step 1: Set Up Crush SFTP SERVER

1. Install crush sftp server from <a href="http://www.crushftp.com/"> http://www.crushftp.com/
2. Extract the zip file and run CRUSHFTP.exe. The following dialogue box is opened
 
 ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/crushftpexe.PNG)

3. Click on "Create New Admin User". Provide the username and password to create the new admin user.
4. Click on "Start Temporary Server" to start sftp. SFTP server starts with the following message

![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/crushftpexe.PNG)

5.To configure sftp polling path as read only log on to server <a href="http://127.0.0.1:8080/"> http://127.0.0.1:8080/
  Create a new user by navigating "Admin"---> "User Manager" -----> "Add".
  
  ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/crushftpexe.PNG)
  ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/crushftpexe.PNG)
  
6.To configure the sftp path click on the newly created user. Drag file from Server to user and give it read only access.
  ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/crushftpexe.PNG)

7. Now log on to the sftp server with credentials of newly created user to check if the path has correctly configured.
8. 
### Step 2: Import Mule project

### Step 3: Running project in standalone server

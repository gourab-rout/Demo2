#Sftp File Polling

Purpose
=======

Read files from read only Sftp folder.

Components Used To Develop Project
==================================

1. CrushFTP
2. Anypoint Studio
3. mule-ee-distribution-standalone-3.7.1
4. apache-maven-3.3.3-bin

Project setup
==============

### Step 1: Set Up Crush SFTP Server

1. Download crush sftp server from <a href="http://www.crushftp.com/download.html"> http://www.crushftp.com/download.html.
2. Download the zip as per the operating system.
   Extract the zip file and run CRUSHFTP.exe. The following dialogue box is opened
 
    ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/crushftpexe.PNG)

3. Click on "Create New Admin User". Provide the username and password to create the new admin user.
4. Click on "Start Temporary Server" to start sftp. SFTP server starts with the following message

   ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/serverstarted1.PNG)

5.To configure sftp polling path as read only, log on to server <a href="http://127.0.0.1:8080/"> http://127.0.0.1:8080/.
  After log in below page is displayed.

![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/admin.PNG)
  
  Create a new user by navigating "Admin"---> "User Manager" -----> "Add".
  
  ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/usermanager1.png)
  
6.To configure the sftp path click on the newly created user. Drag file from Server to user and give it read only access.
  ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/sftp%20path%20conf1.PNG)

7. Now log on to the sftp server with credentials of newly created user to check if the path has correctly configured.
 
### Step 2: Import Mule project

1. To import first extract the project "sftp-file-poll.zip". Then import as "Maven based Mule Project from pom.xml"

    ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/sftp%20path%20conf1.PNG)
    
2. The studio run time is to be Mule Server 3.6.0 EE and studio should have been updated with munit plugins.

### Step 3: Code Functinality details

1. By default sftp connector does not handle duplicate file polling. 
2. To handle this scenario a custom java code is wriiten, which changes the connector functionality to avoid duplicate file processing. These java file area available under src/main/java/ and in package org.mule.trasport.sftp.
3. This java file is injected as the message receiver class for the sftp connector as shown below.

    ![ScreenShot](https://raw.githubusercontent.com/indiramallick1988/Demo2/master/tool/sftp%20path%20conf1.PNG)
    
4. 



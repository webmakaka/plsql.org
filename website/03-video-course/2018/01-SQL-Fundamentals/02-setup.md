---
layout: page
title:  Oracle MOOC: SQL Fundamentals (2018)
permalink: /video-courses/2018/sql-fundamentals/setup/
---

<br/>

# Oracle MOOC: SQL Fundamentals (2018) : Setup


The following is a setup checklist for the SQL Fundamentals MOOC:

1. Complete prep
2. Install VM
3. Start VM
4. Connect as SYS
5. Run Setup Scripts
6. Connect as User
7. Validate Scripts

Click each sub-page in the left navigator and perform the steps outlined on those pages.

Alternatively, download the <a href="//files.plsql.ru/video-course/2018/01-SQL-Fundamentals/GettingStarted_SQL.pdf">Getting Started (PDF)</a>.

Congratulations! Now you are ready to practice the code examples or homework assignments provided in this course.


<br/>

## Preparation

1. Join the MOOC Community
2. Introduce yourself in the MOOC Community
3. Bookmark the MOOC Community because we'll add discussions, answer questions and provide clarifications throughout the delivery the course.
4. Note the dates when the lessons will be released in the Schedule section.
5. Begin your Setup.


<br/>

## Download and Install Pre-built Developer VM


**Requirements**

To be able to download and install the pre-built developer VM successfully, make sure your system meets the below requirements:

1. At least 2GB RAM. Default VM is 1G RAM, for better performance increase.
2. At least 15GB of free space (Note: virtualization works best with contiguous space so it is a good idea if on Windows to run a defrag program, and make sure you are using NTFS for your file system to handle large files on Windows.)
3. 2GHz Processor (a lesser processor will be acceptable but slower)
4. Mozilla Firefox 2.0 or higher, Internet Explorer 7 or higher, Safari 3.0 and higher or Google Chrome 1.0 or higher
5. Adobe Acrobat reader
6. Admin privileges on your virtual machine box

<br/>

**Setup**

1. Access  Oracle Technology Network Developer Day VM at http://www.oracle.com/technetwork/database/enterprise-edition/databaseappdev-vm-161299.html
2. Under the Setup section, select Accept License Agreement
3. Download and install Oracle VM VirtualBox on your host system (if not installed on your system already (Hint: Click the download link provided for your platform, under Oracle VM VirtualBox Base Packages)
4. Click Oracle DB Developer VM to download the file from this page.


<br/>

## Start Oracle Virtual Box Manager and Import the Appliance

1. Launch the Oracle Virtual Box Manager.
2. Select File > Import Appliance.
3. In the Appliance to Import page, select DeveloperDaysVM2017-06-13_01.ova appliance file, and click Next.
4. On the Appliance Settings page, make sure the location of the 2 virtual disks is on the drive with sufficient disk space, and click Import.
5. The Software License Agreement dialog displays. Click Agree.
6. After the import, the DeveloperDaysVM2017-06-13_01 virtual machine is ready to be powered on.
7. Double-click Oracle DB Developer VM to launch it.



<br/>

## Connect to the database as SYS

1. Start Oracle SQL Developer inside the VM.
2. Create a New Oracle SQL Developer Database Connection.
3. In the Connections navigator, right-click Connections and select New Connection from the context menu.
4. The New / Select Database Connection dialog box appears. Enter the following details for the new connection:

    Connection Name	setup_mooc
    Username	SYS
    Password	oracle
    Role	SYSDBA
    Hostname	localhost
    Port	1521
    Service Name	orcl
    
Ensure that you select the Save Password check-box.

5. Click Test to test the new connection.
6. If the Status shows Success, click Connect to make the connection.
7. Once the connection is made, a SQL worksheet opens up automatically.




<br/>

## Run the Setup Scripts to Create the Required Schema


Once your database connection is made, follow these steps to install the schema and database objects for the course.

To install the required schema into the database:

1. Download the <a href="//files.plsql.ru/video-course/2018/01-SQL-Fundamentals/labs.zip">labs.zip</a>  file and expand it.  You will find the following folders:

* setup_files: This folder contains all the script files required to setup your HR schema tables required for the demos and homework.

* code_ex: This folder contains all the script files that we have used in our demos in the videos.

* lab_scripts: This folder contains scripts that you will need while doing your homework.

* cleanup_scripts: This folder also contains scripts that you will need while doing your homework.

2. Navigate to labs/setup_files folder.

3. Locate setup.sql file and run it from the SQL Developer Worksheet.



<br/>

## Connect as User

As a best practice, it is suggested that you don’t use the SYS connection to execute code examples or homework.

Alternatively, you can use any one of the below user accounts to create a new connection for practicing homework:

    USERNAME	PASSWORD
    ora1	ora1
    ora21	ora21
    ora22	ora22
    ora23	ora23
 
If you are interested to try the code examples demonstrated in the videos, use the teach_a account:

    Username: teach_a
    Password: teach_a

Congratulations! You have successfully completed the setup required to practice the code examples or homework assignments created for this MOOC.


<br/>

## Validate Setup

After connecting as a user (ora1/ora21/ora22/ora23), validate the setup as follows:

Verify the HR schema by executing the following queries in the SQL worksheet:

    SELECT count(*) FROM employees;
    
Expected result: 20 rows

    SELECT count(*) FROM tab;
    
Expected result: 9 rows

    SELECT count(*) FROM departments;

Expected result: 8 rows



<br/>

## Demo Scripts

* The scripts used in the videos are available in the labs/code_ex folder.
* The naming convention of the script files are as follows:

    code_<Lesson number>_<Part number>.sql

* For example, if you want to access the code examples in Lesson 2 - Part 3 video, open the file named code_02_03.sql.

---
layout: page
title:  Oracle MOOC SQL Fundamentals (2018)
permalink: /video-courses/2018/plsql-fundamentals/setup/
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

Alternatively, download the <a href="//files.plsql.ru/video-course/2018/02-PLSQL-Fundamentals/GettingStarted_PLSQL.pdf">Getting Started (PDF)</a>.

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
4. Click Oracle DB Developer VM to download the file from this <a href="http://www.oracle.com/technetwork/database/enterprise-edition/databaseappdev-vm-161299.html">page</a>.


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


All the code examples used for demonstrating PL/SQL concepts in the videos use HR (Human Resources) schema. All the homework assignments are based on the AD (Academic) schema.

To install the required schemas into the database:

1. Download the <a href="//files.plsql.ru/video-course/2018/02-PLSQL-Fundamentals/setup_files.zip">setup_files.zip</a> file into your VM, and extract the zip folder
2. Locate setup.sql from the extracted zip files, run it from the SQL Developer worksheet



<br/>

## Connect as User

As a best practice, it is suggested that you don’t use the SYS connection to execute code examples or homework.

Alternatively, you can use any one of the below user accounts to create a new connection for practicing homework:

    USERNAME	PASSWORD
    ora1	ora1
    ora2	ora2
    ora3	ora3
    ora4	ora4
 
Congratulations! You have successfully completed the setup required to practice the code examples or homework assignments created for this MOOC.


<br/>

## Validate Setup


After connecting as a user (ora1 / ora2 / ora3 / ora4), validate the setup as:

1. Verify the HR schema by executing the following queries in the SQL worksheet:

    SELECT count(*) FROM employees;

Expected result: 107 rows

    SELECT count(*) FROM tab;

Expected result: 22 rows

    SELECT count(*) FROM departments;

Expected result: 27 rows

NOTE: All the videos use HR schema to demonstrate the code examples.

2. Verify the AD schema by executing the following queries in the SQL worksheet:

    SELECT count(*) FROM ad_course_details;

Expected result: 15 rows

    SELECT count(*) FROM ad_departments;

Expected result: 4 rows

NOTE: All the homework assignments are based on the Academic (AD) schema.

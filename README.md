# Relational-Database-Administration

## Introduction
In this project, I will assume as a role of data adminstrator to perform data admintrastion tasks across three different databases (PostgreSQL, MySQL server, IBM DBS server) at a data analytics consulting company.  
Tasks to perform across three databases: 
-  start by installing and configuring a database, managing users and performing a backup
-  move on to recovery, indexing, optimization and automation of routine tasks
-  restore a database, create an index, create a view and connect to a database from the command line.  
This project is sectioned into three parts: (i) PostgreSQL server, (ii) MySQL server (iii) clouded based database. 

#### Environment:
To complelete  this lab, we will be using the Cloud IDE based on Theia and PostgreSQL database running in Docker container which provided by IBM skill network.   
#### Technologies and Tools: 
- shell commands  

## 1. PostgreSQL Server  
### 1.1 Installation/Provisioning & Configuration 
- Setting up the lab environment
- download the lab setup bash file from 
```wget ```  
<img src="https://imgur.com/8E1OQai.png">
- run bash file  
```bash```  
<img src="https://imgur.com/H9RflPI.png">

### 1.2: User Management  
     1.2.1: Create a User 
```create user```  
<img src="https://imgur.com/sGmPMsJ.png">  
#### 1.2.2: Create a Role 
``` create role ```  
<img src="https://imgur.com/bFmu79Q.png">  
#### 1.2.3: Grant Privileges to Role   
``` GRANT CONNECT ON DATABASE _DB_NAME TO assigned_user ```  
<img src="https://imgur.com/SewA0IN.png">  
#### 1.2.4: Grant privilieges to the "BackUp" Role
``` GRANT CONNECT ON DATABASE _DB_NAME TO assigned_user ```  
<img src="https://imgur.com/y47g3uB.png">  

### 1.3: Backup a database on PostgreSQL Server 
using phpadmin UI   
<img src="https://imgur.com/gfW4NvR.png" width="650" height="400">


## 2. MySQL Server
<sub> bfdkfhskdhjkfhksjhfjkshdjfkhsjfhjhhdfjkshjfsdfs </sub>  
### 2.1: Installation/Provisioning & Configuration    

### 2.2: Recovery MySQL server using a previous backup   
#### 2.2.1: Restore the provided backup file onto MySQL server 
use ``` source <backup.file>``` command to restore the database  
##### 2.2.2: Find the table data size
use ``` select count(*) from table_name;``` to find the actual data size 

### 2.3 Indexing  
#### 2.3.1: Baseline query performance 
<sub> looking at how long the query ``` select * from table_name where condition``` takes to retrieve the data from unindexed table </sub>  
#### 2.3.2: Create an Index 
use ``` create index column_new_name on table_name(columns_that_needed_to_index)```  
#### 2.3.3 Document the improvement in query performance  
re-run the query again to compare the performance before indexing and after indexing

### 2.4: Storage Engines  
#### 2.4.1: Find the supported storage engines  
use ``` show engines```  
#### 2.4.2: Find the storage engine of a table  
use ``` select table_name, engine from information_schema.tables where table_name = "table_you_need_to_find"```

### 2.5: Automation of Routine Tasks 

## 3. IBM Db2 instance   
### 3.: Restore the table billing   
3.1.1 Restore the table billing
3.1.2 Create a view 
3.1.3 Baseline query performance 
3.1.4 Create an index 
3.1.5 Document the improvement in query performance  
### 3.2: Create a View  
### 3.3: Indexing  
### 3.4: Connecting to IBM DB2 from Command Line  



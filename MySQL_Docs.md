# MySQL_Docs

#### What is MySQL?

MySQL is currently the most popular database management system software used for managing the relational database. It is open-source database software, which is supported by Oracle Company. It is fast, scalable, and easy to use database management system in comparison with Microsoft SQL Server and Oracle Database.MySQL follows the working of a client/server architecture.MySQL supports many Operating Systems like Windows, Linux.

**MySQL INSTALLATION**
  
```bash
sudo apt update
sudo apt install mysql-server -y
```
**secure installtion**

```bash
sudo mysql_secure_installtion
.....
```

**MySQL login**

```bash
sudo mysql -u root -p
```
   
**How to exit the database**

```bash
exit (or) \q
```
    


#### Create a MySQL New User:-

![image](https://user-images.githubusercontent.com/91359308/164618635-021aae64-c33b-4996-bdc0-df0b4e04e03d.png)

#### To grant all privileges to MySQL User on all databases:-

![image](https://user-images.githubusercontent.com/91359308/164618698-e43771d2-1ed5-4471-9a3e-327452a9aecf.png)

#### To grant insert privileges to a MySQL user:-

![image](https://user-images.githubusercontent.com/91359308/164619089-96d53733-976d-4be5-9b3b-143ab81622a0.png)

#### To show all the privileges in a specified user:-

![image](https://user-images.githubusercontent.com/91359308/164619150-fa0ccbad-0241-4c82-b1fd-357a572f5f6a.png)

#### List out the details of users:-

![image](https://user-images.githubusercontent.com/91359308/164619600-2d0a46a7-303a-4764-9a51-2ec690af9005.png)



#### Create a Database:- 

![image](https://user-images.githubusercontent.com/98270930/164432767-f103370c-7ba6-42c6-9d05-5f881fb1b58e.png)

#### Show the Created Database:- 

 ![image](https://user-images.githubusercontent.com/98270930/164433044-e189e893-5549-4b81-8f05-42d63a4506a6.png)

#### Enter into the specified Database:- 

 ![image](https://user-images.githubusercontent.com/98270930/164433288-a061e2e5-26aa-4b93-90fe-cdb70cd822ec.png)
 
 #### Delete the Database:-
 
 ![image](https://user-images.githubusercontent.com/98270930/164434562-50e2d6f2-6e5f-4de9-9bb2-522124a8d163.png)


#### Database Table Creation Syntax
```bash
    CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
```
#### MySQL ALTER TABLE Statement

##### 1) ALTER TABLE - ADD Column:-
 ```bash

  ALTER TABLE table_name
    ADD column_name datatype; 
```
##### 2) ALTER TABLE - DROP COLUMN:-
 ```bash

  ALTER TABLE table_name
    DROP COLUMN column_name;  
```
##### 3) ALTER TABLE - MODIFY COLUMN:-
 ```bash

  ALTER TABLE table_name
    MODIFY COLUMN column_name datatype;   
```
#### MySQL Copy/Clone/Duplicate Table:-
 ```bash
    CREATE TABLE new_table_name  
      SELECT column1, column2, column3   
        FROM existing_table_name;    
```

####  MySQL INSERT INTO Statement:-
 ```bash
    INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...); 
                                            [or]
    INSERT INTO table_name VALUES (value1, value2,...valueN),( value1, value2,...valueN ),...........,( value1, value2,...valueN );                                      
```

####  MySQL UPDATE Statement:-
 ```bash
    UPDATE table_name  
        SET column1 = value1, column2 = value2, ...
            WHERE condition;                                               
```

#### MySQL ORDER BY:
```bash
    SELECT column1, column2, ...
        FROM table_name
            ORDER BY column1, column2, ... ASC|DESC; 
```

#### LIMIT - The LIMIT clause is used to specify the number of records to return.
```bash
    SELECT column_name(s)
        FROM table_name
            WHERE condition
                LIMIT number; 
```
#### Basic Syntax of MySQL 

|S.NO|SYNTAX|DESCRIPTION|
|---|----|-----|
|1.|CREATE DATABASE [db-name];  |To create a new database.|
|2.|SHOW DATABASES;|List out the databases.|
|3.|USE [db-name];|Enter into the specified database.|
|4.|DROP DATABASE [db_name];|To delete the specified database.|
|5.|CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';| Create a new user|
|6.|GRANT permission_type ON database.table TO 'username'@'localhost';| To grant privileges to a user account |
|7.|GRANT INSERT ON * . * TO 'username'@'localhost';|To grant insert privileges to a MySQL user|
|8.|SHOW GRANTS FOR username;|To display all the current privileges held by a user|
|9.|GRANT ALL PRIVILEGES ON * . * TO 'database_user'@'localhost';|To grant all privileges to MySQL User on all databases|
|10.|GRANT ALL PRIVILEGES ON database_name.* TO 'database_user'@'localhost';|To grant all privileges to a user account on a specific database|
|11.|GRANT ALL PRIVILEGES ON database_name.table_name TO 'database_user'@'localhost';|To grant all privileges to a user account over a specific table from a database |
|12.|REVOKE permission_type ON database.table TO 'username'@'localhost';|Revoke Privileges MySQL User Account|
|13.|DROP USER 'username'@'localhost';|Remove an Entire User Account|
|14.|TRUNCATE TABLE table_name;|It is used to delete the data inside a table.|
|15.|SHOW TABLES; | List out all the tables in specified database.|
|16.|RENAME old_table TO new_table;| To rename the name of the table|
|17.|DESC table_name|Describe the specified table details.|
|18.|DROP TABLE  table_name;|It is used to delete complete the data in the table.|
|19.|DELETE FROM table_name WHERE condition; |To delete the row of the table using where condition.|
|20.|SELECT column1, column2, ...FROM table_name; |To view the specified colums details in specified table.|
|21.|SELECT * FROM table_name; |To view a details of the entire specified table.|

### Reference:-

For more details visit this page - https://www.javatpoint.com/mysql-tutorial

# How to set root password for MySQL root user in Ubuntu 20.04 LTS:

1. We have check the mysql version and the status of mysql

 ```bash
 mysql --version
 sudo systemctl status mysql.service
 ```
 ![image](https://user-images.githubusercontent.com/91359308/166138918-cacf2890-a7e8-4a1c-ad89-227c7a48518b.png)

 
 2. Enter into mysql with out password:

 ```bash
 sudo mysql
 ```
 ![image](https://user-images.githubusercontent.com/91359308/166138993-54153ae9-4d2b-462b-b149-794d61669c89.png)

3. we have to change mysql database

![image](https://user-images.githubusercontent.com/91359308/166139023-9d79602a-2f7e-4e15-b856-ea9a603ade3a.png)

4.  Set the root password:

![image](https://user-images.githubusercontent.com/91359308/166139074-bcb64de1-9a0c-44c3-ae4c-9eb959b404b9.png)

5. Login to mysql using new currently reset password:

![image](https://user-images.githubusercontent.com/91359308/166139117-42c7ebba-d76f-4834-a715-0a45f3fe9eb2.png)



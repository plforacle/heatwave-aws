# Access your MySQL DB System

## Introduction

In this lab, you will create and configure ????

_Estimated Lab Time:_ 20 minutes

### Objectives

In this lab, you will be guided through the following tasks:

- Connect MySQL Shell to MySQL
- Load Sample TPCH Data to MySQL DB System

### Prerequisites

- An Oracle Trial or Paid Cloud Account
- Some Experience with MySQL Shell
- Must Complete Lab 1

## Task 1: Connect MySQL Shell to MySQL

1. You can access the MySQL DB system using the host name and the admin user
credential from any client machine. MySQL Shell 8.0 is required. On a command
prompt, connect to MySQL

    ```bash
    <copy>mysqlsh <username>@<MySQL Host Name> --mysql</copy>
    ```

    **For example:**

    mysqlsh admin@xxxx.dbsystem.us-east-1.aws.mysqlheatwave.com – mysql

    **NOTE:** Currently only classic MySQL protocol is supported. To connect from
    MySQL Shell via classic protocol, use the option --mysql. For more details:
    [MySQL Shell guide] (<https://dev.mysql.com/doc/mysql-shell/8.0/en/mysqlsh.html>)

2. You are now connected to MySQL and are ready to import data to MySQL

    ![CONNECT](./images/06connect-myslqsh.png "connect-myslqsh ")

## Task 2: Load Sample TPCH Data to MySQL DB System

Load performance depends on the network latency and compute resource of the compute instane where mysql shell is installed.

1. Download DDL script to create the TPCH database and tables

    ```bash
    <copy>curl -X GET https://objectstorage.us-phoenix-1.oraclecloud.com/n/mysqlpm/b/tpch/o/tpch_ext_ddl.sql > tpch_ext_ddl.sql</copy>
    ```

2. Download TPCH sample data file (1GB of data)

     ```bash
    <copy>curl -X GET https://objectstorage.us-phoenix-1.oraclecloud.com/n/mysqlpm/b/tpch/o/tpch_sf_1.zip > tpch_sf_1.zip</copy>
    ```

3. unzip the file

    ```bash
    <copy>unzip tpch_sf_1.zip</copy>
    ```

4. Create the database and tables

    ```bash
    <copy>mysqlsh -h<mysql host name> -uadmin -p<mysql admin password> --mysql --file tpch_ext_ddl.sql</copy>
    ```

5. Import the sample data

You may now proceed to the next lab.

## Acknowledgements

- **Author** - Perside Foster, MySQL Solution Engineering

- **Contributors** - Mandy Pang, Principal Product Manager,
Nick Mader, MySQL Global Channel Enablement & Strategy Manager
- **Last Updated By/Date** - Perside Foster, MySQL Solution Engineering, September 2022

# Connect to and your MySQL DB System

## Introduction

In this lab, you will connect to your HeatWave Database using MySQL Shell. Then you will load Sample TPCH Data to the  HeatWave databse system.

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

    mysqlsh admin@xxxx.dbsystem.us-east-1.aws.mysqlheatwave.com --mysql

    **NOTE:** Currently only classic MySQL protocol is supported. To connect from
    MySQL Shell via classic protocol, use the option --mysql. For more details:
    [MySQL Shell guide] (<https://dev.mysql.com/doc/mysql-shell/8.0/en/mysqlsh.html>)

2. You are now connected to MySQL and are ready to import data to MySQL.

    To exit enter

    ```bash
    <copy>\q</copy>
    ```

    ![CONNECT](./images/mysqlshellloginexit.png "mysql shell login exit")

## Task 2: Load Sample TPCH Data to MySQL DB System

1. Connect to the MySQL DB system

    ```bash
    <copy>mysqlsh <username>@<MySQL Host Name> --mysql</copy>
    ```

2. Load TPCH sample data file (10GB of data)

     ```bash
    <copy>util.loadDump("https://objectstorage.us-ashburn-1.oraclecloud.com/p/Y5YBAp2U5NPEwFsgXLdWpHU_J-ZredOrg9vggNrusKr102AJa9NMsvUg-u3WSVqE/n/idazzjlcjqzj/b/tpch_bucket/o/tpch_1024/@.manifest.json",{progressFile: "progress.json",threads: 16})</copy>
    ```

    ![CONNECT](./images/mysqlshellloginexit.png "mysql shell login exit")

3. View tpch database

a.

```bash
<copy>\sql</copy>
```

b.

```bash
<copy>SELECT table_name, table_rows FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'tpch';</copy>
```

## Acknowledgements

- **Author** - Perside Foster, MySQL Solution Engineering

- **Contributors** - Mandy Pang, Principal Product Manager,
Nick Mader, MySQL Global Channel Enablement & Strategy Manager
- **Last Updated By/Date** - Perside Foster, MySQL Solution Engineering, September 2022

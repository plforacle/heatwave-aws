# Create MySQL Database HeatWave  and Cluster

## Introduction

In this lab, you will create and configure ????

_Estimated Time:_ 20 minutes

### Objectives

In this lab, you will be guided through the following tasks:

- Create a Virtual Cloud Network
- Create MySQL HeatWave Database
- Add a HeatWave Cluster to MySQL Database System

### Prerequisites

- An Oracle Trial or Paid Cloud Account
- Some Experience with MySQL Shell

## Task 1: Create MySQL HeatWave Cluster

1. Log on to MySQL Database Service Console
    1.1. On your web browser, go to:

    ```bash
    <copy>https://mysqlheatwave.com</copy>
    ```

2. Enter the provided username and password to sign in to the page. NOTE: These are the Basic Authentication Credentials provided to you for the Beta program. Do not confuse these with your personal credentials. These credentials grant access to the site and this only applies for the beta testing.

    ![IMAGE?????](./images/ssh-ls.png "ssh-ls ")

3. Enter the provided Cloud Account Name. This is the MySQL HeatWave OCI Cloud
    Account Name that was provided to you.

    ![IMAGE?????](./images/ssh-ls.png "ssh-ls ")

4. Enter the provided OCI account credential. This is your email address and the password that was provided to you

    ![IMAGE?????](./images/ssh-ls.png "ssh-ls ")

5. Once you are logged on, you will see the MySQL Database Service console page:

    ![IMAGE?????](./images/ssh-ls.png "ssh-ls ")

## Task 2: Create MySQL Database for HeatWave

1. On the DB Systems Console, click “Create MySQL DB System” button
2. On the “Create MySQL DB System” panel
    2.1 Display Name: Enter a name for the DB System

    ![IMAGE?????](./images/ssh-ls.png "ssh-ls ")

    2.2 Description: Enter a description
    2.3 Administration credentials: Enter an administrative username and password for the MySQL database. These credentials allow access to the MySQL Database System. Make sure to save them, you will need them later to access the MySQL Database System via tools like MySQL Shell.

    ![IMAGE?????](./images/ssh-ls.png "ssh-ls ")

    2.4 Hardware: Specify the Database Storage Size
    2.5 Availability Zone: Auto Placement is on by default. If you want to specify an available zone to place the MySQL DB System, turn it off and select the AZ

    ![IMAGE?????](./images/ssh-ls.png "ssh-ls ")

    2.6 Endpoint:
    2.6.1 Allowed Client Addresses: Specify IP range(s) of your client IP addresses, which you will use to access the MySQL DB System instance in the steps later. Multiple CIDR ranges can be specified via a semi-colon separated list in the form of xxx.xxx.xxx.xxx/yy;xxx.xxx.xxx.xxx/yy;…
    Note that 0.0.0.0/0 is not supported at this time.
    2.6.2 Port: 3306
    2.6.3 X Plugin Port: 33060
    2.7 Press “Create” to create the DB System

3. Once the instance is created, click to see the detailed information such as Host Name. You will use the Host Name to connect to the instance.
    ![IMAGE?????](./images/ssh-ls.png "ssh-ls ")
## Acknowledgements

- **Author** - Perside Foster, MySQL Solution Engineering
- **Contributors** - Mandy Pang, MySQL Principal Product Manager,  Priscila Galvao, MySQL Solution Engineering, Nick Mader, MySQL Global Channel Enablement & Strategy Manager, Frédéric Descamps, MySQL Community Manager
- **Last Updated By/Date** - Perside Foster, MySQL Solution Engineering, July 2022

# Day17: Install and configure postgresql on database server

## Today's task:

States that there is a new application to be deployed in `Nautilus` infra in `Stratos DC` and this application uses postgresql as db. so need to setup PostgreSQL db server as required.
![alt text](task.png)

## Steps:

### Step1: ssh login to the db server(`stdb01`) and verify postgresql and its status

![alt text](<Screenshoots/1. ssh login to db server and check psql.png>)

### Step2: Login as the db administrator (`postgres`) using `sudo -u postgres psql`

![alt text](<Screenshoots/2. login as db admin postgres.png>)

### Step3: Create the user with the password

![alt text](<Screenshoots/3. create user.png>)

### And verify user created (`\du`)

![alt text](<Screenshoots/4. verify user created.png>)

### Step4: Create the database

![alt text](<Screenshoots/5. create database.png>)

### And again verify database created (`\l`)

![alt text](<Screenshoots/6. verify db created.png>)

### Step5: Grant privilege of the database created for the user.

![alt text](<Screenshoots/7. Grant all privileges to the user.png>)

### And once again verify the necessary privilege by listing the databases along with their owner and privileges data. (`\l`)

![alt text](<Screenshoots/8. verify privilages.png>)

### Note: **_As the task specifies not to restart the PostgreSQL server service, we'll directly quit using \q_**

### And done!

![alt text](<Screenshoots/9. done.png>)

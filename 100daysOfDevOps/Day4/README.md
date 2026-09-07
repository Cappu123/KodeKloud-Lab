# Day 4: Script Execution Permissions

The day's task is to put the necessary exebutable permissions for a shell script file found in ```/tmp/xfusioncorp.sh```.
Task detail: ![alt text](Screenshoots/task.png)

## Steps

### Step1: Check the file permission using long list (```ls -l```)
![alt text](<Screenshoots/1. look for the file permisions.png>)

### Step2: Change the file permission using ```a+rx /tmp/xfusioncorp.sh```
***What it means***:
```a```== ***for all users***
```+rx``` == ***add permission to read and execute the file***

## Then verify the execusion using ```/tmp/xfusioncorp.sh```
![alt text](<Screenshoots/2. change all users execute and verify.png>)

## Done👌
![alt text](<Screenshoots/3. done.png>)
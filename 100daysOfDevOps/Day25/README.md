# Day 25: Git Merge Branches

The overall objective of the day's task is to create a git branch, add a file in it, add and commit the change, then merge it into the master and finally push all changes to the remote server.

## Step1: Let's `ssh`login to the server and navigate to the repo.

![alt text](<Screenshots/1. ssh login and navigate to the repo.png>)

## Step2: Create a new git branch and checkout to it.

`git checkout -b xfusion`
![alt text](<Screenshots/2. create the branch.png>)

### Then verify:

![alt text](<Screenshots/3. confirm.png>)

## Step3: Copy the required file into the current repo, then verify.

![alt text](<Screenshots/4. copy the file here.png>)

## Step4: Add and commit the change.

![alt text](<Screenshots/5. git add and commit from the branch.png>)

## Step5: Switch back to the master branch and merge the newly created branch

`sudo git merge xfusion`
![alt text](<Screenshots/6. switch to master and git merge.png>)

## Step6: Push all the latest changes from both branches(master and xfusion) into the remote origin.

`sudo git push master` and `sudo git push xfusion`
![alt text](<Screenshots/7. git push the branch latest.png>)
![alt text](<Screenshots/8. also push the latests of master into the remote repo.png>)

## Done😊![alt text](image.png)

![alt text](<Screenshots/9. done.png>)

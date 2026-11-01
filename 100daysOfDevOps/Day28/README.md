# Day 28: Git Cherry Pick

_This task teaches how to select a specific commit from one branch and apply it to another branch. Unlike `merge` or a `rebase`, which move the entire branches or blocks of history, `cherry-pick` acts as a surgical copy-and-paste tool for individual changesets._

## Task Description:

![alt text](Screenshots/task.png)

## Step-by-step Solution Procedure

### 1. First we need to `ssh login` to the storage server, then navigate to the target `git` repository.

![alt text](<Screenshots/1. ssh login to storage server and navigate to the repo.png>)

### 2. Then let's check the branches, and make sure to update the local `master` branch to the latest.

![alt text](<Screenshots/2. check branches, then make sure to update the local master branch to the latest.png>)

### 3. Now we need to checkout to our target branch and log the commit history to copy the 7-figure hash text of the targeted commit(with a commit message `update info.txt` as mentioned by the task description).

![alt text](<Screenshots/3. checkout to feature branch, log the commit history and copy the hash of the needed.png>)

### 4. Then we checkout back to the master branch to `cherry-pick` the specific commit from the `feature` branch to the `master`.

![alt text](<Screenshots/4. checkout back to the master branch and cherry-pick the targeted commit from the feature branch.png>)

### 4. Finally push changes then we're good.

![alt text](<Screenshots/5. finally push changes..png>)

Done!
🫡
![alt text](<Screenshots/6. Done.png>)

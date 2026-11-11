# Day 30: Git hard reset

Today's task focuses on `Git Hard Reset`

## Problem Statement:

The problem explains how to cleanup a Git repository by resetting its history and work tree to a specific commit message as mentioned in the task description(_add data.text file_) in our case. and push the updated state to the remote repository.
![alt text](Screenshots/task.png)

## Steps

_1. SSH login into the storage server and log the commit history._
![alt text](<Screenshots/1. login to storage server and git log the commit history.png>)
![alt text](<Screenshots/2. commit history list two.png>)

_2. We can also short list the commit history in one line._
![alt text](<Screenshots/3. can also git commit oneline.png>)

_3. Now we `git hard reset` to the specific commit mentioned above using the commit hash to make it the `HEAD`_
![alt text](<Screenshots/4. git reset --hard to the specific commit to be HEAD.png>)

_4. Forcefully push the changes into the remote server_
![alt text](<Screenshots/5. forcefully push the changes.png>)

we forcefully pushed changes because `---hard reset` rewrites the local commit history so it will fall back from the remote latest commits. But once we use ``--force` to push, the local and remote repositories both will be rewritten their commit history to the target HEAD.
so it tells the remote to ignore mismatches and make it to the local state.

_5. Completed!_
![alt text](<Screenshots/6. done!.png>)

# Day 29: Manage Git Pull Requests

## Task description

The day's task requires, pushing a featuring branch, creating a pull request in `Gitea`, and merging the pull request without deleting the source branch.
![alt text](Screenshots/task1.png)
![alt text](Screenshots/task2.png)
![alt text](Screenshots/task3.png)

## A Step-by-step procedure

_1. Login to the storage server as `max` and check the github repo, log the commit status_
![alt text](<Screenshots/1. step1.png>)
![alt text](<Screenshots/2. story already pushed to remote git repo.png>)
![alt text](<Screenshots/3. git log to see sarah's commit.png>)

\_2. Login to `Gitea` as `max` then create the `pull request`
![alt text](<Screenshots/4. dashboard.png>)
![alt text](<Screenshots/5. repo check2.png>)
![alt text](<Screenshots/6. pull request.png>)

### Make sure to put the correct _from_ and _into_ merge information and _tom_ as a reviewer as mentioned by the task description.

_3. Now, logout and signin using `tom`'s credentials to review the pull request._
![alt text](<Screenshots/7. login as tom for review.png>)

_4. Check pull requests and review._
![alt text](Screenshots/7.1.png)
![alt text](<Screenshots/8. check pull requests.png>)

_5. Now add a merge commit to merge the request._
![alt text](<Screenshots/9. create merge commit to merge.png>)
![alt text](<Screenshots/10. merged.png>)

_6. Finally we've successfully created a pull request and merged it on `Gitea`'s UI._
![alt text](<Screenshots/11. done.png>)

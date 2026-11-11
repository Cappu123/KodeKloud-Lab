# Day31 Git Stash

## The day's task focuses of `git stash` practices and version control operations.

## Task overview:

Problem requires to list, apply and manage uncommited and stashed local changes. Stashed changes are changes we're making progress of and then have WIP(_WORK IN PROGRESS_) label when we list them using `git stash list`. Then are not seen in the local directory when we `git status`
![alt text](Screenshots/task.png)

## Steps:

_1. First we ssh login to the storage server, navigate to the target git repository and list the stashed changes(the ones with `WIP`) using `git stash list`_
![alt text](<Screenshots/1. login to storage server and apply stash to the identified change.png>)

### As we can see from the `git status` output above, there were nothing to commit, meaning the stashed ongoing changes are not added to our local repository.

_2. Now let's apply the stashes using the identifier `stash@{1}` and once again see the `git status` outputs._

### Now the stashed change is applied to our local repository.

_3. Finally lets commit and push the change to the remote using `git commit` and `git push`._
![alt text](<Screenshots/2. commit and push un-stashed change..png>)

*4. End of today's task*😋
![alt text](<Screenshots/3 done.png>)

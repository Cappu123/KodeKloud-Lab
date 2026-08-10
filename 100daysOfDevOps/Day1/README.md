# Day 1: Linux User Setup with Non-Interactive Shell

This task requires to create a user with non interactive shell on one of the app servers.
![alt text](<screenshots/Day1 task.png>)

## What is a *non-interactive shell* ?
It is a command line environment that executes pre-written  scripts or automated commands without expecting human input, showing a prompt, or reading standard user configuration files like ```.bashrc.```

## It's Key Features
1. No prompt
2. No keyboard input (It reads commands from a file, pipe, or argument instead of a user)

## Common use cases
1. Running shell scripts (```./script.sh```)
2. Automated cron jobs. (cron jobs are automated tasks that run in the background in an os on a schedule.)
3. CI/CD pipeline executions.
4. Remote command execution via SSH (Eg ``` ssh host``` command)

## Steps done
1. After ssh logging to the server, Before writing command, need to know the distribution the os is using. through the command ```cat /etc/os-release```
![alt text](<screenshots/1 login to the app server and see the distribution system am using.png>)

2. Knowing the server uses `CentOS` OS and `CentOS Stream` distribution.
3. Used ```sudo useradd -r -s /sbin/nologin/kareem``` to create the user "kareem" with no password aging and expiration.
![alt text](<screenshots/2. create the system user Kareem which needs not to login or no password expiration.png>)

The flags ```-r```:  to create system user.
          ```-s /sbin/nologin```: Rejects interactive shell logins. The user can not login directly.

4. Verify user creation through ```getent passwd kareem```
![alt text](<screenshots/3. verify kareem systemuser created.png>)

The ```getent```(get entries looks app for the information) and ```passwd``` contains users.

search files can be ```ets/passwd```(users), ```etc/group```(groups) and ```etc/hosts```(network hosts)
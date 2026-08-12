# Day10 Linux Bash Scripts
This task requires to create a bash script on one of the app servers(```stapp01``` in this case) that should accomplish the f/g tasks
1. creates zip archive(named ```xfusioncorp_beta.zip```) of the directory(```/var/www/html/beta```)
2. save the created archive in the ```/archives/``` dirctory on itself.
3. copy the archived file to a backup server, Nautilus Storage Server(```ststr01```)
4. While copying the archive to the remote server, make sure it doesn't ask for password
5. DONOT use sudo inside the script

# Steps done
1. before writing the script on app server ```stapp01``` make sure zip package is installed using ```sudo dnf install zip unzip```(Found to be already installed)
![alt text](<Screenshoots/from stapp01 install zip unzip and create rsa key pair.png>)

2. Now generate rsa key in the app server ```stapp01``` and then copy it inside ```~/.ssh/authorized_keys``` of the backup storage server ```ststr01``` using the command ```ssh-copy-id natasha@ststr01```
![alt text](<Screenshoots/generate rsa key pair and copy it to storage backup server.png>)

3. Verify passwordless login to the remote storage server ```ststr01```
![alt text](<Screenshoots/confirmed passwordless login to the storage backup server.png>)

4. Now create the file and write the script
![alt text](<Screenshoots/create the shell script file.png>)

![alt text](Screenshoots/script.png)

5. Make the script executable using the command ```chmod +x beta_archive.sh``` so that the respective user can be able to run it. and then execute it using ```./beta_archive.sh```
![alt text](Screenshoots/verify.png)
6. Finally checked for successful implementation.
![alt text](Screenshoots/final.png)
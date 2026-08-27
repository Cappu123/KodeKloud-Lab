# Day 15: Setup SSL for Nginx

Today's task Day require to install and setup ```ssl``` certificate to ```nginx``` of one of the appservers in ```stratos datacenter```.

## Task overview
* Install and configure ```nginx``` on ```stapp01```
* Move the *self signed certificate* which is inside a temporary location to its appropriate place for secure access.

* Serve a simple html file securely.

* Validate ```https``` access from ```jumphost```
![alt text](Screenshoots/task.png)

## Step-by-step Execution
1. Login to ```stapp01``` and install ```nginx```.
![alt text](<Screenshoots/1. install nginx.png>)

2. Start, enable and verify nginx status.
![alt text](<Screenshoots/2. start enable and verify nginx.png>)

3. Move the certificate files to the appropriate secure folder.
![alt text](<Screenshoots/3. move cert file to appropriate directory.png>)

4. Put very restrictive file permissions for the secure files.
![alt text](<Screenshoots/4. proper files permission.png>)

5. Create a dedicated ```nginx``` configuration for ```SSL``` server.
![alt text](<Screenshoots/5. add config file nginx.png>)

6. Serve secured html file.
![alt text](<Screenshoots/7. write the html index file.png>)

7. Test ```nginx``` for correct configuration and reload it.
![alt text](<Screenshoots/6. test nginx configuration.png>)

8. Finally logour, ```curl``` from the remote host(```jump host```)
![alt text](<Screenshoots/7. test for nginx curl https from jumphost.png>)

9. Finally Successfully completed.👏🎉🥳🎊
![alt text](<Screenshoots/8. success.png>)
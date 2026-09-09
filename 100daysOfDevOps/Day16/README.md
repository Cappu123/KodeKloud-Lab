# Day 16: Install and Configure Nginx as an LBR

Today's task states that a degradation in website performance is observed. thus, application is being deployed on a high availability stack. Migration is taking place but only the ```LBR``` server is pending. then it basically requires to..

A. install nginx on lbr(if its not installed)  
B. configure the nginx as per mentioned in the task requirement  
C. Make sure apache is up and running in all app servers and also donot change it's port.  
D. Then finally should be able to access the load balancer from jumphost.
![alt text](Screenshoots/task.png)

### Steps to solve the task
## Step1: curl to the load balancer server  ```stlb01``` is not working.
```curl http:stlb01:80```
![alt text](<Screenshoots/1. curl to lbr not working.png>)

## Step2: Collect ```ip addresses``` info for all app servers
![alt text](<Screenshoots/1. collect ip addresses of all appservers.png>)

## Step3: Verify apache is running in all app servers and it's port(```8086``` in our case)
![alt text](<Screenshoots/1. check apache port and status on app servers1.png>)
![alt text](<Screenshoots/2. also for stapp02 and stap03.png>)

## Step4: Verify an already installed nginx, enable, start and verify it on the load balancer(```stlb01```)
![alt text](<Screenshoots/3. check, start, enable and verify nginx on load balancer.png>)

## Step5: Open the ```nginx``` configuration file ```/etc/nginx/nginx.conf``` and start editing it.

![alt text](<Screenshoots/4. open config file of ngindx.png>)
***Existing ```http``` block,***
![alt text](<Screenshoots/5. existing http block.png>)

***Add the load balancing upstream servers(Backend servers) using the default robin hood algorithm***
![alt text](<Screenshoots/5. add loadbalancig app servers on the upstream.png>)

***Existing ```server``` block,***
![alt text](<Screenshoots/6. existing config2.png>)

***Add proxy configuration to the upstream backend servers***
![alt text](<Screenshoots/7. add proxy to app servers line.png>)

## Step6: Now test the nginx configuration for success using ```sudo nginx -t ```
![alt text](<Screenshoots/8. test the config.png>)

## Step7: Finally back to the jumphost and verify http curl to the load balancer
```curl http://stlb01:80```
![alt text](<Screenshoots/9. finally curl successfull.png>)

## Task done successfully!🎊🎇🎇🎇🎇🎊
![alt text](<Screenshoots/10. done.png>)



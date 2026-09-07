# Day 16: Install and Configure Nginx as an LBR

Today's task states that a degradation in website performance is observed. thus, application is being deployed on a high availability stack. Migration is taking place but only the ```LBR``` server is pending. then it basically requires to..

A. install nginx on lbr(if its not installed)  
B. configure the nginx as per mentioned in the task requirement  
C. Make sure apache is up and running in all app servers and also donot change it's port.  
D. Then finally should be able to access the load balancer from umphost.
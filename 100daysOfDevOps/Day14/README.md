# Day 14: Linux Process Troubleshooting

## The task: 
Today's task mentions the unavailability of apache service on one of the app servers. It then requests to identify and resolve it.
![task](Screenshoots/task.png)

## Lets dive into troubleshooting
## 1. First lets identify on which app server the service is down. (Found out to be on ```stapp01```)
![alt text](<Screenshoots/1. apache not working on stapp01.png>)

## 2. Lets also check for ```stapp02``` and ```stapp03``` and make sure its running on port ```3000``` as given on the task- instruction.
![alt text](<Screenshoots/4. apache working find on stapp02.png>)
![alt text](<Screenshoots/5. also make sure apache is running on port 3000 on stapp02.png>)![alt text](<Screenshoots/6. apache running on stapp03 and on port 3000.png>)

## 3. Now We identify the issue, as another service is running on the port ```3000```
![alt text](<Screenshoots/2. find the cause of the problem1.png>)
![alt text](<Screenshoots/3. Find the cause of the problem 2.png>)

## 4. So now we need to check which service is running on port ```3000```
![alt text](<Screenshoots/7. check wat is running on port 3000 stapp01.png>)
![alt text](<Screenshoots/8. sendmail service is runningon port 3000.png>)

## 5. Found out to be ```sendmail``` service. Now we got 3 options. 
* *Kill the ```sendmail``` PID (Process Id) so that we can free the port*
* *Change the port ```sendmail``` is using to some another random unused port* 
    ## OR 
* *Let the ```apache``` run on another port*
### As the task mentions the apache should run on port ```3000```, Lets go with alternative 1(Kill the sendmail process).

## 6. Kill the PID of sendmail
![alt text](<Screenshoots/9. kill the pid of sendmail.png>)

## 7. Now start apache, and verify service running
![alt text](<Screenshoots/10. Now apache is started,running on port 3000 on stapp01.png>)

## Task successfully completed for today!
<img src="https://iam-weijie.github.io/wave/hand-emoji.svg" alt="Animated Waving Hand" width="30" height="30">

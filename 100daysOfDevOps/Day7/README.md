# Day7: Passwordless SSH authentication

This task requires to configure passwordless SSH from the jump host server of user "thor" to all application servers.
![alt text](<screenshots/day7 task.png>)

## What steps are done technically 
1. logged in to all app servers with their respective sudo users and generate rsa key after checking that its not already present.
![alt text](<screenshots/day7 check if rsa key already present.png>)
![alt text](<screenshots/day7 generate rsa key for each users on each app servers.png>)

2. once again generate rsa key on the jump host server using the thor user.
![alt text](<screenshots/day7 generate rsa key for thor in jumphost.png>)

3. the the final command ```ssh-copy-id tony@stapp01``` (being applied to all app servers stapp02 and stapp03 also), did the job of copying the thor user's public rsa key and put it under each app servers' ~./.ssh/authorized_keys file
![alt text](<screenshots/day7 copy thor's public key in each app servers.png>)

4. then verify the success by proving to login to each app servers with their sudo users from jump host thor user without being prompted to enter password.
![alt text](<screenshots/day7 finally successful password less authentication.png>)

## What happens during login afterwards 
1. thor user says: "I want to login as "tony"(for eg in app server 1)
2. stapp01 checks for /home/tony/.ssh/authorized_keys.
3. It finds thor's public key there.
4. It sends a cryptographic challenge.
5. thor proves it owns the matching private key.
6. Authentication succeeds without the need for password input. 

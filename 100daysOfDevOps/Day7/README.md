# Day7: Passwordless SSH authentication

This task requires to configure passwordless SSH from the jump host server of user "thor" to all application servers.

## What steps are done technically 
- logged in to all app servers with their respective sudo users and generate rsa key.
- once again generate rsa key on the jump host server using the thor user.
- the the final command ```ssh-copy-id tony@stapp01``` (being applied to all app servers stapp02 and stapp03 also), did the job of copying the thor user's public rsa key and put it under each app servers' ~./.ssh/authorized_keys file
- then verify the success by proving to login to each app servers with their sudo users from jump host thor user without being prompted to enter password.

## What happens during login afterwards 
1. thor user says: "I want to login as "tony"(for eg in app server 1)
2. stapp01 checks for /home/tony/.ssh/authorized_keys.
3. It finds thor's public key there.
4. It sends a cryptographic challenge.
5. thor proves it owns the matching private key.
6. Authentication succeeds without the need for password input. 

# Day8 Install Ansible

This task requires to install Ansible 4.7.0 using only pip3. Also we need to make sure that ansible binary is available globally. 

## What it means by *** globally?
1. All users on the system can run it(which means the application is installed system-wide rather than inside a restricted user directory)
2. It can be executed from any folder without typing its full file path(for example: typing ```ansible``` instead of ```/user/local/bin/ansible```

## What do we mean by global directories and local directories??
*** Local directories: ```~/.local/bin/``` or ```/home/user/.local/bin/```

*** Global directories: ```/usr/bin``` or ```/usr/local/bin```

### Steps done
- install ansible 4.7.0 using pip3: ```pip3 install ansible===4.7.0```
- verify installation location(for global): ```which ansible``` which showed the global directory as ```/usr/local/bin/ansible```

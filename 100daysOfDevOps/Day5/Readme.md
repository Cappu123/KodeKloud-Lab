# Day5: SElinux Installation and Configuration

This task requires the Installation and Configuration of SElinux, which is opted to enhance security of applications and servers. 

## Key reasons to use SELinux include: 
## Damage Containment:** If a web server is compromised, SELinux prevents the attacker from accessing user data or other system parts, even if they gain root privileges.

## Mandatory Access Control(MAC): Unlike traditional discretionary Access Control(DAC), where users can change file permissions, SELinux policies are defined by admins and cannot be overridden

## Preventing Privilege Escalation: SELinix secures against malware that attempts to gain higher privileges(eg. from user to root)

## Compliance: For organizations like finance, healthcare, MAC is required.

## Container Security: It isolates containerized applications to prevent escapes that could compromise the host system.

## Tasks given

1. Install the required SELinux packages.

2. Permanently disable SELinux for the time being,

3. No need to reboot the server

4. The status of SELinux after reboot should be disabled.

## Steps 
`ssh[username]@[servername]` [starts secure, encrypted connection with the server with given credintials from my remote computer.] ::

`cat /etc/os-release` [This command helps to identify the Linux distribution and version being used. because it indicates which package manager(apt, dnf) to use to install packages ] ::

`sestatus` [To see the status of SELinux] ::
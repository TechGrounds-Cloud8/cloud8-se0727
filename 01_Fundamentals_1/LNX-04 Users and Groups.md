# Users and groups
Linux is a multi-user system, which means that more than one person can interact with the system at the same time.
A system administrator or someone with those rights can manage the users and groups by creating and removing users and assign them to different groups .

## Key terminology

useradd Command: useradd [OPTIONS] USERNAME (general syntax)

Only root or users with sudo privileges can use the useradd command to create new user accounts.
When you use the command useradd it creates a new user account according to the options u give on the command line and the default values setu would the user to have and which u can set in the /etc/default/useradd file.

In Linux all groups are stored in mainly two groups:
The primary user’s group is stored in the /etc/passwd file and the supplementary groups, if any, are listed in the /etc/group file.
It says file, so it is not a directory but a file u need to read.

Listing All Groups: to list all groups on Ubuntu, run the command: cat /etc/group
That should output/give all the groups.

After adding the user u need to give it a password. (sudo passwd username)

In Linux Ubuntu, the sudo group controls the sudo users. So we need to add the new user to the sudo group with the following command:
usermod -aG sudo [username]
After that I have tested the access of the user: root access.
The commands u use are:
su - username
sudo whoami
root


## Exercise

* Create a new user in your VM. 
    The new user should be part of an admin group.
    The new user should have a password.
    The new user should be able to use ‘sudo’

* Locate the files that store users, passwords, and groups. See if you can find your newly created user’s data in there.



### Sources

https://linuxize.com/post/how-to-create-users-in-linux-using-the-useradd-command/
https://linuxize.com/post/how-to-create-groups-in-linux/ls
https://websiteforstudents.com/how-to-list-all-user-groups-on-ubuntu-18-04-16-04-with-examples/ls
https://linuxapt.com/blog/161-find-out-which-groups-a-user-belongs-to-in-ubuntu-20-04
https://phoenixnap.com/kb/linux-sudo-command
https://linuxize.com/post/how-to-create-a-sudo-user-on-ubuntu/




### Overcome challenges

I was sometimes confused whether group was a file, and whether it did contain the groups.

### Results
![alt text](..) 

test

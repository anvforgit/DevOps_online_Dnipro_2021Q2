
# Task 5.2

####  1) 
Each line of the /etc/passwd file contains seven comma-separated fields:
##### username:password:UID:GID:comment:home directory:default shell


For example, here is an entry for our user anv:
anv:x:1000:1000:anv,,,:/home/anv:/bin/bash
    username – anv
  password – stored in the /etc/shadow file
    UID – 1000
    GID – 1000
    comment – full name of the user is anv
    home directory – /home/anv
    default shell – /bin/bash
   
   
    Each entry in the /etc/group file contains four fields. A colon separates each field. The following is the format for an entry:
#### groupname:group-password:GID:username-list

etc/group Defines the default system group entries for system groups that support some system-wide tasks, such as printing, network administration, or electronic mail. 
Many of these groups have corresponding entries in the /etc/passwd file. Because most of the linux systems use a UPG scheme, a new entry is automatically created in /etc/group when a new user is added. 
The group name is the same as the username. 

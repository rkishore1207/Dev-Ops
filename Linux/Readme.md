# Linux
* Downloading `Oracle Virtual Box` and install `CentOS` and complete required configuration with the VMs.
## Command Syntax
* command [options] [arguments]
* **options** -> 
    1. Modify the way of command works
    2. consists of hypen followed by a single letter
    3. Accepts multiple options and sometimes group together after the hypen
* **Arguments** ->
    1. Arguments are optional
    2. Command assumes default argument if none is specified
## File Permissions
* Every file and directory in your account can be protected from other users by permissions.
* 3 Types of Permissions
    1. r-read
    2. w-write
    3. x-execute
* Each permission (rwx) can be controlled at three levels.
    1. u-users
    2. g-group
    3. o-everyone on the system
* File permission can be displayed by execute #ls -l

&emsp;&emsp; -rwxrwxrwx
* Command to change permission

&emsp;&emsp; chmod
* -> chmod u-r command => it will remove the read access for the command file
* -> chmod g+w command => it will add the write access for the command file
* -> chmod a-r command => it will remove all the read access to all the permissions that is (including users,groups and everyone).
* in description => prefix **d** represents directory and **-** represents file.

### File Permission based on Numbers
    1. 0 -> ---
    2. 1 -> --x
    3. 2 -> -w-
    4. 3 -> -wx
    5. 4 -> r--
    6. 5 -> r-x
    7. 6 -> rW-
    8. 7 -> rwx
## File Ownership
* There are 2 types of owners for a file or directory.
* **chown** change the ownership of file
* **chgrp** change the group ownership fo file
* **-R** change the recursive ownership of file
* `actual user` can not able to change the permission access, only `root user` able to change the directory or file permissions.
* Command for switching into root directory is `su -`.
## Help Command
* **Whatis** -> just give what it is about within two lines
* **--help** -> give complete description about that command
* **man** -> (manual) it is give same content which was given by --help but in a well structured and organized manner.
## Tab and Up Arrow
* Tab key helps to complete the commands
    1. chm'TAB'
    2. ls l'TAB' -> lists all files that start with **l**
* Up arrow helps to get back the previou commands
## Pipes
* Pipe (|) is used to connect the output of one command into the input of another command.
* `ls -l | more` this command restrict the list within one page and suggests more in the down then hit **space** it shows more lists and hit **q** it will come out.
* `ls -l | tail -1` this command returns the last item in the lists.
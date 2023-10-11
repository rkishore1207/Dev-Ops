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
## Adding Texts to Files
* There are three ways to do that.
    1. vi editor
    2. ls -ltr command (Remote command)
    3. Echo
* `echo > fileName` it will ovverride the content in the file.
* `echo >> fileName` it will append the current command to the previous commands.
* `cat fileName` is used to open any file in Linux.
* `date >> fileName` add the current date in the file
## File display command
    1.cat
    2.head
    3.tail
    4.more
    5.less
* Copy command -> `cp sourcePath destinationPath` it's a relative path 
* `less` is for restricting content in one page and hit **jorUpArrow** it will remove one line and **korDownArrow** it will show one line.
## File Management Command
* `mv` (move) it will move the file into the destination path
* If we didn't specify the destination path then it will **rename** the particular file. 
* `mkdir` it will create the new directory
* `rm` it will remove the directore, and `rm -Rf` it will delete the file with the contents also.
* `chgrp name:name directory` it will change the access to both the user and group.
## Filters or Text Processor Commands
    1. cut
    2. awk
    3. grep and egrep
    4. sort
    5. uniq
    6. wc
### WC (word count)
* `wc fileName` -> it will return the line count , words count, bytes that are presented in the file.
* `wc -l` -> newLines count
* `wc -w` -> words count
* `wc -c` -> bytes 
* `ls -ltr | wc -l` -> return the no of files and directories in the location. but it will include the **total** line also, so we should subtract 1 from the result.
* `ls -ltr | grep dr` -> to list the directories in the location
* `ls -ltr | grep dr | wc -l` -> count of all directories
* **Word Count** command is only for files not for directories. 
* <u>To list only diretories in the location is `ls -d */`.</u>
### grep and egrep
* grep is used to filter the list by some keywords that is, it is exactly like **search**.
* `grep -i keywords fileName` -> it couldn't consider the cases
* `grep -v keyword filName` -> it returns the result by except the keyword matching lists.
* `grep -n keyword filName` -> it returns the list with the **line number**.
* `grep -c keyword filName` -> it will return the matched **count**.
* grep can also return the keyword matching result while showing the direcotries or files lists also -> `ls -ltr | grep -i keyword`
* `grep -vi keyword fileName | awk '{print$1} '` -> it will return the non matched results first word itself.
* `grep -vi keyword fileName | awk '{print$1} ' | cut -c1-3` -> it will return the non matched results first word's 3 characters only.
* **egrep** is for filtering the lists by multiple keywords.
* `egrep -i "keyword1|keyword2" fileName`.
### awk command
* Mainly awk command is used for extract fields from file or an output.
* `awk '{print $1}' fileName` -> it will print first column of a file
* `awk '{print $1,$3} fileName'` -> it will print first and third column 
* `awk '{print $NF}' filName` -> print last column
* `awk '/keyword/{print $0}' fileName` -> we can able to search through **awk** command hence it will results the matched rows 
* `echo "Hello world" | awk '{$2="kishore";print $0;}'` -> it will replace the second column name with what we gave => output is **Hello kishore**.
* `awk -F: '{print$1}' fileName` -> **-F:** it will separate the row by **:** and extract what ever column we want.
* `awk -F/ '{print$1}' fileName` -> separate by **/**
* `cat fileName | awk '{if($2=="kishore") print $0;}'` -> it will print all the row which has 'kishore' in their 2nd column.
* `awk '{length($0) > 10; print}' fileName` -> it will print all the row which has greater than **10** characters
* `awk '{print NF}'` -> return no of columns of every row.
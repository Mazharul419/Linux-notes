# Linux-notes

### File Management

mkdir makes directories

rmdir - removes directories

rm - removes files 

(-r) removes directory and associated content

cd - changes directory 

( ..) goes up one level 

( /) goes to root directory

pwd - prints working directory

touch - updates timestamp of existing file, creates new file if no existing

echo - prints set text 

- also can overwrite (>) existing file or append (>>) set text to a new file

cat - prints contents of existing file 

- also can overwrite (>) or append (>>)  contents to a new or existing file

grep - searches string of text within file/folder

cp - copies a file or directory

### -rwx rwx rwx 

-Directory/File/Link information

1- rwx - User rights

2- rwx - Group rights

3- rwx - Other rights

chmod - modifies permissions for files

e.g., chmmod u+x, g+r, o-w [filename].file  - users: adds execute permission, group: adds read permission, others: removes write permission for filename

chmod ug=rw, o=r example.txt - sets permission for users and groups to read and write only, sets other permissions to read only

chown - modifies owner of a file (req. sudo)

chgrp - modifies group of a file (req. sudo)

e.g., 

sudo chown newuser example.txt - changes owner of example.txt file to newuser
sudo chgrp admin example.txt - changes group of example.txt file to admin group

sudo chown newuser:admin example.txt - does both above commands


sudo -R newuser:admin example_directory - changes ownership of directory and contents



owner and group info found using ls -l command

### User Management

whoami - specifies which user you are logged in as

exit - logs out of current user

sudo - super user do - applies special priveleges to run commands

sudo useradd newuser
sudo passwd newuser

adds new user

su - newuser

switch to newuser as substiture user

sudo usermod -aG sudo newuser

Adds newuser to sudoers group and grants them with sudo priveliges - need to be logged in as sudo user to execute this


sudo deluser newuser sudo

Removes newuser from sudoers group and revokes their sudo priveliges

cat /etc/group - contains groups

sudo groupadd devops - adds devops groups to user groups
sudo usermod -aG devops newuser - assigns "newuser" to "devops" group

groups - lists groups current user is part of

sudo gpasswd -d newuser devops - removes "newuser" from "devops" group

sudo groupdel devops - removes "devops" group from groups

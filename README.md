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

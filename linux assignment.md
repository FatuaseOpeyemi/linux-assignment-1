### Assignment

1.  Creation of *altschool* login user with home directory: `sudo useradd -m Altschool`
2.  Set the password for *altschool* user:  `sudo passwd altschool` `password: password123`
3.  Login to *altschool* user account : `su - altschool`
4.  Create the requested directories (_code, tests, personal and misc_): `mkdir code tests personal misc`

  




|  | Description | Commands |
|--------|------------|----------|
| 1      | Change directory to the tests directory using absolute pathname                 | `cd /home/altschool/tests`     |
| 2      | Change directory to the tests directory using relative pathname                  | `cd tests`         |
| 3      | Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory                  | `echo "Hello A" > /home/altschool/misc/fileA`          |
| 4      | Create an empty file named fileB in the misc directory                  | `touch /home/altschool/misc/fileB`         |
| 5      | Copy contents of fileA into fileC                  | `cp /home/altschool/misc/fileA /home/altschool/misc/fileC`         |
| 6      |  Move contents of fileB into fileD                | `mv /home/altschool/misc/fileB /home/altschool/misc/fileD`          |
| 7      | Create a tar archive called misc.tar for the contents of misc directory                  | `tar -cvf misc.tar misc`          |
| 8      | Compress the tar archive to create a misc.tar.gz file  | `gzip misc.tar`         |
| 9      | Create a user and force the user to change his/her password upon login                 |i. create new user: _gabriel_ `sudo useradd gabriel` <br> ii. force **gabriel** password change on login: `sudo passwd -e gabriel`         **or** `sudo chage -d 0 gabriel`|
| 10      | Lock a users password | `sudo passwd -l gabriel`         |
| 11     | Create a user with no login shell                 |  `sudo useradd -s /usr/sbin/nologin gabriel`        |
| 12     | Disable password based authentication for ssh                  | Use `sudo vim /etc/ssh/sshd_config` and set `PasswordAuthentication no`       | 
| 13     | Disable root login     | Use `sudo vim /etc/ssh/sshd_config` and set `PermitRootLogin no`          |
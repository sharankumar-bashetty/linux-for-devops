Understanding the Folder Structure:

/boot --> stores all files regarding booting the system
/usr --> have user installed stuffs
/var --> stores logs files, cache, tempo memory
/etc --> stores system config files
/root --> home directory of root user
/home --> default location for home users
/tmp	Temporary files (cleared on reboot).
/dev	Contains device files (e.g., /dev/null, /dev/sda1, /dev/sda2).

User management:
Since linux is multi user OS, multiple users can work simultaneously.
Below are some important files that are invlolved in enabling it:

/etc/passwd --> stores user account details
/etc/group --> stors group information
/etc/shadow --> stores encrypted user passwords.
/etc/gshadow --> stores encrypted group details.

Creating Users:
Create a new user → sudo useradd username
Create user with home directory → sudo useradd -m username
Create user with bash shell → sudo useradd -m -s /bin/bash username
Create user with full name/comment → sudo useradd -m -c "Full Name" username

Setting and Changing Passwords:
Set password for a user → sudo passwd username
Change current user password → passwd

Deleting Users:
Delete a user → sudo userdel username
Delete user along with home directory → sudo userdel -r username

Modifying Users:
Rename a user → sudo usermod -l newname oldname
Change user home directory → sudo usermod -d /new/home -m username
Change user default shell → sudo usermod -s /bin/bash username
Lock user account → sudo usermod -L username
Unlock user account → sudo usermod -U username

Group Management:
Create a new group → sudo groupadd groupname
Delete a group → sudo groupdel groupname
Add user to a group → sudo usermod -aG groupname username
Remove user from a group → sudo gpasswd -d username groupname

Switching Users:
Switch to another user → su username
Switch to root user → sudo su
Run command as another user → sudo -u username command

Viewing User and Group Information:
Show current logged-in user → whoami
Display user ID and groups → id username
Show logged-in users → who
List all system users → cat /etc/passwd
List all groups → cat /etc/group

Sudo Access Management:
Give sudo access to a user → sudo usermod -aG sudo username
Edit sudo permissions safely → sudo visudo

File Ownership (User Related):
Change file owner → sudo chown username file
Change file owner and group → sudo chown username:group file

Account Expiry and Password Policies:
Set account expiry date → sudo chage -E YYYY-MM-DD username
Check password aging details → sudo chage -l username
Force password change on next login → sudo chage -d 0 username

File and Directory Navigation:
Show current working directory → pwd
List files and directories → ls
List all files including hidden → ls -la
Change directory → cd directory_name
Go to parent directory → cd ..
Go to home directory → cd ~

Creating Files and Directories:
Create an empty file → touch file.txt
Create a directory → mkdir dirname
Create nested directories → mkdir -p dir1/dir2/dir3

Copying Files and Directories:
Copy a file → cp source destination
Copy directory recursively → cp -r source_dir destination
Copy with confirmation before overwrite → cp -i source destination

Moving and Renaming:
Move file or directory → mv source destination
Rename file or directory → mv oldname newname

Deleting Files and Directories:
Delete a file → rm file.txt
Delete directory → rm -r dirname
Force delete without prompt → rm -f file.txt
Force delete directory → rm -rf dirname

Viewing File Content:
Display file content → cat file.txt
View file page by page → less file.txt
Show first lines of file → head file.txt
Show last lines of file → tail file.txt
Monitor file in real time → tail -f file.txt

File Permissions:
Change file permissions → chmod 755 file.txt
Add execute permission → chmod +x file.txt
Remove write permission → chmod -w file.txt

File Ownership:
Change file owner → chown user file.txt
Change owner and group → chown user:group file.txt

Searching Files and Content:
Find files by name → find . -name "file.txt"
Search text inside files → grep "text" file.txt
Search recursively in directory → grep -r "text" dir

File Information:
Show file type → file file.txt
Show file details → stat file.txt
Check disk usage of file/dir → du -sh dirname

Disk and Storage:
Show disk space usage → df -h
Show directory size → du -h

Links (Important in DevOps):
Create soft link → ln -s target linkname
Create hard link → ln target linkname

Archive and Compression:
Create tar archive → tar -cvf file.tar dir
Extract tar archive → tar -xvf file.tar
Create compressed archive → tar -czvf file.tar.gz dir
Extract compressed archive → tar -xzvf file.tar.gz


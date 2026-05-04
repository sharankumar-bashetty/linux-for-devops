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

SOme commands:
create user: adduser username
To set or change a user’s password: passwd username



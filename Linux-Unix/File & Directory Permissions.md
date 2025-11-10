## Interpreting File Permissions
For individual *files:*
* **Read (r):** Permission to access the file's contents (e.g., using `cat` or `less`.)
* **Write (w):** Permission to modify the file's contents using `append` or a text editor like `nano`.
* **Execute (x):** Execute the contents of a file, whether it is a compiled binary or bash shell script.
For entire *directories:*
* **Read (r):** Permission to view the contents of a directory (e.g., using `ls`.)
* **Write (w):** Allows one to modify the contents of a directory (e.g., using `mv` or `rm`.)
* **Execute (x):** Allows one to enter a directory using `cd`, get extended information on a directory `ls -l`, or pass through the directory to a directory underneath.
When using `ls -l`, *d* represents that an entry is a directory
> [!Remark]
> The `-` character means that a permission for any of the three actions is not possible. 
## Octal Permissions
* - represents a value of zero.
* r represents a value of 4
* w represents a value of 2
* x represents a value of 1
For instance, a file with permissions `-rw-r-x---` has a permission value of `650`. `rw-=4+2; r-x=5,---=0`.
Or we can go the other way around. A file with permission value of `770` means that both the file **[[OWNER]] and [[GROUPS]]** associated with the file have the permission to read, write and execute, but all other users cannot.
## Modding File Permissions
File permissions are managed using ``chmod``:
* `chmod ug+rwx example.txt`: Grants all three permission types to a file **for the user and group (ug).**
* `chmod o+r example2.txt`: 
* `chmod a+x librewolf.appimage`: Makes an appimage executable.
* `chmod -R 777 INSTALL.sh`: Grants everyone the right to read, write, and execute this shell script.
File **ownership** is managed using `chown` and `chgrp`.
## User Permissions
See [[User Permissions]] for more on how users interact with file permissions.
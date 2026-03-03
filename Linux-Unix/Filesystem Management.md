## Interpreting File Attributes
Run `ls -l` in any directory and verbose details on all items will appear.
- **File type:** If this starts with a d, it is a directory. If it starts with an l, it is a link. If it does not start with either of these characters, it is a file. More detail in the section "interpreting file permissions".
- **Links:** Column two shows the number of links.
- **Owner/Group:** Shows who owns the file, and the group that it's in
- **Modification Date:** The month, day and time at which a file was modified respectively.
- **Name:** File name.
## Moving Files
- `cp`, `mv` and `rm` can be found in the [[Common Utilities & Tools|common utilities]] notes page.
##### Symbolic Links
Issuing `ls -i` or `ls -i <FILE/DIRECTORY NAME>` will procure the inodes for each file or directory. The **inode** is a numerical fingerprint that can be used to identify a file. The inode remains the same even if the human-readable file name is modified.

To create a *soft* symbolic link to an item, enter the directory in which you want the symbolic link to be procured, then issue `ln -s /path/to/file`. The integrity of the symbolic link can be verified using `cat` and ensuring that the link's contents match that of the original file. Issuing `ls -l` should show something similar to `FILENAME -> /path/to/FILENAME`.
- Issuing `ln` without the `-s` flag will create a *hard* symbolic link. 
- This means that when the original file is moved or deleted, the link does not become stale.
## Editing Files
For editing files, see: [[ex-vi Handbook|vi]].

To append something to a file, issue `echo 'TEXT' > FILENAME`.
To append an entire output, issue `COMMAND_NAME > FILENAME`. For instance, `ls -l ~/.cache > filesystem.txt` would append the output (stdout) of `ls -l ~/.cache` to the text file. To preserve the original contents of `filesystem.txt`, use `ls -l ~/ >> filesystem.txt` with two >> symbols. Note that using stdout is *redirecting* the output to that file, so using it means any output that would be expected from issuing a command will not appear. The reverse of stdout is stdin, where file contents are fed into a command or file.

stdout will ignore any output categorized as an error message. To capture error messages, use `stderr`.  Issuing `ls -l /root` without elevated privileges results in an error, so using `ls -l /root 2> error_output.txt` will write that error message to the file and the command will fail silently.  
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
> [!Remark] Hint
> The `-` character means that a permission for any of the three actions is not possible. 
##### Octal Permissions
* - represents a value of zero.
* r represents a value of 4
* w represents a value of 2
* x represents a value of 1
For instance, a file with permissions `-rw-r-x---` has a permission value of `650`. `rw-=4+2; r-x=5,---=0`.
Or we can go the other way around. A file with permission value of `770` means that both the file **[[User Permissions|OWNER]] and [[User Permissions#Groups|GROUPS]]** associated with the file have the permission to read, write and execute, but all other users cannot.
##### Modding File Permissions
File permissions are managed using ``chmod``:
* `chmod ug+rwx example.txt`: Grants all three permission types to a file **for the user and group (ug).**
* `chmod o+r example2.txt`: 
* `chmod a+x librewolf.appimage`: Makes an appimage executable.
* `chmod -R 777 INSTALL.sh`: Grants everyone the right to read, write, and execute this shell script.
File **ownership** is managed using `chown` and `chgrp`.
## User Permissions
See [[User Permissions]] for more on how users interact with file permissions.

- `chgrp <GROUP NAME> example.txt`: Changes the group that a file belongs to.
- `chown <USER> example.txt`: Changes the owner of the file.
- `chown <GROUP NAME>:<USER> example.txt`: Changes both the group and owner that a file belongs to.
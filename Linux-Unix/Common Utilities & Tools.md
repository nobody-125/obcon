## Arch Linux  (pacman)
* ``pacman -Rdd`` : Skip dependency checks when removing a package
* ``pacman -Scc``: Clear pacman cache
* ``pacman -Qdtq | pacman -Rns -``: Remove orphan packages
* ``pacman -Qqd | pacman -Rsu --print -``: Ibid.
## Gentoo Linux
* `emerge -av <PACKAGE_REPO>/<PACKAGE>`: Install package from specific repository, provides verbose description and requires confirmation
## Shell Commands
#### Help
- `info`: Verbose details on what a command does.
- `man`: Load the manpages for a command
- `<COMMAND> --help`: Similar to `man`
- `whatis <COMMAND>`: Prints the first line of the manpage for a command
#### Filesystem mgmt.
* `cp`: Copy/paste
	* `cp -R`: Copy files recursively
* `find`: Locate files
* `grep`: Locate patterns in files
	* `grep -v '/$' <foo>` Print only lines that do not end with `/` in file `foo`.
* `ls`: List files in directory
	* `ls -l`: Verbose (ownership and permissions).
* `lsblk`: Lists available physical storage devices.
* `mv`: Move or rename a file.
	* `mv <file_name> <new_file_name`: Renames a file.
* `rm`: Remove files or directories
	* `rm -f`: Force the removal of nonexistent files/args.
	* `rm -rf:` Remove a directory and all its contents
* `touch`: Create a file
*  `whereis` shows full path of (shell) commands
##### System information
- `cat /sys/class/power_supply/BAT0/capacity`: Show battery capacity
- `uname`: Print system information
	- `uname -r`: Current kernel version
- `uptime`: Show system uptime
- `whoami`: Display current user
## Transferring Data
* `curl`: transfer data from the internet
* `wget`: transfer data from websites
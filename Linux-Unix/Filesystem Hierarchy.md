1. /bin: Essential binaries (ls, cp, mv, rm, cat)
2. /sbin: Lower-level system binaries (fsck, halt, reboot)
3. /etc: Systemwide configuration files, like /etc/fstab and /etc/passwd.
4. /usr: RO files and user-installed software, user-installed binaries:
	* ``/usr/share/wallpapers/:`` Location of all default KDE wallpapers.
	* ``/usr/share/firefox/:`` Location of the FF binary.
5. /var: Variable or temporary files, like /var/cache
6. /tmp: Temporary files, usually destroyed upon reboot.
7. /home: Personal files or configurations.
	* ``~/.var``: Similar to /var.
8. /dev: Device files that represent physical hardware components (sda, nvme, null)
9. /root: Home directory for the root user, not the same as /.
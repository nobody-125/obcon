## User
A _user_ is anyone who uses a computer. In this case, we are describing the names which represent those users. It may be Mary or Bill, and they may use the names Dragonlady or Pirate in place of their real name. All that matters is that the computer has a name for each account it creates, and it is this name by which a person gains access to use the computer. Some system services also run using restricted or privileged user accounts.
Managing users is done for the purpose of security by limiting access in certain specific ways. The [superuser](https://en.wikipedia.org/wiki/Superuser "wikipedia:Superuser") (root) has complete access to the operating system and its configuration; it is intended for administrative use only. Unprivileged users can use several programs for controlled [privilege elevation](https://wiki.archlinux.org/title/List_of_applications/Security#Privilege_elevation "List of applications/Security").
* A user can be added with `useradd -m <username>`.
* Passwords are managed through `passwd`.
## Groups
*See: `man group.5`*
The `/etc/group` FILE defines groups on the system. The `groups` command shows group membership. All groups can be listed with `cat`.
* Adding a group can be achieved with `groupadd <group>`.
* Adding a user to a group can be achieved with `usermod -aG <groups> <username>`. Omit the `a` from `-aG` to remove the user from all groups except `<groups>`.
* Delete a group with `groupdel <group>`.
##### Common User Groups
* **adm:** Admin group with full read access to **JOURNAL** files.
* **systemd-journal:** Provides RO access to the systemd logs
* **wheel:** Administration group commonly used for priviledge escalation/administrative action. Gives access to `sudo` and `su`.
##### SGID & SUID
Files with SGID and SUID respectively will **always** execute as:
* The **group** that owns the file (SGID)
* The **user** that owns the file
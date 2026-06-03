##### 1. Partition
Data on a Linux operating system is organized by a partition table, usually MBR or GPT. Partitions define the blocks set aside for data to be stored and can be primary, extended or logical.
* Primary: Typical subdivision of a disk, limited to 4 on a MBR table
* Extended: Allows for greater than 4 partitions through principles of containerization
* Logical partition: Virtualized partition that exists within an extended partition
A partition's *purpose* is typically defined by partition kind. This metadata, stored in the partition table, declares what the partition will be used for, which is used by bootloaders and installers to interpret how to treat the partition.
##### 2. Filesystems
The filesystem is a hierarchical storage structure that organizes files and subdirectories. These are traditionally implemented through the kernel with the exception of the *File System in User Space* (FUSE).
	VFS allows Linux to support a great number of filesystems - ext4, btrfs, vfat, xfs, etc.
Once a partition kind is prepared, the `mkfs` utility can be used to automatically generate a filesystem. `mkfs` will make multiple backups of the superblock, which is responsible for helping the OS interpret and manage the file system correctly.

Filesystems are typically identified by device name (e.g., `/dev/sda1`). However, in the event that device names change, they can still be correctly matched to their UUID. Since kernel name descriptors for block devices are not persistent, UUIDs are used in configuration files like `/etc/fstab`.
##### 3. /etc/fstab
`fstab` automates mounting filesystems at boot time, defines how file systems and data sources should be treated when starting the system, and can be configured to do various things at boot time, such as running `fsck`.

`fstab`, derived from file system table, contains the fields *device-spec*, *mount-point*, *fs-type*, *option*, *dump* and *pass*.
* *device-spec*: The device name - can be UUID or simply the partition name
* *mount-point*: Where the contents of the device may be accessed after mounting
* *fs-type*: kind of filesystem to be mounted
* *options*: allows for customization, `defaults` refers to pre-determined set of options
* `dump`: outdated system that defines how often the filesystem should be backed up by the `dump` program.
* `pass`: indicates the order in which `fsck` will check the devices for errors at boot.
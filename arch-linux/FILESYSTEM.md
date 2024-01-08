<p align="center">
    <a href="#arch-linux-filesystem" style="font-size: 24px;">Filesystem</a> |
    <a href="#commands" style="font-size: 24px;">Commands</a> |
</p>

### Arch Linux Filesystem
|     |     |
| --- | --- |
| **/bin** | Essential command binaries |
| **/boot** | Contains the kernel and initial ramdisk |
| **/dev** | Device files |
| **/etc** | System-wide configuration files |
| **/home** | Home directories for regular users |
| **/lib, /lib64** | Essential shared libraries and kernel modules |
| **/mnt, /mnt** | Directories for temporarily mounting filesystems |
| **/opt** | Typically used for third-party software |
| **/proc** | A virtual filesystem that provides process and kernel information |
| **/root** | Home directory for the root user |
| **/run** | Run-time variable data |
| **/sbin** | Essential system binaries |
| **/srv** | Data for services provided by the system |
| **/sys** | A virtual filesystem that exposes information about devices, drivers, and some kernel features |
| **/tmp** | Stores temporary files |
| **/usr** | Secondary hierarchy for read-only user data |
| **/var** | Variable data such as logs, spool files, and temporary e.g. /var/log |

## Commands

| Topic | Command | Description | Example Usage |
| --- | --- | --- | --- |
| Checking and Repairing |  |  |  |
|  | `e2fsck` | Check ext2, ext3, or ext4 filesystems. | `e2fsck /dev/sdX1` |
|  | `fsck` | Check and repair a filesystem. | `fsck /dev/sdX1` |
|  | `xfs_repair` | Repair an XFS filesystem. | `xfs_repair /dev/sdX1` |
| Creating a Filesystem |  |  |  |
|  | `mkfs.btrfs` | Create a Btrfs filesystem. | `mkfs.btrfs /dev/sdX1` |
|  | `mkfs.ext4` | Create an ext4 filesystem. | `mkfs.ext4 /dev/sdX1` |
|  | `mkfs.xfs` | Create an XFS filesystem. | `mkfs.xfs /dev/sdX1` |
| Listing Drives and Partitions |  |  |  |
|  | `fdisk` | Manipulate disk partition table. | `fdisk -l` |
|  | `gparted` | GUI partition editor for disk partitions. | `gparted` |
| Managing Filesystem Labels and UUIDs |  |  |  |
|  | `e2label` | Set an ext2, ext3, or ext4 filesystem label. | `e2label /dev/sdX1 NewLabel` |
|  | `xfs_admin` | Change the UUID of an XFS filesystem. | `xfs_admin -U newUUID /dev/sdX1` |
| Mounting and Unmounting |  |  |  |
|  | `mount` | Mount a filesystem. | `mount /dev/sdX1 /mnt` |
|  | `mount -a` | Mount all filesystems listed in /etc/fstab. | `mount -a` |
|  | `umount` | Unmount a filesystem. | `umount /mnt` |
| Searching Files |  |  |  |
|  | `find` | Search for files in a directory hierarchy. | `find /path/to/search -name "filename"` |
|  | `locate` | Find files by name. | `locate filename` |
| Traversing and File Management |  |  |  |
|  | `cd` | Change the current directory. | `cd /path/to/directory` |
|  | `cp` | Copy files or directories. | `cp file1 file2` |
|  | `lsblk` | List block devices, including information about whether or not each device is mounted. | `lsblk` |
|  | `mv` | Move or rename files. | `mv file1 file2` |
|  | `rm` | Remove files or directories. | `rm filename` |
|  | `pwd` | Get present working directory. | `pwd` |
|  | `touch` | Create an empty file or update the access and modification times of a file. | `touch filename` |
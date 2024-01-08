<p align="center">
    <a href="#arch-linux-filesystem-structure" style="font-size: 24px;">Filesystem</a> |
    <a href="#commands" style="font-size: 24px;">Commands</a> |
</p>

In Arch Linux, a **filesystem** is a method used to control how data is stored, organized, managed,and retrieved on storage devices. The filesystem also provides a way to **identify**, **access**, and **modify** the stored **information**. Arch Linux supports various filesystem types, each with its own advantages, disadvantages, and unique characteristics.

| Filesystem | Description |
| --- | --- |
| **Btrfs** | **Btrfs** is a Linux native filesystem that offers features such as **subvolumes**, **snapshots**, and integrated **RAID** support. It is considered stable and is known for its flexibility and reliability. |
| **Ext4** | **Ext4** is a widely used and well-established filesystem in the Linux community. It is known for its stability, performance, and compatibility with older **Ext2** and **Ext3** filesystems. |
| **F2FS** | **F2FS (Flash-Friendly File System)** is designed for **NAND-based flash storage** devices. It is optimized for use in **solid-state drives (SSDs)** and offers features tailored for flash memory. |
| **ZFS** | While not a native Linux filesystem, **ZFS** is known for its advanced features such as data **integrity**, **snapshots**, and built-in **RAID** support. It requires a significant amount of **ECC RAM** to run effectively. |

Arch Linux follows the **Filesystem Hierarchy Standard (FHS)** for operating systems using the **systemd** service manager. This standard defines the directory structure and organization for the operating system, ensuring **consistency** and **compatibility** across different systems.

The filesystem in Arch Linux is typically created on a **partition**, inside **logical containers** such as **LVM**, **RAID**, and **dm-crypt**, or on a regular file. After creating a new **filesystem**, it can be **mounted** to make it **accessible** for use.

### Arch Linux Filesystem Structure
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
|  | `touch` | Create an empty file or update the access and modification times of a file. | `touch filename` |
<p align="center">
    <a href="#arch-linux-filesystem" style="font-size: 24px;">Filesystem</a> |
    <a href="#common-commands" style="font-size: 24px;">Commands</a> |
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

### Commands

|     |     |
| --- | --- |
| **cd** | Change the current directory |
```bash
cd /home/user1/Documents
```
| **cp** | Copy files and directories |
| **fdisk** | Create and manage disk partitions |
| **find** | A versatile tool for searching files and directories based on various criteria, such as name, type, and size, with results generated in real-time. |
| **gdisk** | GPT fdisk, a disk partitioning tool |
| **locate** | A faster option that relies on a pre-built database for quick file searches but may not provide real-time results. |
| **ls** | List directory contents |
| **mkdir** | Create a new directory |
| **mkfs** | Make a file system on a disk partition |
| **mount** | Mount a file system |
| **mv** | Move/rename files and directories |
| **parted** | Create and manage disk partitions with a more user-friendly interface |
| **pwd** | Print the current working directory |
| **rm** | Remove files and directories |
| **rmdir** | Remove a directory |
| **umount** | Unmount a file system |
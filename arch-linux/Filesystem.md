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

| Topic | Command | Description | Example |
| --- | --- | --- | --- |
| Checking and Repairing |  |  |  |
|  | `e2fsck` | Check ext2, ext3, or ext4 filesystems. | `e2fsck /dev/sdX1` |
|  | `fsck` | Check and repair a filesystem. | `fsck /dev/sdX1` |
|  | `xfs_repair` | Repair an XFS filesystem. | `xfs_repair /dev/sdX1` |
| Creating a Filesystem |  |  |  |
|  | `mkfs.btrfs` | Create a Btrfs filesystem. | `mkfs.btrfs /dev/sdX1` |
|  | `mkfs.ext4` | Create an ext4 filesystem. | `mkfs.ext4 /dev/sdX1` |
|  | `mkfs.xfs` | Create an XFS filesystem. | `mkfs.xfs /dev/sdX1` |
| Managing Filesystem Labels and UUIDs |  |  |  |
|  | `e2label` | Set an ext2, ext3, or ext4 filesystem label. | `e2label /dev/sdX1 NewLabel` |
|  | `xfs_admin` | Change the UUID of an XFS filesystem. | `xfs_admin -U newUUID /dev/sdX1` |
| Mounting and Unmounting |  |  |  |
|  | `mount` | Mount a filesystem. | `mount /dev/sdX1 /mnt` |
|  | `mount -a` | Mount all filesystems listed in /etc/fstab. | `mount -a` |
|  | `umount` | Unmount a filesystem. | `umount /mnt` |
| Viewing Mounted Filesystems |  |  |  |
|  | `df` | Display information about mounted filesystems. | `df -h` |
|  | `lsblk` | List block devices, including information about whether or not each device is mounted. | `lsblk` |

### Other Commands

|     |     |
| --- | --- |
| **cd** | Change the current directory |
```bash
cd ~/Documents
```
|     |     |
| --- | --- |
| **cp** | Copy files and directories |
```bash
cp file.txt ~/Documents
```
|     |     |
| --- | --- |
| **fdisk** | Create and manage disk partitions |
```bash
fdisk -l
```
|     |     |
| --- | --- |
| **find** | A versatile tool for searching files and directories based on various criteria, such as name, type, and size, with results generated in real-time. |
```bash
find ~/ -iname "*.txt"
```
|     |     |
| --- | --- |
| **gdisk** | GPT fdisk, a disk partitioning tool |
```bash
gdisk /dev/sda
```
|     |     |
| --- | --- |
| **locate** | A faster option that relies on a pre-built database for quick file searches but may not provide real-time results. |
```bash
locate myfile.txt
```
|     |     |
| --- | --- |
| **ls** | List directory contents |
```bash
ls -la ~/username
```
|     |     |
| --- | --- |
| **mkdir** | Create a new directory |
```bash
mkdir ~/NewDirectory
```
|     |     |
| --- | --- |
| **mkfs** | Make a file system on a disk partition |
```bash
mkfs.ext4 /dev/sda1
```
|     |     |
| --- | --- |
| **mount** | Mount a file system |
```bash
mount /dev/sdb1 /mnt/data
```
|     |     |
| --- | --- |
| **mv** | Move/rename files and directories |
```bash
mv file1.txt ~/Documents
```
|     |     |
| --- | --- |
| **parted** | Create and manage disk partitions with a more user-friendly interface |
```bash
parted /dev/sda
```
|     |     |
| --- | --- |
| **pwd** | Print the current working directory |
```bash
pwd
```
|     |     |
| --- | --- |
| **rm** | Remove files and directories |
```bash
rm file1.txt
```
|     |     |
| --- | --- |
| **rmdir** | Remove a directory |
```bash
rmdir ~/OldDirectory
```
|     |     |
| --- | --- |
| **umount** | Unmount a file system |
```bash
umount /mnt/data
```
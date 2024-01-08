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
cd ~/Documents
```
|     |     |
| --- | --- |
| **cp** | Copy files and directories |
```bash
cp file.txt ~/Documents
```
| **fdisk** | Create and manage disk partitions |
```bash
sudo fdisk -l
```
| **find** | A versatile tool for searching files and directories based on various criteria, such as name, type, and size, with results generated in real-time. |
```bash
sudo find / -iname "*.txt"
```
| **gdisk** | GPT fdisk, a disk partitioning tool |
```bash
sudo gdisk /dev/sda
```
| **locate** | A faster option that relies on a pre-built database for quick file searches but may not provide real-time results. |
```bash
locate myfile.txt
```
| **ls** | List directory contents |
```bash
ls -la ~/username
```
| **mkdir** | Create a new directory |
```bash
mkdir ~/NewDirectory
```
| **mkfs** | Make a file system on a disk partition |
```bash
sudo mkfs.ext4 /dev/sda1
```
| **mount** | Mount a file system |
```bash
sudo mount /dev/sdb1 /mnt/data
```
| **mv** | Move/rename files and directories |
```bash
mv file1.txt ~/Documents
```
| **parted** | Create and manage disk partitions with a more user-friendly interface |
```bash
sudo parted /dev/sda
```
| **pwd** | Print the current working directory |
| **rm** | Remove files and directories |
```bash
rm file1.txt
```
| **rmdir** | Remove a directory |
```bash
rmdir ~/OldDirectory
```
| **umount** | Unmount a file system |
```bash
sudo umount /mnt/data
```